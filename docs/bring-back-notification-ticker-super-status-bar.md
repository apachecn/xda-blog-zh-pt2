# 用超级状态栏带回通知信息

> 原文：<https://www.xda-developers.com/bring-back-notification-ticker-super-status-bar/>

似乎抬头通知已经永远伴随着我们了，尽管它们实际上是在 2014 年随着 Android 5.0 Lollipop 引入的。不过在那之前，我们曾经有一个叫做“通知滚动条”的东西，当通知到达时，它会在状态栏中显示新通知的预览。虽然这个功能已经被遗忘很久了，但很多人都试图通过第三方应用程序恢复这个功能。我们之前详细介绍了一个使用自动化应用 Tasker 的[解决方案，但是如果你想要一个设置简单一点的解决方案，可以看看一个叫做“超级状态栏”的应用。](https://www.xda-developers.com/android-bring-back-notification-ticker-tasker/)

在很大程度上，超级状态栏作为一个状态栏的替代品，覆盖在你现有的状态栏之上。这意味着它不需要 root 访问权限就能工作，因为它实际上并没有取代你现有的状态栏。尽管如此，它支持对 UI 和行为进行大量定制，因此除了简单地启用通知滚动条之外，您还可以使用该应用做很多事情。这包括启用双击睡眠手势，通过在状态栏上滑动来快速更改亮度和音量，设计状态栏图标，显示电池条等等。这款应用有一个高级版本，价格为 1.99 美元，可以解锁所有手势动作和风格，并让你定制指示器、跑马灯通知、电池条和颜色。

如果你通过 ADB 授予 app WRITE _ SECURE _ SETTINGS 权限，超级状态栏还可以为你隐藏抬头通知。我们在运行基于 Android 10 的 ColorOS 7.1 的 OPPO Find X2 Pro 上测试了这一点，令人惊讶的是，尽管 OPPO 对 Android 进行了大量定制，但该应用程序仍然运行良好。

如果你对超级状态栏感兴趣，那么你现在就可以从谷歌 Play 商店链接下载它。如果你想留下任何直接的反馈，也可以看看开发者在 XDA 的论坛帖子。

**[超级状态栏 XDA 论坛线程](https://forum.xda-developers.com/android/apps-games/app-super-status-bar-ticker-text-t4065545)**