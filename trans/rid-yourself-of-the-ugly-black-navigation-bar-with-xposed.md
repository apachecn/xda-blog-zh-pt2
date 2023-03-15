# 用 Xposed 摆脱难看的黑色导航栏

> 原文：<https://www.xda-developers.com/rid-yourself-of-the-ugly-black-navigation-bar-with-xposed/>

Xposed Framework 开启了一种新的方式来定制我们的设备，而不必手动挑选和重建我们最喜欢的 rom。该框架也给了我们一个机会来修改股票 rom，使其具有以前只在 OEM 皮肤上看到的花哨功能，如 TouchWiz 和 Sense。

许多新设备现在都带有屏幕导航按钮，而不是物理硬件按钮。在 Android 4.4 KitKat 之前，这种导航栏在屏幕底部采用黑色实线的形式。这不是 Android 最漂亮的部分，因此偏执的 Android 的馅饼控件和新的沉浸式模式的再现很受欢迎。

幸运的是，您现在可以轻松地在屏幕上隐藏这个工具栏。你所需要的只是一个由 XDA 资深会员 [zst123](http://click.xda-developers.com/api/click?format=go&key=f0a7f91912ae2b52e0700f73990eb321&loc=http%3A%2F%2Fwww.xda-developers.com%2Fandroid%2Fcontrol-your-in-app-fonts-with-perappfonts-xposed-module%2F&v=1&libId=5e9f6e92-fcf5-4859-8c45-a599cc53968f&out=http%3A%2F%2Fforum.xda-developers.com%2Fmember.php%3Fu%3D5402474&ref=https%3A%2F%2Fwww.google.pl%2F&title=Control%20Your%20In-App%20Fonts%20with%20PerAppFonts%20Xposed%20Module%20%E2%80%93%20xda-developers&txt=zst123&jsonp=vglnk_jsonp_13880805510786) 开发的模块——这位开发者也给我们带来了像[每应用字体控制](http://www.xda-developers.com/android/control-your-in-app-fonts-with-perappfonts-xposed-module/)这样的伟大功能。这个特殊的模块允许用户隐藏不需要的黑条。然后，您只需轻触屏幕底部，即可将其恢复。不用说，您需要安装一个 Xposed 框架，并且您的设备必须是 rooted 用户才能使用这个模块。

你可以从[模块线程](http://forum.xda-developers.com/showthread.php?t=2581428)中抓取最新的 APK。也有一个 YouTube 视频可以在线程中使用，其中演示了效果。