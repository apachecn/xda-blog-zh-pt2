# XDA 之最:Xposed 框架

> 原文：<https://www.xda-developers.com/xposed-best-of-xda/>

Xposed Framework 顾名思义，在软件中，这意味着它允许通用代码被用户代码覆盖，以扩展或修改功能。换句话说，这将系统代码“暴露”给框架，这需要 root 权限，并允许您插入不同的*模块*，带来不同或额外的修改。

Xposed 可以让你轻松地连接到软件，并在之前、之后或代替它们应用指令和更改。虽然定制的 rom 仍然是可靠的和有组织的选择，但是这个框架可以真正开放操作系统的区域，否则将需要很多额外的时间。这最终意味着你可以修补和访问许多东西，否则这些东西需要耗费时间刷新 rom 和其他方法——最好的部分是该系统是模块化的，这意味着你可以随时轻松地启用或禁用你安装的任何附加软件，允许你精确地选择你想要的。

## 模块能做什么？

有很多很多模块，尽管我们希望能在这里一一列出，我们还是会列出我们认为能代表 Xposed 范围的模块。重力盒可能是最受欢迎的模块之一，因为它在一个包中结合了 Xposed 的许多优点。它允许你调整你的用户界面的许多角落和缝隙，以及获得有用的功能，如饼图控件。还有许多其他定制模块，如用于 TouchWiz ROMs 的 [Wanam](http://forum.xda-developers.com/xposed/modules/app-wanam-xposed-customize-stock-t2383484) ，对扩展电源菜单或不同状态栏图标的单独调整也很突出。如果你想要一个 UI 调整，搜索它-你可能会找到它。但是这些包在一个模块中提供了许多模块和功能。

对于那些想要优化体验的人来说，你有很多工具可以使用。例如， [Amplify](http://forum.xda-developers.com/xposed/modules/mod-nlpunbounce-reduce-nlp-wakelocks-t2853874) 可以显著减少唤醒锁的数量，并在几乎不损失功能的情况下获得大量电池电量。 [BootManager](http://forum.xda-developers.com/xposed/modules/app-bootmanager-t2432359) 让你配置哪些应用程序在系统启动时运行，这样你就不必去寻找无用的进程，也不必在真正需要时才加载它们。[原生剪切板](http://forum.xda-developers.com/xposed/modules/native-clip-board-beta-t2784682)为文本选择菜单增加了剪贴板功能，允许你存储多个复制的元素，以便在你需要的时候以你想要的任何顺序粘贴。[抬头隐藏](http://repo.xposed.info/module/com.lewisjuggins.headsuphide)允许你向上、向左或向右滑动 Lollipop 的抬头通知来隐藏它们，而不是消除它们。[精彩的弹出视频](http://forum.xda-developers.com/xposed/modules/mod-pop-video-floating-window-t3039872)通过轻松触发的浮动 YouTube 或浏览器视频，使 Android 上的媒体体验更加无缝和高效。

有些模块也在更深的层次上改变了系统或应用程序的运行方式，这也非常有用。例如， [ActivityForceNewTask](http://repo.xposed.info/module/com.germainz.activityforcenewtask) 让其他应用程序启动的应用程序远离前者，允许你在它们之间来回切换，而不会让召唤的应用程序消失。 [AppSettings](http://forum.xda-developers.com/xposed/modules/mod-app-settings-v1-9-2014-05-14-t2437377) 可以改变应用程序的通用设置，比如它们的 DPI，旋转行为，它们是否是沉浸式的，它还允许坚持通知(这是个人的最爱)。还有像 [XPrivacy](http://forum.xda-developers.com/xposed/modules/xprivacy-ultimate-android-privacy-app-t2320783) 这样专注于隐私的模块，可以通过向应用程序提供虚假或无效的信息来防止应用程序泄露敏感数据，还有大量面向安全的模块。

试图总结 Xposed 无穷无尽的功能是一项艰巨的任务，还有许多其他模块值得一试，我们没有列出。许多模块也是特定于特定手机或特定 OEM 的 rom 的，所以一定要在你的设备的子论坛中寻找专用位。如果你想得到一个包含许多简短描述的详细列表，可以去 [Xposed Modules Collection](http://forum.xda-developers.com/xposed/modules/index-xposed-modules-collection-post-t2327541) 线程，四处看看或者搜索你想要的。 [Xposed 论坛](http://forum.xda-developers.com/xposed)也是一个开始搜索和学习模块的好地方，用户可以随时帮助你——只要确保你先搜索你的问题，然后在适当的帖子里发帖。无论您做什么，Xposed 的起点应该是 [Xposed 信息线程](http://forum.xda-developers.com/xposed/xposed-installer-versions-changelog-t2714053)，我们鼓励您通读它，以便更好地理解平台以及安装过程和功能的基础。我们不能夸大该网站搜索功能的重要性，无论何时你有任何疑问或将踏上新的 XDA 之旅，首先寻求搜索按钮的建议总是明智的！

## 我需要什么？

安装 Xposed 的第一步是[在我们的论坛上阅读它的信息线索](http://forum.xda-developers.com/xposed/xposed-installer-versions-changelog-t2714053)。首先，必须说明的是，与大多数这种深度和广度的事情一样，这个过程存在一些固有的风险。然而，通过注意、计划和精确的执行，这些可以很容易地被最小化或完全消除。如果您确实打算安装 Xposed，请确保访问您设备的子论坛或 rom 的线程，并快速查看不兼容或可能出现的任何问题，因为该过程可能因设备或 ROM 而异。记住:**搜索按钮是你的朋友**，所以先去找他！

根据您的 Android 版本和 ROM，安装框架本身可能相当简单。棒棒糖用户可以在这里找到需要的文件[。如帖子中所述，你必须刷新**x 曝光-sdk21-arm-*。在自定义恢复中压缩**文件并安装 **XposedInstaller_3.0-alpha*。apk** 用于允许您管理模块的应用程序。旧版本的 Android 可以在这里找到安装程序 apk 列表。请记住，一些 Lollipop ROMs(即 TouchWiz ROMs)不受 Lollipop Alpha 官方版本的支持，但有解决方法](http://forum.xda-developers.com/showthread.php?t=3034811)[。首先，检查你的设备和 ROM 是否与 Xposed 完全兼容(无论是在 Xposed 论坛的帖子里还是你的设备子论坛里),然后仔细阅读下面的步骤。](http://forum.xda-developers.com/xposed/unofficial-xposed-samsung-lollipop-t3113463)

至于安装模块的过程，大部分都可以很容易地从 Xposed 应用程序中访问，该应用程序的特点是[有一个超过 600 个模块的大存储库](http://repo.xposed.info/module-overview)，你可以下载——是的，有这么多。虽然它们中的一部分在功能上重叠或者不提供全球兼容性，但是它们中的一些可以单独地完全革新你的电话的许多方面。它就像安装一个模块一样简单，通过选中一个框并重新启动来激活它。与安装程序本身一样，明智的做法是在开始之前确保模块是兼容的。但是如果出现问题，您可以在启动时按下硬件键，等待振动提示，然后再次轻敲同一个键四次或更多次(为了安全起见，您可以重复轻敲该键)，从而禁用框架本身。

**有用资源:**

以一种简化的方式来谈论 Xposed 消除了系统背后的复杂性，因为注入这样一个广泛的调整框架是非常难以实现的，尤其是以一种安全和优化的方式。这就是为什么资深公认开发人员 rovo89 被认为是 XDA 有史以来最聪明的开发人员之一，他对这项事业的承诺甚至战胜了 Lollipop 的 Android 运行时带来的巨大障碍。

作为最后一轮建议，请记住，许多模块可以看到彼此之间的冲突，因此最好了解它们做什么以及它们涉及到什么，以预测或理解任何可能的问题。随着您对该平台的熟悉和了解，您将会发现，您将能够为您的用例找到最佳配置，并避免问题或错误。永远开放地阅读、学习和理解社区发展的作品。经验也很重要，所以不要害怕尝试——但一定要小心谨慎。最后，请务必始终友好和文明，并记住给予应有的信任，因为没有我们网站开发人员的不懈努力，这一切都是不可能的。

我们希望你喜欢我们的展示和我们社区的所有优点，如果你迷路了，我们会在这里帮你走出困境！