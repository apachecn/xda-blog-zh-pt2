# 开发者为索尼 Xperia M4 Aqua 带来主线 Linux 内核支持，带有非官方的 Android 11 定制 ROM

> 原文：<https://www.xda-developers.com/sony-xperia-m4-aqua-mainline-linux-kernel-android-11-custom-rom/>

在过去的几周里，我们发了很多关于[Android 11 官方更新](https://www.xda-developers.com/android-11-update-tracker/)和[基于 Android 11 的定制 rom](https://www.xda-developers.com/android-11-custom-rom-list/)的帖子。甚至还有一个特殊的[定制通用系统映像(GSI)版本](https://www.xda-developers.com/developer-boots-android-11-22-older-devices-project-treble-gsi/)，任何人都可以通过它在他们的 Project Treble 兼容设备上体验 Android 11。然而，在通用内核开发领域还没有取得类似的成就。如果特定 Android 智能手机的每一个硬件组件都可以[升级到主流 Linux 内核](https://www.xda-developers.com/samsung-galaxy-siii-samsung-galaxy-note-ii-htc-hd2/)，那么该设备应该能够引导任何常规的 GNU/Linux 发行版，而无需额外的更改，这也使得它更容易跟上新的 AOSP 版本。现在，资深内核开发人员 Pavel Dubrova，也就是 XDA 成员 Cubbins 展示了一台索尼 Xperia M4 Aqua，它实际上在 AOSP 11.0 定制 ROM 下运行主线 Linux 内核。

**[索尼 Xperia M4 阿卡 XDA 论坛](https://forum.xda-developers.com/m4-aqua)**

像所有安卓设备一样，2015 年的索尼 Xperia M4 Aqua 运行在经过修改的 Linux 内核上。谷歌通常会采用一个主线 Linux 内核版本，然后对其进行修改，以支持当时最新的 Android 版本——他们称之为“Android 公共内核”。芯片组制造商(在这种情况下，高通)然后采用 Android 通用内核，并对其进行进一步修改，以制作 SoC 专用内核。OEM/ODM(如索尼)然后采用特定于 SoC 的内核，并做进一步的更改以支持他们的硬件或额外的供应商组件——我们称之为特定于设备的内核。

因为 Linux 内核是在 GNU GPL v2 许可证下发布的，所以所有发布内核分支(包括商业设备上发布的 Linux 内核 blobs)的实体都需要根据请求提供其内核的源代码。索尼确实发布了基于 Linux 内核 3.10 的 Xperia M4 Aqua(代号“郁金香”)的内核源代码，但考虑到这款手机太旧了，无法支持 Project Treble，官方源代码树不足以将现代版本的 Android(或任何 Linux 发行版)移植到这款设备上。

Pavel 也参与了 [postmarketOS](https://www.xda-developers.com/postmarketos-touch-optimized-linux-distro/) 项目，他已经[从零开始为 Xperia M4 Aqua 创建了一个定制设备树](https://github.com/bartcubbins/device_sony_tulip-mainline)到[启用主线 Linux 内核](https://github.com/bartcubbins/kernel_kanuti_mainline)支持(注意，这里的“主线”和[谷歌自己的“项目主线”](https://www.xda-developers.com/android-q-project-mainline-security/)并不相关)。开发者还为这款手机上传了一个现成的 flash AOSP 11.0 版本，它与预编译的 Linux 内核 5.9 RC7 一起发布。

到目前为止，ROM 中还缺少许多特定于硬件的特性，但这没什么，因为我们仍处于早期阶段，随着时间的推移，这些特性将在源代码端得到修复。我们希望官方对 Linux 内核中几乎所有关键硬件组件的支持将为未来版本的 Android 和其他基于 Linux 内核的操作系统移植到 Xperia M4 Aqua 和类似的其他设备铺平道路。如果你想了解更多，看看下面链接的 XDA 主题。

**[Android 11 采用主线 Linux 内核为索尼 Xperia M4 Aqua — XDA 线程](https://forum.xda-developers.com/m4-aqua/rom-android-11-mainline-linux-kernel-t4172351)**