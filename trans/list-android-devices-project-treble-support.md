# 这是一个更新了 Project Treble 支持的 Android 设备列表

> 原文：<https://www.xda-developers.com/list-android-devices-project-treble-support/>

尽管苹果能够让他们的大部分设备，甚至是许多老款设备，保持最新的软件(有时会涉及[相当有争议的功能](https://www.xda-developers.com/apple-confirms-slows-down-older-iphones-aging-batteries/))，但安卓设备制造商在保持设备最新方面取得了不同程度的成功。像 Essential 和谷歌这样的设备制造商在提供安全补丁方面做得很好，而其他制造商可以一次推迟几个月的更新。这还不包括主要的软件更新，比如从 Android Nougat 到 Android Oreo，这是一个安装在[上的软件版本，仅略多于 1%的 Android 设备](https://www.xda-developers.com/tag/android-distribution/)。为了应对缓慢的 Android 更新，谷歌推出了项目 Treble 。

Project Treble 是对 Android 工作方式的一次重大重构。本质上，它将 Android 操作系统(Android“框架”)与供应商硬件抽象层(HALs)分离开来，后者允许操作系统与设备的硬件协同工作。在 Project Treble 之前，Android 框架和 HALs 通常位于同一区域(系统分区)。有了 Treble，Hal 就被移到了他们自己的区域(一个供应商分区)，现在以一种更加标准化的方式与 Android 框架进行通信。这样做的好处是，它允许三星、LG、HTC 和其他公司修改现有的 Android 框架，同时等待高通等供应商提供更新的 HALs。理论上，这意味着**更新应该更快**。

然而，对于 Android 爱好者社区来说，Project Treble 还提供了另一个好处:无需多次黑客攻击就能快速启动正常运行的 AOSP rom。现在，对于那些希望享受定制 rom 的人来说，这并不是一个完美的解决方案，例如 [LineageOS 或 resurrence Remix](https://www.xda-developers.com/lineageos-15-1-resurrection-remix-available-project-treble/)，因为仍然可能有一些挥之不去的问题或某些硬件无法工作，因为它在 AOSP 还不被支持(例如[虹膜扫描仪](https://www.xda-developers.com/iris-scanners-native-support-android-p/))，但它无疑导致了一场[革命，为以前从未拥有它们的设备定制 rom](https://www.xda-developers.com/how-project-treble-revolutionizes-custom-roms-android-oreo/)。

Treble 项目是如此令人兴奋，我敢肯定你想知道你的设备是否兼容 Treble。我们之前已经写了一篇关于如何在你的 Android 设备上检查 Project Treble 兼容性的教程，但是为了节省你的麻烦，我们也将这些设备分类到一个方便的列表中，你可以在下面参考。

随着我们了解到官方和非官方的支持高音的新设备的更新，该列表将不断更新。这个列表**不会涵盖每一个支持高音**的设备——这将使这个列表太长，因为**谷歌要求每一个[认证的 Android 设备](https://www.xda-developers.com/check-phone-tablet-certified-android-before-buying/)发布 Android 8.0 Oreo 及以上版本以支持高音**。

* * *

## 设备正式更新，支持 Project Treble

### 谷歌

### 荣誉/华为

### 一加

### 小米

### 多方面的

* * *

## 设备非正式地更新了项目高音支持

* * *

如果你的设备收到了 Android Oreo 的更新，并且你认为它应该在这个列表中，请查看我们关于[的指南，了解你的设备是否支持 Project Treble](https://www.xda-developers.com/project-treble-android-oreo/) 和**请在下面留下评论，以便我们更新这篇文章！**

此外，请查看我们的[项目高音设备开发论坛](https://forum.xda-developers.com/project-treble/trebleenabled-device-development)，了解所有通用定制 rom 的最新更新，如 LineageOS 和复活混音！最后，看看我们关于[如何刷新通用系统镜像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/)的指南，以防你有一个支持高音的设备，并且你想安装一个定制的基于 AOSP 的 ROM！