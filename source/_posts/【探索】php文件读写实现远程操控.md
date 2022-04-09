---
title: 【探索】php文件读写实现远程操控
categories:
  - 文档
tags:
  - PHP
excerpt: >-
  最近在学习php，掌握了一点小基础和语法，于是尝试直接使用表单+文件读写的方式来进行远程操控。（初学，代码可能不是那么大佬，勿喷）说明index.php
  --相当于input端，可以向服务器发送...
date: 2021-01-29 03:30:00
---

最近在学习php，掌握了一点小基础和语法，于是尝试直接使用表单+文件读写的方式来进行远程操控。（初学，代码可能不是那么大佬，勿喷）说明index.php --相当于input端，可以向服务器发送...
<!-- more -->
最近在学习php，掌握了一点小基础和语法，于是尝试直接使用表单+文件读写的方式来进行远程操控。  
**（初学，代码可能不是那么大佬，勿喷）**

#### 说明

![FKCRU~Z94Z51}R83HJUPJ6F.png](https://old.blog.fwder.cn/usr/uploads/2021/01/46261671.png "FKCRU~Z94Z51}R83HJUPJ6F.png")

index.php --相当于input端，可以向服务器发送数据，也可跳入json.php查看返回数据。  
json.php --查看返回数据。  
output.php --输出input的数据。  
return.php --output后return返回数据端。  
p2p.php,uploads --用于文件传输。  
updata,version.php --用于查询是否更新。  
json.txt --存储return信息。  
message.txt --存储input信息。

* * *

php端写好了，接下来就用python写个控制程序就可以了。

在写python操控程序上，我只添加了“弹出信息框”，如果可以的话还可以再加。

因为刚学写的太简陋了，所以就不发Github了。但还是要发在博客上记录一下。

睡觉去了。

下面这个是源码，请按照说明或者自看源代码使用。

[control.zip](https://old.blog.fwder.cn/usr/uploads/2021/01/4068788841.zip)