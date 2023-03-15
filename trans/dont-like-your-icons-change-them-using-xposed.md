# 不喜欢你的图标？使用 Xposed 更改它们！

> 原文：<https://www.xda-developers.com/dont-like-your-icons-change-them-using-xposed/>

Android 是一个非常灵活的操作系统，其中几乎所有的东西都可以调整以适应你的个人需求。然而，当从 Play Store 下载一个应用程序时，会出现一个问题，它碰巧有一个难看的图标。幸运的是，您有一些方法来改变图标，甚至它显示的应用程序名称。其中之一是重新编译应用程序，并设置一个新的图标和名称，但往往因为 smali 和 XML 代码中的错误而不起作用。第二种方法是使用主题，但那是为支持主题引擎的 rom 用户保留的奢侈品。

前面提到的两种方法都很不方便，并且需要一些开发知识或定制的基于 AOSP 的 rom，这是一些用户希望避免的。幸运的是，您可以用一个方便的 Xposed 模块完成同样的任务。你需要做的就是下载 XDA 资深会员 [GalaxyInABox](http://forum.xda-developers.com/member.php?u=5267689) 的 xSuite。xSuite 允许您轻松地将应用程序的图标和显示名称更改为您选择的任何名称。

要享受这些好东西，根你的手机，安装 Xposed 框架，并前往[模块线程](http://forum.xda-developers.com/xposed/modules/app-xsuite-changes-icon-apps-t2751706) 。