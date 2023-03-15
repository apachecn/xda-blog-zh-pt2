# 棉花糖来了！

> 原文：<https://www.xda-developers.com/xposed-for-marshmallow-is-here/>

Xposed 是 Android 爱好者最喜爱的工具之一，因为它允许进行各种修改来扩展我们最喜爱的设备的功能。然而，每一个新的 Android 版本都会带来对下一个版本的短暂等待。

> 棉花糖的等待结束了！

[x 公布的版本 76 在这里支持 Android 6.0 棉花糖](http://forum.xda-developers.com/showthread.php?t=3034811)。Xposed 的创造者和 XDA 摇滚明星 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 一直在努力工作，以便将 Xposed 的惊人功能带到 Marshmallow，尽管 Android 6.0 是一个很大的升级，rovo89 勇敢地面对复杂情况，现在有了一个更新的框架，支持你需要的大部分内容。

但是，有一些限制:

*   许多模块可能需要更新。给模块开发者时间来更新他们的模块！
*   在撰写本文时，客户端只在安装了 SuperSU 的情况下进行了测试，因此 dm-verity 和一些 SELinux 规则被禁用。否则，其中一些会与系统分区的修改相冲突。
*   对偏好设置文件的访问可能会被 SELinux 阻止，Xposed 目前无法解决这个问题。然而，rovo89 建议保持 SELinux 启用，并强制优先考虑安全性。
*   并非所有的 Xposed APIs 都经过了全面的测试，虽然系统启动时没有来自框架的任何错误消息，但有些函数可能仍然需要针对 Marshmallow 进行调整。
*   rovo89 指出，JIT 和“优化”编译器可能会产生一些问题。由于这些在棉花糖中是新的，与 Xposed 结合可能会有意想不到的后果。这可能导致挂钩无法正常工作或崩溃。

排除这些限制，Xposed 应该可以在你的棉花糖 ROM 上工作，这意味着你将能够再次释放你手机上的更多潜力！请记住**许多您喜欢的模块可能需要更新**，所以请务必检查相关的线程，使用搜索按钮，并给开发人员足够的时间来进行必要的更改和调整。

[转到线程](http://forum.xda-developers.com/showthread.php?t=3034811)找到新棉花糖安装程序的下载链接，同时确保**仔细阅读公开帖子**以确保你了解所有的更改。你也可以在[讨论帖](http://forum.xda-developers.com/xposed/discussion-xposed-marshmallow-t3249095)中讨论最新的变化。对于那些在 Lollipop 上的人，要知道 rovo89 正计划在未来几天内发布 5.0 和 5.1 的新版本，回推对 Marshmallow 所做的一些更改，并且他也将很快将这些更改推送到 GitHub。

Xposed 是 XDA 最喜欢的修改之一，如果你一直在等待扩展你的棉花糖 ROM 的功能，并收回升级时丢失的功能，请确保前往论坛进行实验和讨论——只是记得要小心，并使用搜索按钮进行良好的衡量！