---
title: 【教程】如何在handsome主题上加入Revolvermaps地球
categories:
  - 教程
tags:
  - handsome
  - handsome主题
  - Typecho
excerpt: >-
  访问别人博客有时就能看到一个这样能显示访客信息的“小地球”，还能随意转动，看起来非常有趣：点左下角的logo进入网站看一看，是Revolvermaps的一个地球来访者的3D地球显示的访客信息地图...
date: 2021-02-19 03:54:00
---

访问别人博客有时就能看到一个这样能显示访客信息的“小地球”，还能随意转动，看起来非常有趣：点左下角的logo进入网站看一看，是Revolvermaps的一个地球来访者的3D地球显示的访客信息地图...
<!-- more -->
访问别人博客有时就能看到一个这样能显示访客信息的“小地球”，还能随意转动，看起来非常有趣：

![Revolvermaps](https://old.blog.fwder.cn/usr/uploads/2021/02/1177659886.png "Revolvermaps")

点左下角的logo进入网站看一看，是Revolvermaps的一个地球来访者的3D地球显示的访客信息地图。RevolverMaps，是一个免费的网站3D地图统计工具，采用Revolver Maps Graphics Engine图形引擎，同时提供JavaScript版本和flash版本。

## 安装过程

整个安装过程还是非常非常地简单。

我们先打开这个[Revolvermaps网站](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cucmV2b2x2ZXJtYXBzLmNvbQ==)，一开始就能看到这个熟悉的地球。

![](https://old.blog.fwder.cn/usr/uploads/2021/02/3799091779.png)

地球上的标记就是正在访问此网站的用户的地理位置信息，地球上的红点代表了曾经在这个地方有一位用户访问过这个网站。

往下翻，就能看到熟悉的一串html代码。

\[scode type="yellow"\]这里我标注的代码可能和复制的代码不完全相同，请复制官网的版本即可。\[/scode\]

> <script type="text/javascript" src="[https://rf.revolvermaps.com/0/0/6.js?i=5ss3etfqual&](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9yZi5yZXZvbHZlcm1hcHMuY29tLzAvMC82LmpzP2k9NXNzM2V0ZnF1YWwmYW1w);m=7&c=e63100&cr1=ffffff&f=arial&l=0&bv=90&lx=-420&ly=420&hi=20&he=7&hc=a8ddff&rs=80" async="async"></script>

\[scode type="blue"\]这里可区分为直接使用和自定义使用，我们先直接复制代码过来。\[/scode\]

复制完代码后，进入handsome后台，选择“更换外观--设置外观--开发者设置--全局右侧边栏广告位”，将复制的代码粘贴即可。

\[scode type="green"\]如果嫌弃地球上方“广告”两字的，打开“/usr/themes/handsome/component/sidebar.php”文件，搜索“广告”二字（handsome8.0.0 大约在111行），把它改为“地球”就可以了。\[/scode\]

* * *

当然，如果原本设置的代码生成的地球挤在一个广告栏里显得太小，你还可以在Revolvermaps网站上对地球大小样式颜色等进行调整处理，这里就不过多赘述。

旁边的“每日Pixiv热门”控件下面就是地球的实际效果了。

感谢观看~