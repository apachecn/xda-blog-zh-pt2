# 小米红米 Note 7 支持 Camera2 API，因此谷歌相机端口现在可以在没有解锁的引导加载器的情况下工作

> 原文：<https://www.xda-developers.com/redmi-note-7-camera2-api-google-camera/>

谷歌摄像头端口在我们的论坛上变得非常受欢迎，因为许多人认为它们是在[各种设备](https://www.xda-developers.com/google-camera-hdr-xiaomi-redmi-note-3/)上[大幅提高图像质量](https://www.xda-developers.com/google-camera-hdr-ported/)的简单方法。通过移植的谷歌相机应用程序，你可以在非谷歌设备上使用谷歌卓越的 HDR+优化以及他们的肖像模式。然而，Google Camera 需要 Camera2 API 支持才能工作，这使得这个本来很容易的修复需要更多的步骤才能正常工作。

[**谷歌相机 Mods XDA 论坛**](https://forum.xda-developers.com/apps/google-camera-mods)

过去大多数小米设备都缺乏开箱即用的 Camera2 API 支持。为了启用 API，大多数小米设备要么需要 root 来修改他们的 build.prop，要么只需要一个解锁的引导加载程序来运行 fastboot 命令。一些最近的设备，如 POCO F1、小米 Mi 8 和小米 Mi Mix 2S，都有小米默认启用的 [Camera2 API 支持，这样就不需要解锁引导加载程序、根设备或安装任何 Magisk 模块来使用谷歌相机。一旦谷歌相机端口可用，最终用户可以简单地安装应用程序，享受图像质量的改善。](https://www.xda-developers.com/google-camera-port-xiaomi-poco-f1-xiaomi-mi-8-se-ee-xiaomi-mi-mix-2s/)

令人欣慰的是，似乎与 Android Pie 一起发布的较新的小米设备默认启用了 Camera2 API，以符合 Android Pie 的 CTS 要求。[小米新发布的](https://www.reddit.com/r/Xiaomi/comments/aj064z/redmi_note_7_lavender_has_hal3api2_enabled_by/)红米 Note 7(设备代号:lavender)就是这种情况，在设备的[固件中可以看到:](https://github.com/TadiT7/xiaomi_lavender_dump/blob/lavender-user-9-PKQ1.180904.001-V10.2.3.0.PFGCNXM-release-keys/system/system/build.prop)

```
persist.vendor.camera.HAL3.enabled=1
```

这意味着红米 Note 7 上默认启用 Camera2 API。一旦一个合适的谷歌摄像头端口通过感兴趣的开发人员的努力工作而变得可用，用户就可以简单地安装应用程序，根据需要微调设置，并享受改进。

虽然小米设备(以及 Redmi 子品牌的设备)不会因为启动加载器解锁而失去保修，但这仍然是许多人会避免在他们的设备上采取的步骤。现在，你不需要解锁引导加载程序或 root 红米 Note 7 来实现这一特定目的。

* * *

[**故事 Via:/r/小米**](https://www.reddit.com/r/Xiaomi/comments/aj064z/redmi_note_7_lavender_has_hal3api2_enabled_by/)