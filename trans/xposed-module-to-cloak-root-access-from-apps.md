# 用于隐藏应用程序的 Root 访问权限的暴露模块

> 原文：<https://www.xda-developers.com/xposed-module-to-cloak-root-access-from-apps/>

在 Android 中修改你的*/系统*分区需要 root。它只不过是执行 *su* 命令，然后给你机会把文件推到分区上，还有其他的事情。具有 root 访问权限的用户应该非常小心，因为相对容易对设备进行软砌砖和/或导致引导循环。有几个应用程序代理 root 访问，大量应用程序需要这种访问才能工作。

Root 是备份*/数据*，修改一些内核值等等所必需的。但是，即使自动授权被激活，如何防止应用程序获得根权限呢？答案以 Xposed 框架模块的形式出现。

XDA 论坛成员 [devadvance](http://forum.xda-developers.com/member.php?u=2804938) 创建了一个模块，可以防止外壳访问对某些应用可见。此解决方案允许您保留您最喜爱的超级用户或超级用户设置，并控制设备上可用的其他应用程序。甚至有可能为根应用程序阻塞 su 库，但是您需要记住，如果您决定测试它，您将失去根访问权。开发者提供了一个已经测试过的流行应用列表，root 隐藏成功。

这个模块可以从[开发线程](http://forum.xda-developers.com/showthread.php?t=2574647)下载或者直接从 Xposed 数据库下载。您的设备必须是根设备，并且已经安装了 Xposed，但是您已经知道了这一点。