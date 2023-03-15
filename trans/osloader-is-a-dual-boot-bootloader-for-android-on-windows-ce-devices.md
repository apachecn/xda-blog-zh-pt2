# OSLoader 是 Windows CE 设备上 Android 的双引导引导程序

> 原文：<https://www.xda-developers.com/osloader-is-a-dual-boot-bootloader-for-android-on-windows-ce-devices/>

还记得 XDA 的好日子吗？那时生活简单，运行 Windows Mobile 的掌上电脑被认为是最先进的。在谷歌推出 Android 颠覆智能手机行业后，许多开发人员开始尝试将流行的开源操作系统移植到他们的 Windows Mobile 设备上，其中最受欢迎的成果可以从不朽的 HTC HD2 的形式中看出来。

2010 年， [Gen.Y DualBOOT](http://forum.xda-developers.com/showthread.php?t=623792) 项目在 XDA 启动，旨在为 WM 设备带来 Windows Mobile 和 Android 双启动引导程序。然而，它并没有优化为在运行 Windows CE 的横向触摸屏设备上运行，包括几个独立的 GPS 单元。XDA 资深成员[jwoergbauer](http://forum.xda-developers.com/member.php?u=1890170)用 MortScript 重写了该项目，以扩展其对这种 Windows CE 设备的支持，结果是 OSLoader。

请注意，OSLoader 本身并不在设备上安装 Android，仍然使用 HaRET 来引导 Android。此外，要真正运行 Android，您仍然需要一个适用于您的设备的 Android 版本。也就是说，OSLoader 提供了一种便捷的方式来选择在启动时启动哪个操作系统。

一如既往，更多细节、下载链接和安装/使用说明可以在[论坛帖子](http://forum.xda-developers.com/showthread.php?t=2057216)中找到。