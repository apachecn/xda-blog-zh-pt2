# 在没有 TWRP 的三星 Galaxy 设备上安装自定义 rom 和 GSI

> 原文：<https://www.xda-developers.com/how-to-install-custom-roms-or-gsis-on-samsung-galaxy-devices-without-twrp/>

三星推出了其“Galaxy”品牌智能手机和平板电脑，高度改进的 Android 软件版本，最新一代被称为 [One UI](https://www.xda-developers.com/tag/one-ui/) 。除了与普通安卓系统在用户界面/UX 方面的差异之外，三星的安卓设备还有一个独特之处，那就是它与其他制造商的设备相比非常独特。韩国 OEM 在他们的产品中用自己的协议替代常规的快速启动机制。内部以北欧神话中的人物命名，在设备上运行的代码片段被称为“Loke”的[，而远程端(通常是 PC)组件被称为“Odin”。](https://forum.xda-developers.com/showpost.php?p=7552304)

**[如何下载 Odin 固件来降级、升级或恢复您的三星 Galaxy](https://www.xda-developers.com/download-stock-odin-firmware-samfirm/)**

缺乏快速启动兼容接口听起来像是修改场景的一个巨大障碍，但售后开发者社区总是设法将他们的手放在*泄露的* Odin 二进制文件上来完成事情。自定义协议本身在很久以前就被逆向工程，产生了一个跨平台的开源 flash 工具，叫做 [Heimdall](https://glassechidna.com.au/heimdall/) 。人们可以从源代码编译 Heimdall，或者简单地获取 Odin 的补丁版本，以便[让他们的三星 Galaxy 设备](https://www.xda-developers.com/samsung-galaxy-s10-plus-s10e-s10-exynos-rooted-magisk-canary/)扎根，安装像 TWRP 一样的定制恢复，并执行[许多其他刷新工作](https://www.xda-developers.com/samsung-galaxy-s9-galaxy-note-9-snapdragon-root/)。

一旦你安装了 TWRP，你就可以很容易地用 LineageOS 这样的定制 Android ROM 来替换三星的 Android 版本。即使你的三星型号没有定制的 rom，你也可以在技术上[安装一个通用的系统镜像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)，前提是该设备符合 Project Treble 标准，并且带有一个可解锁的引导程序。然而，将 TWRP 移植到最近运行 Android 10/One UI 2 的三星设备(例如 [Galaxy S20](https://forum.xda-developers.com/galaxy-s20) 系列)是一项[复杂的任务](https://www.xda-developers.com/twrp-lead-explains-android-10-support-custom-recovery/)。稳定的定制恢复的不可用性直接阻碍了在这种型号上安装定制 ROMs 的能力。

XDA 的年轻成员 kkoo 现在想出了一个聪明的主意来绕过这些障碍。鉴于三星的官方固件包只不过是一个 [LZ4](https://github.com/lz4/lz4) 压缩档案的集合，一个类似打包的定制 ROM(或 GSI)可以使用 Odin 进行闪存。目标设备的[验证引导](https://www.xda-developers.com/android-pie-rollback-protection/)功能必须事先禁用，这可以通过安装 Google 提供的[空 vbmeta 镜像来实现。](https://dl.google.com/developers/android/qt/images/gsi/vbmeta.img)

所有你需要遵循的指导都已经发布在下面链接的论坛帖子里了。XDA 初级会员描述的过程需要在运行 Windows 的电脑上执行一些命令行脚本。同一个论坛帖子中还链接了刷新和配置 GSI 的说明。

**[使用 Odin 在没有 TWRP](https://forum.xda-developers.com/galaxy-s10/how-to/guide-how-to-install-custom-rom-using-t4114435) 的三星 Galaxy 设备上安装自定义 ROM/GSI**