# Android-x86 项目发布 Android 9 Pie RC，而 Bliss OS 发布 Android 10 alpha build for PCs

> 原文：<https://www.xda-developers.com/android-x86-project-releases-android-9-pie-rc-while-bliss-os-releases-android-10-alpha-build/>

# Android-x86 项目发布 Android 9 Pie RC，而 Bliss OS 发布 Android 10 alpha build for PCs

Android-x86 项目现在已经发布了第一个稳定的基于 Pie 的 PC 版本，而 Bliss OS 已经发布了基于 Android 10 的 alpha 版本。

今年 1 月早些时候，Android-x86 项目[发布了 Android 8.1 Oreo 的第一个稳定版本](https://www.xda-developers.com/android-x86-stable-android-8-1-oreo/)。对于不知道的人来说，Android-x86 是一个开源社区项目，旨在将 Android 带到运行 x86 或 x86-64 架构的 PC 上。在 Oreo 版本中，该团队添加了大量新功能，如自由窗口模式，以使 Android 在 PC 上运行得更好。从那以后，该团队一直在努力开发 Android 9 Pie 版本，现在已经推出了第一个 Android 9 Pie 候选版本(RC ),可以在虚拟机或桌面上运行。

据 Android Police 报道，该版本带来了谷歌在 Android 9 Pie 中引入的所有功能，以及对桌面硬件的扩展兼容性。虽然这个版本提供了一个接近传统 Android 的界面，但它确实包含了更适合鼠标和键盘等传统输入设备的附加功能。这些新功能包括一个带有开始菜单的可选任务栏和一个可以用作替代启动器的最近应用托盘。以下是主要特性的完整列表:

*   使用最新的 LTS 内核 4.19.80 支持 64 位和 32 位内核和用户空间。
*   Mesa 19.0.8 支持 Intel、AMD、Nvidia、QEMU(virgl)的 OpenGL ES 3.x 硬件加速。
*   通过 SwiftShader 支持 OpenGL ES 3.0，用于在不支持的 GPU 设备上进行软件渲染。
*   在采用英特尔高清和 G45 显卡家族的设备上支持硬件加速编解码器。
*   支持从 UEFI 安全引导并安装到 UEFI 磁盘。
*   一个基于文本的 GUI 安装程序。
*   向 grb-EFI 添加主题支持。
*   支持多点触控、音频、Wifi、蓝牙、传感器、摄像头和以太网(仅限 DHCP)。
*   自动安装外部 usb 驱动器和 SD 卡。
*   添加任务栏作为替代启动器，将开始菜单和最近应用托盘放在屏幕顶部，并支持自由窗口模式。
*   在没有已知传感器的设备上启用 ForceDefaultOrientation。肖像应用可以在横向设备中运行，而无需旋转屏幕。
*   通过本机桥接机制支持 arm arch 应用程序。(设置-> Android-x86 选项)
*   支持从非官方版本升级。
*   为较新的英特尔和 AMD GPUs 添加实验性 Vulkan 支持。(通过高级选项-> Vulkan 支持启动)
*   通过以太网模拟 WiFi 适配器，增加 app 兼容性。
*   对虚拟机的鼠标集成支持，包括 VirtualBox、QEMU、VMware 和 Hyper-V。

如果你想自己测试最新的 Android-x86 Pie RC 版本，你可以点击下面的链接获取指导。你也可以从 [Fosshub](https://www.fosshub.com/Android-x86.html) 或者 [OSDN](https://osdn.net/rel/android-x86/Release%209.0) 那里获得预建的图像。但是，在您将它安装到您的系统之前，请务必查看下面的已知问题列表:

*   Google Play 服务有时可能会在 32 位图像上崩溃。
*   挂起和恢复在某些设备上不起作用。
*   Nvidia GPU (nouveau)有时可能会挂起。
*   VMware 的 3D 支持已中断。(只有非加速模式有效)
*   如果启用了 Vulkan，则拍照不起作用。

如果你对在你的电脑上运行 Android 9 不感兴趣，而你更喜欢运行 Android 10，那么你会很高兴知道 Bliss OS 已经发布了一个适用于电脑的 Android 10 alpha 版本。Bliss OS 本质上是 Android-x86 的一个分支，它提供了额外的功能，如任务栏集成，以便在 PC 上获得更好的用户体验。然而，值得注意的是，Bliss OS 的最新版本是实验性的，并不打算用作日常驱动程序。尽管如此，对于那些希望在个人电脑上运行 Android 10 的人来说，这是一个有趣的项目。你可以通过访问我们下面链接的论坛上的开发线程来下载最新的基于 Android 10 的 Bliss OS 12 版本。

**[极乐 OS 12 XDA 论坛](https://forum.xda-developers.com/android/software/bliss-os-x86-pc-s-12-x-development-t4004419)**

* * *

**来源:[Android-x86](https://www.android-x86.org/releases/releasenote-9-0-rc1.html)**

**Via: [安卓警察](https://www.androidpolice.com/2019/11/19/android-x86-project-9-0-pie-release-candidate/)**