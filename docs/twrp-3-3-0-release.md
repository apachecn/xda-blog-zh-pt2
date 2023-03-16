# TWRP 3.3.0+将不再需要安装拉链，增加了重新启动到 EDL 模式按钮，等等

> 原文：<https://www.xda-developers.com/twrp-3-3-0-release/>

对于大多数用户来说，安装任何类型的售后软件修改，无论是自定义 ROM，自定义内核，或其他工具，都需要使用像 TWRP 定制恢复。多年来，TWRP 一直是 XDA 社区的首选康复解决方案。它是开源的，支持数百种设备。它提供了完整备份和恢复、ADB 侧加载等功能。如今，该项目已经升级到 3.3.0-0 版本，带来了许多解密方面的改进、新功能以及对 TWRP 安装方式的重大改变。

完整的变更日志概述了 TWRP 解密支持的许多改进，可以在下面找到，但对于用户来说，最重要的变化将是安装自定义恢复的新方式。目前，在带有 A/B 分区的设备上安装 TWRP 需要临时启动 TWRP，然后使用安装程序脚本永久安装。今后，用户将在恢复中看到一个新的“安装恢复 ramdisk”选项。这意味着用户可以启动 TWRP，然后安装它，而不需要下载一个单独的 ZIP 文件。XDA 资深知名开发人员 [Dees_Troy](https://forum.xda-developers.com/member.php?u=912474) 与 XDA 知名开发人员 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 合作，通过为 TWRP 修改 Magisk 的启动映像补丁来实现这一点。Dees_Troy 表示，该团队这次将提供安装程序 zip，让人们有机会从旧版本进行更新，但未来的 TWRP 版本将不会有单独的安装程序脚本。

另一个与用户最相关的变化是包含了一个“重启到 EDL 模式”按钮。如果有合适的工具，紧急下载模式可以帮助您[完全解除设备](https://www.xda-developers.com/unbrick-oneplus-6t-t-mobile-international/)的锁定，但是进入该模式的按钮组合并不像重启恢复方法那样为用户所熟知。

以下是更新的完整变更日志:

**TWRP 3.3.0-0 变更日志**

*   合并 AOSP 9.0 r3(迪斯 _ 特洛伊)
*   使用 ANDROID_ROOT 变量代替硬编码到/system (CaptainThrowback)
*   在 9.0 上解密 FBE 和元数据解密(Dees_Troy)
*   vold 解密更新(CaptainThrowback 和 nijel8)
*   支持 LED 类设备上的振动(非同步)
*   元数据解密支持 Pixel 3 (Dees_Troy)
*   支持通过构建标志旋转显示(vladimiroltean)
*   重启至 EDL 模式按钮(mauronofrio)
*   支持 FFS 设备上的 MTP(bigbiff)
*   更新 FDE 解密，以支持密钥大师 3 和 4 (Dees_Troy)
*   检测 mkfs.f2fs 版本以正确格式化 f2fs 分区(Dees_Troy)
*   允许 TWRP 对 zip 安装使用 md5 和 sha256 校验和(bigbiff)
*   TWRP 可以在没有缓存分区(bigbiff)的 AB 设备上使用/data/cache/recovery 和/persist/cache/recovery
*   切换 TWRP 的部分高级菜单以使用选项列表框
*   使用 magiskboot 允许重新打包启动映像来安装 TWRP (Dees_Troy，当然要感谢 topjohnwu)

您可以从下面的官方网站为您的设备下载最新版本的定制恢复。版本 3.3.0-0 将为所有支持的设备构建，因此如果您的设备目前正在维护，那么您应该会在几个小时或几天内看到更新。不过，构建框中大约有 450 个设备，所以有些设备可能无法构建。请务必查看您设备的 XDA 论坛，因为您设备的 TWRP 维护者可能会在版本上线时发布更新。

[**为您的设备下载 TWRP**](http://twrp.me/Devices)

最后，一定要从 Google Play 下载官方应用。当新版本的自定义恢复可用时，该应用程序会提醒您。它还能让你从你的设备上下载最新版本。