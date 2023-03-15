# Android TV 可以获得 Google Play 即时应用、PIN 码购买等功能

> 原文：<https://www.xda-developers.com/android-tv-gets-google-play-instant-apps-pin-code-purchases-board-auto-low-latency-mode-gboard-more/>

Android TV 是谷歌的智能电视平台，拥有超过 7000 个 Android TV 上的 Google Play 应用。尽管面临来自其他本土替代产品的激烈竞争，该平台仍取得了稳步成功。Android TV 现在的月活跃用户同比增长 80%，全球前 10 大智能电视原始设备制造商中有 7 家采用了 Android TV，电视运营商超过 160 家。谷歌最近宣布了 Android TV 的 [Android 11 开发者预览版，今天，作为其 11 周 Android 系列的一部分，谷歌强调了 Android TV 的最新更新将给智能电视带来的变化和改进。更好的是，*这些功能中的大多数*也将适用于旧版本的 Android TV (9 和 10)。](https://www.xda-developers.com/android-tv-cast-connect-library-enable-remote-control-support-casted-videos/)

## 电视上的 Google Play 即时

Android 即时应用首次在 Google I/0 2016 上展示。有了即时应用程序，用户可以试用应用程序，而无需实际安装它们。[即时应用](https://www.xda-developers.com/google-play-store-android-instant-apps/)的工作原理是将一个本地应用分解成小部分，这样可以更快地加载和下载，然后快速执行。它显示了一个应用程序的 UI 屏幕，一旦关闭，它就会被删除，不需要卸载，因为它一开始就没有安装。

现在，谷歌通过 Google Play Instant 将即时应用体验带到了电视上。Android 电视应用程序的开发者现在可以[允许用户通过 Google Play Instant on TV 在 Google Play 上即时试用他们的应用程序](https://developer.android.com/training/tv/start/start#instant-experience)。用户体验后可以选择安装 app。这应该会派上用场，因为与智能手机相比，智能电视的存储容量通常有限。

## 支持 Play Store 的 Android 电视仿真器

谷歌还让开发者更容易测试他们的应用程序，因为官方的 Android 电视模拟器现在支持 Google Play。开发者现在将能够通过模拟器更快地测试订阅，而不是需要一直在真实设备上测试，这在电视上相当麻烦。

## PIN 码购买

Android TV 上的 Google Play 现在将允许用户输入 PIN 码而不是密码，从而使用户更容易进行购买。

## 宽带电视

用于 Android TV 的 Gboard 现在有了新的布局和功能，可以更好地利用语音到文本和预测打字。这应该会使输入数据变得更容易，尤其是通过不是为大量打字而设计的遥控器。

## 自动低延迟模式

自动低延迟模式(ALLM)于 2020 年 6 月首次被发现，作为即将推出的谷歌“Sabrina”安卓电视加密狗的一项功能。自动低延迟模式是 [HDMI 2.1 规范](https://www.hdmi.org/spec21Sub/AutoLowLatencyMode)的一项功能，允许设备向连接的电视发送信号，使其禁用任何可能增加视频显示延迟的后处理功能。许多电视将这一功能作为“游戏模式”进行营销，因为它对减少游戏时的延迟最有用。

正如[谷歌提到的](https://developer.android.com/training/tv/games#auto-low-latency-mode)，在 Android 11 和更高版本中，一个窗口可以通过请求最少的后处理来请求使用自动低延迟模式或游戏模式，如果可用的话。这对于游戏和视频会议应用程序尤其有用，在这些应用程序中，低延迟比最好的图形更重要。谷歌也向我们澄清，这是 Android TV 上唯一专属于 Android 11 的功能，它还需要进一步由设备制造商单独采用。

应用程序开发人员可以通过在他们的 Android 清单中包含 ALLM 选项来准备他们的应用程序，或者通过操作系统版本来分支他们的代码，然后操作系统将自动使用 ALLM(如果它可用)或正常运行(如果它不可用)。

## 精简库改进

最新的 leanback 库专注于简化应用导航和兼容性，改进了诸如更简单的[顶部标签导航](http://developer.android.com/training/tv/start/libraries#leanback-tabs-library)、通过媒体标题的[分页](http://developer.android.com/training/tv/start/libraries#leanback-paging-library)以及跨移动和电视的[共享代码库](http://developer.android.com/training/tv/start/layouts#appcompat-themes)等功能。

* * *

如前所述，只有自动低延迟模式是 Android 11 独有的功能。基于 Android 9 的 Android TV 和基于 Android 10 的 Android TV 也将提供其他功能。