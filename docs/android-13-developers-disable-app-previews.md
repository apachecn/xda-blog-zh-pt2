# Android 13 可以让开发者禁用多任务菜单中显示的应用预览

> 原文：<https://www.xda-developers.com/android-13-developers-disable-app-previews/>

# Android 13 可以让开发者禁用多任务菜单中显示的应用预览

Android 13 可以让开发者在不使用 FLAG_SECURE 的情况下，禁止应用预览显示在多任务菜单中。如何阅读，在这里！

在 Android 上，开发者可以通过设置 FLAG_SECURE 来防止应用被截屏。这有一个预期的副作用，即阻止应用程序预览显示在多任务菜单中，因为这些预览实际上是应用程序在上次使用状态下的截图。银行应用程序和受 DRM 保护的应用程序(如网飞)通常会使用这个受保护的标志，但这是阻止预览显示的唯一方法。现在看来, [Android 13](https://www.xda-developers.com/android-13) 将允许开发者仅禁用那些图像预览，同时仍然允许用户拍摄截图。

正如*斯珀*所发现的，Android 13 引入了[setrecentscreenshotpenabled](https://developer.android.com/reference/android/app/Activity#setRecentsScreenshotEnabled(boolean))API。开发人员希望使用这一特性有几个原因。我能想象的最重要的一点是，在处理敏感数据时，它信任用户来决定截图是否安全。目前， [FLAG_SECURE](https://developer.android.com/reference/android/view/WindowManager.LayoutParams#FLAG_SECURE) 通常用于保护显示版权内容的应用程序的内容被捕获，它的副作用是不允许应用程序预览显示在多任务菜单中。

假设你需要给某人发送一个银行转账的截图。您的银行应用程序的开发人员可以选择设置 FLAG_SECURE，或者使用新的 setRecentsScreenshotEnabled API 来禁用多任务预览中显示的应用程序截图。如果您想要发送该传输的屏幕截图，则在启用 FLAG_SECURE 时无法发送。然而，用户可能不希望在多任务菜单中显示他们银行的敏感信息，如他们的银行余额或最近的转账。这个 API 的引入正好解决了这个问题。

这当然是一个利基问题的解决方案，但我相信还有其他类似的情况。开发者使用 FLAG_SECURE 来隐藏最近菜单中的应用预览绝对是一种变通方法，并不真正用于这种用途，很高兴看到谷歌让开发者可以选择如何隐藏这些应用预览。

* * *

**来源:** [斯珀](https://blog.esper.io/android-13-deep-dive/#disable_recents_screenshotting)