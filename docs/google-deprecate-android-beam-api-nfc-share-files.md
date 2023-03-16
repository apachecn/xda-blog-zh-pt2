# 【更新 2:不回来了】谷歌正在贬低用于与 NFC 共享文件的 Android Beam API

> 原文：<https://www.xda-developers.com/google-deprecate-android-beam-api-nfc-share-files/>

# 【更新 2:不回来了】谷歌正在贬低用于与 NFC 共享文件的 Android Beam API

Android Beam 用于 Android 上的 NFC 文件共享目的。谷歌现在不赞成这些 API，所以开发者将不得不寻找替代品。

**更新 2(美国东部时间 2019 年 5 月 8 日下午 5 点 44 分):**谷歌已经向 [*TechRadar*](https://www.techradar.com/news/android-q-wont-have-android-beam) 证实，Android Beam 不会出现在最终的 Android Q 版本中，也不会回来了。撕开。

**更新 1(美国东部时间 2019 年 1 月 5 日下午 5:20)**:提交的 Android Beam APIs 已经合并。如果 Android Beam 功能在 Android 的未来版本中完全消失，不要感到惊讶。

还记得 Android Beam 吗？在支持 NFC 的非接触式支付终端激增之前，Android Beam 是 NFC 技术唯一潜在的有用应用。Android 4.1+ API 允许你将两部智能手机放在一起，共享小文件，如图像、联系人、网页或文档。然而，现在几乎没有人使用它，所以当我们看到谷歌准备弃用这个 API 时，我们并不感到惊讶。

对于那些不熟悉的人来说， [Android Beam](https://developer.android.com/training/beam-files/) 使用 NFC 来启动两个设备之间的握手。由于 NFC 不能真正用于传输大文件(它太慢了)，这两个设备然后通过蓝牙或 Wi-Fi 直接连接来传输文件。我最后一次使用 Android Beam 是在我寻找一种方法来重新映射 Bixby 按钮时，从 Galaxy S8 商店单元传输截图。从那以后，我真的没有发现任何直接将文件从一部智能手机传输到另一部智能手机的需要——4G LTE 已经足够快，以至于我通常能够通过电子邮件、电报、Hangouts、Discord 或我使用的其他通信渠道快速发送文件。虽然我不确定缺乏使用是不是谷歌放弃 Android Beam API 的原因，但我不会错过这个功能。

不过，API 不会在一夜之间变得不可用。谷歌正在一个名为 android.sofware.nfc.beam 的新 android 平台功能标志后面门控该功能。在运行未来版本 Android(可能是 Android Q)的设备上，Android Beam 支持将不会默认启用。设备制造商必须声明支持 android.software.nfc.beam，就像他们已经声明支持 nfc 本身一样。我们不知道谷歌是否会在 Android 兼容性定义文件(CDD)中添加新的要求，以迫使未来推出或更新到 Android Q 的设备不声明支持 Android Beam，但鉴于谷歌正在反对该 API，很明显他们希望开发者寻找替代方式来启动文件传输。例如，谷歌的文件似乎不依赖于 Android Beam API 的快速离线文件传输功能。