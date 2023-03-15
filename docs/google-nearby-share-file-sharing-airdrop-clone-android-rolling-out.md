# 谷歌附近的共享，其文件共享隔空投送克隆的安卓系统，推出

> 原文：<https://www.xda-developers.com/google-nearby-share-file-sharing-airdrop-clone-android-rolling-out/>

**更新 1(****08/31/2020****@****01:20AM****ET):**Google nearly Share 正在大范围铺开。滚动到底部了解更多信息。下面保留了 2020 年 8 月 4 日发表的文章。

去年，我们了解到谷歌正在为 Android 准备一项新的文件共享服务。在早期的迭代中，这种文件共享服务最初被称为“[快速共享](https://www.xda-developers.com/fast-share-android-beam-airdrop-android/)”，但谷歌最终在开发过程中将其更名为“[附近共享](https://www.xda-developers.com/fast-share-google-upcoming-airdrop-service-renamed-nearby-sharing/)”。一月份，我们在[提前看到了这个功能](https://www.xda-developers.com/nearby-sharing-airdrop-for-android-file-sharing/)，六月底，谷歌开始在最新的 Google Play 服务测试版上与一些用户一起测试这个服务。今天，谷歌宣布，他们终于向数百万运行 Android 6.0 及以上版本的 Android 智能手机推出了 Nearby Share。

对于那些没有意识到的人来说，Android 从来没有一种简单、快速、*和*统一的方式来在设备之间共享文件。[在 Android 10](https://www.xda-developers.com/google-deprecate-android-beam-api-nfc-share-files/) 之前，大多数 Android 设备都可以访问 Android Beam，这是一种文件共享服务，要求用户一起点击手机，通过 NFC 发起握手，然后通过蓝牙或 Wi-Fi Direct 传输文件。然而，Android Beam 已被弃用，而且比隔空投送慢，后者是 iOS 上的文件共享服务，已存在多年，被数百万 iPhone 和 iPad 用户使用。隔空投送可以让你快速与附近的任何 iPhone 或 iPad 用户共享文件。T4 有安卓上的文件共享服务，可以说和隔空投送一样简单快捷，但它们都要求用户要么下载第三方应用，要么拥有特定智能手机制造商的设备。由于谷歌对 Google Play 服务的控制，谷歌在推出简单、快速和统一的文件共享服务方面拥有独特的优势。在中国以外销售的绝大多数 Android 设备上都安装了 Google Play 服务，无论制造商是谁。这就是 Nearby Share 一个简单、快速、统一的 Android 文件共享服务。

通过 Nearby Share，Android 用户只需轻点一个按钮，就可以快速地将文件分享给附近的用户。点击应用程序中的“共享”按钮后，用户可以通过选择“附近的共享”选项来共享文件。附近的用户将会收到有人想要与他们分享内容的通知。用户将始终可以选择“接受”或“拒绝”文件，因此在没有明确确认的情况下，文件不会被传输。点击“接受”后，将使用最佳可用通信协议传输文件:蓝牙、蓝牙低能耗、WebRTC 或点对点 WiFi。因此，即使发送方和接收方设备都完全离线，也可以共享文件。

谷歌设计这一功能时考虑到了隐私。例如，您可以匿名发送和接收文件。您还可以选择当您打开“附近的共享”时，哪些联系人(全部、部分或无)能够立即看到您。

或许 Nearby Share 最棒的地方在于，谷歌正在让它跨平台。虽然我们不知道 iOS 的兼容性，但谷歌证实他们正在努力将该功能扩展到其他平台。该公司证实，该功能将在未来几个月内用于 Chromebooks。事实上，如果你启用一些功能标志，Chrome OS 上已经有了[。更多的通用操作系统支持，如 Windows T3 等 T2，将通过谷歌 Chrome 提供。](https://www.xda-developers.com/chrome-os-supports-google-nearby-share-file-sharing-feature/)

从今天开始，选择运行 Android 6.0 或更高版本的谷歌 Pixel 和三星 Galaxy 智能手机将开始获得附近的份额。由于这一功能已经融入到 Google Play 服务中，它最终将适用于更多的 Android 智能手机。查看[该支持页面](https://www.xda-developers.com/androids-nearby-share-now-works-windows-google-chrome/)了解该功能如何工作的更多信息。

* * *

## 更新:谷歌附近的共享现在广泛推出

谷歌似乎正在更广泛地推出附近的共享服务。我们现在已经在几款设备上发现了这一功能，如华硕 ZenFone 7 Pro、一加诺德、努比亚 Red Magic 5S 和 LG Velvet。所有这些设备都运行 Google Play 服务 20.30.19 稳定版。其他拥有一加、小米、Honor、Realme 和诺基亚手机的用户也提到他们已经收到了该功能。

要访问附近的共享，请前往“设置”>“Google”>“设备连接”>“附近的共享”,或“设置”>“已连接的设备”>“连接偏好设置”>“附近的共享”(此菜单并非在所有操作系统版本和/或 OEM 皮肤上都可用)。如果此设置对您可见，您也可以编辑快速设置来添加附近的共享磁贴。

正如截图所示，号码验证似乎是一个新添加的功能。