# 使用 Xposed 使用密码保护您的设备

> 原文：<https://www.xda-developers.com/secure-your-device-with-a-knock-code-using-xposed/>

就在几个小时前，我们谈到了一个 Xposed 模块，当与兼容的内核结合使用时，用户[可以控制他们的唤醒手势](http://www.xda-developers.com/android/handle-your-kernel-level-wake-gestures-with-xposed/ "Handle Your Kernel-Level Wake Gestures with Xposed")。这种唤醒手势功能最类似于 HTC 的 Motion Launch，让用户通过简单的手势唤醒他们的设备并启动各种应用程序。

如果您不想使用手势来启动应用程序，而是想使用手势来保护您的设备，该怎么办？LG 通过新手机上的密码安全系统提供这种功能。但是多亏了 XDA 公认的开发者 MohammadAG 和 Xposed 框架的魔力，你也可以在你的设备上使用它。

这种实现有一些注意事项。对于初学者来说，要想在设备关闭时输入密码，你必须先打开屏幕，然后才能输入密码。此外，该模块目前只兼容 Android 4.4，但很快就会为 4.2 和 4.3 添加兼容性。最后，虽然使用密码相当方便，但这不是一种非常安全的锁定设备的方法。这是因为由于 Xposed 的限制，存储代码的文件是全球可读的。此外，这实际上相当于一个 2x2 PIN 密码，破解起来并不困难。

如果你想在你自己的设备上获得敲敲风格的功能，去[模块线程](http://forum.xda-developers.com/xposed/modules/mod-knock-code-screen-t2768502)那里试试吧。