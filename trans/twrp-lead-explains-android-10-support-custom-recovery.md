# TWRP 领导解释了为什么定制恢复需要时间来支持 Android 10

> 原文：<https://www.xda-developers.com/twrp-lead-explains-android-10-support-custom-recovery/>

# TWRP 领导解释了为什么定制恢复需要时间来支持 Android 10

TWRP 领导和 XDA 资深公认开发人员 Dees_Troy 强调了 Android 10 支持自定义恢复的一些挑战。请继续阅读！

[甜品名不](https://www.xda-developers.com/android-10-android-q-brand-redesign/)，[安卓 10](https://www.xda-developers.com/tag/android10/) 是当季的风味。几家知名 OEM 厂商的旗舰产品已经收到了他们的官方更新，而其他几家则由于 Android 10 定制 rom 而体验了新的操作系统版本。谷歌也[对 Android 10 的采用率](https://www.xda-developers.com/google-project-treble-improved-os-android-adoption/)非常满意，这是因为 Project Treble 和多年来所做的其他一系列改变。不幸的是，虽然 Android 10 带来了它自己的快乐，但它也给像 TWRP 这样的定制恢复带来了一些困难。TWRP 首席开发者和 XDA 资深公认开发者 [Dees_Troy](https://forum.xda-developers.com/member.php?u=912474) 强调了恢复在正式支持 Android 10 的道路上面临的一些问题。

正如 Dees_Troy 所说，TWRP 对 Android 10 的支持还需要一段时间。他的声明是针对谷歌 Pixel 3 和谷歌 Pixel 4，以及将搭载 Android 10 作为基础版本的设备而言的。搭载旧版本 Android 并随后更新到 Android 10 的旧非像素设备不受影响。

据 dev 称，Android 10 为 AOSP 近年来的恢复实施带来了一些最大的变化。AOSP 恢复中的组件已被移动到子文件夹中，这使得将更改合并到 TWRP 更加耗时。对 ramdisk 所做的更改，例如从没有链接库的静态二进制文件转移到动态链接，也为开发人员提供了如何根据这些更改最好地前进的决策。即使做出了这些决定，新的挑战也会出现，比如根据这种动态链接将系统分区挂载到/system。Android 10 还引入了开发者所说的“超级”分区——包含一堆更小分区的分区；Google 将只读的 ext4 文件系统用于超级分区中的新动态分区。这给开发人员带来了新的挑战，例如用户如何安装 GApps，以及如何为用户提供正确的工具来管理和更改超级分区上的动态分区。

所有这些变化和随之而来的反应需要进行一些修改，同时讨论如何最好地处理这种情况。最终结果是，TWRP 官方将需要一段时间来实现对 Android 10 的全面支持。

* * *

**来源:[TWRP](https://twrp.me/site/update/2019/10/23/twrp-and-android-10.html)**