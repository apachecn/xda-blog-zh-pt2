# 小米 Mi A1 和 Mi 9 的后代 X 定制 ROM 增加了“Guardia”，这是一个后台权限监视器

> 原文：<https://www.xda-developers.com/descendant-x-custom-rom-xiaomi-mi-a1-mi-9-adds-guardia-background-permission-monitor/>

Android 开放、无围墙的花园设计给了用户定制的自由。由于活跃的售后开发社区，Android 用户可以享受大量的功能，否则谷歌或原始设备制造商不会实现。以 Android 新的高级权限管理控制系统 Permissions Hub 为例，该系统在早期泄露的 Android Q builds 中出现，但谷歌没有在公开版本中发布。相关的代码片段仍然存在于 AOSP，后来被 LineageOS 团队在[分叉，现在普通用户可以通过](https://www.xda-developers.com/lineageos-dropping-superuser-addonsu-implementation-favor-magisk-manager/) [LineageOS 17.1](https://www.xda-developers.com/lineageos-17-1-android-10-officially-available/) 访问。XDA 资深成员 Dil3mm4 现在又以他们自己的方式尝试增强许可机制。新的后台权限监视器被称为“Guardia ”,是他们最新定制的 ROM“后代 x”的一部分。

对于那些不熟悉 Descendant X 的人来说，它是一个基于 Android 10 的通用系统映像(GSI)，由 XDA 公认的开发者 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 在 AOSP GSI 维护。与任何其他定制 ROM 类似，Descendant X 也可以以设备特定的 zip 形式提供。开发者尚未更新 Guardia 的 GSI 版本，但你现在可以通过闪烁小米 Mi 9 和 Mi A1 的最新后代 X 包来访问权限监控功能。

**X 后裔下载讨论线程:[米 9](https://forum.xda-developers.com/Mi-9/development/cepheus-descendant-x-android-ver-10r32-t4062951/)| |[米 A1](https://forum.xda-developers.com/mi-a1/development/tissot-descendant-x-android-ver-10r32-t4062959/)**

**[米 9](https://forum.xda-developers.com/Mi-9) [XDA 论坛](https://forum.xda-developers.com/Mi-9) || [米 A1 XDA 论坛](https://forum.xda-developers.com/mi-a1)**

用户可以在设置>隐私下找到 Guardia。开启该功能后，Guardia 将开始在后台运行，并通知您请求权限的应用。您可以为不同的场景(例如位置访问和摄像头)定制警报类型，甚至可以将 Google apps 和/或系统应用程序放在一个允许列表中，这样您就不会受到数百个此类信息丰富但令人讨厌的警报的困扰。

鉴于谷歌将在即将发布的 Android 11 中引入过多的[操作系统范围的权限相关变化](https://www.xda-developers.com/android-11-beta-1-update-live-google-pixel-2-3-3a-4-xl-device-controls-api-quick-settings-media-controls/)，我们希望开发者将通过在这些修订的基础上集成组件来进一步改进 Guardia。

除了后台权限监视器，最新版本的 Descendant X(版本 10r40)还引入了【2020 年 7 月安全补丁、一些时钟流主题和粉丝最喜欢的通知滚动条。以下视频展示了此版本中的所有变化:

**后裔 X: [下载](https://downloads.descendant.me/)| |[XDA 讨论线程(GSI)](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/arm64-ab-descendant-x-android-ver-10r32-t4064891)**