---
title: 【探索】记一次在 Android 下编译 Xmrig 的过程
categories:
  - 教程
tags:
  - Xmrig
  - CMake
  - 项目编译
  - Android
excerpt: >-
  前言之前只在 Windows 平台上跑过 xmrig ，理所应当的使用的是 msys2 进行无捐编译。现在有了30多台 Android
  设备，决定让它们锻炼锻炼筋骨，于是就有了这篇文章。过程起初...
date: 2022-03-13 03:41:00
---

前言之前只在 Windows 平台上跑过 xmrig ，理所应当的使用的是 msys2 进行无捐编译。现在有了30多台 Android 设备，决定让它们锻炼锻炼筋骨，于是就有了这篇文章。过程起初...
<!-- more -->
#### 前言

之前只在 Windows 平台上跑过 xmrig ，理所应当的使用的是 msys2 进行无捐编译。

现在有了30多台 Android 设备，决定让它们锻炼锻炼筋骨，于是就有了这篇文章。

#### 过程

起初通过msys2+ndk进行交叉编译，后来因为无法编译出libuv和hwloc两个库而以失败告终。

最后在Github的xmrig项目中的一个issue 和 [https://xmrig.com/docs/miner/build/ubuntu](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly94bXJpZy5jb20vZG9jcy9taW5lci9idWlsZC91YnVudHU=) 找到了灵感：

> ### [XZiar](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9naXRodWIuY29tL1haaWFy) commented
> 
> termux下可以直接编译。<br/>[https://xmrig.com/docs/miner/build/ubuntu](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly94bXJpZy5jb20vZG9jcy9taW5lci9idWlsZC91YnVudHU=)<br/>按advanced build来。<br/>不过安卓下libuv编译有点问题，`./build_deps.sh`完成后要单独去libuv目录下用cmake再编译一次，然后把生成的libuv\_a.a替换script/deps/lib下的libuv.a。

## 使用Termux进行编译

首先，给termux换源。

```
sed -i 's@^\(deb.*stable main\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/termux-packages-24 stable main@' $PREFIX/etc/apt/sources.list
sed -i 's@^\(deb.*games stable\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/game-packages-24 games stable@' $PREFIX/etc/apt/sources.list.d/game.list
sed -i 's@^\(deb.*science stable\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/science-packages-24 science stable@' $PREFIX/etc/apt/sources.list.d/science.list
apt update && apt upgrade
```

> [https://mirror.tuna.tsinghua.edu.cn/help/termux/](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9taXJyb3IudHVuYS50c2luZ2h1YS5lZHUuY24vaGVscC90ZXJtdXgv)

第二步，根据官方advanced build提供的脚本来安装库。

`sudo apt-get install git build-essential cmake automake libtool autoconf binutils vim wget gzip tsu`

注意：在执行后续脚本时会需要执行ar和link -lib命令，Termux中默认不提供此命令，所以需要手动pkg安装。

`pkg install binutils`

第三步，`git clone https://github.com/C3Pool/xmrig-C3.git`（建议使用C3pool的无捐版）

并且，`mkdir xmrig-C3/build && cd xmrig-C3/scripts`

第四步，在执行此步时，需要注意wget在下载时会报ssl错误，此时需要编辑`vim build.hwloc.sh`文件，加上跳过验证证书的参数“--no-check-certificate”之后再执行`./build_deps.sh`

> 引用 [https://blog.csdn.net/qq\_51085767/article/details/118102099](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzUxMDg1NzY3L2FydGljbGUvZGV0YWlscy8xMTgxMDIwOTk=)

执行完毕后，因为脚本在Android环境下运行有Bug，所以完成后需要进入libuv目录下用cmake再编译一次，然后把生成的libuv\_a.a替换script/deps/lib下的libuv.a。

之后，`cd ../build`

第五步，`cmake .. -DXMRIG_DEPS=scripts/deps` ，完成之后 `make -j$(nproc)` 即可。

#### END