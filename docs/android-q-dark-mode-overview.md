# 到目前为止我们所知道的关于 Android Q 黑暗模式的一切

> 原文：<https://www.xda-developers.com/android-q-dark-mode-overview/>

在我们的第一篇[帖子](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)中，我们详细介绍了从我们获得的正在开发的 Android Q 版本中发现的变化，我们简要地谈到了让每个人都兴奋的黑暗模式。综上所述，谷歌在 Android Q 中内置的黑暗模式可以通过显示设置中新的“黑暗模式”选项来启用。黑暗模式可以始终关闭、始终开启，也可以在晚上自动启用，在早上禁用。黑暗模式主题系统用户界面(音量面板，电源菜单，快速设置面板，通知)，设置应用程序和框架(强调颜色等)。).

*上图:谷歌 Pixel 3 XL 上 Android Q 中的黑暗模式。下图:谷歌 Pixel 2 XL 上 Android Pie 中的 Light 主题。*

然而，谷歌不仅仅希望系统元素是黑暗主题。他们还努力确保所有的第一方应用程序在用户切换开关时都支持黑暗模式。像[消息](https://www.xda-developers.com/android-messages-redesign-dark-mode/)、[电话](https://www.xda-developers.com/google-phone-v26-dark-theme/)、[联系人](https://www.xda-developers.com/google-contacts-adds-dark-theme/)、[新闻](https://www.xda-developers.com/google-news-5-5-dark-theme/)、[玩游戏](https://www.xda-developers.com/google-play-games-dark-theme/)、 [YouTube](https://www.xda-developers.com/youtube-dark-mode-android-roll-out/) 、[地图](https://www.xda-developers.com/google-maps-manual-dark-mode-navigation/)等谷歌应用已经更新了面向用户的黑暗模式切换，而其他应用如[谷歌 Chrome](https://www.xda-developers.com/android-q-system-dark-mode-theme/) 仍在消除谷歌 I/O 2019 之前的任何缺陷。谷歌也开始鼓励第三方应用程序开发者在他们的应用程序中采用黑暗主题，因为该公司承认这对电池寿命很有好处(至少在配有有机发光二极管显示屏的智能手机上)。)

为了帮助开发者更新他们的应用程序，支持 Android Q 的黑暗模式，谷歌正在提供一个新的开发者选项，似乎可以强制所有应用程序都改为黑暗模式。这个选项并不适合那些想把所有东西都设置成暗模式的用户，因为系统很难为所有没有暗模式的应用程序选择正确的颜色。幸运的是，谷歌已经为应用程序支持黑暗模式奠定了基础，已经有许多应用程序在启用 Android Q 的覆盖黑暗模式选项后看起来很好，即使该应用程序没有面向用户的黑暗模式切换。这里收集了 24 个不同应用的截图，展示了当使用 Android Q 的 override dark mode toggle 强制使用黑暗模式时，它们的样子。并不是每个应用程序看起来都一样好，我将在下面向你展示。

### 在 Android Q 中实现黑暗模式

在 API level 8 (Android 2.2 Froyo)中，Google 为资源引入了[-夜间限定符](https://developer.android.com/guide/topics/resources/providing-resources)。应用开发者可以使用 [UiModeManager](https://developer.android.com/reference/android/app/UiModeManager.html#MODE_NIGHT_AUTO) 中的 setNightMode 在白天和夜晚模式之间切换。但是，如果设备的 API 级别为 22 或更低，setNightMode 要求设备处于车载模式或停靠模式。 [AppCompat v23.2](https://developer.android.com/reference/android/support/v7/app/AppCompatDelegate.html#mode_night_follow_system) 带来了 DayNight 实现，允许像 Reddit 客户端这样的应用程序使用 appcompatdeletegate . setdefaultnightmode()根据一天中的时间自动在白天和夜晚主题之间切换。API level 28 (Android 9 Pie)使得 MODE _ NIGHT _ FOLLOW _ SYSTEM(setDefaultNightMode()的默认值)遵循设置- >开发者选项- >夜间模式中用户自定义的系统设置。谷歌正在对 AppCompat 中的 DayNight API 进行改进，特别是在“经常遇到的问题”方面，比如 WebView 的问题。最后，谷歌启用了[夜间模式检测](https://android.googlesource.com/platform/frameworks/base/+/master/core/res/res/values/config.xml#3422)，并在 Android Q 的框架中[屏蔽了没有](https://android.googlesource.com/platform/frameworks/base/+/master/core/res/res/values/config.xml#915) [MODIFY_DAY_NIGHT_MODE](https://android.googlesource.com/platform/frameworks/base/+/master/core/res/AndroidManifest.xml#3841) 签名/特权权限的应用。后一种变化意味着应用程序不能再修改系统范围的夜间模式，这使得最近的一个消息错误在 Android Pie 中困扰用户。

**更新:**对 [AndroidX](https://www.xda-developers.com/googles-androidx-aosp/) 支持库的[更新](https://android-review.googlesource.com/c/platform/frameworks/support/+/878201)将使开发者更容易在设备进入节电模式时自动启用应用程序中的黑暗模式。

### 安卓 Q 强制黑暗模式

像 Snapchat、Slack、AOSP 电子邮件、AOSP 消息、AOSP 拨号器和许多其他应用程序都有夜间资源限定符，即使它们没有为用户提供在夜间模式下使用应用程序的方法。其他没有硬编码夜间资源限定符的应用程序，如脸书和 Instagram，在 Android Q 的覆盖黑暗主题打开时，可能会也可能不会看起来很好。Instagram 看起来不错，而脸书需要做很多工作。从我的测试来看，覆盖夜间模式开发者选项与可访问性设置中的颜色反转非常不同——也许谷歌打算在 Android Q 开发者预览正在进行的时候，用这个功能来帮助开发者为他们的应用程序创建黑暗模式。不过，在 Android Q 的源代码发布或谷歌发布相关文档之前，我们不会确切知道这项功能是如何工作的。

Android Q 中的覆盖黑暗模式在使用 WebViews 的应用程序中是最糟糕的。

在来自谷歌的 Chris Banes 和 Alan Viverette 的“[一个像素颜色的成本](https://www.youtube.com/watch?v=N_6sPd0Jd3g)”演讲中，两人鼓励开发者通过以下方式实现深色主题:

*   在 AppCompat 中使用 DayNight API。股票小工具会自动响应夜间模式的变化，或者你也可以在你的应用程序中添加一个开关。
*   通过调用 getTheme()在运行时动态应用覆盖主题。applyStyle()。更多信息可以在之前的演讲中找到[这里](https://www.youtube.com/watch?v=TIHXGwRTMWI)。
*   构建你的应用依赖于使用主题属性，如 colorForeground、colorControlNormal、colorAccent 等。
*   为您的资源添加夜间限定词。-night 限定符应该用于难以提取主题颜色的资源。
*   启用反转颜色模式(设置->颜色->颜色反转)来快速了解您的应用程序在黑暗模式下的外观。如果你想对你的应用进行颜色反转的截图，你应该知道[颜色反转不会出现在截图](https://stackoverflow.com/questions/34873839/how-to-capture-screen-with-color-inversion-done-using-accessibility-in-android)中。

在发布时，Android Q 的黑暗模式将扩展到第一方的谷歌应用程序，但我们希望第三方应用程序能够迅速将黑暗主题应用到他们的应用程序中。此外，我们希望当用户启用系统范围的设置时，更多的应用程序自动改变到他们的夜晚主题。目前，我见过的唯一一个在 Android Q 的全系统黑暗模式启用时自动改变主题的应用是谷歌联系人。我们将在几个月后 Android Q 发布时看到事情的发展，但是对所有正在阅读这篇文章的开发者来说:拥抱黑暗的一面吧！

【LineageOS 供稿人[乔伊·里佐利](https://wiki.lineageos.org/contributors.html)供稿。