# Xposed 框架现在与 Android 4.4 兼容

> 原文：<https://www.xda-developers.com/xposed-framework-now-compatible-with-android-4-4/>

时不时地，股票光盘可能会缺少我们喜欢的东西。定制 ROM 开发人员经常用代码创造奇迹，并提供有用的解决方案，但不是每个人都能够或愿意加载定制 ROM。

你一定听说过由 XDA 知名开发者 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 开发的[x exposed Framework](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/)。我们已经[写了大量关于 x exposed](http://www.xda-developers.com/tag/xposed/)的文章，我们甚至有一个常规的[x exposed Tuesday](http://www.xda-developers.com/android/xda-xposed-tuesday-xuimod-customizations-xda-developer-tv/)功能，展示了各种示例模块。

进入一些技术细节，Xposed 框架是对 */system/bin/app_process* 的修改，用于在启动时加载 JAR 文件，这允许开发人员通过简单的修改来创建应用程序。这是一个完美的选择，运行一个定制的 ROM 来加载我们最喜欢的模块。

最近，rovo89 更新了他的工作，以支持 Android 4.4 KitKat。它仍处于测试阶段，但 rovo89 预计最终版本将很快准备就绪。与以前版本兼容的模块应该继续工作，如果它们不依赖于 KitKat 中已经改变的 AOSP 内部的话。但是，它与艺术不兼容。也就是说，未来可能会增加艺术兼容性。但就目前而言，一切都不确定。

如果你是一个快乐的 KitKat 用户，并且想用它来使用你最喜欢的模块，那就进入[开发线程](http://forum.xda-developers.com/showthread.php?p=24267797)，安装最新的 APK。

*【非常感谢资深版主[4 月 3 日](http://forum.xda-developers.com/member.php?u=4478812)的提示！]*