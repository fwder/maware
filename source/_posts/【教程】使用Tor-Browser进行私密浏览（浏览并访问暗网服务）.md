---
title: 【教程】使用Tor Browser进行私密浏览（浏览并访问暗网服务）
categories:
  - 教程
tags:
  - Tor
  - 暗网
excerpt: >-
  [scode
  type="yellow"]如果想直接看手机版教程的请加QQ群672027707，进群密码和网桥IP请在文章下面回复以后，即可在文章顶部和底部看到
  抱歉，本站暂不提供 Tor 网桥...
date: 2021-06-13 17:05:00
---

\[scode type="yellow"\]如果想直接看手机版教程的请加QQ群672027707，进群密码和网桥IP请在文章下面回复以后，即可在文章顶部和底部看到 抱歉，本站暂不提供 Tor 网桥...
<!-- more -->
\[scode type="yellow"\]如果想直接看手机版教程的请加QQ群672027707，进群密码和网桥IP请在文章下面回复以后，即可在文章顶部和底部看到 抱歉，本站暂不提供 Tor 网桥，请自行翻墙到 [https://bridges.torproject.org/bridges](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9icmlkZ2VzLnRvcnByb2plY3Qub3JnL2JyaWRnZXM=) 获取网桥或连接代理使用\[/scode\]

> **Tor Project, Inc.** 是一家[位于西雅图](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvU2VhdHRsZQ==)的 501(c)(3) 研究教育[非营利组织，](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvTm9ucHJvZml0X29yZ2FuaXphdGlvbg==)由计算机科学家[Roger Dingledine](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvUm9nZXJfRGluZ2xlZGluZQ==)、[Nick Mathewson](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3cvaW5kZXgucGhwP3RpdGxlPU5pY2tfTWF0aGV3c29uJmFjdGlvbj1lZGl0JnJlZGxpbms9MQ==)和其他五人创立。Tor 项目主要负责维护[Tor](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvVG9yXyhhbm9ueW1pdHlfbmV0d29yaw==)) "Tor（匿名网络）")匿名网络的软件。\[\[4\]\]([https://en.wikipedia.org/wiki/The\_Tor\_Project#cite\_note-torproject-corepeople-4)](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9lbi53aWtpcGVkaWEub3JnL3dpa2kvVGhlX1Rvcl9Qcm9qZWN0I2NpdGVfbm90ZS10b3Jwcm9qZWN0LWNvcmVwZW9wbGUtNCk=)

Tor 网络就是我们所称的“暗网”。

其实暗网并不可怕，只是由特定算法来限制各种内容的获取与分享，只提供给部分有权限的人罢了。可怕的是有心之人在上面进行非法活动。

![Tor标志](https://old.blog.fwder.cn/usr/uploads/2021/06/2966061253.png "Tor标志")

\[scode type="red"\]本文章仅从技术方面讨论tor匿名网络的连接方法，请勿用作其他非法用途。本网站将不负任何责任。  
详见[用户协议](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9pbmRleC5waHAvYWJvdXQuaHRtbA==)。\[/scode\]

## 安装Tor Browser

### 下载地址

官方网站下载地址：  
[点此进入（需要科学上网）](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cudG9ycHJvamVjdC5vcmcvZG93bmxvYWQv)

为了让没有魔法工具的朋友也能使用Tor，我把各个系统的安装包都放在了我的OneDrive上，没有魔法工具的同学请在这里下载即可。  
[点此进入（适合没有魔法工具的朋友）](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9jbG91ZC5md2Rlci5jbi9Db2RlL1Rvci8=)  
在里面根据你的系统版本进行下载即可。

### 安装方法

在上面的链接下载对应系统的安装包，安装即可。

Windows：Tor Browser会自动安装到桌面上，如有需要可以更改安装路径。

Android：直接安装即可。

## 使用方法

### Windows

点击桌面上的“Start Tor Browser”。

![点击桌面图标](https://old.blog.fwder.cn/usr/uploads/2021/06/289439302.png "点击桌面图标")

打开Tor浏览器，首次使用会弹出以下页面：

![Tor引导页面](https://old.blog.fwder.cn/usr/uploads/2021/06/1252397552.png "Tor引导页面")

只要在中国肯定是不能直接访问Tor网络的，所以我们点击“配置”：

![Tor网络配置](https://old.blog.fwder.cn/usr/uploads/2021/06/3419395949.png "Tor网络配置")

**如果你有VPN：**

请使用你的VPN的监听端口来连接Tor网络。

以v2rayN为例子，打开v2rayN：

![v2rayN](https://old.blog.fwder.cn/usr/uploads/2021/06/299788166.png "v2rayN")

双击右下角的v2rayN图标：![双击点击](https://old.blog.fwder.cn/usr/uploads/2021/06/939112488.png "双击点击")

点击参数设置。

![点击“参数设置”](https://old.blog.fwder.cn/usr/uploads/2021/06/3631145852.png "点击“参数设置”")

根据图中箭头依次设置好v2rayN，端口可以更改为其他的端口。

![v2rayN代理设置](https://old.blog.fwder.cn/usr/uploads/2021/06/2492154574.png "v2rayN代理设置")

然后最小化v2rayN，再次打开Tor浏览器，选择“使用代理访问互联网”，填写地址和你刚刚设置的端口，连接即可进入。

![v2rayN代理设置](https://old.blog.fwder.cn/usr/uploads/2021/06/3915972068.png "v2rayN代理设置")

* * *

**如果你有VPN但不想使用VPN作为Tor的代理，想直接使用网桥：**

你可以进入 [https://bridges.torproject.org/bridges](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9icmlkZ2VzLnRvcnByb2plY3Qub3JnL2JyaWRnZXM=) 获取最新的共享网桥，配置方法见下。（此方法所获取的网桥大概率无法使用，请悉知）

**如果你想自己搭建网桥：**

去国外或者香港的云服务器提供商购买一个vps并参照官方文档搭建即可使用。

* * *

成功连接上Tor后，会出现如下图的页面：

![浏览器页面](https://old.blog.fwder.cn/usr/uploads/2021/06/1975337491.png "浏览器页面")

那么恭喜你，成功进入了Tor网络，你可以进行彻底的进行无痕浏览了。

* * *

\[scode type="red"\]本文章仅从技术方面讨论tor匿名网络的连接方法，请勿用作其他非法用途。本网站将不负任何责任。  
详见[用户协议](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9pbmRleC5waHAvYWJvdXQuaHRtbA==)。\[/scode\]

hide如果想直接看手机版教程的请加QQ群672027707，进群密码和网桥IP请在文章下面回复以后，即可在文章顶部和底部看到 抱歉，本站暂不提供 Tor 网桥，请自行翻墙到 [https://bridges.torproject.org/bridges](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9icmlkZ2VzLnRvcnByb2plY3Qub3JnL2JyaWRnZXM=) 获取网桥或连接代理使用/scode

> 本文资源全部来源于网络，请在下载之后24小时之内删除。