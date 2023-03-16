# 如何在不禁用 OTA 更新的情况下在小米米 A1 上启用 Camera2 API

> 原文：<https://www.xda-developers.com/enable-camera2-api-xiaomi-mi-a1/>

# 如何在不禁用 OTA 更新的情况下在小米米 A1 上启用 Camera2 API

想在小米 Mi A1 上启用 Camera2 API 以便使用谷歌相机 HDR+端口吗？这里有一个指南，告诉你如何做到这一点，而不会强迫你在更好的相机和能够拍摄 OTA 之间进行选择！

像 Mi A1 这样的多个小米设备都支持 Camera2 API，但默认情况下它是不启用的。这很遗憾，因为这意味着我们论坛上流传的各种[谷歌摄像头端口](https://www.xda-developers.com/tag/google-camera/)将无法工作。我们已经展示了谷歌相机 HDR+模块如何[极大地提高小米手机](https://www.xda-developers.com/google-camera-hdr-xiaomi-redmi-note-3/)的图片质量，再加上这些端口带来的所有其他简洁的功能，如人像模式、AR 贴纸等，人们被这些相机模块吸引也就不足为奇了。

在小米手机上启用 Camera2 API 是可能的，但是，这个过程需要您启动您的设备并对系统属性进行一些更改，以便启用 API。对像 build.prop 这样的系统文件进行任何修改通常意味着你不能再接受 OTA 更新，但谢天谢地有一种方法可以在不修改任何系统文件的情况下**启用 Camera2。**

这份来自 XDA 知名开发商 [flex1911](https://forum.xda-developers.com/member.php?u=5120185) 的小米 Mi A1 分步指南将引导您解锁您的引导加载程序并启动设备，以便您可以通过 setprop 命令启用 Camera2 API，但一旦更改为启用 Camera2，您可以完全卸载 Magisk 并重新锁定引导加载程序，以便您可以再次接受官方 OTA。

这实际上是对 build.prop 进行修改的一种相当常见的方法，而不需要让您的设备永久解锁/启动(从而防止您使用 OTA)，但对于新手来说，有这样一个详细的指南是很好的。如果你想享受小米 A1 上的谷歌摄像头端口，而不牺牲接受 OTA 更新的能力，那么请查看下面的源代码链接中的指南。

[**如何在小米米 A1 上启用 camera 2 API**](https://forum.xda-developers.com/mi-a1/how-to/guide-how-to-enable-hal3-camera2api-t3747073)