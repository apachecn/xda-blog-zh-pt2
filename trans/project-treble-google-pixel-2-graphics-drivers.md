# Project Treble 在行动:谷歌 Pixel 2 的图形驱动程序作为应用程序预装

> 原文：<https://www.xda-developers.com/project-treble-google-pixel-2-graphics-drivers/>

# Project Treble 在行动:谷歌 Pixel 2 的图形驱动程序作为应用程序预装

由于 Project Treble，谷歌 Pixel 2/2 XL 的图形驱动程序作为供应商应用程序预装，这意味着它可以通过 Play Store 进行更新。

今年宣布的最大的 Android 相关新功能之一甚至没有在谷歌的传统硬件或软件活动中宣布。名为 [Project Treble](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/) ，这是迄今为止对 Android 底层系统架构的最大改变。它将操作系统模块化，使其与供应商组件分开，有望缩短原始设备制造商发布新的 Android 更新的时间，因为他们不再需要等待像高通这样的芯片制造商更新他们的代码。Treble 项目可能会使[将 AOSP 的新版本移植到支持 Treble 的设备上](https://www.xda-developers.com/project-treble-custom-rom-development/)变得更加容易，这就是为什么我们觉得它如此迷人。关于 Treble 的另一个有趣的花絮是，它可以允许像[从谷歌 Play 商店](https://www.xda-developers.com/android-o-users-will-update-graphics-drivers-through-play-store/)更新图形驱动程序这样的事情。

这是在今年谷歌 I/O 的一次演讲中宣布的，你可以在这里查看:

随着新的[谷歌 Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) ，我们终于有了充分利用这一点的设备。当我在威瑞森商店挖掘这些设备上有趣的应用程序时，我发现了几件有趣的事情:首先是[隐藏的黑暗主题](https://www.xda-developers.com/hidden-dark-theme-google-pixel-2/)，其次是图形驱动程序的 APK 文件。

app 安装为“Pixel 2017 图形驱动”，包名`com.google.pixel.wahoogfxdrv`。它安装在目录`/vendor/app/wahoo_gfxdrv/wahoo_gfxdrv.apk`中，这意味着它是供应商分区的一部分，因此更新可能由供应商(在这种情况下是高通)而不是谷歌来处理。

由于没有人长期拥有谷歌 Pixel 2/Pixel 2 XL，我们不知道这款应用是否会出现在这些设备的 Play Store 上。但既然它是一个应用程序，这意味着它不应该需要一个完整的 OTA 来更新。通过谷歌 Play 商店更新图形驱动程序是支持 Project Treble 的设备独有的——这意味着任何使用 Android Oreo 启动的设备以及[一些更新到它的设备](https://www.xda-developers.com/project-treble-android-o-exist-flagship/)，如[华为 Mate 9](https://www.xda-developers.com/android-oreo-emui-6-huawei-mate-9/) 。