# Google Play 服务不再支持 Android ICS (API 14-15)

> 原文：<https://www.xda-developers.com/google-play-services-dropping-support-android-ics-api-14-15/>

总有一天，我们必须继续前进。这可能包括一段特殊的关系、一份工作或一些琐碎的事情，如旧版本的 Android，Google Play 服务就是这种情况。Android 4.0 冰淇淋三明治是 7 年前发布的，谷歌认为是时候让这个古老的甜点退休了。本周，该公司宣布 Google Play 服务将停止支持 API 14 和 API 15。这包括 Android 版本 4.0 到 4.0.4。

当提到 Android 的主要版本时，很多人都会谈到 Android 碎片化。在最新的例子中，Android Pie 在 4 个月前发布，但市场上一些最大的智能手机原始设备制造商现在正在为更新进行公开测试。这些主要版本的更新确实带来了一些最受关注的新功能(因为它们向 AOSP 添加了新的 API)，但由于 Google Play 服务，还有大量新功能被添加到智能手机中。

由于这一消息，任何运行冰淇淋三明治的人都将不再获得 Google Play 服务的更新。具体来说，运行 Android 4.0 至 4.0.4 的设备将不再从谷歌 Play 商店更新 14.7.99 版以上的 Play Services APK。老实说，不到 1%的活跃 Android 设备运行的是不再接收 Google Play 服务更新的 Android 版本。截至 10 月下旬,《冰激凌三明治》仅在 0.3%的活跃安卓设备上运行。诚然，这仍然不到 600 万台活跃设备，但当全球有超过 20 亿台时，这是一个非常小的数量。

由于今年早些时候新的 SDK 版本的变化，每个库都可以独立发布，并可能更新自己的 minSdkVersion。当前支持 API 级别 14 或 15 的应用程序在更新到较新的 SDK 版本时会遇到构建错误。自然，要修复这些构建错误，Google 推荐的行动方针是将 API 级别 16 作为支持的最低 API 级别。然而，仍然有 600 万活跃的 Android 设备，一些开发者可能希望继续支持他们。

如果你是这些开发者中的一员，那么你可以通过一些配置和代码管理来做到这一点。您可以使用不同版本的 Google Play 服务构建多个支持不同最低 API 级别的 apk。要做到这一点，开发人员需要使用 Gradle 中的构建变体特性，这样你就可以为你的应用的旧版本和新版本定义构建风格

* * *

[**来源:谷歌**](https://android-developers.googleblog.com/2018/12/google-play-services-discontinuing.html)