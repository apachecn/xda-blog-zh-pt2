# 索尼 Xperia 10 II 获得官方支持引导加载程序解锁

> 原文：<https://www.xda-developers.com/sony-xperia-10-ii-gets-official-support-for-bootloader-unlocking/>

# 索尼 Xperia 10 II 获得官方支持引导加载程序解锁

索尼 Xperia 10 II 是索尼最新获得官方 bootloader 解锁支持的智能手机。继续阅读，了解更多信息！

索尼 Xperia 10 II(读作 Xperia 10“Mark 2”)是日本 OEM 厂商最新的中端智能手机。这款智能手机提供了索尼标志性的 21:9 宽高比和三后置摄像头设置，具有专用的超广角和长焦传感器，但有点过时的[高通骁龙 665](https://www.xda-developers.com/qualcomm-snapdragon-665-snapdragon-730g/) SoC 可能会让潜在买家失望。索尼已经[公布了与这款手机对应的内核源代码](https://www.xda-developers.com/sony-xperia-1-10-ii-upload-kernel-source-code/)，并且[将其添加到他们的*开放设备计划*](https://www.xda-developers.com/sony-xperia-10-ii-added-open-devices-program/) 中，以促进第三方开发。现在，原始设备制造商正在增加官方支持解锁索尼 Xperia 10 II 的引导加载程序。

**[索尼 Xperia 10 II XDA 论坛](https://forum.xda-developers.com/sony-xperia-10-ii)**

索尼通过*开放设备计划*提供 AOSP 构建指南，其中有经验的开发人员可以利用设备树作为基础，将 LineageOS 等流行的定制 rom 移植到 Xperia 10 II。如果没有解锁的引导程序，你就无法启动定制的 ROM 甚至是 [GSI](https://www.xda-developers.com/tag/generic-systemimage/) ，这意味着官方引导程序解锁支持的到来应该有助于 kickstart 设备上真正的售后开发。

像往常一样，你可以前往[索尼的在线引导加载程序解锁门户](https://developer.sony.com/develop/open-devices/get-started/unlock-bootloader/)和[按照要求的步骤](https://www.xda-developers.com/sonys-open-device-program-releases-an-updated-guide-for-unlocking-bootloader-of-the-xperia-devices/)获得引导加载程序解锁。如果你找不到确切的型号，不用担心——索尼[错误地](https://forum.xda-developers.com/sony-xperia-10-ii/how-to/bootloader-unlockable-t4137491)将其列为“Xperia X10 II”。

值得一提的是，解锁索尼 Xperia 设备的引导加载程序会清除包含 DRM 密钥的 trim area (TA)分区。没有这些独特的按键，你无法访问索尼专有的音频和视频功能，但至少[索尼不再破坏相机的功能](https://www.xda-developers.com/sony-xperia-android-pie-unlock-bootloader-drm-fix-camera/)。另一方面，Xperia 10 II 的一些运营商版本可能不符合 bootloader 解锁的要求。您可以通过在默认拨号器应用程序中拨打`*#*#7378423#*#*`并检查服务信息>配置>寻根状态下的资格，从服务菜单中验证这一点。