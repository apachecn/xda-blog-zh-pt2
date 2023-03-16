# UBports GSI 将 Ubuntu Touch 带到任何支持 Treble 的 Android 设备上

> 原文：<https://www.xda-developers.com/ubports-gsi-brings-ubuntu-touch-to-any-project-treble-supported-android-device/>

在兼容的 Android 设备上启动 AOSP 通用系统映像(GSI)的能力是 T2 项目的最佳成果之一，但是在通用内核开发领域还没有类似的成就。谷歌确实要求每个新版本的 Android 都有一个[最低 Linux 内核版本要求](https://www.xda-developers.com/google-mandating-linux-kernel-versions-android-oreo/)，但你仍然不能简单地在你的 Android 智能手机上闪存一个通用的 ARM Linux 发行版并期望它能工作，因为事实上大多数 Android 设备都没有使用主流的 Linux 内核。有一个名为 [UBports](https://www.xda-developers.com/ubuntu-to-show-off-community-ports-on-oneplus-one-sony-xperia-z1-at-mwc-2016/) 的社区驱动项目，旨在将 Ubuntu Touch(流行的 Ubuntu Linux 发行版的移动版本)引入 Android 设备，但[他们的设备支持](https://devices.ubuntu-touch.io/)迄今为止相当少。

然而，XDA 公认的开发商 erfanoabdi 正试图从一个不同的角度解决这个问题。开发人员没有等待特定于设备的补丁在[主线 Linux 内核源代码树](https://github.com/torvalds/linux)中登陆，而是成功地创建了一个 GSI 风格、平台无关的 Ubuntu Touch 映像，可以安装在任何 Project Treble 兼容设备上。

听起来很熟悉？嗯， [erfanoabdi](https://forum.xda-developers.com/member.php?u=6298645) 就是几个月前成功[将 Ubuntu Touch 移植到小米红米 Note 7](https://www.xda-developers.com/developer-ports-ubuntu-touch-to-the-xiaomi-redmi-note-7/) 的人。与最初版本不同，目前的 GSI(仍然基于 Ubuntu 16.04 LTS 版)几乎是日常驱动的材料。得益于内置的 [Anbox](https://www.xda-developers.com/anbox-allows-you-to-run-android-apps-on-any-gnulinux-os/) 环境，你可以收发电话，连接蓝牙外设，使用 GPS，甚至运行 Android 应用程序。

## 我的设备与 Ubuntu Touch GSI 兼容吗？

大概是的。该 GSI 的底层供应商界面是针对基于 Android 9 Pie 的固件进行测试的，尽管 GSI 也可以在基于 Android 8.0 和 8.1 的旧供应商映像上工作。此外，您需要修补股票内核，使其与 [Project Halium](https://www.xda-developers.com/halium-is-an-open-source-project-working-towards-a-common-base-for-non-android-mobile-operating-systems/) 兼容。这部分有点复杂，因为目前还没有办法即时修补 Android 设备的现有启动映像。您可以从源代码构建 halium-boot，也可以通过在内核源代码上手动应用适当的补丁来编译您的普通内核的独立修改版本。点击了解更多[。](https://github.com/ubports/porting-notes/wiki/Generic-system-image-(GSI)#how-to-build-patched-kernel-or-halium-boot)

一旦你完成了补丁部分，你应该可以像其他安卓 GSI 一样安装 Ubuntu Touch GSI 了。刷新过程将要求您格式化您的数据分区，因此请提前执行备份。

**Ubuntu Touch (UBports) GSI: [下载](https://build.lolinet.com/file/halium/GSI/)| |[XDA 讨论线程](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/gsi-ubuntu-touch-ubports-t4110581)**