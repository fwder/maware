---
title: 【探索】试着在博客中插入一个Bilibili内嵌播放器
categories:
  - 探索
tags:
  - 博客相关
excerpt: >-
  这是一个测试handsome中加入b站内嵌播放器的页面
  来源：BV1B54y1R7uq可以看到，经过一系列设置之后，可以将b站内嵌播放器插入到博客中。番剧也可以添加吗？具体添加方法？https:...
date: 2021-01-27 12:54:00
---

这是一个测试handsome中加入b站内嵌播放器的页面 来源：BV1B54y1R7uq可以看到，经过一系列设置之后，可以将b站内嵌播放器插入到博客中。番剧也可以添加吗？具体添加方法？https:...
<!-- more -->
### 这是一个测试handsome中加入b站内嵌播放器的页面

![妹红口也薯条.jpg](https://old.blog.fwder.cn/usr/uploads/2021/01/3420975516.jpg "妹红口也薯条.jpg")

来源：BV1B54y1R7uq

可以看到，经过一系列设置之后，可以将b站内嵌播放器插入到博客中。

#### 番剧也可以添加吗？具体添加方法？

[https://www.bilibili.com/video/BV1xp4y1x7Sk](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cuYmlsaWJpbGkuY29tL3ZpZGVvL0JWMXhwNHkxeDdTaw==)

1.  首先，需要将上面的视频内嵌代码从视频下的“分享”中复制过来，如果是视频就直接粘贴到博客，同时在自定义css中插入以下样式：
    
    ```
    
    .iframe_video {
        position: relative;
        width: 100%;
    }
    
    @media only screen and (max-width: 767px) {
        .iframe_video {
            height: 15em;
        }
    }
    
    @media only screen and (min-width: 768px) and (max-width: 991px) {
        .iframe_video {
            height: 20em;
        }
    }
    
    @media only screen and (min-width: 992px) and (max-width: 1199px) {
        .iframe_video {
            height: 30em;
        }
    }
    
    @media only screen and (min-width: 1200px) {
        .iframe_video {
            height: 40em;
        }
    }
    
    .iframe_cross {
        position: relative;
        width: 100%;
        height: 0;
        padding-bottom: 75%
    }
    
    .iframe_cross iframe {
        position: absolute;
        width: 100%;
        height: 100%;
        left: 0;
        top: 0
    }
    ```
    
2.  视频直接粘贴即可引入相应视频；
3.  如果想插入番剧，先找到番剧那一集对印的BV号，再进入[BV转av](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly90b29sLmxpdW1pbmd5ZS5jbi9hdmJ2Lw==)页面，获取av号（aid）;
4.  之后将上面的内嵌代码对应的bv和aid(av)号修改即可（cid应该不用管）；
5.  内嵌代码：
    
    ```
    <iframe src="//player.bilibili.com/player.html?aid=839991345&bvid=BV1B54y1R7uq&cid=244362085&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
    ```
    
6.  如果想要实现播放器其他功能，可以在给iframe 这个标签添加 class="iframe\_video" iframe\_video这个类名。如下：
    
    ```
    <iframe class="iframe_video" src="//player.bilibili.com/player.html?aid=971163886&bvid=BV1xp4y1x7Sk&cid=244362085&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>
    ```
    
7.  插入效果：
8.  （带有class标签的）；

1.  （没有class标签的）；

看起来都是可以的呢~