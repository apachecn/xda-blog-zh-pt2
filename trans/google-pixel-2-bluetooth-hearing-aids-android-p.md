# 谷歌 Pixel & Pixel 2 将在 Android P 上支持蓝牙助听器

> 原文：<https://www.xda-developers.com/google-pixel-2-bluetooth-hearing-aids-android-p/>

Google I/O 2018 正在[快速接近](https://www.xda-developers.com/google-i-o-2018-may-8-shoreline-amphitheater/)。我们期待在活动中了解更多关于 [Android P](https://www.xda-developers.com/tag/android-p/) 的新内容。谷歌已经[向我们](https://www.xda-developers.com/everything-new-android-p-developer-preview/)展示了[首个 Android P 开发者预览版](https://www.xda-developers.com/android-p-developer-preview-1-google-pixel-xl-pixel-2-xl/)的新功能，但是还有很多好东西该公司尚未公布。[导航手势](https://www.xda-developers.com/android-p-iphone-x-navigation-gesture/)据传将在活动中出现，据称它们会让人想起 [iPhone X pill bar 手势。](https://www.xda-developers.com/android-p-iphone-x-navigation-gesture-2/)由于 Android 开源项目，我们能够跟踪下一个 Android 版本中即将推出的一些功能，并且我们发现了一个会让听力障碍者兴奋不已的功能:支持蓝牙助听器。根据一系列代码提交，谷歌 Pixel 和 Pixel 2 智能手机将原生支持连接蓝牙助听器。

支持蓝牙的助听器的优势在于，它允许听力障碍者在听周围声音的同时，仍能享受标准的蓝牙功能，如打电话或听音乐。目前，重听人不能将他们的蓝牙助听器设备与大多数 Android 设备直接连接(尽管他们可以将他们的设备连接到 iPhones。)蓝牙无线助听器的制造商通常会提供一个额外的蓝牙设备(如 [ReSound Phone Clip+](https://www.resound.com/en/hearing-aids/accessories/phone-hearing-aid) )，它可以夹在人身上，充当助听器和 Android 智能手机之间的桥梁。不得不携带第二个蓝牙设备并不理想，这就是为什么谷歌一直致力于通过对蓝牙无线助听器的原生支持来使 Android 更容易访问。

* * *

## Google Pixel & Pixel 2 在 Android P 中本地支持蓝牙助听器

11 月，我们[发现了一些承诺，即](https://www.xda-developers.com/android-getting-support-for-bluetooth-hearing-aids/)建议在 Android 的下一版本中对蓝牙助听器提供原生支持。当时，实施还处于开始阶段。但是当我们接近 Google I/O 时，与助听器相关的代码提交数量[已经大幅增长](https://android-review.googlesource.com/#/q/hearing-aid+(status:open+OR+status:merged))。现在安卓系统中有了一个[助听器蓝牙模式](https://android-review.googlesource.com/549481)，一个[助听器管理器](https://android-review.googlesource.com/#/c/platform/system/bt/+/546902/)，等等。再次引发我们对这个话题兴趣的最新代码提交是一系列标题为“禁用除 Pixel 之外的所有平台的助听器配置文件”的提交[我认为这是不言自明的，不是吗？](https://android-review.googlesource.com/#/q/topic:enable-hearing-aid-only-for-pixel+(status:open+OR+status:merged))

正如您在提交描述中看到的，无线蓝牙设备的新助听器配置文件将在 AOSP 禁用，但默认情况下会为 Google Pixel、Google Pixel XL、Google Pixel 2 和 Google Pixel 2 XL 启用。这是通过在蓝牙系统应用程序的覆盖图中将布尔值`profile_supported_hearing_aid`设置为 true 来实现的，如下所示。

这些更改的提交已经合并。然而，由于我们离 Google I/O 和 Android P Developer Preview 2 的预期发布如此之近，我不认为我们会在下一个预览版中看到这个功能。相反，我希望最早能在开发者预览版 3 中看到它，但它肯定会出现在 p 的第一个稳定版本中。

当其他设备开始接收 Android P 更新时(如[小米 Mi Mix 2S](https://www.xda-developers.com/xiaomi-mi-mix-2s-android-p-developer-preview/) 或[华为 Mate 10 Pro](https://www.xda-developers.com/huawei-mate-10-pro-android-p/) )，那么将由他们来启用对这一新蓝牙配置文件的支持。希望将来有更多的 Android 设备支持这一功能，因为可访问性似乎是 iOS 仍然胜过 Android 的一个领域。谷歌在 I/O 有一个致力于 Android 可访问性的[会议，我们希望在那里了解更多关于这个特性的信息。我们将在活动中为您带来最新的 Android 新闻。](https://events.google.com/io/schedule/?section=may-8&sid=5b089699-0940-4e9d-98d2-0ca9938b8680)