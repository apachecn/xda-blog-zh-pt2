# SuperFreezZ 是 Greenify 的开源替代品，它会杀死后台运行的应用程序

> 原文：<https://www.xda-developers.com/superfreezz-freeze-background-apps/>

在 Android 智能手机上，任务管理器被广泛认为是不必要的。我们大多数人可能都同意这种观点，但现实是仍然有许多行为不端的 Android 应用程序，大多数任务“杀手”实际上除了清除最近的应用程序视图外，并没有做任何有用的事情(这并没有真正“杀死”应用程序)，许多用户还没有升级到对后台应用程序实施了更多限制的新 Android 版本。这就是为什么直到今天，像 [Greenify](https://www.xda-developers.com/greenify-keeps-your-android-running-smoothly/) 和 [Brevent](https://www.xda-developers.com/brevent-is-an-open-source-alternative-to-greenify-works-without-root/) 这样的应用程序仍然非常受欢迎。许多用户对 Greenify 和 Brevent 都深信不疑，但由于它们是闭源的，一些用户对它们持谨慎态度。如果你正在寻找一个开源的替代品，看看 XDA 青年成员 hcur 的 SuperFreezZ。

该应用程序的工作方式就像 Greenify 在非根模式下的工作方式一样。它使用辅助服务来自动进入设置并强制关闭应用程序。您可以选择允许应用程序访问 UsageStats API，以便它可以检测和杀死不常用的应用程序。你可以称之为“冻结”、“休眠”，或者随便什么，SuperFreezZ 会杀死你选择的在后台运行的应用程序。在应用程序的设置中，你可以在屏幕关闭时启用应用程序冻结，这需要禁用“电源按钮立即锁定”选项，并且你可以更改应用程序必须处于非活动状态才能被杀死的时间。

一个应用被 SuperFreezZ 强制关闭并不意味着它不能再次启动备份，尤其是在 Android 牛轧糖上。有一种方法可以防止旧版本 Android 上的应用程序在后台唤醒，但它需要使用一个隐藏的 ADB 命令。或者，你可以完全[禁用任何应用](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)、[甚至系统应用膨胀软件](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)，阻止它运行。如果这太复杂，那么你可以使用类似 [Shelter](https://www.xda-developers.com/shelter-open-source-sandboxing-app/) 或 [Island](https://forum.xda-developers.com/android/apps-games/closed-beta-test-incoming-companion-app-t3366295) 的应用程序来隔离使用 Android 原生工作档案功能的应用程序。

超级用户有许多不同的方法来控制他们设备上运行的应用程序。像 SuperFreezZ 这样的应用只是众多选择之一。即使它不是最强大或最健壮的，它也是免费和开源的，这可能是你们中的一些人安装它的足够理由。你可以从 F-Droid 下载这个应用程序，或者从 GitLab 上的源代码编译这个应用程序。如果你有任何问题，你可以在 XDA 论坛的帖子里发表。

**[从 F-Droid](https://f-droid.org/packages/superfreeze.tool.android/)** [**下载 SuperFreezZ 访问 XDA 线程**](https://forum.xda-developers.com/android/apps-games/superfreeze-t3816388) [**查看源代码**](https://gitlab.com/SuperFreezZ/SuperFreezZ/)