# 谷歌可能很快会在 Android 中添加内置的蓝牙跟踪器检测功能

> 原文：<https://www.xda-developers.com/google-bluetooth-tracker-detection-feature-android-in-development/>

蓝牙追踪器已经迅速成为热门的科技商品。虽然像 Tile 这样的公司多年来一直提供蓝牙标签，但正是苹果的 [AirTags](https://www.xda-developers.com/apple-airtags-review/) 帮助这些微型设备获得了主流普及。如果你使用的是安卓系统，你通常需要从标签制造商那里下载一个单独的应用程序来监控、扫描和控制你的设备。但似乎谷歌可能很快会让你无需下载第三方应用程序就能扫描附近的追踪器。

最近 APK 对谷歌的一次拆解显示，谷歌正致力于将蓝牙跟踪器检测功能集成到安卓系统中。该功能将是 Google Play 服务的一部分，因此它应该允许谷歌以最小的努力将其带给大众。在最新版本的 Play 服务中，*9 to 5 谷歌*已经发现了与“陌生设备警报”和蓝牙低能耗标签“检测到陌生标签通知”相关的字符串。

根据以下字符串，该功能将能够检测苹果的 AirTag、Tile 标签和 Finder 标签。

```
<string name=”atag_device_name”>ATag</string>

<string name="”finder_device_name”">查找标签</string>

<string name="”tile_device_name”">磁贴标签</string>
```

除了检测之外，谷歌似乎还将允许 Android 用户拨打一个已识别的标签。这将类似于苹果让你在未知的 AirTags 上播放声音。

谷歌在 3 月中旬开始致力于内置蓝牙标签检测功能。它仍在开发中，尚未向用户推出。目前还不清楚谷歌计划何时向安卓用户提供该服务。这个功能也完全有可能永远不会出现。我们会密切关注，如果我们了解到任何关于标签检测功能的新细节，我们会及时通知您。

谷歌也在为第三方 Android 应用开发超宽带 API。该 API 将改善对基于 UWB 的追踪器的支持，并允许开发人员利用超宽带技术在其应用程序中提供新的功能和用例。

* * *

**来源** : [9to5Google](https://9to5google.com/2022/03/29/android-bluetooth-tracker-detection/)