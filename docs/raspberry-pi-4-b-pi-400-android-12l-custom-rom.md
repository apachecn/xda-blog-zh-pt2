# 开发者将 Android 12L 移植到 Raspberry Pi 4

> 原文：<https://www.xda-developers.com/raspberry-pi-4-b-pi-400-android-12l-custom-rom/>

本月初，谷歌发布了 Android 12L 的稳定版。对于大多数 Pixel 用户来说，你需要通过 OTA 下载最新版本，然后享受新版本。由于这里是 XDA，一些有创意的修改者已经让新的 Android 版本在更非传统的设备上运行，比如 Nexus 7 2013 。现在，XDA 资深成员 [KonstaT](https://forum.xda-developers.com/m/konstat.7223862/) 已经为 Raspberry Pi 4 Model B 提供了一个成熟的 Android 12L 端口

在过去，同一个开发者已经得到了在 Pi 上工作的 Android 版本，但这是我们看到的第一个 Android 12L 版本，特别是以非官方的 LineageOS 19.1 ROM 的形式建立的。该版本还与 Raspberry Pi 400 兼容，这是一款内置在紧凑型键盘中的基于 ARM 的 PC。

树莓 Pi 上的 Android 12L 大部分都工作正常，尽管有一些 bug，这是应该预料到的。例如，硬件加速的视频解码和编码还没有准备好。官方的 Raspberry Pi 相机模块目前无法与内置摄像机正常工作，一些第三方相机应用程序也无法正常工作。最后但同样重要的是，SELinux 被设置为 permissive。

虽然这对大多数树莓 Pi 爱好者来说不太有用，但这可能是一种摆弄 Android 12L 的好方法——如果你是一个修补爱好者，并且有树莓 Pi 4 Model B 或树莓 Pi 400。如果您有兴趣尝试一下，开发人员可以在开发线程上找到说明和下载链接。

**[非官方 LineageOS 19.1 基于 Android 12L 为树莓 Pi 4 型号 B 和 Pi 400](https://forum.xda-developers.com/t/4356891/)**

就安装而言，ROM 支持从普通的 microSD 卡启动。也可以在刷新兼容的 EEPROM 映像后，从外部 USB 存储介质启动。你可以选择去谷歌化的体验，或者[下载一个合适的 GApps 包](https://www.xda-developers.com/download-google-apps-gapps/)。