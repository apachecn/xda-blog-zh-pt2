# BetterBatteryStats 2.3 增加了对 Android Oreo 和非 root 设备的支持

> 原文：<https://www.xda-developers.com/betterbatterystats-2-3-android-oreo-support-unrooted/>

# BetterBatteryStats 2.3 增加了对 Android Oreo 和非 root 设备的全面支持

BetterBatteryStats 的 2.3 版本于本周发布。此次更新带来了对 Android Oreo 的全面支持，UI 改进，对底层主题的更好支持，以及最重要的功能，对非根设备的支持。

某些 Android 设备的电池寿命还有很多不足之处。频繁的唤醒锁和优化不佳的应用程序会对电池造成严重破坏。谷歌已经通过像 Doze Mode 这样的功能解决了这些问题，但仍有许多工作要做。这就是像 [BetterBatteryStats](https://redirect.viglink.com/?format=go&jsonp=vglnk_152112918422211&key=f0a7f91912ae2b52e0700f73990eb321&libId=jesp1gnu01000n4o000DAll1ay572&loc=https%3A%2F%2Fwww.xda-developers.com%2Fsearch%2Fbetterbattery&v=1&out=http%3A%2F%2Fforum.xda-developers.com%2Fshowpost.php%3Fp%3D68103329%26postcount%3D30843&ref=https%3A%2F%2Fwww.xda-developers.com%2F&title=Search%20for%20%22betterbattery%22%20-%20xda-developers&txt=BetterBatteryStats%20Updated%20to%20v2.2.0.0%20RC1) 这样的应用程序派上用场的地方。你可以使用该应用程序来跟踪这些唤醒锁，并关注一切。

BetterBatteryStats 的 2.3 版本于本周发布。此次更新带来了对 Android Oreo 的全面支持，UI 改进，对[底层](https://www.xda-developers.com/substratum-petition-google-custom-overlay-android-p/)主题的更好支持，以及最重要的功能，对非根设备的支持。该应用的高级功能需要 root 访问权限，但现在用户可以通过连接你的手机并在你的电脑上运行 ADB 命令来使用一些工具。下面列出了三个命令。

ADB-d shell pm grant com . ask sven . betterbatterystats Android . permission . battery _ STATS

ADB-d shell pm grant com . ask sven . betterbatterystats Android . permission . dump

ADB-d shell pm grant com . ask sven . betterbatterystats Android . permission . package _ USAGE _ STATS(适用于 Android 5.0 以上版本)

虽然植根于一个设备将总是给你最大的控制，但当开发者为那些不能或不想经历这个过程的人提供选择时，这是很好的。如果你对这款应用有任何疑问，请务必[查看开发者活跃的 XDA 论坛](https://forum.xda-developers.com/apps/betterbatterystats)。

### 完整变更日志:

*   完整的 android O 支持
*   现在完全支持非根设备(使用 ADB 添加了 perms)
*   UI 改进和 I18N
*   更好地支持底层主题化
*   基于崩溃报告的修复
*   添加了应用分析