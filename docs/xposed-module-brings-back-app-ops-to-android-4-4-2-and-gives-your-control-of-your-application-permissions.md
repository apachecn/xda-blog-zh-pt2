# Xposed 模块带回 Android 4.4.2 上的 App Ops，让你控制自己的应用权限

> 原文：<https://www.xda-developers.com/xposed-module-brings-back-app-ops-to-android-4-4-2-and-gives-your-control-of-your-application-permissions/>

就在昨天，我们[谈到了 FunkyAndroid 的同事报告的对 Android 4.4.2 源代码的一些更改](http://www.xda-developers.com/android/source-code-commits-in-android-4-4-2-kot49h-reveal-flash-sms-attack-fix-and-app-ops-removal/)。最重要的变化之一是取消了 App Ops，这是一个非常方便的管理应用程序权限的工具。谷歌框架工程师 [Dianne Hackborn](https://plus.google.com/105051985738280261832/posts) 声明[故意隐藏它](https://plus.google.com/+DannyHolyoake/posts/FkfBxA5i3iG)，因为该实用程序仅供谷歌内部调试使用。

虽然 App Ops 最初是供内部使用的，但它受到了许多 XDA 用户的喜爱，他们只是希望一切尽在掌握之中。幸运的是，XDA 论坛成员 [caspase](http://forum.xda-developers.com/member.php?u=4477302) 决定利用他的编程技能，创建一个 Xposed 框架模块，将 App Ops 带回 Android 4.4.2！

开发人员将他的工作描述为一个快速而肮脏的黑客，实现了 *:android:show_fragment* ，并将选项添加回设置应用程序。用更专业的语言来说，这个模块恢复了设置库中的这个[提交](https://android.googlesource.com/platform/packages/apps/Settings/+/37f06a4)。Caspase 还将他的更改集成到设置应用程序中，因此不再需要外部启动器来将应用程序操作恢复到最新的 KitKat 版本。

要使用该模块，您的设备必须是 rooted 用户，并且必须安装 Android 4.4 的 [Xposed Framework](https://www.xda-developers.com/android/xposed-framework-2-4-exits-beta-brings-official-kitkat-support-and-bug-fixes/) 。你可以在[的原始线程](http://forum.xda-developers.com/showthread.php?t=2564865)中找到更多关于变更以及模块本身的信息。