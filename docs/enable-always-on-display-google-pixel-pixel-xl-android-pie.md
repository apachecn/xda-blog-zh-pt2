# 在运行 Android Pie 的 Pixel & Pixel XL 上启用始终显示

> 原文：<https://www.xda-developers.com/enable-always-on-display-google-pixel-pixel-xl-android-pie/>

# 在运行 Android Pie 的 Google Pixel & Pixel XL 上启用始终显示

新的 Magisk 模块可以让你在 Google Pixel 和 Pixel XL 上启用总是显示，但你必须运行 Andorid Pie，你可能已经这样做了。

长期以来，“始终显示”一直是许多设备的一项功能。具有讽刺意味的是，谷歌设备直到 Pixel 2 和 Pixel 2 XL 才拥有它，他们称之为“环境显示”。不幸的是，谷歌并没有从 2016 年开始将该功能正式移植到第一代 Pixels 上，可能是因为电源效率低下的原因。但是我们有一些好消息要告诉你:你现在可以在谷歌 Pixel 和 Pixel XL 上启用永远显示。我自己测试过这个方法，它没有任何问题。XDA 的高级成员 shagbag913 发布了一个 Magisk 模块，它能做到这一点，所以你需要 root。如果你已经有了，你可以按照这个教程:

1.  从线程下载模块
2.  在您的设备上打开 Magisk Manager
3.  从左侧导航菜单中，转到模块
4.  点击底部的“+”FAB
5.  选择您刚刚下载的 AODEnabler.zip
6.  点击重启
7.  就是这样！

完成该过程后，设备上将自动启用“始终显示”。您可以在“设置>显示>环境显示”下切换此设置。请记住，尽管 Pixel 和 Pixel XL 都有 AMOLED 屏幕，能够完全关闭屏幕上未使用的像素，但让显示器一直开着会影响电池寿命。

该方法目前仅适用于 Android Pie。作者提到稍后会添加对 Android Oreo 和 lower 的支持。这个模块使用一个 RRO 覆盖层，它将 Always on Display 字符串设置为“true ”,并将其打包成一个 APK。然后，该模块将覆盖图复制到/system/product/overlay/，这就是为什么它目前只在 Android Pie 上工作。你还需要获得 Magisk 17.0+。您可以从 XDA 门户网站上的 [Magisk Hub](https://www.xda-developers.com/magisk-hub-2/) 下载最新版本的生根解决方案。

[**一直在显示使能线程**](https://forum.xda-developers.com/pixel-xl/themes/display-enabler-magisk-module-android-9-t3857025)