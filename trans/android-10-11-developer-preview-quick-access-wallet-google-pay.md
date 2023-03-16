# Android 10 的隐藏快速访问钱包现在可以在 Android 11 中使用

> 原文：<https://www.xda-developers.com/android-10-11-developer-preview-quick-access-wallet-google-pay/>

谷歌刚刚发布了 Android 11 开发者预览版(T1 ),重点是提高操作系统中的 T2 安全性和可用性。除了与 Android 10 相比的[新开发者选项](https://www.xda-developers.com/android-11-developer-preview-new-development-features/)和[的变化，Android 11 开发者预览版中还出现了其他一些在之前版本中被取笑但没有发布的功能。其中一个新增功能是快速访问钱包功能，它可以让你直接从功能菜单中调出保存在 Google Pay 中的卡。](https://www.xda-developers.com/android-11-developer-preview-changes/)

快速访问钱包首次出现在第四个 Android Q beta 版本中，名为“ [Show cards & passes](https://www.xda-developers.com/android-q-google-pay-power-menu/) ”。它当时并不工作，即使谷歌在稳定发布后将其列为 Android 10 功能中的“快速钱包访问”，该功能仍然令人惊讶地缺失。XDA 的主编[米沙·拉赫曼](https://www.xda-developers.com/author/mishaalrahman/)，后来的[设法激活了这个功能](https://www.xda-developers.com/android-10-quick-wallet-access-google-pay/)，他可以添加自己的卡，或者通过简单地打开电源菜单(即长按电源按钮)访问已经保存在 Google Pay 中的卡。

*Android 10 中的快速访问钱包预览版*

在 Android 10 中，快速访问钱包功能显然仅限于谷歌 Pixel 设备，并且只能使用谷歌支付进行支付。几个月来，谷歌没有分享任何关于该功能的进一步细节。但随着 Android 11 的推出，谷歌预计将通过扩展对 Google Pay 之外的支持来改善它。任何支付应用程序现在都将能够实现[QuickAccessWalletService](https://developer.android.com/reference/android/service/quickaccesswallet/QuickAccessWalletService)API，以便用户可以直接从电源菜单访问保存在该特定应用程序中的卡、优惠券或门票。

要实现该功能，支付应用程序需要在其清单中添加所需的权限，即[Android . permission . bind _ QUICK _ ACCESS _ WALLET _ SERVICE](https://developer.android.com/reference/android/Manifest.permission.html#BIND_QUICK_ACCESS_WALLET_SERVICE)。这将允许系统绑定服务，即使在应用程序使用时间不够长的情况下，也不会终止应用程序。为了能够在 Android 11 的其他应用程序中使用快速访问钱包，用户将需要通过设置>系统>手势来启用该功能。用户还必须在设置中的点击&支付选项中选择他们的默认支付应用。

如果你有一个 Pixel 设备，并想试用新的开发者预览版，你可以点击下面的链接，刷新你的特定设备的系统包。请注意，您将需要一个未锁定的引导加载程序，并且您必须在开始该过程之前备份您的数据。

**[如何为谷歌 Pixel 等设备下载 Android 11 开发者预览版](https://www.xda-developers.com/how-to-download-android-11-developer-preview-for-google-pixel-and-other-android-devices/)**

**[如何在你的谷歌 Pixel 智能手机上安装 Android 11 开发者预览版](https://www.xda-developers.com/how-to-install-android-11-r-developer-preview-beta-1-google-pixel-2-3-4-3a-xl/)**

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**