---
title: 【转载】使用adb免root迁移应用数据
categories:
  - 转载
tags:
  - adb
  - 迁移应用数据
excerpt: >-
  【本页面转载至BD.温馨小窝，感谢贵站的帮助！】买到新手机，首先要做的一件事就是迁移手机数据。现在的手机都带有换机app，因此减少了不少难度。例如小米换机，可以实现图片、联系人、短信、软件等数据...
date: 2021-02-19 04:22:00
---

【本页面转载至BD.温馨小窝，感谢贵站的帮助！】买到新手机，首先要做的一件事就是迁移手机数据。现在的手机都带有换机app，因此减少了不少难度。例如小米换机，可以实现图片、联系人、短信、软件等数据...
<!-- more -->
【本页面转载至[BD.温馨小窝](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly93d3cuYmx1ZXNkYXduLnRvcC8|cD00MTk=)，感谢贵站的帮助！】

买到新手机，首先要做的一件事就是迁移手机数据。现在的手机都带有换机app，因此减少了不少难度。

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200903211707-461x1024.jpg)

例如小米换机，可以实现图片、联系人、短信、软件等数据一键迁移

但是我们可以注意各大换机app都说明了无法迁移非同品牌手机的应用数据

### 小米换机的原话

为什么旧手机为非小米手机无法迁移应用数据？

因为小米换机在非小米手机上无对应权限，因此无法迁移应用数据

* * *

这就麻烦了，手机上有些单机游戏想迁移到新手机继续玩，或者软件有些重要数据不得不迁移到新机该怎么办。

欢迎我们万能的ADB (Android Debug Bridge，即安卓调试桥)

### 下载ADB工具包

* * *

新版ADB已弃用备份功能，最好下载下面的旧版

[云盘下载](https://old.blog.fwder.cn/index.php/go/aHR0cHM6Ly9wYW4uYmFpZHUuY29tL3MvMWMxUHZIeG0=)

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200906215257.jpg)

这是ADB工具包的内容，你可以解压进任何路径

### 配置环境变量（Windows）

* * *

因为平台工具只是解压进了一个路径，直接用cmd是找不到adb的

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200903220758.jpg)

* * *

第一步 右击`此电脑`单击`属性`

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200903221404-1.jpg)

第二步 找到`高级系统设置`并点击`环境变量`

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200903221442-1.jpg)

第三步 找到`系统变量`中的`Path`并点击`编辑`

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200903221605.jpg)

第四步 新建`环境变量`并将ADB工具包解压的路径填入，点击`确定`

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200903221645-1.jpg)

* * *

命令行出现adb版本号即为成功

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200906110443-1.jpg)

### 迁移应用数据

* * *

使用USB连接你的旧手机，手机进入`开发者选项（关于手机——连续点击版本号即可激活）`开启`USB调试`

连接完成后输入`adb devices`，如果列表显示device，就说明连接成功了

我们可以使用`adb shell pm list packages`来列出所有已装软件的包名

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200906115435-1.jpg)

备份应用数据使用`adb backup`命令

```
adb backup [-system|nosystem] -all [-apk|-noapk] [-shared|-noshared] -f <ab包储存位置> <应用包名>
// [-system|nosystem] 是否包含系统应用，默认为-system，一般备份全部应用时才用到
// -all 带有此参数会备份所有应用
// [-apk|-noapk] 备份数据的同时是否备份apk，默认为-noapk
// [-shared|-noshared] 是否备份设备内置存储或SD卡的内容，比如音乐、图片和视频，默认为-noshared
// -f <ab包储存位置> 选择备份的文件存放在哪里，可根据喜好自行替换
// <应用包名> 备份单个应用需要知道包名
```

* * *

#### 单应用备份（例）

```
adb backup -f D:\gugugu.ab com.PigeonGames.Phigros
```

不带`-apk`参数的命令要求新机已安装此app

然后手机会弹出这么个东西，直接点击`备份我的数据`即可，文件大小决定了时间的长短，需要耐心等待

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/IMG_20200821_165221-576x1024.jpg)

指定路径出现ab包就说明备份成功了

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200906130707.jpg)

#### 还原备份

拔下旧手机，插入新手机，同样手机要开启`USB调试`

使用`adb devices`查看设备，确保已连接

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/20200906131338.jpg)

```
adb restore D:\gugugu.ab
// 还原备份命令，选择之前备份的ab包位置即可
```

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/Screenshot_2020-08-21-17-13-14-763_com.android.ba_-461x1024.jpg)

点击`恢复我的数据`，等一会就好了。打开应用看下，内容完全一致代表迁移成功（

![](https://www.bluesdawn.top/wp-content/uploads/2020/09/IMG_20200821_172850-scaled.jpg)

* * *

#### 全部备份

```
// 一句命令全部备份，还原步骤同上
adb backup -apk -shared -all -f D:\backup.ab

// 不备份系统应用，换新机时可以用
adb backup -apk -nosystem -shared -all -f D:\backup.ab

// 不备份系统应用和内置存储媒体等内容
adb backup -apk -nosystem -noshared -all -f D:\backup.ab

// 备份全部用户应用数据，但不备份apk
adb backup -noapk -nosystem -noshared -all -f D:\backup.ab
```