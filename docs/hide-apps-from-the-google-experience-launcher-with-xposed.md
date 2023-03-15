# 使用 Xposed 隐藏 Google 体验启动器中的应用程序

> 原文：<https://www.xda-developers.com/hide-apps-from-the-google-experience-launcher-with-xposed/>

如果你喜欢保持事情最小化，你显然已经尝试隐藏不必要的应用程序。隐藏一个大的文件列表很容易，但有时人们想从应用程序抽屉中隐藏一个图标，而不是实际禁用它。如果没有合适的工具或先进的发射器，这可能会很棘手。不久前，我们推出了[智能隐藏计算器](http://www.xda-developers.com/android/smart-hide-calculator-is-a-calculator-that-stealthily-hides-your-files/)，这是一个隐藏在计算器用户界面后面的文件的应用程序。现在，由于有了 Xposed 模块，我们也可以隐藏应用程序。

XDA 论坛成员 [depressiveRobo](http://forum.xda-developers.com/member.php?u=5538788) t 发布了一个 Xposed 框架模块，该模块隐藏了应用程序抽屉中的应用程序。目前，它与谷歌体验启动器一起工作，这是大多数 KitKat ROMs 中的默认启动器。这个模块非常容易使用。你所要做的就是选择一系列要隐藏或显示的应用程序，然后重启你的设备。当然，您可以通过反向执行几乎相同的操作来轻松恢复您的更改。因为它是一个 Xposed 模块，所以您的设备必须是根设备并且安装了 Xposed Framework。

如果你有什么要隐藏的，我知道你有，你应该访问[模块线程](http://forum.xda-developers.com/showthread.php?t=2606601)并尝试一下。您也可以从 Xposed 框架模块数据库下载它。