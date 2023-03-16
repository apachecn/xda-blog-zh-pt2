# Magisk 19.4 带来了 Android 10 和产品分区支持，并增加了新的系统根实现

> 原文：<https://www.xda-developers.com/magisk-194-android-10-product-partition-support-new-system-root-implementation/>

# Magisk 19.4 带来了 Android 10 和产品分区支持，并增加了新的系统根实现

最新的 Magisk v19.4 支持 Android 10 A/B 设备、产品分区支持和新的系统根实现。继续阅读，了解更多信息！

XDA 公认的开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 的 [Magisk](https://www.xda-developers.com/tag/magisk/) 最初是一个无系统的 root 方法，多年来已经发展成为一个比普通 root 更加多样化和强大的工具。但即使在今天，如果您需要 root，为您的设备推荐的 root 方法很可能会提到为 root 安装 Magisk。Magisk 的最新更新以 Magisk 19.4 版本的形式出现，它带来了对 Android 10 的支持、对产品分区的支持以及新的系统根实现。

Android 支持两种类型的分区布局:传统分区方案(ramdisk 位于/boot 分区中，挂载为 rootfs，system 挂载在/system)和[较新的 A/B 分区方案](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)，系统挂载为 rootfs。谷歌已经强制要求使用 Android 9 Pie 的设备必须使用[系统根](https://source.android.com/devices/bootloader/system-as-root)(作为对[项目 Treble](https://forum.xda-developers.com/project-treble) 所做的部分改变)，而 A/B 分区仍然是一个推荐但可选的功能，因为它需要进行一些改变。在 Android 10 中，[根文件系统不再包含在 ramdisk](https://source.android.com/devices/bootloader/system-as-root) 中，而是合并到 system 中。

Magisk 从第一个 Google Pixel 开始就支持系统根设备，但是使用的实现存在一些问题。在 Magisk v19.4 中，Magisk 实际上将系统挂载到/ (root)，作为新的 system-as-root 实现的一部分。这是一个很大的变化:/system 不再是有效的挂载点，根目录不再是 rootfs，而是 system，覆盖系统也不同了。此次更新和更改允许 Magisk 在具有全功能 MagiskHide 的 A/B 设备上支持 Android 10。模块开发人员现在还可以正确地修改产品分区中的文件。对运行 Android 10 的纯 A 设备的支持将在未来的更新中推出。

Magisk 更新的变更日志可以在找到[。模块和根开发者也被鼓励阅读这里的](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2)[发行说明](https://github.com/topjohnwu/magisk_files/blob/6510533d6a8bb751152539919f57bb616c2405af/notes.md)。

**[从 XDA 论坛](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)下载 Magisk**