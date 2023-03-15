# 移动 ODIN 让你从设备刷新固件

> 原文：<https://www.xda-developers.com/mobile-odin-lets-you-flash-firmware-from-device/>

链火的能力无止境。XDA 版主和公认的开发者现在提出移动 ODIN，允许你从你的设备本身刷新固件。没错，您不再需要将设备连接到电脑。

好吧，这不是完全正确的-移动奥丁目前不能闪存坑，引导加载程序，或 EFS 分区。你仍然需要你的电脑。暂时如此。但是如果你想闪存一个新的内核、系统、DBData、数据、缓存、参数或者调制解调器分区，Mobile ODIN 可以做到。正如开发商所说，

> 支持所有分区，松散文件也是如此。tar 文件和. tar.md5 文件。移动 ODIN 甚至会在闪烁前检查 MD5 签名。虽然在理论上移动奥丁可以重新分区和闪存 EFS 和 bootloaders，它会怯懦地拒绝这样做，为了你自己的安全。

手机奥丁建兴是专为 XDA。可以在安卓市场上找到 pro 版[。现在，移动奥丁专业有一些额外的津贴，定期，旧奥丁没有。例如，Chainfire 包括 ever root——一个在你刷新 ROM 时为其定位的选项。有了它，你也可以自动刷新超级用户和移动 ODIN 本身，所以当你重新启动你的新 ROM 时，你就可以再次刷新了。](https://market.android.com/details?id=eu.chainfire.mobileodin.pro)

并非所有设备都兼容。但 Chainfire 在第二次更新中推出了八款兼容的新设备，他说他愿意与三星手机合作。如果你在不兼容的设备上安装应用程序，应用程序将允许你创建一个转储文件，你可以在应用程序的线程中发布该文件。如果可以，也为您的设备发布一个 PIT 文件。最后，开发者说，他需要一个运行 ClockworkMod5 的内核，尽管它*可能*与 CWM3 或 4 一起工作。

要查看您的设备是否兼容——或者是否有兼容计划——并进行试用，请仔细[阅读源代码线程](http://forum.xda-developers.com/showthread.php?t=1347899)。