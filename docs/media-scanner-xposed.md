# 使用 Xposed 有效优化您的介质扫描仪服务

> 原文：<https://www.xda-developers.com/media-scanner-xposed/>

# 使用 Xposed 有效优化您的介质扫描仪服务

这个公开的模块帮助您有效地优化设备上的媒体扫描仪服务。

通常，引导时会扫描外部存储器上的所有媒体文件。执行此操作的服务称为媒体扫描器，它将输出保存在媒体存储中。Android 的开发人员已经努力优化它，但媒体扫描仍然是一项在重启后的最初几分钟内非常有效地消耗电池的服务。

媒体扫描仪服务本身不提供偏好设置菜单，它在后台运行，因此您无法控制它。如果没有 Xposed 框架，你就不能这么容易地做到。XDA 论坛成员 thomashofmann 决定通过创建一个提供一些调整的模块来解决媒体扫描仪的问题。使用此模块，您可以轻松地选择要扫描的文件夹，在前台运行该过程，或者在您希望运行的任何位置触发扫描。还有更多功能，可以通过启动应用程序抽屉中的模块图标来访问。

要使用该模块，您的设备必须是 rooted，并且运行 Android 4.0.4 或更高版本。Xposed Framework 还不能与 ART 一起工作，所以这个和其他模块显然不能与我们最喜欢的操作系统 Android 5.0 Lollipop 的最新版本一起使用。

您可以通过访问[exposed Media Scanner Optimizer 论坛线程](http://forum.xda-developers.com/xposed/modules/xposed-xposed-media-scanner-optimizer-t2942609)了解更多关于媒体扫描仪及其行为的信息。当然，模块也可以在那里找到。