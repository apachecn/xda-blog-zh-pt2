# 自定义 DPI，而不影响 Google Play

> 原文：<https://www.xda-developers.com/custom-dpi-without-upsetting-google-play/>

如果你曾经改变过你的设备的 DPI 值，试图获得一些更有价值的屏幕空间，你无疑会注意到这个调整带来的最不幸的副作用。这导致一些应用程序在 Play Store 中不可用，要么被标记为与您的设备不兼容，要么根本不显示。

有几种方法可以解决这个问题，例如返回到股票 DPI 值，侧加载应用程序，或者安装一个修改的 Play Store/Google 服务框架 APK。然而，定期做这些是很乏味的。XDA 的资深成员[汉姆斯泰尔](http://forum.xda-developers.com/member.php?u=3808696) 提出了一个替代的解决方案，以一个基于 Windows 的工具的形式，应该可以使纠正这个问题变得稍微轻松一点。

Google Play DPI Fix Tool 是一个简单易用的解决方案，只需点击几下鼠标，您就可以将设备连接到 PC，然后为设备本身和 Play Store 指定自定义的 DPI 值，从而确保所有应用程序都可用并与您的设备兼容。这个工具的伟大之处在于，它不依赖于现有的修改文件，而是直接从您的设备中获取相关的 APK 文件，并在推回它们之前自动修改它们。在 Android 版本 2.3 到 4.2.1 上测试过，这应该可以兼容绝大多数野外设备。有一些先决条件，如播放商店 APK 的文件名和安装一些你可能已经安装的东西，如 ADB 驱动程序和 JRE。

如果你是一个使用自定义 DPI 的爱好者，并且想尝试一下，请查看[应用程序线程](http://forum.xda-developers.com/showthread.php?p=37326035)。