# Android P 允许应用程序在不禁用指纹解锁的情况下锁屏

> 原文：<https://www.xda-developers.com/android-p-action-lock-screen/>

# Android P 允许应用程序在不禁用指纹解锁的情况下锁定屏幕

Android P 为可访问性服务添加了一个新的设备动作。它允许应用程序锁定屏幕，而不需要密码/PIN/模式。

Android P 的第一个开发者预览版已经发布了近一周，但我们仍在拆包一些好东西。功能和变化的列表太长了，我们不得不[把它](https://www.xda-developers.com/everything-new-android-p-developer-preview/)分成[两部分](https://www.xda-developers.com/android-p-dp1-google-pixel-xl-pixel-2-xl-minor-features/)。与任何更新一样，一些最好的东西隐藏在表面之下。普通消费者不会注意到的特点。Android P 中的一个这样的功能是应用程序可以锁定屏幕，而无需禁用锁定屏幕上的指纹。

以前，应用程序可以通过设备管理 API 锁定屏幕。这种方法的问题是它重置了指纹解锁。因此，每次应用程序锁定你的手机，你就不得不再次输入烦人的密码/个人识别码/模式。Nova Launcher 是一个通过使屏幕变黑并将超时时间变短来解决这个问题的应用程序。开发者在 Android P 中就不用用那种巧妙的招数了。

Android P 为辅助功能服务添加了两个新的设备动作。我们对这个帖子感兴趣的是[GLOBAL _ ACTION _ LOCK _ SCREEN](https://developer.android.com/reference/android/accessibilityservice/AccessibilityService.html#GLOBAL_ACTION_LOCK_SCREEN)。如前所述，它只是允许应用程序锁定屏幕。你不必输入密码/个人识别码/模式。这个功能对于自动化应用程序来说非常棒，[比如 Tasker](https://www.xda-developers.com/tasker-google-play-beta-program/) ，用来控制设备动作。Tasker 的 [TouchTask](https://play.google.com/store/apps/details?id=com.balda.touchtask&hl=en) 的开发者已经开始在应用中实现这一点。