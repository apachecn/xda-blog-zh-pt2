# 树莓 Pi 4 和 3 获得基于 Android 10 的非官方 LineageOS 17.1

> 原文：<https://www.xda-developers.com/developer-ports-lineageos-17-1-based-on-android-10-to-the-raspberry-pi-4-b-3-b-and-3-b/>

自从 2012 年发布以来，Raspberry Pi 已经成为单板计算机(SBC)的代名词。这款信用卡大小的计算机的最新版本 [Raspberry Pi 4](https://www.xda-developers.com/raspberry-pi-4-upgraded-cpu-4gb-of-ram-dual-4k-displays/) ，配备了[高达 8GB 的内存](https://www.xda-developers.com/raspberry-pi-4-8gb-ram/)和 ARM64 支持。Raspberry Pi Foundation 提供 Raspberry Pi OS(以前称为 Raspbian)作为默认操作系统，同时官方也支持 Windows 10 IoT Core 等各种专注于物联网的发行版。现在，XDA 资深成员 [KonstaT](https://forum.xda-developers.com/member.php?u=7223862) 已经能够以 LineageOS 17.1 的形式为树莓 Pi 4 (B)和树莓 Pi 3 (B/B+)编译完整的 Android 10 版本。

**[树莓派 XDA 论坛](https://forum.xda-developers.com/raspberry-pi)**

Peter Yoon，在 [android-rpi](https://github.com/android-rpi) 社区中以 [peyo-hd](https://github.com/peyo-hd) 闻名，和其他几个贡献者最初开始努力将 android 移植到 Raspberry Pi 板上。为了确保稳定性， [KonstaT](https://forum.xda-developers.com/member.php?u=7223862) 在构建 LineageOS 时进一步从 Android Things 固件中提取了一些片段。最重要的是， [Eric Anholt](https://github.com/anholt) 为 Broadcom VideoCore 4 GPU(存在于 Raspberry Pi 中)提供的开源 Linux 图形驱动程序堆栈使整个移植过程变得不那么麻烦。

工作特征的完整列表包括以下内容:

*   音频(HDMI、3.5 毫米插孔、USB 麦克风、蓝牙扬声器/耳机等)
*   音频 DAC(使用 PCM512x DACs，例如 Hifiberry DAC+)
*   蓝牙
*   摄像头(使用官方 Pi 摄像头模块和带有 SwiftShader 软件渲染器的 UVC USB 网络摄像头)
*   GPIO
*   GPS(使用外部 USB 模块，如 U-Blox 7)
*   以太网
*   硬件加速显卡(V3D/VC4)
*   HDMI 显示器
*   I2C
*   红外遥控器(使用外部 GPIO 红外模块，如 TSOP4838)
*   RTC(使用外部 GPIO I2C 模块，如 DS3231)
*   串行控制台(使用外部 GPIO 串行控制台适配器，例如 PL2303)
*   精力
*   触摸屏/多点触控(使用官方 7 英寸显示屏和 SwiftShader 软件渲染器)
*   USB(鼠标、键盘、存储器等)
*   无线保真
*   无线网络共享

与典型的 Android 智能手机不同， [*bootloader 解锁*](https://www.xda-developers.com/tag/bootloader-unlock/) 的概念不适用于 Pi。你需要下载具体型号的 LineageOS 镜像文件，写入 microSD 卡(> =8GB)，将卡插入 Pi，开机即可。由于您不需要在开始时定制恢复来刷新 ZIP 文件，因此没有单独的恢复来下载，尽管 TWRP 是作为预配置的恢复环境提供的。

**为树莓 Pi 下载 linegeos 17.1(Android 10):[Pi 4b](https://forum.xda-developers.com/raspberry-pi/orig-development/dev-lineageos-17-1-android-10-raspberry-t4139059)| |[Pi 3b/B+](https://forum.xda-developers.com/raspberry-pi/orig-development/dev-lineageos-17-1-android-10-raspberry-t4139051)**

Raspberry Pi 4/3 上的 LineageOS 运行在 32 位模式下，因此你必须选择 Google apps 包的 ARM 变体。此外，上述版本要求 HDMI 显示器使用扩展显示识别数据(EDID)来报告支持的分辨率。如果您的显示器不兼容，并且在启动屏幕后看不到 Android 启动动画，那么您可能需要手动更改`/system/build.prop`中`debug.drm.mode.force`属性的值。