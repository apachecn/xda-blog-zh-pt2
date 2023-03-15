# 如何在运行 GSIs 的高通设备上启用 VoLTE

> 原文：<https://www.xda-developers.com/how-to-enable-volte-qualcomm-devices-running-generic-system-images-gsis/>

# 如何在运行通用系统映像(GSI)的高通设备上启用 VoLTE

VoLTE-Fix mod 可用于恢复运行通用系统映像的大多数 Project Treble 兼容高通设备对 LTE 语音的支持。

谷歌的[项目 Treble](https://forum.xda-developers.com/project-treble) 无疑是 Android OS 自诞生以来最大的一次重组。山景城巨人完全修改了 Android 操作系统框架和供应商驱动程序 Linux 内核相互交互的方式，以减少 Android 平台版本碎片。最重要的是，Project Treble 还使得[在任何支持的设备上启动 AOSP 通用系统镜像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)成为可能。XDA 的开发者社区长期以来一直在[发布自己的定制 GSI](https://www.xda-developers.com/phh-custom-android-10-gsi-adds-better-support-razer-phone-new-my-device-settings/)和额外的设备特定补丁，但是在这些版本中有一些已知的限制。例如，高级蜂窝服务，如 LTE 语音(VoLTE)和 Wi-Fi 通话(VoWiFi)通常在 GSIs 上中断。

与传统的电路交换式网络不同，VoLTE 和 VoWiFi 由 IP 多媒体子系统(IMS)提供支持。一个典型的带有高通调制解调器的 Android 设备带有一个特殊的特权应用程序，作为无线电接口层(RIL)和这些 IMS 服务之间的联系。理论上，在安装 GSIs 以使 VoLTE 工作之后，可以从库存固件中提取适当的 IMS APK 以及必要的共享对象，并将其推送到各自的目的地。这正是 **VoLTE-Fix** mod 的用武之地。

由 Khushraj Rathod 开发的这款 mod 在本质上是相当通用的。你可以安装它从一个自定义的恢复像 TWRP 在一个 flashable ZIP 文件的形式或选择安装程序外壳脚本来做你的工作。开发人员还描述了一个手动安装过程，在安装 GSI 后，您需要手动移动文件并设置所需的属性值。如果你想知道的话，请注意 IMS APK 是闭源的。

**VoLTE-Fix 在运行 GSIs 的高通设备上启用 VoLTE:[下载](https://github.com/KhushrajRathod/VoLTE-Fix/releases) || [来源](https://github.com/KhushrajRathod/VoLTE-Fix/)**

请记住，某些原始设备制造商(如三星)不喜欢遵循多媒体电话服务(MMTel)标准。他们的 IMS 实现是完全专有的，因此你不能在使用这种模式的设备上启用 VoLTE。