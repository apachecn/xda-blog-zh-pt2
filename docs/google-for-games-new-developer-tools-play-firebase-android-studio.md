# Google for Games 2020:新的 Google Play、Firebase 和 Android 工具

> 原文：<https://www.xda-developers.com/google-for-games-new-developer-tools-play-firebase-android-studio/>

# 新的 Google Play、Firebase 和 Android Studio 工具在 Google for Games 上面向游戏开发者发布

在 Google for Games 2020 期间，谷歌宣布了 Google Play、Firebase、Android Studio 和更多面向 Android 游戏开发者的新工具。

虽然为了限制新冠肺炎的传播，游戏开发者大会(GDC)被取消了，但谷歌正在举办完全在线的“游戏谷歌”开发者峰会。今天，该公司宣布了许多新工具，包括 Google Play、Firebase、Android Studio 以及更多面向移动游戏开发者的工具。这是最新消息。

## Google Play 的新功能

*   **Google Play 资产交付:**通过 Google Play 中的资产交付，游戏资产可以动态交付给用户，因此他们可以更快地开始游戏。这项功能建立在谷歌的应用捆绑基础设施之上。在这里了解更多。
*   **Android vitals 原生崩溃符号化:**您现在可以将原生调试符号上传到 Google Play 控制台，以调试原生崩溃，并获得从 Android vitals 获取数据的额外好处。这个功能[现在正在公测](https://developer.android.com/games/preview)。
*   **Android vitals Performance insights with Android Performance Tuner:**Play 控制台中 Android Vitals 的新性能见解使您可以更轻松地在许多不同设备上优化游戏的帧速率和保真度。加入开发者预览版并在[安卓游戏 SDK](https://www.xda-developers.com/google-android-game-sdk/) 中集成新的安卓性能调音器库，即可解锁[这一功能。](https://developer.android.com/games/preview)
*   **面向 Unity 开发者的 Play Billing Library 2:**如果您在 Unity 中使用 Android SDK，现在您可以访问 Google Play Billing Library v2 的所有功能。这包括允许用户用现金支付和在游戏外显示应用内购买的功能。在这里了解更多。
*   **预注册游戏第一天自动安装:**谷歌将很快[启用预注册游戏第一天自动安装](https://www.xda-developers.com/google-play-store-automatically-install-preregistered-apps-games/)。

*   **Android Studio 剖析器:**系统跟踪剖析器已经被彻底改造成“允许你检查和可视化你的代码是如何被执行的细节。”Google 还增加了本地内存分析功能，以帮助您找到内存泄漏。这个功能在 Android Studio 4.1 中可用，[现在在金丝雀](https://developer.android.com/studio/preview)中。在直播会话中了解更多[。](https://www.youtube.com/watch?v=JXQBdMNDL7k)
*   用于 Visual Studio 的 Android 游戏开发扩展: Google 推出了一款新工具，可以与您的 Visual Studio 工作流集成。该工具将使从您的项目中生成 APK 文件、将您的游戏部署到 Android 设备或仿真器、或者从 Visual Studio 中调试您的 Android 游戏变得更加容易。这个特性现在是开发者预览版中的[。要了解更多信息，](https://developer.android.com/games/preview)[请观看直播会议](https://www.youtube.com/watch?v=JXQBdMNDL7k)。
*   **Android GPU Inspector:** 新的 Android GPU Inspector 工具将使您能够查看游戏的渲染阶段和 GPU 计数器。谷歌希望这将允许图形工程师优化他们游戏的帧速率和电力使用。[谷歌和高通在 Android GPU Inspector 上合作](https://www.qualcomm.com/news/onq/2020/03/23/gaming-snapdragon-now-faster-google-and-updateable-gpu-drivers)，它支持大多数 Android 设备中的 GPU，包括骁龙 SOC 的 Adreno GPUs。由于这种合作关系，游戏开发者将能够直接向高通提供反馈，以便他们可以改进 Adreno GPU 软件驱动程序。高通将为精选开发者提供一个测试版驱动程序(Adreno 图形开发驱动程序),以便他们可以快速测试他们的优化并提出增强建议。然后，最终的驱动程序将通过谷歌 Play 商店在选定的设备上提供。这项功能[已经在开发者预览版](https://developer.android.com/games/preview)中，但已经由几家游戏工作室在 Pixel 4、Pixel 4 XL、三星 Galaxy Note 10 和三星 Galaxy S10 上进行测试。[观看直播](https://www.youtube.com/watch?v=7n9vTYs17_Q)了解详情。
*   【Unity 的游戏包注册:谷歌正在引入一个包注册，将 Google APIs，如 Google Play Billing、Android App Bundles、Google Play Asset Delivery、Google Play Instant 和 Firebase for Games 都放在一个地方。文档可在[这里](https://developer.android.com/games/develop/build-in-unity)获得，但将在[游戏谷歌](https://www.youtube.com/watch?v=JXQBdMNDL7k)期间详细解释。
*   Crytek 宣布支持 Android:Crytek 的 CRYENGINE 将在今年夏天晚些时候增加一个完整的 Android 管道。你可以从 [Crytek 的网站](https://www.cryengine.com/beta)了解更多。

## Firebase 的所有新内容都在谷歌游戏上发布了

*   **Cloud Firestore for C++和 Unity:**Google 的 Cloud Firestore SDK 的一个版本，这是一个基于云的 NoSQL 数据库，具有多区域可靠性、原子事务和实时监听器等功能，现已面向 C++和 Unity 开发人员推出。由于这是一个开放的 alpha 版本，谷歌警告说，Cloud Firestore SDK for Unity 缺少一些高级查询功能，API 很有可能在未来几个月内发生变化。谷歌称 [Firebase 实时数据库](https://firebase.google.com/docs/database)不会消失，因为云 Firestore 仅仅是另一种更适合某些情况的选择。
*   **Firebase Unity SDK 现在与 Unity Package Manager 兼容:**在支持的 Unity SDK 版本中，Firebase 将保持最新，插件将不再需要与您的游戏资产混合。这个过程是通过一个名为 Unity 外部依赖管理器(EDM4U)的开源工具自动完成的。
*   **Google Analytics 中的新分析:** Google 在 Google Analytics 中增加了新的报告，这对游戏开发者可能会很有用。一些新的仪表板侧重于用户获取、用户保留、用户参与和用户货币化，而一些新的报告包括首次购买者、收入心跳、用户参与和每日活跃用户/每月活跃用户趋势(DAU/MAU)。要开始使用这些新报告，你必须[将你的 Firebase 项目链接到谷歌分析账户](https://firebase.googleblog.com/2019/07/firebase-google-analytics-upgrade.html)，然后打开谷歌分析控制台。欲了解更多详情，[请访问分析帮助中心](https://support.google.com/analytics/answer/9713967)。
*   **新的登陆页面:**为了配合谷歌游戏，谷歌用全新的设计更新了游戏产品页面 [Firebase。](https://firebase.google.com/games)

* * *

密切关注 [Android 开发者 YouTube 频道、](https://www.youtube.com/channel/UCVHFbqXqoYvEWM1Ddxl0QDg) [Android 开发者博客](https://android-developers.googleblog.com/)、 [Firebase 博客](https://firebase.googleblog.com/)和[谷歌开发者博客](https://developers.googleblog.com/2020/03/join-us-for-digital-google-for-games.html)以获取谷歌游戏的最新消息。