# Chrome OS 64 Beta 让多个 Android 应用程序同时运行，无需暂停

> 原文：<https://www.xda-developers.com/chrome-os-64-android-apps-simultaneous/>

去年，[谷歌为部分 Chromebooks](https://www.xda-developers.com/xda-external-link/google-demos-how-android-apps-work-and-look-on-chromebooks/) 发布了 Play Store，并宣布 Android 应用程序将可在 Chrome OS 上使用。现在，多种 Chromebooks 都支持 Android 应用程序，谷歌一直在努力改善 Android 应用程序以及整个 Chrome OS 的用户体验。最近几个月，我们已经看到谷歌致力于在平板模式下增加[分屏](https://www.xda-developers.com/chrome-os-dev-channel-enable-splitscreen-tablet-mode/)，以及[通知内联回复](https://www.xda-developers.com/chrome-os-notifications-inline-reply/)。

现在，Reddit 上的一名用户(通过 *Chrome Unboxed* ) 注意到，Android 应用中的并行任务在 Chrome OS 64 Beta 中可用。对于一些背景，Android 应用程序在不聚焦时会暂停它们的状态。这种行为在智能手机上是有意义的，但在可以同时运行多个 Android 应用的桌面上就不一样了。

如果用户运行带有实时数据或游戏的应用程序，当用户在 Chromebook 上点击离开应用程序时，应用程序会暂停，导致用户体验不佳。对于桌面用户来说，打开的应用程序的预期行为是，即使当焦点转移到另一个窗口时，它也将保持活动和运行。这就是所谓的真正的多任务处理。

Android 应用程序暂停状态的行为没有意义，因为用户可以在 Chromebook 上比在智能手机上更容易地看到他们所有打开的应用程序。此外，与移动设备相比，桌面设备支持真正的多任务处理更有意义。暂停行为因此增加了混乱，不符合桌面用户的期望。

这个问题的纠正很简单:当用户切换到另一个窗口时，允许应用程序继续运行而不暂停它们的状态。Android 上的并行任务允许操作系统保持所有应用程序运行和打开，直到用户暂停活动或退出应用程序。为了启用该功能，请在 Chrome OS 中打开 Android 设置页面，然后进入开发者选项。一路向下滚动，寻找一个开关，即使焦点在另一个窗口上，也可以让 Android 应用程序继续运行。

谷歌 Pixelbook 上的 Chrome OS 63 Stable 不支持 Android 应用程序中的并行任务。另一方面，运行 Chrome OS 64 Beta 的宏碁 Chromebook 15 确实支持并行应用，这是通过 *Chrome Unboxed* 打开的，并在下面的视频中展示。

*Chrome Unboxed* 表示，启用并行应用程序后有了显著的差异，多个应用程序可以并行运行，没有暂停或任何数据丢失。因此，用户体验要好得多，并且符合桌面用户的期望。

Chrome OS 64 的稳定版本有可能不会包含该功能，但包含的可能性很高。如果在 Chrome OS 64 Stable 中发现它，用户就少了一个不使用 Chrome OS 的理由，因为它继续留下其以网络为中心的标签，并成为一个越来越多功能的操作系统。

* * *

[**来源:/u/clubtech**](https://www.reddit.com/r/chromeos/comments/7k18x6/fyi_chromeos_64_beta_has_a_toggle_to_allow_true/)

[**Via: Chrome 拆箱**](https://chromeunboxed.com/news/android-parallel-tasks-incoming-chrome-os-64/)