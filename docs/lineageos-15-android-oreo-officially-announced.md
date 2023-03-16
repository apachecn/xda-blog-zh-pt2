# 基于 Android 8.1 奥利奥的 LineageOS 15.1 已经正式公布

> 原文：<https://www.xda-developers.com/lineageos-15-android-oreo-officially-announced/>

继 2016 年底 CyanogenMod 的[消亡之后，它的](https://www.xda-developers.com/the-death-of-cyangenmod-and-whats-in-store-for-the-future/)[继任者](https://www.xda-developers.com/official-lineageos-builds-start-rolling-out-for-nexus-6p-nexus-5x-nexbit-robin-and-more/)、 [LineageOS](https://www.xda-developers.com/xda-forums-dedicated-to-lineage-os-now-live/) 的人气直线上升。在 700 多名贡献者的帮助下，项目[发展到支持](https://www.xda-developers.com/happy-birthday-to-lineageos/)180 多种设备，覆盖 180 多万用户。现在，这个团队已经准备好迈向下一个里程碑:重新基于 Android 8.1 Oreo。在 12 月戏弄我们之后，这个团队今天[宣布](https://www.lineageos.org/Changelog-16/)linea geos 15.1 已经准备好了。

安装最广泛的 Android 定制 ROM 现在提供了 Android 8.0 和 Android 8.1 Oreo 带来的所有功能。这意味着[通知通道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)和[打盹](https://www.xda-developers.com/customize-notification-snooze-duration-android-oreo/)，[画中画模式](https://www.xda-developers.com/netflix-pip-mode-picture-android-8-1/)，支持[自动填充框架](https://www.xda-developers.com/android-os-autofill-framework-will-finally-resolve-a-long-standing-lag-issue-with-password-managers/)，[更好的后台应用和服务限制](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)以提高内存性能/电池，[智能文本选择](https://www.xda-developers.com/android-oreo-smart-text-selection-stable-google-chrome/)，等等。更不用说，LineageOS 还提供了所有的功能，如[隐私保护](https://www.xda-developers.com/protecting-your-privacy-app-ops-privacy-guard-and-xprivacy/)、[现场展示](https://www.xda-developers.com/lineageos-adding-livedisplay-quick-settings-tile/)，以及更多的[，你可以在我们的配套文章](https://www.xda-developers.com/lineageos-15-feature-list-overview-screenshots-video/)中读到。

[**LineageOS 15.1 特性列表概述**](https://www.xda-developers.com/lineageos-15-feature-list-overview-screenshots-video/)

随着 LineageOS 15.1 的推出，该团队还发布了另一项重大消息。他们正式引入了[设备支持需求章程](https://www.xda-developers.com/lineageos-device-support-requirements-charter/)，这是一份[文件](https://github.com/LineageOS/charter/blob/master/device-support-requirements.md)，它概述了 LineageOS 及其维护者的构建必须满足的所有需求，以使构建被视为“正式的”这是车队向前迈出的关键一步，因为它清楚地表明了车队对质量的承诺。该文档本身并不太长，但总的来说，它确保了 LineageOS 15.1 的官方版本尽可能地支持所有基本硬件，并接收针对所有高调安全漏洞的补丁。

现在，来看看宣布支持 LineageOS 15.1 的实际设备。目前，该列表在第一轮中并不是很大，但随着时间的推移，更多的开发人员可能会在完成设备启动并满足设备支持要求章程中规定的要求后添加到该列表中。具体来说，我们被告知，由于缺乏对 HAL1 摄像机工作的支持，一些设备无法接收 LOS 15.1，但他们正在努力。此外，虽然 LOS 15.1 是今天宣布的，但夜间版本要到周一他们的构建服务器开始制作时才会准备好。

## 最初官方支持 LineageOS 15.1 的设备列表

## 装置

在你安装这些版本之前(一旦它们上线)，你需要[解锁你设备的引导程序](https://www.xda-developers.com/root/)，并且刷新一个[自定义恢复，比如 TWRP](https://www.xda-developers.com/how-to-install-twrp/) 。

像往常一样，官方 LineageOS 版本不预装超级用户二进制文件。相反，根据您手机的 SoC 架构，您还需要安装此处列出的文件之一。或者，你也可以安装 [Magisk](https://forum.xda-developers.com/apps/magisk) 或者 [SuperSU](https://forum.xda-developers.com/apps/supersu) 。

至于谷歌应用程序，它们不会预装在 LineageOS 15.1 版本中。 [Open Gapps](https://forum.xda-developers.com/android/software/pa-gapps-continuation-t3098071) 目前不提供 Android 8.1 Gapps(具体来说，SetupWizard APK 仍然是 8.0)，因此该团队建议您从 [MindTheGapps 这里](https://androidfilehost.com/?w=files&flid=170282)获取它们。

最后，在你刷新这些版本之前，建议你备份你的应用和数据。最推荐的方式是使用一个 app，比如 [Titanium Backup](https://play.google.com/store/apps/details?id=com.keramidas.TitaniumBackup) 或者一个免费的替代品，比如 [oandbackup](https://f-droid.org/packages/dk.jens.backup/) 。两者都需要 root 访问权限才能运行。

现在，要实际安装该版本，这取决于您当前安装了什么。

如果你运行的是 LineageOS 14.1 的官方版本**，那么你可以按照这些步骤**执行，而不需要清除数据**。**

1.  从上面的链接或通过内置的更新程序下载更新。如果你是从更新应用程序下载的，你需要使用菜单中的“导出”选项将构建保存到你的内部存储。
2.  下载 Gapps 软件包和上面链接的超级用户软件包之一。
3.  启动进入恢复状态。
4.  格式化系统分区。
5.  刷新 LineageOS 15.1 版本，然后刷新 Gapps 和超级用户软件包。
6.  重启。

如果你**没有**运行 LineageOS 14.1 的正式版本(即。还有什么)，然后你按照上述相同的一套指示，除了你必须**在闪烁**之前擦除数据。

## 动手+功能

有兴趣在安装前了解 LineageOS 15.1 提供的功能吗？在我们的 YouTube 频道上查看 Miles 的实践视频！另外，请务必查看我们的[随附文章](https://www.xda-developers.com/lineageos-15-feature-list-overview-screenshots-video/)，其中介绍了 LOS 15.1 提供的几乎所有功能！它甚至有一切的截图和一个视频来引导你！

## 关于非官方建筑的说明

仅仅因为你的设备不是上面列出的设备之一，并不意味着你不能享受 LineageOS！由于该项目是开源的，这意味着任何独立的开发者都可以基于其源代码构建一个定制的 ROM。然而，质量可能相差很大，所以如果你刷新了一个非官方的版本，有些东西坏了，不要惊讶。另一方面，[一些非官方版本](https://www.xda-developers.com/lineageos-honor-view-10-huawei-mate-10-pro-project-treble/)相当接近稳定，完全可以在你的设备上刷新。

在我们的论坛上有许多非官方的 LineageOS 版本，什么能工作或者不能工作很大程度上取决于设备。在你开始在你的设备上刷新一个定制的 ROM 之前，请仔细阅读任何论坛帖子的原文——这会让你省去很多麻烦！

## 新壁纸

随着新版本的推出，一套新的壁纸！这些壁纸都来源于 [Unsplash](https://unsplash.com/) 。你可以看看下面的壁纸，如果你有兴趣在一个非线性地理构建中使用它们的话。你也可以在下面下载。请注意，我们提供的是未经旋转的原始壁纸，因此它们也非常适合您的桌面显示器！

[**下载 LineageOS 15.1 官方壁纸**](https://www.androidfilehost.com/?fid=890129502657585215)

## 支撑线

从事这项工作的开发人员是在业余时间无偿工作的，所以请考虑尽你所能支持这个项目。你可以在下面列出的所有官方社交媒体渠道上关注他们，或者在下面向他们捐款，以示支持。