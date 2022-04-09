---
title: 【转载】一个纯用html画的铃仙
categories:
  - 分享
tags:
  - html
  - 东方Project
  - 铃仙
excerpt: >-
  这是一个纯用html绘画的铃仙，下面放效果图~前排说下这个html画铃仙不是我做的，是国外的一位东方厨大佬做的，我是从B站上转载的。b站的up主叫做：甘楽ぶんしょう这是他的个人空间。这是原视频的...
date: 2021-02-18 21:45:00
---

这是一个纯用html绘画的铃仙，下面放效果图~前排说下这个html画铃仙不是我做的，是国外的一位东方厨大佬做的，我是从B站上转载的。b站的up主叫做：甘楽ぶんしょう这是他的个人空间。这是原视频的...
<!-- more -->
![lingx.jpg](https://old.blog.fwder.cn/usr/uploads/2021/02/1328965460.jpg "lingx.jpg")

* * *

> 这是一个纯用html绘画的铃仙，下面放效果图~

![铃仙](https://old.blog.fwder.cn/usr/uploads/2021/02/1411511055.png "铃仙")

前排说下这个html画铃仙不是我做的，是国外的一位东方厨大佬做的，我是从B站上转载的。

b站的up主叫做：[甘楽ぶんしょう](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9zcGFjZS5iaWxpYmlsaS5jb20vMzgxODY3MDc=)这是他的个人空间。

这是[原视频](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cuYmlsaWJpbGkuY29tL3ZpZGVvL0JWMWY1NDExNzd5WQ==)的置顶评论：

> 身为一个合格的铃仙厨，看到这么多人也对源码感兴趣激起了我的好奇心，我印象中至少12年我就看过这个html绘铃仙的视频了，时隔多年再看见确实很想知道来源。我首先在YouTube上找到了最早上传的该视频，从上传作者处了解到转载源在niconico上，n站上可查询的最早发布的该视频是[https://www.nicovideo.jp/watch/sm336877](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cubmljb3ZpZGVvLmpwL3dhdGNoL3NtMzM2ODc3)，可惜视频已经被删。虽然最重要的原作者是谁我暂时没有结果，但巧的是我在Discord上和我一位荷兰的东方厨朋友求助时他告知我一位德国的东方众可能保有这段视频中出现的源代码，后来经他帮助我联系上了这位朋友，他给我提供了这段视频中的代码，我转存在（[https://gitee.com/touhousupport/codes/xyi6wszebom7u5rf8d0vh92](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9naXRlZS5jb20vdG91aG91c3VwcG9ydC9jb2Rlcy94eWk2d3N6ZWJvbTd1NXJmOGQwdmg5Mg==)）想要的朋友可以自取，最后异常感谢给我提供帮助的Jason Maurer和Maribel Hearn。  
> 顺便，前排向女朋友表白，她并没有吃醋

视频简介：

> 来源：[https://www.reddit.com/r/ProgrammerAnimemes/comments/l0adys/sweaty\_waifu\_drawing\_speedrun/](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cucmVkZGl0LmNvbS9yL1Byb2dyYW1tZXJBbmltZW1lcy9jb21tZW50cy9sMGFkeXMvc3dlYXR5X3dhaWZ1X2RyYXdpbmdfc3BlZWRydW4v)  
> meme来源：[https://knowyourmeme.com/memes/sweaty-speedrunner](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9rbm93eW91cm1lbWUuY29tL21lbWVzL3N3ZWF0eS1zcGVlZHJ1bm5lcg==)  
> 想看原版视频请移步 [https://www.bilibili.com/video/](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cuYmlsaWJpbGkuY29tL3ZpZGVvLw==)[BV1vK4y1Q7HF](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cuYmlsaWJpbGkuY29tL3ZpZGVvL0JWMXZLNHkxUTdIRg==)，感谢 @Megalo\_PaleWhite 的熟肉搬运～  
> 源代码放在 [https://gitee.com/touhousupport/reisen/blob/master/reisen.html](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9naXRlZS5jb20vdG91aG91c3VwcG9ydC9yZWlzZW4vYmxvYi9tYXN0ZXIvcmVpc2VuLmh0bWw=)，感谢寻找过程中给我提供帮助的给我提供帮助的Jason Maurer和Maribel Hearn。

up主将源代码转移到了gitee上，[链接在此](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cuYmlsaWJpbGkuY29tL3ZpZGVvL0JWMWY1NDExNzd5WQ==)，想要的朋友可以自取。

下面就是1000多行的源代码啦，密集恐惧症患者请回避：

```
<html>
<body bgcolor=000000>
<table boder=0 cellpadding=0 cellspacing=0>

<tr height=3>

<td width=3 bgcolor=888888 rowspan=105></td>
<td bgcolor=888888 colspan=54></td>
<td width=3 bgcolor=888888 rowspan=105></td>
</tr>
<tr height=3>

<td width=3 bgcolor=888888 rowspan=20></td>
<td bgcolor=888888 colspan=35></td>
<td bgcolor=72727d colspan=7></td>
<td width=3 bgcolor=888888></td>
<td width=3 bgcolor=888888 rowspan=2></td>
<td width=3 bgcolor=888888 rowspan=4></td>
<td width=3 bgcolor=888888 rowspan=5></td>
<td width=3 bgcolor=888888 rowspan=6></td>
<td width=3 bgcolor=888888 rowspan=7></td>
<td bgcolor=888888 colspan=2 rowspan=8></td>
<td width=3 bgcolor=888888 rowspan=9></td>
<td width=3 bgcolor=888888 rowspan=10></td>
<td width=3 bgcolor=888888 rowspan=11></td>
</tr>
<tr height=3>
<td width=3 bgcolor=888888 rowspan=15></td>
<td bgcolor=888888 colspan=33></td>
<td width=3 bgcolor=72727d></td>
<td bgcolor=ffffff colspan=6></td>
<td width=3 bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td width=3 bgcolor=888888 rowspan=12></td>
<td bgcolor=888888 colspan=31 rowspan=2></td>
<td width=3 bgcolor=72727d rowspan=2></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=ffffff colspan=7></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=72727d rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=ffffff colspan=9></td>
</tr>
<tr height=3>

<td width=3 bgcolor=888888 rowspan=8></td>
<td bgcolor=888888 colspan=29 rowspan=2></td>
<td width=3 bgcolor=72727d></td>
<td bgcolor=ffffff colspan=11></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td bgcolor=b5b5b5></td>
<td bgcolor=ffffff colspan=12></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td width=3 bgcolor=888888 rowspan=4></td>
<td bgcolor=888888 colspan=27></td>
<td width=3 bgcolor=72727d rowspan=4></td>
<td bgcolor=ffffff colspan=4></td>
<td width=3 bgcolor=532237></td>
<td width=3 bgcolor=b5b5b5></td>
<td bgcolor=ffffff colspan=8></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td width=3 bgcolor=888888 rowspan=2></td>
<td width=3 bgcolor=888888></td>
<td bgcolor=72727d colspan=8></td>
<td width=3 bgcolor=888888></td>
<td width=3 bgcolor=888888 rowspan=3></td>
<td bgcolor=888888 colspan=14 rowspan=5></td>
<td width=3 bgcolor=888888 rowspan=4></td>
<td bgcolor=ffffff rowspan=2></td>
<td bgcolor=ffffff></td>
<td bgcolor=b5b5b5 rowspan=2></td>
<td width=3 bgcolor=532237></td>
<td bgcolor=a23445 colspan=3></td>
<td width=3 bgcolor=b5b5b5></td>
<td bgcolor=ffffff colspan=7></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td bgcolor=72727d></td>
<td width=3 bgcolor=ffffff rowspan=8></td>
<td width=3 bgcolor=ffffff rowspan=7></td>
<td width=3 bgcolor=ffffff rowspan=6></td>
<td width=3 bgcolor=ffffff rowspan=5></td>
<td bgcolor=ffffff colspan=4 rowspan=3></td>
<td bgcolor=72727d rowspan=2></td>
<td bgcolor=b5b5b5 rowspan=4></td>
<td bgcolor=a23445 rowspan=3></td>
<td bgcolor=a23445 rowspan=2></td>
<td bgcolor=a23445></td>
<td bgcolor=532237 colspan=3></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=ffffff colspan=6></td>
<td bgcolor=72727d colspan=2></td>
</tr>
<tr height=3>

<td bgcolor=72727d></td>
<td bgcolor=ffffff rowspan=8></td>
<td bgcolor=b5b5b5 rowspan=6></td>
<td bgcolor=a23445 rowspan=4></td>
<td bgcolor=532237></td>
<td width=3 bgcolor=888888 rowspan=21></td>
<td bgcolor=888888 rowspan=29></td>
<td width=3 bgcolor=888888 rowspan=32></td>
<td bgcolor=888888 rowspan=34></td>
<td bgcolor=72727d></td>
<td bgcolor=b5b5b5 colspan=2></td>
<td bgcolor=ffffff colspan=5></td>
<td bgcolor=72727d rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=72727d rowspan=2></td>
<td bgcolor=ffffff rowspan=8></td>
<td bgcolor=b5b5b5 rowspan=5></td>
<td bgcolor=72727d rowspan=2></td>
<td bgcolor=b5b5b5 rowspan=7></td>
<td bgcolor=532237></td>
<td bgcolor=888888 rowspan=13></td>
<td bgcolor=888888 rowspan=36></td>
<td bgcolor=888888 rowspan=37></td>
<td bgcolor=72727d colspan=2></td>
<td bgcolor=b5b5b5 colspan=3></td>
<td bgcolor=ffffff colspan=2></td>
<td bgcolor=72727d rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=b5b5b5 colspan=4></td>
<td bgcolor=72727d rowspan=2></td>
<td bgcolor=532237 rowspan=2></td>
<td bgcolor=888888 rowspan=9></td>
<td bgcolor=888888 rowspan=39></td>
<td bgcolor=888888 rowspan=49></td>
<td bgcolor=888888 rowspan=51></td>
<td bgcolor=72727d colspan=3></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td bgcolor=72727d rowspan=2></td>
<td bgcolor=ffffff rowspan=7></td>
<td bgcolor=532237 colspan=2></td>
<td width=3 bgcolor=b5b5b5></td>
<td width=3 bgcolor=b5b5b5 rowspan=2></td>
<td bgcolor=b5b5b5 rowspan=5></td>
<td width=3 bgcolor=72727d rowspan=2></td>
<td bgcolor=888888 colspan=13></td>
<td bgcolor=a23445 rowspan=3></td>
<td bgcolor=888888 rowspan=54></td>
<td width=3 bgcolor=888888 rowspan=56></td>
<td width=3 bgcolor=888888 rowspan=78></td>
<td bgcolor=888888 rowspan=80></td>
<td bgcolor=888888 colspan=2 rowspan=91></td>
</tr>
<tr height=3>

<td bgcolor=b5b5b5></td>
<td bgcolor=a23445 colspan=3></td>
<td bgcolor=888888 colspan=12></td>
<td width=3 bgcolor=72727d></td>
<td bgcolor=b5b5b5 rowspan=5></td>
<td bgcolor=532237></td>
<td bgcolor=888888 rowspan=6></td>
</tr>
<tr height=3>

<td bgcolor=72727d rowspan=2></td>
<td bgcolor=ffffff rowspan=6></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=a23445 colspan=5></td>
<td bgcolor=b5b5b5 rowspan=5></td>
<td width=3 bgcolor=72727d rowspan=2></td>
<td bgcolor=888888 colspan=10></td>
<td width=3 bgcolor=72727d></td>
<td bgcolor=b5b5b5 rowspan=4></td>
<td bgcolor=888888 rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
<td bgcolor=532237 colspan=2></td>
<td bgcolor=a23445 colspan=4></td>
<td bgcolor=888888 colspan=2></td>
<td bgcolor=50485f colspan=7></td>
<td width=3 bgcolor=72727d rowspan=3></td>
<td bgcolor=b5b5b5 rowspan=3></td>
<td bgcolor=a23445></td>
<td bgcolor=532237></td>
</tr>
<tr height=3>

<td bgcolor=72727d rowspan=3></td>
<td bgcolor=ffffff rowspan=6></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=35></td>
<td bgcolor=888888 rowspan=10></td>
<td width=3 bgcolor=888888 rowspan=7></td>
<td bgcolor=532237 colspan=2></td>
<td bgcolor=a23445></td>
<td bgcolor=a23445 rowspan=2></td>
<td bgcolor=b5b5b5 rowspan=6></td>
<td width=3 bgcolor=72727d rowspan=2></td>
<td width=3 bgcolor=6e5d80></td>
<td bgcolor=b49cba colspan=7></td>
<td bgcolor=72727d></td>
<td bgcolor=888888></td>
</tr>
<tr height=3>

<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=40></td>
<td width=3 bgcolor=888888 rowspan=4></td>
<td bgcolor=888888 rowspan=3></td>
<td bgcolor=532237></td>
<td bgcolor=a23445 rowspan=3></td>
<td bgcolor=b49cba colspan=8></td>
<td bgcolor=b49cba colspan=2></td>
<td bgcolor=50485f></td>
</tr>
<tr height=3>

<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=44></td>
<td bgcolor=888888></td>
<td bgcolor=532237></td>
<td bgcolor=b5b5b5 rowspan=3></td>
<td bgcolor=72727d rowspan=3></td>
<td bgcolor=b49cba colspan=10 rowspan=2></td>
<td bgcolor=e7d9f5 colspan=3></td>
<td bgcolor=b49cba></td>
<td bgcolor=50485f></td>
</tr>
<tr height=3>

<td bgcolor=ffffff rowspan=5></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=46></td>
<td bgcolor=50485f></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=a23445 rowspan=3></td>
<td bgcolor=e7d9f5 colspan=4></td>
<td bgcolor=b49cba></td>
<td bgcolor=50485f></td>
</tr>
<tr height=3>

<td bgcolor=72727d rowspan=6></td>
<td bgcolor=b5b5b5 rowspan=2></td>
<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=69></td>
<td bgcolor=50485f></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=e7d9f5 rowspan=3></td>
<td bgcolor=b49cba colspan=9></td>
<td bgcolor=e7d9f5 colspan=6></td>
<td bgcolor=b49cba></td>
<td bgcolor=50485f></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=69></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=6e5d80></td>
<td bgcolor=e7d9f5 rowspan=3></td>
<td bgcolor=72727d></td>
<td bgcolor=e7d9f5 colspan=3></td>
<td bgcolor=b49cba colspan=5></td>
<td bgcolor=e7d9f5 colspan=6></td>
<td bgcolor=ffffff rowspan=2></td>
<td bgcolor=e7d9f5></td>
<td bgcolor=e7d9f5 rowspan=4></td>
<td bgcolor=6e5d80></td>
</tr>
<tr height=3>

<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=e7d9f5 rowspan=10></td>
<td bgcolor=e7d9f5 colspan=17></td>
<td bgcolor=ffffff rowspan=2></td>
<td bgcolor=b49cba></td>
</tr>
<tr height=3>

<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=69></td>
<td bgcolor=50485f rowspan=3></td>
<td bgcolor=6e5d80></td>
<td bgcolor=ffffff colspan=2 rowspan=4></td>
<td bgcolor=e7d9f5 colspan=12></td>
<td bgcolor=b49cba></td>
<td bgcolor=e7d9f5></td>
<td bgcolor=ffffff rowspan=3></td>
<td bgcolor=b49cba></td>
<td bgcolor=b49cba rowspan=6></td>
<td bgcolor=e7d9f5 rowspan=3></td>
<td bgcolor=50485f rowspan=7></td>
</tr>
<tr height=3>

<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=77></td>
<td bgcolor=b49cba rowspan=4></td>
<td bgcolor=e7d9f5 rowspan=12></td>
<td bgcolor=ffffff rowspan=2></td>
<td bgcolor=e7d9f5></td>
<td bgcolor=e7d9f5 rowspan=6></td>
<td bgcolor=ffffff colspan=2 rowspan=3></td>
<td bgcolor=e7d9f5 colspan=3></td>
<td width=3 bgcolor=ffffff rowspan=2></td>
<td width=3 bgcolor=ffffff></td>
<td width=3 bgcolor=50485f rowspan=5></td>
<td bgcolor=b49cba></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=6e5d80></td>
<td bgcolor=b49cba></td>
<td bgcolor=ffffff rowspan=2></td>
<td bgcolor=e7d9f5 rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=77></td>
<td bgcolor=ffffff rowspan=2></td>
<td bgcolor=ffffff colspan=2></td>
<td width=3 bgcolor=6e5d80></td>
<td bgcolor=e7d9f5></td>
<td bgcolor=6e5d80></td>
<td bgcolor=50485f></td>
<td bgcolor=6e5d80></td>
<td bgcolor=b49cba rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=77></td>
<td bgcolor=50485f rowspan=7></td>
<td bgcolor=6e5d80></td>
<td bgcolor=e7d9f5 rowspan=4></td>
<td width=3 bgcolor=b49cba></td>
<td width=3 bgcolor=6e5d80></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=e7d9f5></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=50485f></td>
<td bgcolor=6e5d80></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=50485f></td>
<td bgcolor=6e5d80></td>
<td bgcolor=e7d9f5></td>
<td bgcolor=b49cba rowspan=8></td>
</tr>
<tr height=3>

<td bgcolor=b49cba rowspan=5></td>
<td bgcolor=e7d9f5 rowspan=7></td>
<td bgcolor=e7d9f5 rowspan=4></td>
<td bgcolor=e7d9f5 rowspan=3></td>
<td bgcolor=e7d9f5></td>
<td width=3 bgcolor=b49cba rowspan=2></td>
<td bgcolor=6e5d80></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=c26b59 rowspan=3></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=c26b59></td>
<td bgcolor=50485f></td>
<td bgcolor=b49cba></td>
</tr>
<tr height=3>

<td bgcolor=e7d9f5 rowspan=6></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=50485f></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=6e5d80></td>
<td bgcolor=532237 colspan=2></td>
<td bgcolor=c26b59></td>
<td bgcolor=6e5d80></td>
<td bgcolor=b49cba rowspan=6></td>
</tr>
<tr height=3>

<td bgcolor=532237 colspan=3></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=c26b59></td>
<td bgcolor=532237 colspan=5></td>
<td bgcolor=50485f></td>
<td bgcolor=6e5d80 rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=b49cba rowspan=4></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=b49cba></td>
<td bgcolor=532237 colspan=5></td>
<td bgcolor=e1a08 colspan=2></td>
<td bgcolor=c26b59></td>
<td bgcolor=532237 rowspan=4></td>
<td bgcolor=ffffff></td>
<td bgcolor=532237></td>
<td bgcolor=6e5d80 rowspan=4></td>
<td bgcolor=b49cba rowspan=9></td>
<td bgcolor=6e5d80 rowspan=2></td>
<td bgcolor=50485f rowspan=8></td>
</tr>
<tr height=3>

<td bgcolor=b49cba rowspan=8></td>
<td bgcolor=532237 colspan=2></td>
<td bgcolor=72343e rowspan=4></td>
<td bgcolor=532237 rowspan=5></td>
<td bgcolor=ffffff></td>
<td bgcolor=532237></td>
<td bgcolor=e1a08></td>
<td bgcolor=fac9b colspan=3></td>
<td bgcolor=fac9b rowspan=3></td>
<td bgcolor=e1a08></td>
<td bgcolor=872814 rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80 rowspan=2></td>
<td bgcolor=b49cba rowspan=9></td>
<td bgcolor=532237 colspan=3></td>
<td bgcolor=72343e rowspan=2></td>
<td bgcolor=ffffff></td>
<td bgcolor=fac9b></td>
<td bgcolor=ffebdc colspan=3></td>
<td bgcolor=fac9b rowspan=5></td>
<td bgcolor=b49cba rowspan=7></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=16></td>
<td bgcolor=b49cba rowspan=4></td>
<td bgcolor=b49cba rowspan=6></td>
<td bgcolor=6e5d80 rowspan=3></td>
<td bgcolor=ffebdc colspan=5 rowspan=4></td>
<td bgcolor=e1a08 rowspan=3></td>
<td bgcolor=50485f></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=2></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=6e5d80 rowspan=14></td>
<td bgcolor=b49cba rowspan=3></td>
<td bgcolor=532237 rowspan=2></td>
<td bgcolor=ffebdc rowspan=3></td>
<td bgcolor=fac9b rowspan=4></td>
<td bgcolor=872814 rowspan=2></td>
<td bgcolor=6e5d80></td>
<td bgcolor=b49cba rowspan=4></td>
<td bgcolor=6e5d80 rowspan=7></td>
</tr>
<tr height=3>

<td bgcolor=532237></td>
<td bgcolor=50485f rowspan=6></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=7></td>
<td bgcolor=50485f rowspan=7></td>
<td bgcolor=b49cba rowspan=2></td>
<td bgcolor=50485f rowspan=6></td>
<td bgcolor=e1a08></td>
<td bgcolor=fac9b></td>
<td bgcolor=ffebdc></td>
<td bgcolor=872814></td>
<td bgcolor=6e5d80 rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80 rowspan=10></td>
<td bgcolor=6e5d80 rowspan=8></td>
<td bgcolor=c26b59></td>
<td bgcolor=e1a08></td>
<td bgcolor=fac9b></td>
<td bgcolor=ffebdc colspan=3></td>
<td bgcolor=d78773></td>
<td bgcolor=ffebdc></td>
<td bgcolor=fac9b></td>
<td bgcolor=872814></td>
<td bgcolor=6e5d80 rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80 rowspan=16></td>
<td bgcolor=872814></td>
<td bgcolor=c26b59></td>
<td bgcolor=e1a08></td>
<td bgcolor=fac9b colspan=5></td>
<td bgcolor=872814 colspan=2></td>
<td bgcolor=6e5d80></td>
<td bgcolor=6e5d80 rowspan=2></td>
<td bgcolor=6e5d80 rowspan=7></td>
<td bgcolor=50485f rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80 rowspan=7></td>
<td bgcolor=6e5d80 rowspan=5></td>
<td bgcolor=6e5d80 rowspan=3></td>
<td bgcolor=6e5d80 rowspan=2></td>
<td bgcolor=872814 rowspan=2></td>
<td bgcolor=c26b59></td>
<td bgcolor=9b4637 colspan=2></td>
<td bgcolor=e1a08></td>
<td bgcolor=dddddd></td>
<td bgcolor=b5b5b5 rowspan=2></td>
<td bgcolor=30150a colspan=3></td>
<td bgcolor=3f292e></td>
<td bgcolor=50485f></td>
<td bgcolor=6e5d80 rowspan=7></td>
</tr>
<tr height=3>

<td bgcolor=d78773></td>
<td bgcolor=e1a08 rowspan=2></td>
<td bgcolor=e1a08></td>
<td bgcolor=ffffff rowspan=3></td>
<td bgcolor=ffffff rowspan=2></td>
<td bgcolor=3f292e></td>
<td bgcolor=4c3b3e rowspan=7></td>
<td bgcolor=4c3b3e rowspan=8></td>
<td bgcolor=4c3b3e rowspan=11></td>
<td bgcolor=3f292e></td>
<td bgcolor=50485f rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80 rowspan=14></td>
<td bgcolor=4c4c4c rowspan=2></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=dddddd rowspan=3></td>
<td bgcolor=d78773></td>
<td bgcolor=72606e rowspan=5></td>
<td bgcolor=4c3b3e rowspan=3></td>
<td bgcolor=4c3b3e rowspan=11></td>
<td bgcolor=30150a></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=6e5d80 rowspan=3></td>
<td bgcolor=50485f rowspan=5></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80></td>
<td bgcolor=30150a></td>
<td bgcolor=dddddd></td>
<td bgcolor=a23445></td>
<td bgcolor=dddddd></td>
<td bgcolor=dddddd></td>
<td bgcolor=3f292e></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=4></td>
<td bgcolor=6e5d80 rowspan=9></td>
<td bgcolor=30150a></td>
<td bgcolor=72606e rowspan=2></td>
<td bgcolor=72606e rowspan=4></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=72343e></td>
<td bgcolor=532237></td>
<td bgcolor=dddddd></td>
<td bgcolor=4c3b3e rowspan=2></td>
<td bgcolor=4c3b3e rowspan=11></td>
<td bgcolor=30150a></td>
<td bgcolor=6e5d80 rowspan=2></td>
<td bgcolor=50485f rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=30150a></td>
<td bgcolor=4c3b3e rowspan=2></td>
<td bgcolor=4c3b3e></td>
<td bgcolor=a23445 colspan=2 rowspan=2></td>
<td bgcolor=72343e rowspan=3></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=30150a rowspan=2></td>
<td bgcolor=3f292e></td>
<td bgcolor=50485f rowspan=6></td>
</tr>
<tr height=3>

<td bgcolor=30150a></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=3f292e></td>
<td bgcolor=4c3b3e></td>
<td bgcolor=72606e rowspan=2></td>
<td bgcolor=4c3b3e rowspan=11></td>
<td bgcolor=30150a></td>
<td bgcolor=50485f rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=30150a></td>
<td bgcolor=4c3b3e rowspan=4></td>
<td bgcolor=30150a rowspan=2></td>
<td bgcolor=72606e rowspan=2></td>
<td bgcolor=3f292e></td>
<td bgcolor=72343e rowspan=2></td>
<td bgcolor=72606e rowspan=2></td>
<td bgcolor=30150a></td>
<td bgcolor=3f292e rowspan=7></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=50485f></td>
<td bgcolor=888888 rowspan=2></td>
<td bgcolor=50485f rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80 rowspan=3></td>
<td bgcolor=30150a></td>
<td bgcolor=3f292e></td>
<td bgcolor=4c3b3e rowspan=2></td>
<td bgcolor=4c3b3e></td>
<td bgcolor=3f292e></td>
<td bgcolor=72606e rowspan=2></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=30150a></td>
<td bgcolor=4c3b3e rowspan=5></td>
<td bgcolor=3f292e></td>
<td bgcolor=30150a></td>
<td bgcolor=888888 rowspan=3></td>
<td bgcolor=50485f rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=30150a rowspan=4></td>
<td bgcolor=4c3b3e rowspan=3></td>
<td bgcolor=4c3b3e rowspan=4></td>
<td bgcolor=3f292e rowspan=5></td>
<td bgcolor=30150a rowspan=5></td>
<td bgcolor=4c3b3e rowspan=2></td>
<td bgcolor=3f292e></td>
<td bgcolor=72606e></td>
<td bgcolor=30150a></td>
<td bgcolor=4c3b3e rowspan=5></td>
<td bgcolor=30150a></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=4c3b3e rowspan=11></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=50485f rowspan=3></td>
<td bgcolor=888888 rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=32></td>
<td bgcolor=3f292e rowspan=5></td>
<td bgcolor=4c3b3e rowspan=7></td>
<td bgcolor=3f292e colspan=2></td>
<td bgcolor=4c3b3e colspan=2 rowspan=6></td>
<td bgcolor=3f292e rowspan=3></td>
<td bgcolor=30150a></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=30></td>
<td bgcolor=3f292e rowspan=4></td>
<td bgcolor=30150a></td>
<td bgcolor=30150a rowspan=3></td>
<td bgcolor=4c3b3e></td>
<td bgcolor=30150a rowspan=3></td>
<td bgcolor=4c3b3e rowspan=10></td>
<td bgcolor=3f292e></td>
<td bgcolor=30150a></td>
<td bgcolor=50485f rowspan=3></td>
<td bgcolor=50485f rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=16></td>
<td bgcolor=3f292e></td>
<td bgcolor=3f292e></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=4c3b3e rowspan=9></td>
<td bgcolor=3f292e></td>
<td bgcolor=30150a></td>
<td bgcolor=888888 rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=28></td>
<td bgcolor=6e5d80 rowspan=3></td>
<td bgcolor=30150a></td>
<td bgcolor=3f292e></td>
<td bgcolor=4c3b3e rowspan=3></td>
<td bgcolor=4c3b3e></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=30150a></td>
<td bgcolor=3f292e rowspan=3></td>
<td bgcolor=4c3b3e rowspan=8></td>
<td bgcolor=3f292e rowspan=2></td>
<td bgcolor=50485f rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=6e5d80></td>
<td bgcolor=30150a></td>
<td bgcolor=30150a></td>
<td bgcolor=4c3b3e rowspan=2></td>
<td bgcolor=3f292e></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=3f292e></td>
<td bgcolor=30150a colspan=4></td>
<td bgcolor=30150a></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=25></td>
<td bgcolor=50485f rowspan=8></td>
<td bgcolor=50485f rowspan=6></td>
<td bgcolor=30150a></td>
<td bgcolor=30150a rowspan=2></td>
<td bgcolor=4c3b3e></td>
<td bgcolor=4c3b3e rowspan=2></td>
<td bgcolor=30150a rowspan=3></td>
<td bgcolor=30150a></td>
<td bgcolor=a98064></td>
<td bgcolor=d2a986 colspan=4></td>
<td bgcolor=3f292e rowspan=4></td>
<td bgcolor=4c3b3e rowspan=6></td>
<td bgcolor=3f292e></td>
<td bgcolor=30150a></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=888888 rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=23></td>
<td bgcolor=50485f rowspan=8></td>
<td bgcolor=50485f rowspan=3></td>
<td bgcolor=3f292e colspan=3></td>
<td bgcolor=30150a colspan=2></td>
<td bgcolor=a98064></td>
<td bgcolor=8a465a></td>
<td bgcolor=f5ddc1 rowspan=4></td>
<td bgcolor=f5ddc1 rowspan=6></td>
<td bgcolor=f5ddc1 rowspan=10></td>
<td bgcolor=d2a986></td>
<td bgcolor=30150a rowspan=2></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=3f292e rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=3f292e></td>
<td bgcolor=d2a986 colspan=2 rowspan=2></td>
<td bgcolor=8a465a rowspan=2></td>
<td bgcolor=3f292e colspan=2></td>
<td bgcolor=8a465a rowspan=4></td>
<td bgcolor=a98064 rowspan=2></td>
<td bgcolor=d2a986></td>
<td bgcolor=a98064 rowspan=4></td>
<td bgcolor=f5ddc1 rowspan=8></td>
<td bgcolor=3f292e rowspan=4></td>
<td bgcolor=4c3b3e rowspan=3></td>
<td bgcolor=30150a rowspan=2></td>
<td bgcolor=50485f rowspan=6></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=12></td>
<td bgcolor=8a465a></td>
<td bgcolor=d2a986 colspan=2></td>
<td bgcolor=a98064 rowspan=7></td>
<td bgcolor=f5ddc1 rowspan=4></td>
<td bgcolor=f5ddc1 rowspan=5></td>
</tr>
<tr height=3>

<td bgcolor=8a465a></td>
<td bgcolor=d2a986></td>
<td bgcolor=f5ddc1 rowspan=4></td>
<td bgcolor=f5ddc1></td>
<td bgcolor=a98064></td>
<td bgcolor=f5ddc1 rowspan=6></td>
<td bgcolor=f5ddc1></td>
<td bgcolor=d2a986 rowspan=7></td>
<td bgcolor=30150a rowspan=3></td>
<td bgcolor=30150a></td>
<td bgcolor=50485f rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=d2a986 rowspan=2></td>
<td bgcolor=f5ddc1 rowspan=6></td>
<td bgcolor=a98064 rowspan=3></td>
<td bgcolor=f5ddc1 rowspan=7></td>
<td bgcolor=d2a986 rowspan=6></td>
<td bgcolor=d2a986></td>
<td bgcolor=3f292e></td>
<td bgcolor=30150a></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td bgcolor=8a465a></td>
<td bgcolor=d2a986 rowspan=3></td>
<td bgcolor=f5ddc1 rowspan=4></td>
<td bgcolor=a98064 rowspan=4></td>
<td bgcolor=3f292e colspan=4></td>
<td bgcolor=30150a colspan=2></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=50485f rowspan=4></td>
</tr>
<tr height=3>

<td bgcolor=d2a986 rowspan=5></td>
<td bgcolor=f5ddc1 rowspan=4></td>
<td bgcolor=d2a986 rowspan=6></td>
<td bgcolor=d2a986 rowspan=3></td>
<td bgcolor=d2a986 rowspan=5></td>
<td bgcolor=30150a colspan=2></td>
<td bgcolor=b5b5b5 colspan=4></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=c26b59></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=10></td>
<td bgcolor=8a465a></td>
<td bgcolor=a98064 rowspan=3></td>
<td bgcolor=f5ddc1 rowspan=4></td>
<td bgcolor=d2a986 rowspan=5></td>
<td bgcolor=72727d></td>
<td bgcolor=b5b5b5 colspan=3></td>
<td bgcolor=72727d></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=c26b59></td>
<td bgcolor=fac9b rowspan=3></td>
<td bgcolor=c26b59></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=50485f rowspan=9></td>
</tr>
<tr height=3>

<td bgcolor=8a465a rowspan=2></td>
<td bgcolor=d2a986 rowspan=2></td>
<td bgcolor=a98064 rowspan=5></td>
<td bgcolor=4c4c4c colspan=2></td>
<td bgcolor=72727d colspan=2></td>
<td bgcolor=c26b59></td>
<td bgcolor=fac9b></td>
<td bgcolor=ffebdc rowspan=7></td>
<td bgcolor=fac9b rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=d2a986 rowspan=2></td>
<td bgcolor=8a465a rowspan=3></td>
<td bgcolor=d2a986 rowspan=4></td>
<td bgcolor=f5ddc1></td>
<td bgcolor=a98064 rowspan=3></td>
<td bgcolor=d2a986 rowspan=3></td>
<td bgcolor=d2a986></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=c26b59></td>
<td bgcolor=fac9b rowspan=2></td>
<td bgcolor=ffebdc rowspan=2></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=9b4637 rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=9></td>
<td bgcolor=50485f rowspan=12></td>
<td bgcolor=8a465a></td>
<td bgcolor=d2a986 rowspan=2></td>
<td bgcolor=8a465a rowspan=2></td>
<td bgcolor=d2a986></td>
<td bgcolor=a98064 rowspan=2></td>
<td bgcolor=a98064 rowspan=3></td>
<td bgcolor=d2a986 rowspan=3></td>
<td bgcolor=d2a986 rowspan=2></td>
<td bgcolor=a98064></td>
<td bgcolor=ffebdc rowspan=3></td>
<td bgcolor=fac9b></td>
<td bgcolor=c26b59 rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=50485f rowspan=5></td>
<td bgcolor=8a465a></td>
<td bgcolor=d2a986 colspan=3></td>
<td bgcolor=a98064></td>
<td bgcolor=a98064></td>
<td bgcolor=9b4637 rowspan=3></td>
<td bgcolor=ffebdc rowspan=3></td>
<td bgcolor=ffebdc></td>
<td bgcolor=e1a08></td>
<td bgcolor=fac9b></td>
<td bgcolor=c26b59></td>
<td bgcolor=9b4637></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=50485f rowspan=7></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=5></td>
<td bgcolor=9b4637 rowspan=3></td>
<td bgcolor=8a465a colspan=8></td>
<td bgcolor=a98064></td>
<td bgcolor=8a465a></td>
<td bgcolor=a98064 colspan=2></td>
<td bgcolor=8a465a colspan=2></td>
<td bgcolor=9b4637 colspan=2></td>
<td bgcolor=e1a08></td>
<td bgcolor=fac9b rowspan=3></td>
<td bgcolor=9b4637 rowspan=3></td>
<td bgcolor=50485f rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=c26b59 colspan=6></td>
<td bgcolor=872814 rowspan=4></td>
<td bgcolor=50485f rowspan=17></td>
<td bgcolor=8a465a colspan=2></td>
<td bgcolor=a98064 colspan=3></td>
<td bgcolor=8a465a colspan=3></td>
<td bgcolor=c26b59 colspan=2></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=50485f rowspan=10></td>
<td bgcolor=50485f rowspan=11></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=888888 rowspan=2></td>
<td bgcolor=50485f rowspan=8></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=19></td>
<td bgcolor=d78773 colspan=4></td>
<td bgcolor=c26b59></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=50485f rowspan=17></td>
<td bgcolor=50485f rowspan=14></td>
<td bgcolor=8a465a colspan=3></td>
<td bgcolor=c26b59 colspan=2></td>
<td bgcolor=fac9b colspan=2></td>
<td bgcolor=fac9b rowspan=4></td>
<td bgcolor=e1a08></td>
<td bgcolor=9b4637></td>
</tr>
<tr height=3>

<td bgcolor=d78773 rowspan=3></td>
<td bgcolor=e1a08 rowspan=9></td>
<td bgcolor=e1a08 rowspan=8></td>
<td bgcolor=e1a08 colspan=2 rowspan=2></td>
<td bgcolor=d78773 rowspan=4></td>
<td bgcolor=50485f rowspan=10></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=fac9b rowspan=3></td>
<td bgcolor=ffebdc colspan=3></td>
<td bgcolor=fac9b rowspan=7></td>
<td bgcolor=872814 rowspan=2></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=50485f rowspan=10></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=ffebdc rowspan=2></td>
<td bgcolor=fac9b rowspan=2></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=50485f rowspan=9></td>
</tr>
<tr height=3>

<td bgcolor=9b4637 rowspan=4></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=ffebdc colspan=3></td>
<td bgcolor=888888></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=16></td>
<td bgcolor=50485f rowspan=10></td>
<td bgcolor=d78773></td>
<td bgcolor=d78773 rowspan=6></td>
<td bgcolor=50485f rowspan=14></td>
<td bgcolor=50485f rowspan=12></td>
<td bgcolor=9b4637></td>
<td bgcolor=fac9b rowspan=3></td>
<td bgcolor=fac9b colspan=2></td>
<td bgcolor=c26b59 rowspan=3></td>
<td bgcolor=9b4637 rowspan=2></td>
<td bgcolor=50485f rowspan=10></td>
<td bgcolor=9b4637 colspan=3></td>
<td bgcolor=888888></td>
</tr>
<tr height=3>

<td bgcolor=e1a08 rowspan=6></td>
<td bgcolor=e1a08 rowspan=3></td>
<td bgcolor=872814></td>
<td bgcolor=872814></td>
<td bgcolor=c26b59 rowspan=2></td>
<td bgcolor=ffebdc rowspan=4></td>
<td bgcolor=ffebdc rowspan=7></td>
<td bgcolor=ffebdc rowspan=8></td>
<td bgcolor=50485f rowspan=10></td>
<td bgcolor=50485f rowspan=6></td>
<td bgcolor=50485f rowspan=8></td>
<td bgcolor=50485f rowspan=7></td>
<td bgcolor=888888 rowspan=16></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=15></td>
<td bgcolor=9b4637></td>
<td bgcolor=50485f rowspan=12></td>
<td bgcolor=50485f rowspan=11></td>
<td bgcolor=872814 rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=d78773 rowspan=4></td>
<td bgcolor=872814 rowspan=3></td>
<td bgcolor=9b4637</td>
<td bgcolor=c26b59 rowspan=3></td>
<td bgcolor=e1a08 rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=d78773 rowspan=4></td>
<td bgcolor=872814></td>
<td bgcolor=888888 rowspan=13></td>
</tr>
<tr height=3>

<td bgcolor=9b4637 rowspan=3></td>
<td bgcolor=50485f rowspan=9></td>
<td bgcolor=fac9b></td>
<td bgcolor=ffebdc rowspan=4></td>
<td bgcolor=fac9b rowspan=4></td>
<td bgcolor=c26b59 rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c></td>
<td bgcolor=d78773></td>
<td bgcolor=9b4637></td>
<td bgcolor=50485f rowspan=3></td>
<td bgcolor=9b4637></td>
<td bgcolor=e1a08></td>
<td bgcolor=9b4637></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c></td>
<td bgcolor=b5b5b5 rowspan=2></td>
<td bgcolor=c26b59></td>
<td bgcolor=d78773 colspan=3></td>
<td bgcolor=872814 rowspan=2></td>
<td bgcolor=872814></td>
<td bgcolor=c26b59></td>
<td bgcolor=e1a08 rowspan=4></td>
<td bgcolor=872814 rowspan=3></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=888888 rowspan=8></td>
<td bgcolor=888888 rowspan=9></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=6></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=72727d></td>
<td bgcolor=72727d></td>
<td bgcolor=c26b59 colspan=5></td>
<td bgcolor=888888 rowspan=4></td>
<td bgcolor=50485f rowspan=2></td>
<td bgcolor=9b4637></td>
<td bgcolor=fac9b></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=72727d></td>
<td bgcolor=888888 rowspan=8></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=6></td>
<td bgcolor=72727d rowspan=2></td>
<td bgcolor=b5b5b5 colspan=3></td>
<td bgcolor=72727d colspan=2></td>
<td bgcolor=b5b5b5 colspan=2></td>
<td bgcolor=72727d colspan=2 rowspan=2></td>
<td bgcolor=4c4c4c rowspan=5></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=e1a08></td>
<td bgcolor=fac9b colspan=3></td>
<td bgcolor=dddddd rowspan=2></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=888888 rowspan=6></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=5></td>
<td bgcolor=b5b5b5 colspan=7></td>
<td bgcolor=4c4c4c rowspan=4></td>
<td bgcolor=dddddd rowspan=3></td>
<td bgcolor=c26b59></td>
<td bgcolor=e1a08 colspan=3></td>
<td bgcolor=d78773></td>
<td bgcolor=dddddd rowspan=3></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c rowspan=3></td>
<td bgcolor=b5b5b5 colspan=6></td>
<td bgcolor=72727d colspan=3></td>
<td bgcolor=888888></td>
<td bgcolor=dddddd></td>
<td bgcolor=ffffff></td>
<td bgcolor=c26b59 colspan=3></td>
<td bgcolor=ffffff colspan=2></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=888888 rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c colspan=2></td>
<td bgcolor=72727d colspan=6></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=4c4c4c colspan=3></td>
<td bgcolor=ffffff colspan=7></td>
<td bgcolor=4c4c4c rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=72727d colspan=3></td>
<td bgcolor=4c4c4c colspan=6></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=4c4c4c colspan=4></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=ffffff colspan=5></td>
<td bgcolor=dddddd colspan=2></td>
<td bgcolor=72727d></td>
</tr>
<tr height=3>

<td bgcolor=532237></td>
<td bgcolor=72343e></td>
<td bgcolor=72727d colspan=4></td>
<td bgcolor=72343e colspan=3 rowspan=3></td>
<td bgcolor=532237 rowspan=5></td>
<td bgcolor=4c4c4c colspan=14 rowspan=9></td>
<td bgcolor=dddddd colspan=5></td>
<td bgcolor=72727d></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=b5b5b5></td>
<td bgcolor=4c4c4c</td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c></td>
<td bgcolor=532237 rowspan=3></td>
<td bgcolor=72343e colspan=5></td>
<td bgcolor=532237 rowspan=2></td>
<td bgcolor=4c4c4c colspan=3></td>
<td bgcolor=72727d></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=b5b5b5 colspan=2></td>
<td bgcolor=72727d></td>
<td bgcolor=72343e></td>
<td bgcolor=532237></td>
<td bgcolor=4c4c4c></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c></td>
<td bgcolor=532237 colspan=2></td>
<td bgcolor=72343e colspan=4></td>
<td bgcolor=532237></td>
<td bgcolor=532237 rowspan=4></td>
<td bgcolor=72343e rowspan=2></td>
<td bgcolor=a23445 rowspan=6></td>
<td bgcolor=72727d colspan=4></td>
<td bgcolor=a23445></td>
<td bgcolor=532237></td>
<td bgcolor=a23445></td>
<td bgcolor=532237></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=4c4c4c rowspan=2></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c></td>
<td bgcolor=532237 colspan=3></td>
<td bgcolor=72343e></td>
<td bgcolor=532237 colspan=4></td>
<td bgcolor=72343e colspan=5></td>
<td bgcolor=a23445 rowspan=6></td>
<td bgcolor=532237 rowspan=2></td>
<td bgcolor=a23445 colspan=4 rowspan=2></td>
<td bgcolor=532237 rowspan=2></td>
<td bgcolor=a23445 rowspan=2></td>
<td bgcolor=532237></td>
<td bgcolor=4c4c4c rowspan=2></td>
<td bgcolor=4c4c4c rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c rowspan=7></td>
<td bgcolor=532237 rowspan=5></td>
<td bgcolor=532237></td>
<td bgcolor=72343e colspan=13></td>
<td bgcolor=532237 rowspan=4></td>
<td bgcolor=a23445></td>
<td bgcolor=532237></td>
<td bgcolor=4c4c4c rowspan=7></td>
</tr>
<tr height=3>

<td bgcolor=72343e colspan=12></td>
<td bgcolor=532237 colspan=3></td>
<td bgcolor=a23445></td>
<td bgcolor=532237 colspan=4></td>
<td bgcolor=a23445 colspan=4></td>
<td bgcolor=532237></td>
</tr>
<tr height=3>

<td bgcolor=4c4c4c rowspan=3></td>
<td bgcolor=72343e colspan=10></td>
<td bgcolor=532237 colspan=5 rowspan=3></td>
<td bgcolor=4c4c4c rowspan=3></td>
<td bgcolor=a23445 colspan=10 rowspan=4></td>
<td bgcolor=532237 rowspan=4></td>
<td bgcolor=4c4c4c rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=532237></td>
<td bgcolor=72343e colspan=6></td>
<td bgcolor=532237 colspan=3></td>
</tr>
<tr height=3>

<td bgcolor=532237 colspan=7></td>
<td bgcolor=4c4c4c colspan=3></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=532237 rowspan=3></td>
</tr>
<tr height=3>

<td bgcolor=888888 rowspan=5></td>
<td bgcolor=4c4c4c colspan=32 rowspan=2></td>
<td bgcolor=532237></td>
<td bgcolor=888888 rowspan=7></td>
</tr>
<tr height=3>

<td bgcolor=532237 colspan=11 rowspan=2></td>
<td bgcolor=532237></td>
</tr>
<tr height=3>

<td bgcolor=888888></td>
<td bgcolor=4c4c4c colspan=33></td>
<td bgcolor=4c4c4c></td>
<td bgcolor=888888></td>
</tr>
<tr height=3>

<td bgcolor=888888 colspan=3></td>
<td bgcolor=4c4c4c colspan=41></td>
<td bgcolor=888888 colspan=3></td>
</tr>
<tr height=3>

<td bgcolor=888888 colspan=5></td>
<td bgcolor=4c4c4c colspan=37></td>
<td bgcolor=888888 colspan=5></td>
</tr>
<tr height=3>

<td bgcolor=888888 colspan=8></td>
<td bgcolor=4c4c4c colspan=33></td>
<td bgcolor=888888 colspan=7></td>
</tr>
<tr height=3>

<td bgcolor=888888 colspan=12></td>
<td bgcolor=4c4c4c colspan=27></td>
<td bgcolor=888888 colspan=10></td>
</tr>
<tr height=3>

<td bgcolor=888888 colspan=19></td>
<td bgcolor=4c4c4c colspan=15></td>
<td bgcolor=888888 colspan=17></td>
</tr>
<tr height=3>

<td bgcolor=888888 colspan=54></td>
</tr>
</table></body></html>
```