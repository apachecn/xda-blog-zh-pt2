# 开发者可以限制 Android Go 设备下载他们的应用

> 原文：<https://www.xda-developers.com/developers-exclude-android-go-oreo-downloading-apps/>

# 开发者可以限制 Android Go 设备下载他们的应用

添加了新的 Google Play 控制台排除规则，以限制 Android Oreo (Go Edition)设备(也称为 Android Go 设备)上的用户下载您的应用程序。

Android Oreo (Go Edition)，也简称为 Android Go，是谷歌针对新兴市场日益增长的重要性的解决方案，在新兴市场，廉价设备占据主导地位。Android Go 是针对低端硬件优化的 Android 8.1 Oreo[；它基本上只是一套](https://www.xda-developers.com/android-go-optimizes-android-o-to-run-on-low-end-devices/)[构建配置和特殊的 Go 版应用](https://www.xda-developers.com/android-go-old-android-8-1-oreo/)，设计用于在内存只有 512MB 的硬件上运行。([现已倒闭](https://www.xda-developers.com/zte-no-longer-qualcomm-smartphones-threatening-axon-9/) ) [中兴 Tempo Go](https://www.xda-developers.com/zte-announces-blade-v9-blade-v9-vita-tempo-go/) 、[阿尔卡特 1X](https://www.xda-developers.com/alcatel-alcatel-5-3-1-series-smartphones-1t-10-7-tablets-1x-android-go-phone/) 、[诺基亚 1](https://forum.xda-developers.com/nokia-1) 、[诺基亚 2.1](https://www.xda-developers.com/nokia-5-1-nokia-3-1-nokia-2-1-announced/) 只是运行 Android Oreo (Go 版)的部分廉价手机。对于寻求新用户的开发者来说，优化他们的应用程序以在低端硬件上运行是非常重要的。但如果你没有兴趣或无法合理地优化你的应用程序以在 Go edition 设备上运行，那么你会很高兴地知道，Google Play 控制台现在允许你添加排除规则，以防止你的应用程序被下载到这些设备上。

不过，用户仍然可以侧装你的 APK。如果你只是希望防止预算硬件上的用户对你的应用程序体验不佳(从而对你的应用程序评价很差)，那么这是一个快速的方法来防止这种情况发生在至少一小部分预算设备上。不过，无论如何，最好尽可能优化你的应用程序，因为大多数 Android 用户都是预算有限的硬件。

如果你想为 Android Oreo (Go Edition)设备设置设备排除规则，那么这里有关于如何做的说明，从谷歌的支持页面复制到下面的 f [。这些说明还告诉你如何基于通过安全网认证 API(就像](https://support.google.com/googleplay/android-developer/answer/7353455#safetynet)[网飞](https://www.xda-developers.com/netflixs-safetynet-exclusion-is-actually-a-new-feature-in-the-google-play-console/))来排除用户，但我们真的希望你不必诉诸于此。

#### 为 SafetyNet 或 Android (Go 版)设置设备排除规则

1.  登录您的[游戏控制台](https://play.google.com/apps/publish/)。
2.  选择一个应用。
3.  在左侧菜单中，选择**设备目录**。
4.  选择“排除的设备”选项卡。
5.  在“排除规则”旁边，选择**管理排除规则**。
6.  在“安全网排除”或“Android Go 排除”旁边，选择一个选项:
    *   **安全网排除项目**
        *   *不排除基于安全网认证 API* 的设备:默认选择。
        *   *仅排除未通过基本完整性* *y* 测试的设备:这有助于您确定特定设备是否已被篡改或修改。
        *   *排除未通过基本完整性测试的设备，以及未经谷歌认证的设备*:这有助于您确定特定设备是否被篡改、修改或未经谷歌认证。
    *   **Android Go 排除项**
        *   *不排除 Android Go 设备*:默认选中。
        *   *排除 Android Go 设备*:阻止运行 Android Oreo (Go 版)的设备在 Google Play 上安装你的应用。