# 开发者让 Android P 在摩托罗拉 Moto Z 上运行

> 原文：<https://www.xda-developers.com/motorola-moto-z-android-p/>

我们距离 2018 年谷歌 I/O 大会只有 10 天了，预计谷歌将在会上公布关于[安卓 P](https://www.xda-developers.com/tag/android-p/) 的许多细节，比如[传闻中的导航手势](https://www.xda-developers.com/android-p-iphone-x-navigation-gesture-2/)和[材料设计改进](https://www.xda-developers.com/google-chrome-material-design-2-android-p/)。第一个 [Android P 开发者预览版](https://www.xda-developers.com/android-p-developer-preview-1-google-pixel-xl-pixel-2-xl/)可用于 Google Pixel、Pixel XL、Pixel 2 和 Pixel 2 XL，还有很多[我们已经在第一个版本中看到了](https://www.xda-developers.com/everything-new-android-p-developer-preview/)，但是在新版本 Android 的最终发布之前还有很多值得期待的。对于那些没有谷歌 Pixel 手机的人来说，你可能要等很长时间才能让 P 为你的设备所用。然而，我们论坛上的开发者不会等待原始设备制造商正式更新他们的设备(如果有的话)，所以他们会自己动手。一个这样的开发者已经设法在他的摩托罗拉 Moto Z 上启动了第一个 Android P 开发者预览版

摩托罗拉 Moto Z 于 2016 年 6 月发布，搭载高通骁龙 820 片上系统和安卓棉花糖。它已经收到了 Android Nougat 和 [Android Oreo](https://www.xda-developers.com/motorola-rolls-out-android-oreo-moto-z-z2-g5-g5s-more/) 的官方更新，预计不会收到 Android P。XDA 公认的开发者 [erfanoabdi](https://forum.xda-developers.com/member.php?u=6298645) 已经成功将 Android P 移植到他的设备上，这要归功于[非官方项目 Treble compatibility](https://www.xda-developers.com/list-android-devices-project-treble-support/) 。这是我们看到的第二款能够启动 Android P 的非谷歌设备，尽管上一款是运行在 EMUI 形式的厚皮版本上的[华为 Mate 10 Pro。](https://www.xda-developers.com/huawei-mate-10-pro-android-p/)

erfanoabdi 能够通过修改来自 Google Pixel XL (marlin)的现有系统映像来实现这一点。)通过使用名为“ [Capire Le Treble](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/tool-capire-le-treble-terble-vendor-t3774629) 的定制脚本(该脚本允许他在没有/vendor 分区的设备上刷新特定于设备的系统映像)，他能够将修改后的 P 系统映像从 Pixel XL 刷新到之前运行正式 LineageOS 15.1 版本(顺便提一下，该版本将于周一发布)的 Moto Z 上。)

对于那些之前关注过我们的高音项目报道的人来说，你可能想知道这个脚本是如何工作的。本质上，它提取/system/vendor 中的 HALs，并将它们放在要刷新的[通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)中；这样，刷新系统映像就不会覆盖 HALs。经过几次最初的崩溃和一些繁重的调试，他能够让 Android P 启动并运行。这里有一些展示各种 P 用户界面元素和特性的附加图片。

根据 erfanoabdi 的说法，它并不是没有缺陷。像相机、Wifi 和无线电这样的东西目前都不工作。令人惊讶的是，Moto Mods 似乎可以工作，尽管这也有点问题。考虑到所有这一切是多么巨大的一次黑客攻击(Moto Z 不支持 Project Treble，系统映像是修改过的马林映像，而不是从源代码构建的映像)，令人惊讶的是这竟然真的有效。不要指望很快就能把它作为日常驱动来运行；当源代码和 P 的完整版本一起发布时，你可能会有更多功能的 Android P ROMs。