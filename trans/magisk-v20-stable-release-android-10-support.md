# Magisk v20 稳定版现在完全支持 Android 10

> 原文：<https://www.xda-developers.com/magisk-v20-stable-release-android-10-support/>

# Magisk v20 稳定版现在完全支持 Android 10

Magisk 稳定版最新版本现在全面支持安卓最新版本 Android 10，全线。看看吧！

Magisk 在过去几年中变得如此受欢迎，以至于现在没有必要介绍了。但是如果你需要的话，它是一个无系统接口，最初是一个简单的无系统根方法，是当时领先的根方法 [SuperSU](https://www.xda-developers.com/supersu-suhide-updates-bug-fixes/) 的替代方法，并且已经发展成为一个非常有用的工具，允许你进行各种无系统的修改。它允许你从 Android Pie 到 Android KitKat 的所有形状和形式的设备中找到根。现在，Android 10 在稳定分支上也得到完全支持。

Magisk 的最新主要版本对应于第二十个版本(v20)，现在已经到达稳定分支，正式全面支持所有 Android 10 设备。将 Magisk 移植到最新的 Android 版本被证明比以前的版本更棘手，上一个版本 [v19.4 公测版](https://www.xda-developers.com/magisk-194-android-10-product-partition-support-new-system-root-implementation/)，只为 Android 10 带来了部分支持:你只能在 A/B 设备上成功安装它。 [Magisk v20](https://github.com/topjohnwu/Magisk/releases/tag/v20.0) 也带来了对 A-only 设备的支持，使事情回到原点，并使 Magisk 与最新版本的 Android 完全兼容。

v20 稳定版的[变更日志](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2)如下:

*   [MagiskBoot]支持在 DTB fstab 中注入/修改 mnt_point 值
*   [MagiskBoot]支持打补丁 QCDT
*   [MagiskBoot]支持修补 DTBH
*   [MagiskBoot]支持修补 PXA-DT
*   [MagiskInit] [2SI]支持非 A/B 设置(Android 10)
*   [magiskshide]修复了拒绝进程名为“:”的错误
*   [MagicMount]修复了导致/product 镜像无法创建的错误

当然，为了与 Android 10 兼容，更新中包含了一些变化，包括如上所述的一些 bug 修复。如果您有兴趣试用 Android 10，但不想在没有 Magisk root 的情况下继续，那么您现在可以安全地更新到 Android 10，并在我们的论坛中查看 Magisk v20。你可以在这里查看完整的变更日志。

在我们的论坛中查看 Magisk！