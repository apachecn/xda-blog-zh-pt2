# Android 11 通过 Beta 2 达到平台稳定性，现已推出 Google Pixel

> 原文：<https://www.xda-developers.com/android-11-platform-stability-beta-2-available-google-pixel-2-3-3a-4-xl/>

谷歌在 2 月份启动了 [Android 11 开发者预览计划](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel/)，比通常的发布时间表提前了，以便给开发者更多的时间来调整他们的应用程序，以适应新的 Android OS 版本中引入的新平台行为和 API。然而，整个发布周期受到了新冠肺炎疫情的影响。虽然第一个 Android 11 测试版本打算在谷歌 I/O 开发者大会上发布，但该活动的取消导致谷歌发布了一个[即兴的 Android 11 开发者预览版 4，以弥补延迟的](https://www.xda-developers.com/google-android-11-beta-june-3-2020-developer-preview-4-live-release/)。[的第一个测试版于 6 月](https://www.xda-developers.com/android-11-beta-1-update-live-google-pixel-2-3-3a-4-xl-device-controls-api-quick-settings-media-controls/)上线，带来了几个新的变化，集中在人、控制和隐私的主题上。现在，谷歌正在为谷歌 Pixel 设备发布 Android 11 Beta 2。

这是 Android 11 的平台稳定性发布，这意味着 Android 11 的 SDK、NDK API、面向应用的表面、平台行为，以及对非 SDK 接口的[限制已经敲定。谷歌在这里分享了 Beta 2 中](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/)[已解决和已知的主要问题列表](https://developer.android.com/preview/release-notes.html)。展望未来，在接下来的测试版中，Android 11 的行为和 API 的功能将不会有任何变化。因此，开发者现在可以开始更新他们的应用程序，以针对 Android 11 (API 级别 30)，而不必担心未来会有任何意想不到的变化。

与 Android 11 开发者预览版和 Beta 1 版本一样，Beta 2 可安装在 Pixel 2、Pixel 3、Pixel 3a 和 Pixel 4 系列设备上。其他原始设备制造商可能会随后发布自己的版本。你可以前往 [Android 测试版注册页面](https://www.google.com/android/beta)，注册接收谷歌 Pixel 设备的 OTA 更新，或者留意参与 Android 测试计划的原始设备制造商的相应页面。

## Android 11 Beta 2 的变化

### 应用兼容性

应用兼容性是此次发布的主要目标。开发者可以通过在手机或 Android Studio 的模拟器上运行 Android 11 来开始测试他们的应用程序，以确保应用程序运行流畅，所有功能和用户流都按预期工作。开发人员还可以使用支持的 API 在他们的应用程序中集成对通知中的[气泡](https://www.xda-developers.com/googles-messages-beta-now-shows-bubble-notifications-on-android-11/)、[对话](https://www.xda-developers.com/android-11-best-features-not-required/)、[设备控制](https://www.xda-developers.com/android-11-power-menu-device-controls-smart-home-dream/)和[媒体控制](https://www.xda-developers.com/android-11-media-controls/)的支持。

### 测试和调试应用程序的开发人员选项

谷歌还增加了一些新的开发者选项来测试和调试针对 Android 11 的应用。这将包括新的切换来强制启用或禁用更改，而无需更改 targetSdkVersion 或重新编译应用程序进行基本测试。

### 更新目标 Android 版本

谷歌将给开发者一年的时间来改变他们应用的目标版本。这意味着，从 2021 年 8 月开始上传到谷歌 Play 商店的所有新应用，以及从 2021 年 11 月开始对 Google Play 上现有应用的所有更新，都必须针对 Android 11。

### AMA 红迪网

最后，谷歌将在明天，也就是 7 月 9 日，在**太平洋时间下午 12:00/美国东部时间下午 3:00**和**太平洋时间下午 1:20/美国东部时间下午 4:20**之间，在[Android Developers subreddit(/r/Android dev)](https://www.reddit.com/r/androiddev/)上为开发者举办一场 AMA 。来自 Android 工程团队的开发人员将回答与 Android 11 以及一些新工具的应用兼容性相关的问题。您现在可以在[这个帖子](https://www.reddit.com/r/androiddev/comments/hk3hrq/were_on_the_android_engineering_team_ask_us/?utm_source=share&utm_medium=web2x)上提出您的问题，这些问题有望在设定的时间窗口内得到解决。

* * *

谷歌计划在 8 月底左右发布 Android 11“候选发布版本”。这将是 Android 11 最终代码提交到 AOSP git 库之前的最后一次测试。谷歌无意中与 T2 分享了 9 月 8 日的目标稳定发布日期。

我们确实希望在接下来的几个更新中，大多数错误都会被解决，但是如果你是一名开发人员，你可以在这里添加你的反馈以便谷歌解决这些问题。