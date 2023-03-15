# 根任何 HTC 设备与 HTC 快速根

> 原文：<https://www.xda-developers.com/root-any-htc-device-with-htc-quick-root/>

不久前，我们给你带来了一个通用方法[的消息，它可以根化几乎任何 ICS 设备](http://www.xda-developers.com/android/nearly-universal-root-methods-for-most-ics-phones/)。这是一个很好的指南，许多用户仍在使用它，但这并不意味着它是目前唯一的通用根方法。最近发布了另一个多设备根方法，但这次是针对任何 HTC 设备的。

这个工具是由 XDA 公认的开发者 lyriquidperfection 创建的，它不仅仅是生根。它根据你的手机是开机还是关机给出选项。对于 S-On 设备，它提供了一个已知的通用漏洞，让手机植根于 Busybox 和 [SuperSU](http://www.xda-developers.com/android/help-design-the-new-supersu-icon/) 。对于 S-Off 设备，它提供了使用不安全的 *boot.img* 进行 root 的选项。完整的功能列表包括:

> Root 用户使用不安全的“Boot.img”(仅限 S-OFF)或通用漏洞。(开关打开/关闭)
> 
> 即使你的设备处于开机状态，也可以在开机后刷新“HBOOT”图像！
> 
> 备份和刷新后，验证“HBOOT”映像的 MD5 校验和。
> 
> 通过将“adbd”二进制文件修补为不安全来取消设备的根。
> 
> 清除电池状态和 Dalvik 缓存的根工具。
> 
> 根后重启设备到任何模式。
> 
> 独立执行重启命令。
> 
> 彻底的错误检查和稳定的 ADB 框架实施。
> 
> 包括 BusyBox v1.20.2 和 SuperSU v0.96

有些事情需要注意。 *boot.img* 和 HBoot 镜像刷新要求用户获得他们自己的文件，因为这些文件是特定于设备的，不包括在内。用户也要求功能，所以这个工具可能会得到更大的久而久之。要了解更多，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=1870652)。