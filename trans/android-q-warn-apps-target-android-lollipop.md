# Android Q 警告运行 Android Lollipop 或更老版本应用的用户

> 原文：<https://www.xda-developers.com/android-q-warn-apps-target-android-lollipop/>

升级他们的应用程序以支持最新的 Android 平台功能通常对开发者最有利。每一个新的 Android 版本都提供了早期版本所没有的新的 API 和特性。然而，每一个新的 Android 版本也对应用程序的功能增加了新的限制，这是一些应用程序开发者不喜欢的。例如，许多应用程序避免将其目标 API 级别提升到 Android Marshmallow 或更高版本，这样他们就可以避免实现运行时权限。谷歌最终开始打击这种行为，对上传和更新到谷歌 Play 商店的应用程序施加了新的限制，但他们也在 Android Pie 中添加了一个警告，以羞辱仍未更新过 Android 4.1 Jelly Bean 的应用程序。根据 Android 开源项目最近的一次提交，如果用户正在运行的应用程序针对 Android 5.1 Lollipop 或更早版本，Android Q 似乎会警告用户。

## Android 应用的现代化

去年 12 月，谷歌[推出了一项新政策](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)来更新谷歌 Play 商店的安卓应用。根据新政策，从 2018 年 8 月 1 日开始，所有提交给谷歌 Play 商店[的新应用必须以 API 级别 26 或更高为目标(这意味着 Android 8.0 Oreo、Android 8.1 Oreo 或 Android 9 Pie。)此外，从 2018 年 11 月 1 日开始，Play Store 上现有应用的所有更新也必须以 API 级别 26 或更高为目标。这项政策将迫使最活跃的开发和新的应用程序遵守最新版本的 Android 的新的安全，隐私，内存优化和电池节省功能。然而，该政策并不意味着应用程序将在运行旧版本 Android 的设备上停止工作——开发者仍被允许设置自己的最低 API 级别。另一方面，谷歌最新版本的 Android，Android 9 Pie，进一步鼓励应用程序开发者更新他们的应用程序，明确警告用户，当他们运行的应用程序太旧了，可能无法正常工作。](https://www.xda-developers.com/developers-new-app-play-store-api-level-26/)

根据在 AOSP 的的[，这个`PLATFORM_MIN_SUPPORTED_TARGET_SDK_VERSION`被增加到 23。这个构建标志转换成系统属性`ro.build.version.min_supported_target_sdk`。启动任何应用程序的活动时，系统都会使用此属性。系统会检查应用程序的目标 SDK 级别，如果低于`ro.build.version.min_supported_target_sdk`中定义的值，则会向用户显示一条警告消息，提示应用程序可能无法正常工作。](https://android-review.googlesource.com/c/platform/build/+/737545)

就目前而言，Android Q 看起来不会阻止用户运行真正旧的 Android 应用程序。我们可以想象，会有一小部分用户对这样的限制不满意，但他们会直言不讳。有许多很少更新的应用程序被用在没有替代品的专业领域。不过，每次用户在 Android Q 中启动旧应用时显示这一警告可能会让用户抱怨应用被更新或替换。

如果您想查看设备上安装的应用程序的目标 API 级别，可以使用下面链接的应用程序。在我的设备上，有 4 个我经常使用的应用程序会触发这个警告:Titanium Backup、AZ Screen Recorder、Brother iPrint & Scan 和终端模拟器。

最后，我们应该注意到，提交消息表明`PLATFORM_MIN_SUPPORTED_TARGET_SDK_VERSION`标志正在“临时”增加。这意味着谷歌还没有完全决定是否将限制设置在 SDK 级别 23，可能会选择更高或更低的级别。如果我们发现这面旗帜在 AOSP 有任何进一步的变化，我们会让你们都知道。