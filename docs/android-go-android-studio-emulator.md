# [更新:仍在计划中]谷歌正致力于将 Android Go 图像添加到 Android Studio 模拟器中

> 原文：<https://www.xda-developers.com/android-go-android-studio-emulator/>

**更新(美国东部时间 8/29/19 @上午 10:45):**谷歌证实，他们仍在计划为 Android Studio 添加一个 Android Go 模拟器。

Android Go 是谷歌基于 Android 8.1 Oreo 的精简版 Android，旨在运行在较低端的硬件上，降低了 RAM 和存储需求。它是去年宣布的，最近我们看到它达到了它的第一个设备。对于开发者来说，这是一个令人兴奋的前景。虽然一些设备将搭载 Android Go，但[没有什么能阻止定制 ROM 开发者创建自己的 Android Go 版本并在任何设备上运行](https://www.xda-developers.com/android-go-old-android-8-1-oreo/)。这很好，但由于存储和 RAM 的限制，谷歌认为有必要创建 Android Go 特定的应用程序——至少在 [YouTube Go](https://www.xda-developers.com/youtube-go-available-130-countries-worldwide/) 和[谷歌地图 Go](https://www.xda-developers.com/google-maps-go/) 的情况下是如此。在创建应用程序时，开发人员可以使用 Android Studio 模拟器来测试他们的应用程序，但在 Android Go 上却不是这样。你不能在基于 Android Go 的模拟器上测试你的应用，因为谷歌没有添加图像。

然而，根据谷歌代表在 Reddit 上发表的评论，这种情况似乎很快就会改变。据该代表称，谷歌“正在向 Android Studio 的模拟器提供官方 Android Go 图像”。这意味着应用程序开发人员很快就可以测试他们的应用程序在与真实世界的 Android Go 设备相同的条件下如何运行。

显然，这意味着开发人员将不得不等到图像可用，但是如果您不能等待，同一位代表给出了关于现在如何自己模拟它的说明。只需启动 Android Studio 并在 API 级别 19 设置一个 Android Studio 模拟器映像，然后将 RAM 大小减少到 512MB 并降低 JVM 堆大小。这应该足以作为一个测试环境，直到谷歌提供正式的图像在 Android Studio 模拟器中启动。

谷歌表示，他们预见到这种 Android 变体将在未来的设备上运行，该平台的目标是让每个人都可以使用基本的在线计算。第一步是为开发者提供为平台开发应用的工具。

* * *

## 更新:仍在计划中

一名谷歌代表表示，一年多前，他们正在 Android Studio 模拟器中提供官方 Android Go 图像。现在，另一名谷歌员工表示，Android Studio 将在“未来”支持 Android Go 模拟器。这是对一个关于测试 Android Q beta Go 版的问题跟踪线程的回复。我们仍然没有一个坚实的时间框架来实现这一点，但至少我们知道它仍然在工作中。

**来源:[谷歌问题跟踪者](https://issuetracker.google.com/issues/138082683#comment4)**