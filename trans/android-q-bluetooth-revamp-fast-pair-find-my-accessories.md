# Google I/O 2019:在 Android Q 中查找我的配件和新的蓝牙设置

> 原文：<https://www.xda-developers.com/android-q-bluetooth-revamp-fast-pair-find-my-accessories/>

2017 年末，谷歌[宣布](https://www.xda-developers.com/fast-pair-quick-bluetooth-pairing-headphones/)一项名为“快速配对”的新功能。这项功能首次与 Pixel 2 的 [Pixel Buds](https://www.xda-developers.com/google-pixel-buds-google-assistant/) 配件一起推出，旨在改善智能手机与蓝牙配件的首次配对。去年 11 月，[更新了](https://www.xda-developers.com/fast-pair-android-sync-chromebook-support/)Fast Pair，以支持登录同一个谷歌账户的安卓设备之间同步保存的蓝牙连接。在谷歌 I/O 2019 上，谷歌悄悄宣布了一项名为“查找我的配件”的 Fast Pair 新功能。他们还展示了为运行 Android Q 的设备修改的蓝牙设置页面。

## 查找我的配件:新的快速配对功能

Fast Pair 是 Google Fast Pair Service (GFPS)的缩写，是 Google Play 服务的一部分，它支持所有连接到具有 A2DP 或 HFP 配置文件的配件的 Android 6.0+设备。Android 手机(快速配对搜索者)扫描来自附件(快速配对提供商)的 BLE 广播，该附件包含快速配对有效载荷，如果找到，则发送到谷歌的服务器，与他们的提供商模型数据库进行比较。然后会向用户显示一个通知，要求他们“点击以配对”如果用户接受，智能手机和配件之间就会启动蓝牙连接。随后尝试与蓝牙配件配对时，将显示“您保存的设备可用”通知。

谷歌宣布，一项名为“查找我的配件”的新功能将适用于所有支持快速配对的蓝牙配件。如果用户丢失了耳塞，它会在“查找我的设备”应用程序的地图上显示耳塞最后断开的位置，从而帮助用户找到耳塞。它会通过检查连接质量和上次使用时间来告诉您范围，并让您解除配件配对或播放音量渐增的铃声。

 <picture>![](img/b79715230cd0444d84d71fc848892e49.png)</picture> 

"Find My Accessories" in the Find My Device app. Source: Google.

## Android Q 中的新蓝牙功能

在 Android Q 中，谷歌正在迎合真正的无线耳机。他们正在开发的一项新功能是，当用户打开或关闭充电外壳时，会在手机上显示电池通知。谷歌还将致力于改造蓝牙设置页面，作为所有通过蓝牙连接的设备的中央管理。在这里，您可以查看附件的详细电池信息，忘记附件的配对，管理助理和通知设置，更改触摸控制，控制音频调谐，以及切换入耳式检测。

目前，谷歌不打算在蓝牙设置中提供一套标准化的选项。相反，他们仍然更喜欢原始设备制造商提供他们自己的配套应用，但他们敦促原始设备制造商使用 [Slices API](https://www.xda-developers.com/slices-app-actions-android-p-google-assistant/) 来提供可操作的设置切换。新的蓝牙设置页面和通知尚未在 Android Q beta 3 中上线，但它们可能会在未来的测试版中出现。

* * *

## 更多设备支持快速配对

预计今年将推出更多快速配对设备。谷歌表示，他们正在努力支持额外的蓝牙配置文件以及仅限 BLE 的设备。该公司概述了他们如何与 OEM、ODM 和 3PL 提供商合作，让他们都对支持 Fast Pair 感兴趣。例如，谷歌最近[宣布](https://www.xda-developers.com/google-assistant-qualcomm-bluetooth-headset-fast-pair/)与高通合作，在新的高通智能耳机开发套件上支持 Fast Pair。

但是 Fast Pair 并不仅仅适用于更多的耳机和耳塞。它也被无线扬声器制造商所采用，因此我们将在未来几个月内看到该功能扩展到更多的产品类别。谷歌已经承诺该服务[将在今年支持 chrome book](https://www.xda-developers.com/fast-pair-android-sync-chromebook-support/)，但在会议期间，他们还表示他们正在与 Wear OS 团队合作，为智能手表提供支持。

* * *

*注:这一信息是在谷歌的、杰克·克林克和凯瑟琳娜·徐举办的“[蓝牙设备快速配对](https://events.google.com/io/schedule/events/08837fc5-b49c-4ac5-b5d5-ff2bf3869a48)”灯光讲座上公布的。会话未流式传输。*