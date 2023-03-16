# 谷歌宣布改进应用捆绑包、即时应用和应用管理工具

> 原文：<https://www.xda-developers.com/google-announces-improvements-app-bundles-instant-apps-tools/>

每年，谷歌都会举办一场名为 Playtime 的邀请制活动。谷歌邀请来自 Play Store 的应用程序和游戏的选定开发者参加此次活动，分享最新的功能和技巧，以改进他们的应用程序。在今年的活动上，谷歌宣布了对 Android 应用捆绑包、Google Play Instant 和 Google Play 控制台的更新。

## Android 应用捆绑包变化

[在 Google I/O 2018](https://www.xda-developers.com/android-app-bundle-google-play-dynamic-delivery-apk-size/) 上宣布，Android 应用捆绑包是一种打包应用的新方式。如果您选择共享您的签名密钥并上传。aab 文件到 Google Play，Play 中新的动态交付特性将决定将哪些资源打包到一个。提供给用户的 apk 文件。这有时可以显著减小应用程序的大小，提高低存储设备或低数据限制用户的保留率。

尽管谷歌声称应用程序大小平均减少了 35%，但该公司正在推出更多改变，以进一步减少应用程序捆绑包的大小。在 Android Marshmallow 和更高版本的设备上安装时，下载的应用程序包现在将平均比小 8%，比**小 16%。谷歌表示，这是通过支持“未压缩的原生库”实现的，消除了“在设备上存储多个副本的需要”。**

接下来，谷歌想提醒开发者，Android Studio 的最新稳定版本——[3.2 版](https://www.xda-developers.com/android-studio-3-2-emulator-snapshots-energy-profiler/)——允许你部署应用捆绑包。对于游戏开发者来说， [Unity 2018.3 beta](https://blogs.unity3d.com/2018/10/03/support-for-android-app-bundle-aab-in-unity-2018-3-beta/) 还可以让你构建应用捆绑包。对于像游戏这样的大型应用的开发者来说，**大型应用捆绑包**“安装的 APK 大小高达 500MB”现在可以**上传**而不需要扩展文件。但是，大型应用程序支持处于早期访问。

## Google Play 即时更改

宣布的第一个变化是[可玩游戏演示](https://www.xda-developers.com/playable-game-demo-google-play-store/)的新“立即尝试”按钮的大小限制已经从**增加到 10MB** 。此外，如果你错过了新闻，基于 URL 的意图过滤器[不再是你的即时游戏所需要的](https://android-developers.googleblog.com/2018/08/streamlining-developer-experience-for.html)。

其次，Android Studio 3.3 测试版现在允许开发者“发布单个应用捆绑包，并将其或特定模块分类为即时启用。”这意味着您不再需要维护单独的代码，发布单独的可安装的即时应用程序。

最后，可玩的游戏演示功能现在可以用于“高级游戏和预注册活动”

## Google Play 控制台变更

Play 控制台会将 Firebase 测试实验室中的预发布报告与 Android vitals 相链接，以帮助您更好地调试应用程序。如果您在预发布报告中看到 Android 生命体征也出现崩溃，您可以在 Android 生命体征仪表板中查看预发布报告的元数据(反之亦然。)

谷歌还宣布了对其应用管理工具的一些改进:

*   暂时暂停订阅:谷歌正在测试用户暂停订阅而不是取消订阅的能力，让你有机会赢回一些订户。
*   **更改现有套餐价格:**您可以更改套餐价格，而无需在 Play Billing Library v1.2 版中创建新的 SKU。您也可以使计划更改在现有续订日期生效。
*   **更好的指标:**“累积数据、30 天滚动平均指标和不同时间段的汇总”是 Play Console 中核心指标的新增内容。
*   **应用内更新:**使用这个新的 API，你可以提示用户更新应用，而不必让他们离开应用。您可以构建一个全屏 UI，指导用户更新应用程序，或者帮助他们在后台安装应用程序，同时监控更新状态。此 API 处于早期访问阶段。[](https://static1.xdaimages.com/wordpress/wp-content/uploads/2018/10/Google-Play-In-App-Update.jpg)

* * *

最后但并非最不重要的一点是，谷歌推出了[应用成功学院](https://developer.android.com/google-play/academy/)来教育开发者关于 Play 控制台、Google Play 政策和最佳实践，以提高他们应用的质量和业务表现。这是一个免费的程序，目前有英文版本，但将来会有更多的内容和语言版本。