# 谷歌正在为助手的新驾驶模式提供 NFC 标签支持

> 原文：<https://www.xda-developers.com/google-assistant-driving-mode-nfc-tag-support/>

回到 5 月份的谷歌 I/O，谷歌[宣布](https://www.xda-developers.com/google-assistant-driving-mode-waze/)助手将获得专用驾驶模式。新模式带有一个仪表板，旨在最大限度地减少触摸互动。仪表板将导航、拨号器和媒体控制等重要的快捷方式放在前面和中间，同时还显示基于日历等内容的定制建议。驾驶模式本应在“今年夏天在装有谷歌助手的安卓手机上”推出，但我们已经过了夏天，还没有看到该功能的推出。虽然我们仍然不知道该功能何时上线，但我们已经发现了一些关于它如何工作的新信息。具体来说，我们发现有证据表明，谷歌正在通过扫描 NFC 标签来支持启动助手的驾驶模式。

近场通信(Near-field communication，简称 NFC)是一种短程通信协议，通常用于非接触式支付，但也可用于发送预编程数据。NFC 标签可以被编程为[向 NFC 兼容智能手机](https://www.xda-developers.com/tasker-beta-navigation-bar-nfc-tags/)发送特定数据，然后被应用程序拦截，以更改设置、启动网站、启动应用程序等。如果我们对谷歌应用程序中所看到的内容的理解是正确的，那么你就可以通过扫描预编程的 NFC 标签来启动新的助理驾驶模式。

在提供谷歌助手服务的谷歌应用程序中，我在清单文件中发现了一些有趣的东西。如果通过动作“[Android . NFC . action . ndef _ DISCOVERED](https://developer.android.com/reference/android/nfc/NfcAdapter.html#ACTION_NDEF_DISCOVERED)”接收到意图，则可以启动 Google Assistant 驾驶模式仪表板的活动因此，当 NFC 标签向手机发送包含此意图的数据时，可以直接启动谷歌助手的驾驶模式。谷歌表示，用户将能够通过说“嘿谷歌，让我们开车”来启动新的驾驶模式，但在我看来，扫描 NFC 标签比对着手机大喊更快、更可靠、更方便。

还有其他通过 NFC 启动新驾驶模式的参考，例如通过用户扫描相关 NFC 标签时发送的意图，但他们也在设置>连接偏好设置>驾驶模式中选择了“打开驾驶模式前询问”选项。最后，我检查了最新版本的 Android Auto 应用程序的清单，没有发现任何通过 NFC 启动应用程序的支持，所以这一功能不是简单地在从 Android Auto 到 Google Assistant 的驾驶模式的过渡中进行的。

 <picture>![](img/c10d460236abb6e75677f14c95dee23f.png)</picture> 

Google App's AndroidManifest

 <picture>![](img/eec1ae00e34ca939b802c1713468bc8a.png)</picture> 

MorrisShowDashboardActivity in the Google App

谷歌[推荐](https://developer.android.com/guide/topics/connectivity/nfc/nfc#filter-intents)使用 NDEF (NFC 数据交换格式)来格式化 NFC 标签，“当你能够控制标签和写入数据的类型时”因此，谷歌可能打算发布预编程为启动助手驾驶模式的 NFC 标签，他们正在与配件制造商合作开发此类标签，他们正在与汽车制造商合作添加内置 NFC 标签，或者他们可能正在开发这三种标签的组合。我们有望很快找到答案。[谷歌今年宣布的许多新软件功能](https://www.xda-developers.com/tag/google-pixel4/)尚未推出，但这可能是因为谷歌正在等待即将于 10 月 15 日举行的[谷歌制造活动的盛大揭幕。](https://www.xda-developers.com/google-pixel-4-october-15-event/)

我们还无法在自己的设备上启动和运行新的驾驶模式，但我们已经相当接近了。看起来与 Pixel 3 一起启动的[现有驾驶模式](https://www.xda-developers.com/android-pie-driving-mode-android-auto-do-not-disturb/)将被更新，让你选择是否要启动谷歌助手或启用请勿打扰模式(一旦[谷歌逐步淘汰手机的安卓自动界面](https://www.xda-developers.com/android-auto-app-no-longer-supported-google-assistant-new-driving-mode/)，当前的“打开安卓自动”很可能会消失)。有趣的是，我们还在 Android Auto 的设置中发现了一个新的“在手机上使用 Android Auto”选项，这可能与新的“手机屏幕 Android Auto”应用程序有关，据报道，谷歌[正在开发](https://www.xda-developers.com/android-auto-app-no-longer-supported-google-assistant-new-driving-mode/)。