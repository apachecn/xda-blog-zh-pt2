# 禁用带有 x 曝光的空标签的新 NFC 标签弹出窗口

> 原文：<https://www.xda-developers.com/disable-new-nfc-tag-popup-for-empty-tags-with-xposed/>

如果你对 NFC 有所了解，你肯定收到过几次*新标签收集*消息。通常，当您扫描空的或包含简单文本的 NFC 标签时，会出现此消息。然而，有时这可能会变得很麻烦，尤其是当您有另一个应用程序在遇到空标签时执行任务。

谢天谢地，有一个由 XDA 资深成员[穆罕默德·达格](http://forum.xda-developers.com/member.php?u=2011359)开发的~~应用~~模块。如果这个名字听起来很熟悉，它应该。MohammadAG 还负责我们几天前报道过的精彩的 NFC 解锁应用[，以及我们在 XDA 门户网站上介绍过的其他几个应用](http://www.xda-developers.com/android/unlock-your-phone-using-nfc/)。

该模块的唯一目的是在扫描空标签时删除新标签收集对话框。安装就像任何其他的 Xposed 模块一样，非常简单。只需下载、安装并激活该模块。然后重启，你就可以走了。你需要安装 XDA 认可的开发者 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 的 [Xposed 框架](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/ "Say Goodbye to Custom “Stock” Roms and Hello to Xposed Framework") ( [线程](http://forum.xda-developers.com/showthread.php?t=1574401))，并且你的设备必须运行 Android 4.1 或更高版本。

前往[模块线程](http://forum.xda-developers.com/showthread.php?t=2474379)参与行动。如果你想看看源代码，请访问 [Github](https://github.com/MohammadAG/Xposed-Disable-NFC-Tag-Empty) 。