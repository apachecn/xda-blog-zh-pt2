# 基于 Android Pie 的 LineageOS 16 正式发布，面向众多设备

> 原文：<https://www.xda-developers.com/lineageos-16-android-pie/>

定制 ROM 生态系统是相当大和多样化的，但如果有一个定制 ROM，我们可以认为是“最大的”，那么它将是 LineageOS。到 2018 年底，[将近 180 万次活跃安装](https://www.xda-developers.com/1-8-million-android-devices-lineageos/)，这个项目的安装基数无疑是值得注意的，但据说成功主要取决于他们的遗产。LineageOS 是 CyanogenMod 项目的继任者，该项目在 Cyanogen Inc .转移重点后于 2016 年底在[结束。](https://www.xda-developers.com/the-death-of-cyangenmod-and-whats-in-store-for-the-future/)

该项目首次向公众推出的是基于 Android 7.1 牛轧糖的 [LineageOS 14.1](https://www.xda-developers.com/official-lineageos-builds-start-rolling-out-for-nexus-6p-nexus-5x-nexbit-robin-and-more/) ，它本身只不过是现有 CyanogenMod 14.1 源代码的一个分支。然后，它开始发展，并与基于 Android 8.1 Oreo 的 [LineageOS 15.1](https://www.xda-developers.com/lineageos-15-android-oreo-officially-announced/) 走上了一条略有不同的道路，保持了他们以社区为中心的项目高于一切的前提，同时添加了许多有用的、广受欢迎的功能，如全系统黑暗模式以及像[信任界面](https://www.xda-developers.com/lineageos-trust-centralized-interface-security-privacy/)这样以隐私为重点的改进。今天，LineageOS 16.0 继续着这种发展，这是令人难以置信的流行定制 ROM 的最新版本，正如[团队在博客文章](https://lineageos.org/Changelog-22/)中宣布的那样。

通常，随着版本号的变化，会有一个大的平台更新。LineageOS 已经基于最新的 [Android Pie 源代码](https://www.xda-developers.com/android-pie-source-code-aosp/)重新制作。随之而来的是 Android Pie 的所有新功能和改进，包括重新设计的材质主题、新的导航手势等等。

随着基于 Android Pie 的官方版本的发布，LineageOS 14.1 将正式停止，这意味着从现在开始将不再发布新的官方 14.1 版本。大约两个月前，随着构建[从每周一次降低到每月一次](https://www.xda-developers.com/lineageos-15-1-nightly-builds-monthly-14-1-builds/),这终于到来了。就像 13.0 (Android 6.0 棉花糖)和 11.0 (Android 4.4 KitKat)分支一样，14.1 分支将继续开放，供安全补丁等贡献，开发者仍将能够构建新的非官方 14.1 版本。此外，LineageOS 15.1 版本现在将按周而不是按夜构建。

## 支持 LineageOS 16 的设备的初始列表

正如所有初始版本的情况一样，基于 Android Pie 的 LineageOS 16.0 的初始设备名册将从小规模开始，随着维护人员和开发人员完成各自设备的设备启动过程并满足[设备支持要求宪章](https://www.xda-developers.com/lineageos-device-support-requirements-charter/)中规定的要求，将会随着时间的推移而扩展。官方支持的 LineageOS 16.0 设备的初始名单包括 24 种设备，如下所列。请注意，在本文首次发布时，并非所有的构建都是活动的，所以请回来查看您的设备是否有可用的构建。

### 谷歌

### 荣誉/华为

### LeEco

### 联想（电脑的品牌名）

### 摩托罗拉

### 一加

### OPPO

### 三星电子

### 索尼

### 小米

### 新的 LineageOS 15.1 (Android Oreo)设备

另外，许多设备都获得了官方的 LineageOS 15.1 支持，包括:

该团队表示，LineageOS 15.1 仍将处于积极开发中，但新功能可能不会添加，因为大多数开发人员已经转移到 Android Pie 分支。

### 如果我的设备没有列在这里，该怎么办？

仅仅因为你的设备没有列在这里并不意味着你现在不能享受 LineageOS 16。由于它的开源性质，在我们的论坛上有许多设备的非官方版本，随着开发的进展，其中许多将最终成为官方版本。更重要的是:到目前为止，他们中的大多数都是非常稳定的日常司机，偶尔会有小毛病。

如果你想直接进入，查看我们的论坛，为你的设备寻找非官方的基于 Android Pie 的 LineageOS 16 版本。然而，如果你害怕出错，那么等待官方版本的到来是明智的。

**LineageOS 15.1 和 LineageOS 16.0 变更日志**

*   现在可以在更新器中设置自定义自动更新检查间隔(从不/每天一次，每周一次/每月一次)
*   计算器现在通过[样式 API](https://www.xda-developers.com/lineageos-announce-lineagesdk/) 支持黑暗模式
*   在信息通知中增加了“标记为已读”动作
*   Exchange 支持
*   【2018 年 12 月、[2019 年 1 月](https://www.xda-developers.com/january-2019-android-security-google-pixel/)、[2019 年 2 月](https://www.xda-developers.com/february-2019-android-security-update-pixel-essential/)安全补丁已合并
*   Webview 已更新至 Chromium 71.0.3578.99

## 如何从基于 Android Oreo 的 LineageOS 15.1 升级到基于 Android Pie 的 LineageOS 16

如果你不熟悉安装定制 rom 或修改手机的过程，在尝试做任何事情之前，你首先需要[解锁设备的引导程序](https://www.xda-developers.com/root/)并安装一个更新的定制恢复，如 TWRP。然后，一旦 LineageOS 16.0 版本可用于您的设备，您将需要通过 TWRP 安装它们。

幸运的是，这个过程相当简单。如果您目前运行的是官方的 LineageOS 15.1，您可以通过以下方式升级到官方的基于 Android Pie 的 LineageOS 16.0，而无需擦除数据:

1.  从上面提供的链接或内置更新程序下载更新。
2.  从 [OpenGapps](https://www.xda-developers.com/open-gapps-arm-arm64-android-pie-roms/) 下载一个合适的 Gapps 包(如果你正在使用 Gapps ),或者你的设备维护人员推荐的任何 Gapps 包。相应地，如果你是 root 用户/想要 root，你也应该下载最新版本的 [Magisk](https://www.xda-developers.com/how-to-install-magisk/) 。
3.  重新启动进入恢复模式。
4.  (可选)备份系统、引导、供应商和数据分区，以防安装过程中出现问题。
5.  刷新 LineageOS 16.0 版本，然后是 Gapps 包和 Magisk(如果你已经下载了它们)。
6.  重启进入系统。

如果您目前使用的是非官方的 linegeos 15.1/16.0 版本、另一个 ROM 或您设备的库存固件，那么您应该遵循上述相同的说明，记住您还应该在完成安装过程之前擦除用户数据(工厂重置)。此外，确保您的设备使用最新的固件以及最新的 TWRP 版本，以避免冲突和意外的错误。

## 支撑线

LineageOS 是一个由几个开发人员在业余时间开发的社区项目，不依赖任何商业模式。如果你想支持开发团队，你可以在 PayPal 上向他们捐款，这将有助于服务器成本。如果你想看最新的新闻或者和一些维护者交流，你也应该在 Twitter 或者他们的官方子网站上关注他们。要提交错误报告，请参见此处的。如果你想帮助团队将定制的 ROM 翻译成你的语言，你可以按照这里的[的指示来做。](https://wiki.lineageos.org/translate-howto.html)

**在社交媒体上关注 linegeos**

**捐赠给 linegeos**

*   通过 [PayPal](https://paypal.me/LineageOS) 向 LineageOS 捐款