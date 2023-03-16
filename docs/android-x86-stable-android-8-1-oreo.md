# Android-x86 稳定的 Android 8.1 Oreo 映像现已推出

> 原文：<https://www.xda-developers.com/android-x86-stable-android-8-1-oreo/>

# Android-x86 稳定的 Android 8.1 Oreo 映像现已推出

自从 6 月份第一个 Android 8.1 Oreo 发布以来，Android-x86 团队已经发布了第二个 RC 版本，现在他们已经为稳定发布做好了准备。

早在 6 月份，[我们曾报道过 Android-x86 项目](https://www.xda-developers.com/android-x86-android-8-1-oreo/)发布了第一个面向 PC 的 Android 8.1 Oreo 版本。对于那些不知道的人来说，Android-x86 是一个旨在让 Android 在 Intel 和 AMD x86 PCs 上工作的项目。自从 6 月份第一个 Android Oreo 发布以来，他们发布了第二个 RC 版本，现在他们已经准备好稳定发布了。

该团队增加或展示了许多让 Android 在 PC 上运行得更好的功能，比如自由窗口模式。他们在英特尔、AMD 和 NVIDIA 显卡上使用 Linux 内核 4.19.15、OpenGL ES 3.0 硬件加速，也包括 Vulkan 支持，尽管它仍处于试验阶段。也可以在启用 UEFI 安全引导的情况下运行 Android-x86。以下是主要功能的完整列表；

**主要特征**

*   使用最新的 LTS 内核 4.19.15 支持 64 位和 32 位内核和用户空间。
*   Mesa 18.3.1 支持 Intel、AMD、Nvidia、QEMU(virgl)的 OpenGL ES 3.x 硬件加速。
*   通过 [SwiftShader](https://swiftshader.googlesource.com/SwiftShader) 支持 OpenGL ES 2.0，用于在不支持的 GPU 设备上进行软件渲染。
*   在采用英特尔高清& G45 显卡家族的设备上支持**硬件加速编解码器**。
*   支持从 UEFI 安全引导并安装到 UEFI 磁盘。
*   一个基于文本的 GUI 安装程序。
*   向 grb-EFI 添加主题支持。
*   支持多点触控、音频、Wifi、蓝牙、传感器、摄像头和以太网(仅限 DHCP)。
*   自动安装外部 usb 驱动器和 SD 卡。
*   添加[任务栏](https://github.com/farmerbb/Taskbar)作为替代启动器，将开始菜单和最近应用托盘放在屏幕顶部，并支持[自由窗口模式](https://www.youtube.com/watch?v=3D49hDqLxB4)。
*   在没有已知传感器的设备上启用 ForceDefaultOrientation。肖像应用可以在横向设备中运行，而无需旋转屏幕。
*   通过本机桥接机制支持 arm arch 应用程序。(设置-> Android-x86 选项)
*   支持从非官方版本升级。
*   为新的英特尔和 AMD GPUs 增加实验性的 Vulkan 支持。(通过高级选项启动- > Vulkan 支持)
*   对虚拟机的鼠标集成支持，包括 VirtualBox、QEMU、VMware 和 Hyper-V。

此稳定版本可以作为可引导 CD/USB 映像在 64 位和 32 位 x86 系统上运行。请访问下面的源代码链接，阅读完整的发行说明并找到预构建的映像。

* * *

[**来源:安卓-x86**](http://www.android-x86.org/releases/releasenote-8-1-r1) [**Via:安卓警察**](https://www.androidpolice.com/2019/01/16/stable-version-of-android-x86-8-1-oreo-now-available/)