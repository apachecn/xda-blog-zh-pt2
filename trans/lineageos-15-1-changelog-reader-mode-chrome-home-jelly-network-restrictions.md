# LineageOS 15.1 Changelog 18:阅读器模式，Jelly 中的“Chrome Home”，每个应用程序的网络限制等等

> 原文：<https://www.xda-developers.com/lineageos-15-1-changelog-reader-mode-chrome-home-jelly-network-restrictions/>

在所有支持的设备上， [LineageOS 15.1](https://www.xda-developers.com/tag/lineageos-15/) 每周发布一次。除非你虔诚地追随他们的[精神](https://review.lineageos.org)，否则很难跟上流行的基于 AOSP 的定制 ROM 中的新内容，所以团队已经整理了一个变更日志来让你了解 ROM 中的新内容。今天，该团队发布了他们的[第 18 次变更日志](https://lineageos.org/Changelog-18/)，自从他们 4 月 1 日的[最后一次变更日志发布](https://lineageos.org/Changelog-17/)以来，还有很多功能要覆盖。以下是最新消息:

## LineageOS 自 4 月 1 日以来的变更日志

*   现在可以限制每个应用程序的 WiFi 和/或移动数据使用
*   live display 已被重写为 binderized hal
*   “拨号器”现在可以启用“通话中请勿打扰”功能，以避免您在通话时听到通知声音
*   阅读器模式现在可以调整你的显示，使文件和长文本更容易阅读
*   Trebuchet 现在在抽屉里有更智能的应用程序建议。这些会在白天和你插上耳机的时候发生变化
*   Trebuchet 还可以将传统应用程序图标放入自适应图标框中
*   Jelly 有一个新的“到达模式”,可以将顶部的 URL /搜索栏移到底部，以便更容易到达
*   更新程序已经更新为更好的可靠性，它现在通过[样式 API](https://wiki.lineageos.org/sdk/api/styles.html) 支持黑暗模式
*   [5 月安全补丁](https://www.xda-developers.com/android-security-patches-for-may-are-now-available-with-ota-and-factory-images/)已在 15.1 中合并
*   [4 月](https://www.xda-developers.com/nexus-pixel-security-april-2018-ota-factory-images/)和 5 月的安全补丁已在 14.1 中合并
*   Chromium webview 已更新至版本 66 . 0 . 3359 . 139(14.1 和 15.1)
*   键盘现在可以识别匿名文本字段，并且在其中一个字段中输入时不会学习建议
*   FlipFlap 现在忽略低优先级通知(14.1 和 15.1)
*   重新添加了传统预建摄像机 HAL 1 支持
*   SSH 支持已被重新添加

自从定制 ROM 在二月份首次发布以来，它已经为用户提供了大量的功能。这些变化为用户增加了功能丰富的体验。

## 支持的 LineageOS 15.1 设备的当前列表

我们一直在[跟踪](https://www.xda-developers.com/tag/lineageos/)哪些设备获得了 LineageOS 15.1 的官方版本，所以这里是我们当前所有受支持设备的列表:

自从最初发布以来，这个列表已经变得相当广泛了。这份名单上目前缺少的是带有 [A/B 分区](https://www.xda-developers.com/list-android-devices-seamless-updates/)的设备，如谷歌 Pixel 智能手机和小米 Mi A1。LineageOS 团队正在修复他们的 addon.d 脚本(备份[gapp](https://www.xda-developers.com/gapps-package-recommended-rom-developer/)和 [SU addon](https://www.xda-developers.com/addonsu-packages-lineageos-15-1/) 的脚本)，以便它可以与 A/B 设备一起工作。一旦完成，我们应该开始看到 A/B 设备被添加到名册中。

## 杂项变更

### CVE 跟踪器

LineageOS 公共漏洞和暴露(CVE)跟踪器是一个[页面](https://cve.lineageos.org/devices)，用户可以在这里看到他们的设备针对哪些安全漏洞合并了补丁。然而，该页面通常已经过时，因为它需要设备维护人员手动更新设备补丁的状态。在团队的自动修补程序准备就绪之前，他们已经将页面设为私有。

### 行动守则

为了改善他们的公众形象，提升团队的专业性，项目总监们采用了适用于团队所有成员的[行为准则](https://github.com/LineageOS/charter/blob/master/code-of-conduct.md)。

### 隐私政策更新

欧盟的 GDPR 今天生效，因此该小组更新了他们的隐私政策，以包括有关他们的 Gerrit 如何收集一些个人信息的信息。

### LineageOS 14.1 名册变更

基于 Android 7.1 牛轧糖的 LineageOS 14.1 仍然支持大量设备。因为有了[宪章](https://www.xda-developers.com/lineageos-device-support-requirements-charter/)，那时对官方版本的要求没有现在这么严格，所以很多设备暂时还会在 14.1 上。然而，由于“设备树的许可问题”，三星 Galaxy S7 和三星 Galaxy S7 Edge 已从 14.1 版本名单中删除