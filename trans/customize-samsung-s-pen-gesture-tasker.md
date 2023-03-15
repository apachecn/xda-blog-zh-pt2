# Tasker 可以让你拦截三星的笔势做你想做的事

> 原文：<https://www.xda-developers.com/customize-samsung-s-pen-gesture-tasker/>

三星的 S Pen 是完成工作的强大工具，无论你是记笔记、标记文档还是在应用程序中使用手势。如果可以自定义手势的功能，岂不是很酷？有了 [Tasker](http://xda-developers.com/tag/tasker) ，就可以了。

Tasker 的开发者 joo Dias 发现了如何拦截 S Pen 触发的手势事件。使用 Tasker，用户可以从 350 多个操作中进行选择，以前所未有的方式定制 S Pen 体验。例如，您可以打开智能灯、切换“请勿打扰”模式、让设备进入睡眠状态等等。

这里有一个来自开发者的视频，演示了一旦你把笔的手势连接到 Tasker 上，你可以做些什么:

一旦 Tasker 被授予 READ_LOGS 权限，它就能够拦截 S Pen 事件，该权限允许应用程序读取 Android 的系统日志。为了授予 Tasker 此权限，[您需要通过 ADB](https://tasker.joaoapps.com/userguide/en/help/ah_read_logs_grant.html) 手动完成。下载 Tasker 后，您可以使用系统日志中的笔势条目作为上下文来创建配置文件。然后，您可以将一系列操作(或单个操作)绑定到该上下文。因为 Tasker 可以被编程来做基本上任何事情，定制的可能性是无限的。

请注意，只有具有蓝牙功能的 S Pens 的三星设备才支持手势，包括 Galaxy Note 9 和更高版本以及 Galaxy Tab S6 和更高版本。此外，你的设备需要运行普通固件，因为定制的 rom 可能不会为每个手势在 logcat 中发送完全相同的消息。最后，Tasker 仅限于您可以在设备上的“空气手势”设置中配置的手势。

谷歌 Play 商店的 Tasker 售价 3.49 美元，不过你可以从开发者网站下载 7 天试用版[。](https://tasker.joaoapps.com/download.html)

**[Tasker 提示&招数论坛](https://forum.xda-developers.com/u/tasker-tips-tricks)**