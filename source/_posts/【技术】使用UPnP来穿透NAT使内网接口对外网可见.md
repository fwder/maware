---
title: 【技术】使用UPnP来穿透NAT使内网接口对外网可见
categories:
  - 转载
tags:
  - UPnP
  - NAT
  - 公网IP
  - 内网穿透
excerpt: >-
  原文链接http://www.cnblogs.com/mgen/archive/2013/02/03/2890987.html，并修改了部分内容，仅供学习和交流使用。最近有个搭建视频网站的需求，...
date: 2022-02-06 16:38:00
---

原文链接http://www.cnblogs.com/mgen/archive/2013/02/03/2890987.html，并修改了部分内容，仅供学习和交流使用。最近有个搭建视频网站的需求，...
<!-- more -->
> 原文链接[http://www.cnblogs.com/mgen/archive/2013/02/03/2890987.html](https://old.blog.fwder.cn/index.php/go/aHR0cDovL3d3dy5jbmJsb2dzLmNvbS9tZ2VuL2FyY2hpdmUvMjAxMy8wMi8wMy8yODkwOTg3Lmh0bWw=)，并修改了部分内容，仅供学习和交流使用。

最近有个搭建视频网站的需求，现在比较难以解决的问题除了技术之外，还有更重要的是必须节省成本。毕竟是视频网站，所以就需要很大的带宽，而我却没有资本去购买大带宽服务器。

于是我就找到了这个解决办法：

我们都知道：如果服务器和客户端**都在内网环境**下，即双方都通过NAT来接触外网，那么此时客户端是**无法直接和服务器交流**的。

解决方案可以是：

1：把服务器部署在不存在NAT的公网环境下。（没钱买服务器啊啊啊...）

2：使用常见的NAT穿透方法比如[UDP打洞](https://old.blog.fwder.cn/index.php/go/aHR0cDovL2VuLndpa2lwZWRpYS5vcmcvd2lraS9VRFBfaG9sZV9wdW5jaGluZw==)，或者[STUN协议](https://old.blog.fwder.cn/index.php/go/aHR0cDovL2VuLndpa2lwZWRpYS5vcmcvd2lraS9TVFVO)，但是这些方法都需要另一个已知的部署在公网环境下的服务器。（原因同上）

3：就是这篇文章主要讨论的方案，即不需要部署任何公网环境下的服务器，通过路由器支持的[UPnP协议](https://old.blog.fwder.cn/index.php/go/aHR0cDovL2VuLndpa2lwZWRpYS5vcmcvd2lraS9Vbml2ZXJzYWxfUGx1Z19hbmRfUGxheQ==)来把内网的接口绑定到公网接口上。

**这个方法的好处是，我可以构建一个由用户组成的PCDN网络来为我的服务器加速，从而减小服务器的带宽成本。**

UPnP的一大优势就是不会像UDP打洞那样，内网接口不需要先向外部接口发送UDP包来把绑定的公网接口告诉NAT，而且对于对称NAT，UDP打洞是无效的。而UPnP一旦设置成功后，内网接口完全以绑定的公网接口暴露在公网中。

演示程序的运行是这样的：

![](http://images.cnitblog.com/blog/296767/201302/03171059-612035e36bf048be82dfb59479ecac30.png)![成功通过UPnP建立连接](https://old.blog.fwder.cn/usr/uploads/2022/02/1792443583.png "成功通过UPnP建立连接")

具体过程：

> 1.  输出用户Host Name和内网IP地址。
> 2.  通过UPnP把内网IP地址，内部端口号绑定到一个外部端口号上。
> 3.  通过HTTP从外部网站获取公网IP地址。
> 4.  在内网中创建TCP Socket服务器。
> 5.  建立另一个TCP Socket客户端，然后尝试连接上面获取的公网IP和UPnP绑定的外部端口。
> 6.  如果一切没有问题的话，此时会成功连接到服务器，并收到回应！

在.NET环境下使用Windows的UPnP组件需要现在工程中引用：NATUPnP 1.0 Type Library，这是一个COM类库。

下面开始逐句分析源代码，源代码均拟用户已加入下列命名空间：

```
using System.Net;

using System.Net.Sockets;

using System.Text.RegularExpressions;  //提取IP时的正则

using System.Threading.Tasks;          //Task

using System.IO;                       //读取服务器信息用到StreamReader

using NATUPNPLib;                      //Windows UPnP COM组件

首先输出本机（也就是内网接口信息），这个很简单了：

//获取Host Name

var name = Dns.GetHostName();

Console.WriteLine("用户：" + name);

//从当前Host Name解析IP地址，筛选IPv4地址是本机的内网IP地址。

var ipv4 = Dns.GetHostEntry(name).AddressList.Where(i => i.AddressFamily ==AddressFamily.InterNetwork).FirstOrDefault();

Console.WriteLine("内网IP：" + ipv4);
```

接下来就是设置UPnP了，首先需要初始化UPnPNAT类型（他是一个接口，只不过通过CoClass特性把执行导向UPnPNATClass类型），接着通过UPnPNAT的StaticPortMappingCollection来添加或者删除UPnP绑定。注意在没有路由器或者路由器的UPnP不开启的情况下，StaticPortMappingCollection属性可能会返回null。

代码如下：

```
Console.WriteLine("设置UPnP");

//UPnP绑定信息

var eport = 8733;

var iport = 8733;

var description = "Mgen测试";

//创建COM类型

var upnpnat = new UPnPNAT();

var mappings = upnpnat.StaticPortMappingCollection;

//错误判断

if (mappings == null)

{

Console.WriteLine("没有检测到路由器，或者路由器不支持UPnP功能。");

return;

}

//添加之前的ipv4变量（内网IP），内部端口，和外部端口

mappings.Add(eport, "TCP", iport, ipv4.ToString(), true, description);

Console.WriteLine("外部端口：{0}", eport);

Console.WriteLine("内部端口：{0}", iport);
```

如果成功后，你应该可以在路由器的UPnP选项中看到这些数据：

![](https://old.blog.fwder.cn/usr/uploads/2022/02/2350304414.png)

设置好UPnP后，开始获取外网IP地址，可以通过这个网址 [http://checkip.dyndns.org/](https://old.blog.fwder.cn/index.php/go/aHR0cDovL2NoZWNraXAuZHluZG5zLm9yZy8=)。此时只需要发送一个HTTP GET请求，然后把返回的HTML中的IP地址提取出来就可以了，我们用正则来提取IP地址。

代码如下：

```
//外网IP变量

string eip;

//正则

var regex = @"\b\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\b";

using (var webclient = new WebClient())

{

var rawRes = webclient.DownloadString("http://checkip.dyndns.org/");

eip = Regex.Match(rawRes, regex).Value;

}

Console.WriteLine("外网IP：" + eip);
```

OK，这个时候（如果一切顺利的话），一切准备工作都做好了。我们有了：内网IP，内部端口，外网IP，外部端口。那么就可以做一个TCP连接做测试了。

直接建立一个TCP服务端，代表在NAT下的服务器，注意端口号要绑定到UPnP设置时的内部端口。

代码：

```
//在NAT下的服务器

var socket = new Socket(AddressFamily.InterNetwork, SocketType.Stream, ProtocolType.Tcp);

//绑定内网IP和内部端口

socket.Bind(new IPEndPoint(ipv4, iport));

socket.Listen(1);

//在另一个线程中运行客户端Socket

Task.Run(() =>

{

    Task.Delay(1000);

    ClientSocket(eip, eport);

});

//成功连接

var client = socket.Accept();

//服务器向客户端发送信息

client.Send(Encoding.Unicode.GetBytes("=== 欢迎来到Mgen的服务器！===" + Environment.NewLine));

Console.ReadKey(false);
```

上面的ClientSocket方法就是客户端的Socket连接执行，注意TCP协议是不保留数据边界的，因此服务器在发送消息时，后面加了个换行符（Environment.NewLine），然后在客户端接受数据时，使用Socket –> NetworkStream –> StreamReader的嵌套组合，最后由StreamReader的ReadLine读取数据，这样确保会读到最后的换行符。

ClientSocket方法的执行代码：

```
//ip参数和port参数是公网的IP地址，和UPnP中的外部端口

static void ClientSocket(string ip, int port)

{

try

{

    Console.WriteLine("建立客户端TCP连接");

    var socket = new Socket(AddressFamily.InterNetwork, SocketType.Stream, ProtocolType.Tcp);

    socket.Connect(new IPEndPoint(IPAddress.Parse(ip), port));

    using (var ns = new NetworkStream(socket))

    using (var sr = new StreamReader(ns, Encoding.Unicode))

    {

        Console.WriteLine("收到来自服务器的回应：");

        Console.WriteLine(sr.ReadLine());

    }

}

catch (Exception ex)

{

    Console.WriteLine(ex.Message);

}

}
```

OK。