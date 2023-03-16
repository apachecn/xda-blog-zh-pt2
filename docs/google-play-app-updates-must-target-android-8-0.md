# PSA:Play Store 上的所有应用更新现在都必须针对 Android 8.0+

> 原文：<https://www.xda-developers.com/google-play-app-updates-must-target-android-8-0/>

Android 的碎片化问题不仅仅局限于手机和使用号码。这个问题也延伸到了应用程序。许多应用程序开发人员通常会跳过立即优化他们的应用程序到最新的 Android 版本，要么在几个月后支持它，要么完全不支持它。这样做有两个原因:要么是新的 API 不是开发者的优先考虑事项(新的 Android 版本通常需要几个月才能达到相当大的受众，所以它很少在开发者的待办事项列表上)要么是应用程序故意针对旧版本的 Android(例如，Snapchat 多年来一直针对 Android Lollipop，以避免实现 Android Marshmallow 上引入的粒度权限)。

这导致了尴尬的局面，应用程序可以不受任何限制地自由消耗电池，垃圾邮件通知，并在没有询问用户的情况下使用他们想要的所有权限，这是应用程序针对旧 SDK 的结果。你也可能遇到这样的情况，某个应用程序根本无法工作，被迫关闭或崩溃，因为它在最新的 Android 平台上不受支持或未经测试。总而言之，这种情况显然需要谷歌的干预——他们已经干预了。

从今天，11 月 1 日开始，所有上传到谷歌 Play 商店的应用程序更新必须至少针对 API 级——这意味着如果你想根据新的 Google Play 要求向用户推出新的更新，你的应用程序需要开始针对 Android 8.0 Oreo 和更高版本。如果你的应用仍然针对 Android 7.1 牛轧糖或更低版本，你将无法向 Google Play 上传新的 APK，也无法发布更新。请记住，我们讨论的是 targetSdkVersion，而不是 minSdkVersion。

谷歌给了开发者足够的时间来更新他们的应用。针对 API 26 [的截止日期最早是在 2017 年 12 月](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)宣布的，自 8 月以来，应用开发者[已经无法](https://www.xda-developers.com/developers-new-app-play-store-api-level-26/)向 Play Store 上传针对 Android 牛轧糖或更低版本的新应用。同样的要求如今也延伸到了应用程序更新。请记住，最低 targetSdkVersion 现在将开始逐年增加，从 2019 年 8 月(新应用)和 2019 年 11 月(应用更新)开始，应用将被迫支持至少 API 级别 28 (Android 9 Pie)。

对于用户来说，这意味着从今天起发布到 Play Store 的所有应用更新都应该至少支持 Android Oreo 平台的功能，这意味着他们将开始支持自适应图标、通知通道、背景限制等功能。如果你是一名开发者，而你的应用还没有针对 Android Oreo，现在是时候这么做了。