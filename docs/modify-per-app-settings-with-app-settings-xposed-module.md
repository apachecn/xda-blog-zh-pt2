# 使用应用程序设置公开模块修改每个应用程序的设置

> 原文：<https://www.xda-developers.com/modify-per-app-settings-with-app-settings-xposed-module/>

最近，[我们谈论了](http://www.xda-developers.com/android/halo-popup-on-any-rom-using-xposed/ "Halo Popup on Any ROM Using Xposed")一个 Xposed 模块，它通过使用 XDA 公认的开发者 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 和公认的贡献者[钨文迪](http://forum.xda-developers.com/member.php?u=4322181)的强大的 [Xposed 框架](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/ "Say Goodbye to Custom “Stock” Roms and Hello to Xposed Framework") ( [线程](http://forum.xda-developers.com/showthread.php?t=1574401))给大家带来了一点偏执的 Android 体验。那个暴露的模块让任何 Android 4.0+ ROM 的用户都尝到了偏执的 Android 光环的滋味。然而，大多数用户会说，偏执的 Android 最大的定义功能是它的即时和每个应用程序的布局和 dpi 设置。不幸的是，前面介绍的模块没有提供任何东西来复制这一点。

由 Xposed 的创作者自己开发(公认的贡献者[钨文蒂](http://forum.xda-developers.com/member.php?u=4322181)和公认的开发者[罗沃 89](http://forum.xda-developers.com/member.php?u=4419114) )，应用设置 Xposed 模块在一定程度上帮助弥合了这一差距，同时提供了许多对任何 ROM 用户都有用的附加功能。

应用程序设置允许用户修改 DPI、字体大小、屏幕尺寸、xlarge 限定符、区域设置、全屏、标题栏、方向设置等等——所有这些都基于每个应用程序。它甚至允许你撤销权限，修改通知的显示方式，以及改变应用程序在内存中的保存方式。

虽然应用程序设置不能像你在偏执的 Android 上那样直接让你改变布局，但有许多设置是不容易改变的，这使它成为任何人的强大选项。转到[模块线程](http://forum.xda-developers.com/showthread.php?t=2437377)开始。