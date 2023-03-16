# Magisk Canary update 增加了对许多运行 Android Pie 的小米和魅族设备的支持

> 原文：<https://www.xda-developers.com/magisk-canary-update-support-aonly-system-root-android-pie/>

# Magisk Canary update 在 Android Pie 上增加了对只支持系统根设备的支持

Magisk 的“出血边缘”金丝雀发布频道的最新更新带来了对运行 Android Pie 的唯一系统根设备的支持。请继续阅读！

Android 的生态系统支持两种分区布局:传统分区方案(ramdisk 存在于/boot 分区中，挂载为 rootfs，system 挂载在/system)和[较新的 A/B 分区方案](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)，系统挂载为 rootfs。谷歌已经将[系统作为根](https://source.android.com/devices/bootloader/system-as-root)强制用于安装 Android 9 Pie 的设备(作为 Project Treble 所做更改的一部分)，但 A/B 分区仍然是一个推荐但可选的功能，因为它需要进行更改。这意味着将会有新的设备发布 Android Pie，但是会有一个单独的“A-only”分区。对于这些设备，OEM 仍然必须确保手机使用 system-as-root，这反过来意味着 ramdisk 必须合并到系统映像中才能作为 rootfs 安装。对于升级到 Android 9 Pie 的设备，System-as-root 不是强制性的。

这种情况给想要在设备上运行 Magisk 的用户带来了问题。Magisk 已经支持系统根设备，但这仅限于使用较新的 A/B 分区方案的设备。如果 Magisk 安装在他们的 Android Pie 版本上，那么几个中国设备，如[小米 Mi 8 SE](https://forum.xda-developers.com/mi-8-se) 和其他一些设备，显然还有新的[三星 Galaxy S10](https://www.xda-developers.com/tag/samsung-galaxy-s10/) 也是如此，它们利用系统根安装而不使用 A/B 分区，最终将无法启动。

Magisk 现在增加了对仅系统根设备的支持。这个改动目前在 [Canary 构建通道](https://github.com/topjohnwu/magisk_files/tree/master/canary_builds)中可用，构建号 v18.2-e72c6685 (18111)。您也可以通过 Magisk Manager 安装 Canary builds，方法是将更新通道切换到 custom 并粘贴以下链接:

```
 https: 
```

请注意， [canary 发布频道](https://forum.xda-developers.com/apps/magisk/dev-magisk-canary-channel-bleeding-edge-t3839337)被认为是 Magisk 发布的“前沿”,因此，仅推荐给开发人员，而不是普通用户。请不要仅仅为了安装最新版本而安装金丝雀版本。

* * *

[**来源:Magisk Github**](https://github.com/topjohnwu/Magisk/commit/e72c6685edf81706617a3444575c4500b9b8fe6c)

[**论坛链接:Magisk 金丝雀频道发布线程**](https://forum.xda-developers.com/apps/magisk/dev-magisk-canary-channel-bleeding-edge-t3839337/page84)