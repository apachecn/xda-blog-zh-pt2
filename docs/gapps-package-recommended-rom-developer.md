# 始终使用 ROM 开发商推荐的 GApps 包

> 原文：<https://www.xda-developers.com/gapps-package-recommended-rom-developer/>

GApps(Google Apps 的缩写)包是定制 rom 的附件，是在您的设备上获得 Google 应用程序(如 Google Play 服务和 Play 商店)所必需的。开发者不会将谷歌应用捆绑到他们的定制 rom 中，因为这些应用是专有的。相反，ROM 开发人员通常会推荐第三方软件包，这些软件包可以在他们的版本上单独刷新。

例如，LineageOS 15.1 [的第一个版本最近发布了](https://www.xda-developers.com/lineageos-15-android-oreo-officially-announced/)。当时，Open GApps 与 Android 8.1 Oreo 不兼容(具体来说，SetupWizard APK 仍然适用于 Android 8.0)，因此 LineageOS 推荐由 XDA 公认的开发者 [javelinanddart](https://forum.xda-developers.com/member.php?u=5795145) 独立维护的 MindTheGapps 包作为附加包。

然后，第一批基于 Android 8.1 奥利奥的开放 GApps 包[发布](https://www.xda-developers.com/open-gapps-now-supports-android-8-1-oreo-arm-arm64/)。Open GApps 是目前下载 Google Apps 最受欢迎的选择，因为它的频繁更新和灵活性。用户可能期望 LineageOS 将他们对 Google apps 包的推荐从 MindTheGapps 改为 Open GApps，然而事实并非如此。LineageOS 仍然继续官方推荐 MindTheGapps，只有[不情愿地在他们的网站上列出](https://review.lineageos.org/c/208595/#message-8cb850e4_2181a51b)Open gaps 作为备选。

那么为什么 LineageOS 仍然推荐 MindTheGapps 呢？这是因为使用一个未经开发者测试的包可能会有问题。例如，LineageOS 开发人员注意到，[删除股票拨号器应用程序](https://www.reddit.com/r/LineageOS/comments/8358p0/mindthegapps_vs_opengapps/dvfybm0/)(当闪烁“超级”或“股票”打开 GApps 包时发生)可能会**导致紧急呼叫无法工作**，因为框架[依赖于非常具体的意图](https://github.com/LineageOS/android_packages_services_Telephony/blob/lineage-15.1/src/com/android/phone/OutgoingCallBroadcaster.java#L464-L487)来发送。例如，使用不同的拨号器应用程序(如 Google Dialer)可能会中断紧急呼叫功能。

另一个例子是，根据 LineageOS 的一名团队成员的说法，当前开放的 GApps 包[似乎在 LineageOS 15.1](https://review.lineageos.org/c/208595/#message-b91b55ef_f88bce26) 的几个设备上打破了 Google Camera。谷歌相机正式在 Nexus 和 Pixel 设备上工作，但[它已经被非正式地移植到许多其他设备上](https://www.xda-developers.com/google-camera-mod-exynos-portrait-mode-galaxy-s8-s7-note-8/)。

最后，这里的另一个例子是，Open GApps 还不支持 LineageOS 中即将推出的 backuptool v2。 [backuptool v2 是 linegeos](https://review.lineageos.org/c/206139/)中现有工具的新版本，用于备份和恢复/系统附加文件。它现在对带有 A/B 分区的设备有了更好的支持。

总之，**我们并不想在这里大做文章**。获得所有最新的谷歌应用和服务是一个极好的选择，这也是它在社区中如此受欢迎的原因。上面列出的问题并不是包本身的问题，而是 ROM 如何期望某些应用程序存在，但是由于用户的意外修改，它们并不存在。定制的 rom 是由他们的开发者用他们喜欢的包来构建和测试的，如果用户安装不同的包，开发者将不能保证稳定的功能。因此，用户应该始终在任何自定义 ROM 版本之上闪存官方推荐的 GApps 包。