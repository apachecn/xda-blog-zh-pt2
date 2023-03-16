# 为 Android 调试和修改设计的 Linux 发行版 FWUL 发布了 3.0 版本

> 原文：<https://www.xda-developers.com/fwul-android-debugging-distro-3-0/>

# 为 Android 调试和修改设计的 Linux 发行版 FWUL 发布了 3.0 版本

FWUL 是一个用于 Android 调试的定制 Linux 发行版。开发者在几周前宣布了 3.0 版本的发布。

机会是，一生中至少有一次，你需要刷新你的 Android 设备，或者简单地使用 adb 或 fastboot 进行调试。考虑到 Windows 在操作系统市场上占有超过 80%的市场份额，你使用它的机会甚至更高。这就是为什么有时很难在这个平台上正确使用高级调试工具的原因。我甚至在重新安装 adb 几次后，然后使用完整的 Android Studio SDK 工具时遇到了问题。

这就是 FWUL，一个用于 Android 调试的定制 Linux 发行版发挥作用的地方。它是由 XDA 知名开发商[standover x](https://forum.xda-developers.com/member.php?u=5545101)在两年多前发布的[。就在几周前，开发者宣布了发行版 3.0 的发布。以下是完整的变更日志:](https://www.xda-developers.com/forget-windows-use-linux-is-a-usb-bootable-distro-for-your-android-recovery-needs-xda-spotlight/)

*   FWUL 有了自己的[主页](https://fwul.binbash.rocks/)
*   你可能会注意到，我把所有代码都转移到了自己的 gitlab 服务器上。github.com 上的存储库将会保留，但会存档，只读，并且 **过期** 。
*   从发布之日起，新的 Manjaro Arch Linux 基础(意味着**所有 OS 包都是最新的**)
*   此版本的主要 FWUL 组件版本:
    *   内核-> **版本:4.19.13-1** (重大升级
    *   ADB 和 fastboot: android-tools -> **版本:9.0.0_r18-1** (重大升级)
    *   简单-亚行 GUI -> **版本:更新 6**
    *   SALT -> **版本:3.21-4**
    *   罗马-> **版本:1.0-1** (新增)
    *   TeamViewer(请求用户安装)-> **版本:14.0** (主要升级)
    *   bootimgtool-git -> **版本:20150607.g9ccd962-1**
    *   海姆达尔 git-> t0 版:1 . 4 . 2 . r7 . ga 2 cfda-1
    *   xfwm4 -> **版本:4.12.5-1**
    *   lightdm -> **版本:1:1.28.0-1**
    *   xorg-server -> **版本:1.20.3-1**
    *   virtualbox-guest-utils -> **版本:6.0.0-1** (重大升级)
    *   firefox -> **版本:64.0-1**
    *   hexchat -> **版本:2.14.2-1**
    *   testdisk-wip -> **版本:7.1-1**
    *   tmate -> **版本:2.2.1-2**
*   新:为小米设备增加了 [MiFlash](https://code.binbash.it:8443/Carbon-Fusion/build_fwul/issues/62) 阅读 [FWUL 包含的工具&安装人员](https://forum.xda-developers.com/showpost.php?p=70272684&postcount=3)中的简短摘要
*   新:最终[预配置 hexchat](https://code.binbash.it:8443/FWUL/build_fwul/issues/9)
*   新:增加了两个 [android 启动镜像](https://code.binbash.it:8443/FWUL/build_fwul/issues/8)操作工具
*   新:在欢迎界面增加了一个更加清晰的虚拟化警告
*   新:增加了一个用于 ROM 的提取工具-阅读 [FWUL 包含的工具&安装程序](https://forum.xda-developers.com/showpost.php?p=70272684&postcount=3)中的简短摘要
*   新:抛光壁纸。

[**在软件中阅读更多关于 FWUL 的内容&黑客 XDA 论坛**](https://forum.xda-developers.com/android/software-hacking/live-iso-adb-fastboot-driver-issues-t3526755)