# POCO F1 获得 Android Pie 项目 Treble GSIs 的修改供应商

> 原文：<https://www.xda-developers.com/poco-f1-vendor-android-pie-project-treble-gsi/>

由于 POCO 的第一款旗舰设备[的低价](https://www.xda-developers.com/xiaomi-poco-f1-specs-pricing-availability-india/)和 POCO 的[官方支持，POCO F1 在 XDA 论坛上变得非常受欢迎。就在几周前，一些基于 Android 8.1 奥利奥的定制光盘](https://www.xda-developers.com/poco-pick-developers-poco-f1/)[出现在我们的论坛](https://www.xda-developers.com/poco-f1-lineageos-15-1-resurrection-remix-aosip-aosp-extended/)上。后来，第一个 Android Pie 定制 ROM [可用于该设备](https://www.xda-developers.com/lineageos-16-android-pie-poco-f1/)。对于那些不想等待更多特定设备、基于 Android Pie 的定制 rom 并想尝试现有通用系统映像(GSI)之一的人来说，你应该看看这个由 XDA 高级成员 [shahan_mik3](https://forum.xda-developers.com/member.php?u=5162591) 修改的[供应商和引导映像](https://forum.xda-developers.com/poco-f1/development/release-1-vendor-gsi-t3850372)。

对于那些你不知道的人来说，每一台搭载 Android 8.0 Oreo 和更高版本的设备都支持 Project Treble。Project Treble 涉及将 Android 框架从供应商 HALs 中分离出来，因此 Android 操作系统和使您的手机硬件功能的文件是分开的。相反，供应商接口为供应商实现提供了一种与操作系统通信的方式。目标是使 Android 操作系统的升级能够独立于供应商的文件更新，因此，使支持三重功能的设备能够引导纯 AOSP ROM——GSI。Treble 规范是在 Android 8.1 Oreo 和 Android 9 Pie 中完善的，因此大多数使用 Android Pie 之前软件的设备在刷新 GSI 时仍会有一些错误，这些错误只能通过修改供应商的实现来修复。

这正是 shahan_mik3 修改厂商和引导镜像的目的。目前，如果你在小米 POCO F1 的供应商和启动映像上显示任何 Android Pie GSI，你会遇到 VoLTE 和其他一些问题。然而，如果你刷新了这个修改过的厂商镜像，你就可以刷新任何没有 VoLTE 错误的 Android GSI 了。开发人员表示，将来会在他们修改后的供应商和引导映像中添加额外的修复程序。

## 如何为 POCO F1 安装修改后的供应商和启动映像

去[这个线程](https://forum.xda-developers.com/poco-f1/development/release-1-vendor-gsi-t3850372)下载开发者提供的最新修改的厂商和引导镜像。我们也建议你通读前几篇文章。假设你已经有了一个解锁的引导加载程序，你只需启动 TWRP(开发者推荐 XDA 公认的开发者 [TheStrix](https://forum.xda-developers.com/member.php?u=5857684) 的链接[这里](https://forum.xda-developers.com/poco-f1/how-to/xiaomi-poco-f1-unlock-bootloader-custom-t3839405))，格式化用户数据分区(如果 MIUI 之前已经安装并且设备已经加密)，然后刷新修改后的厂商和引导镜像 zip 包。

在闪出 zip 包之后，你可以去我们的[Project Treble device development forum](https://forum.xda-developers.com/project-treble/trebleenabled-device-development)下载你选择的任何 A-only Android Pie GSI。POCO F1 是一款仅支持 A 的设备(也就是说，它没有用于无缝更新的 [A/B 分区](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)，因此您不能闪存任何为 A/B 设备构建的 GSI。此外，由于高通骁龙 845 片上系统的性质，POCO F1 是一款 ARM64 器件，因此您不能闪存任何为 ARM 器件构建的 GSI。最后，如果你计划刷新非 GSI ROM 或 MIUI，你将需要刷新股票供应商图像。否则，您可能会遇到一些错误。

[**为 POCO F1**](https://forum.xda-developers.com/poco-f1/development/release-1-vendor-gsi-t3850372) 下载修改后的供应商图像

[**加入 XDA 小米 POCO F1 论坛**](https://forum.xda-developers.com/poco-f1)

[**加入 XDA 项目三宝论坛**](https://forum.xda-developers.com/project-treble/trebleenabled-device-development)