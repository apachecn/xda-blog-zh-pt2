# 基于 Android 8.1 Oreo 的 Android-x86 现已适用于您的电脑

> 原文：<https://www.xda-developers.com/android-x86-android-8-1-oreo/>

# 基于 Android 8.1 Oreo 的 Android-x86 现已适用于您的电脑

Android-x86 现在已经收到了一个更新，将该项目提升到 8.1-rc1 版本，为用户带来了 Android 8.1 Oreo。

Android x86 是一个非官方的尝试，旨在将谷歌的 Android 操作系统从智能手机移植到个人电脑上。尽管有很多方法可以通过笔记本和 PC 获得 Android 体验，但 Android-x86 没有任何形式的模拟器垃圾邮件和/或广告潜入本机体验。

该项目是完全开源的，并被设计为在具有“x86”架构的计算机上运行，这基本上是采用英特尔芯片的设备。Android-x86 现在已经收到了一个更新，将该项目提升到 8.1-rc1 版本，为用户带来了 Android 8.1 Oreo。基于最新的 Android 8.1 Oreo MR1 版本(8.1.0_r33)，8.1-rc1 包括以下功能:

*   增加了对 64 位和 32 位内核以及用户空间的支持。
*   该版本通过 Mesa 18.1.2 支持针对 Intel/AMD/Nvidia、VMWare 和 QEMU(virgl)的 OpenGL ES 3.x 硬件加速。
*   对于不支持的 GPU 设备，OpenGL ES 2.0 现在可以通过 SwiftShader 进行软件渲染。
*   对于采用英特尔核芯显卡和 G45 显卡家族的设备，现在支持硬件加速编解码器。
*   添加了基于文本的 GUI 安装程序。
*   现在支持从 UEFI 安全引导并安装到 UEFI 磁盘。
*   现在也增加了对 grb-EFI 的主题支持。
*   还支持多点触控、音频、WiFi、蓝牙、传感器、摄像头和以太网(仅限 DHCP)。
*   此版本还增加了外部 USB 驱动器和 SD 卡支持。
*   任务栏，一个可选的启动器(将开始菜单和最近的应用程序托盘放在用户屏幕的顶部)已经被添加到该版本中。
*   对于缺少已知传感器的设备，ForceDefaultOrientation 已启用，这使得纵向应用程序可以在横向设备上运行，而无需用户旋转屏幕。
*   ARM Arch 应用程序现在通过本机桥接机制得到支持。该选项位于设置中的“Android-x86 选项”菜单。

尽管此版本相当稳定，但有两个已知问题:

*   在 32 位图像上，Google Play 服务有时可能会崩溃。
*   对于某些设备，“暂停”和“恢复”功能不起作用。

点击下面的链接阅读完整的发行说明，并找到预建的图像。

* * *

[**来源:Android-x86.org**](http://www.android-x86.org/releases/releasenote-8-1-rc1)