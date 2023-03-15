# 使用通用内核闪存工具进行在线闪存

> 原文：<https://www.xda-developers.com/online-flashing-with-universal-kernel-flash-tool/>

我们在过去已经看到了一些基于 Android 的图像闪烁工具。这些工具，比如 XDA 精英认可的开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 的[Mobile Odin](http://www.xda-developers.com/android/mobile-odin-updated-to-version-3-5/ "Mobile Odin Updated to Version 3.5")([thread](http://forum.xda-developers.com/showthread.php?t=1347899))，让我们避开了传统的为了执行某些刷新任务而必须让设备离线的不便。相反，它们允许我们从 Android UI 内部进行刷新。尤其是 Chainfire 的产品非常有趣，因为你可以在应用的 UI 中注入 MobileOdin 和超级用户，以及刷新整个固件包、无线电等。

看到其他选项出现总是好的，其中一个选项来自 XDA 公认的开发者 [frapeti](http://forum.xda-developers.com/member.php?u=4559222) 。该应用程序不会刷新整个 ROM 包或收音机。其实它只闪内核。然而，它有一个非常精简的用户界面，并在整个过程中提供广泛的反馈，包括防止您刷新不正确的内核，并读取要刷新的映像的 MD5sum，以便您可以验证映像是否被损坏。

类似于前面提到的完整固件包闪存工具 Mobile Odin，通用内核闪存工具不增加你的闪存计数器。目前有四个官方支持的设备，但更多的设备将不可避免地工作。然而，如果你在一个不支持的设备上尝试这个，在继续之前做一个完整的 Nandroid，并做好准备，以防出现意外。

到[原始线程](http://forum.xda-developers.com/showthread.php?t=2477273)开始闪光。