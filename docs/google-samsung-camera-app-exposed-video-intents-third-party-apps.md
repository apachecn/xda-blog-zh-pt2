# 谷歌相机和三星相机应用程序将相机和视频意图暴露给第三方应用程序

> 原文：<https://www.xda-developers.com/google-samsung-camera-app-exposed-video-intents-third-party-apps/>

与 iOS 相比，Android 为应用程序提供了许多相互交互的方式，使开发人员能够构建一些我们期望并喜欢的更常见的 Android 功能。这要归功于 Android 的意图系统，它允许任何应用程序发送任何想要的意图，并允许接收应用程序以创造性的方式处理这些意图。但事实证明，谷歌相机应用程序和三星相机应用程序已将其相机和视频意图暴露给第三方应用程序，这为绕过关键权限的潜在滥用敞开了大门，正如安全研究人员在 *[Checkmarx](https://www.checkmarx.com/blog/how-attackers-could-hijack-your-android-camera)* 所展示的那样。

Android 上的 [Intents 被描述为“*消息传递对象，促进应用组件*之间的通信”，简单来说就是 Intent 允许应用互相发送数据。例如，当你试图从文件管理器中向 WhatsApp 这样的应用程序共享文件时，你是在向 WhatsApp 发送将文件作为数据的意图。任何应用程序都可以发送它想要的任何意图，并且由接收应用程序通过在其清单文件中定义相同的意图来决定它想要监听哪个意图。接收应用程序还决定如何对这些意图做出反应。此外，接收应用程序还可以确保仅当从特定白名单应用程序(显式意图)或持有特定权限的应用程序(受保护的意图)发送意图时，才执行操作。事实证明，上述相机应用程序中未受保护的意图可能会被坏人利用。](https://developer.android.com/guide/components/intents-filters)

*Checkmarx* 发现谷歌相机应用程序和三星相机应用程序有未受保护的意图来触发像拍照和录制视频这样的动作。在这种情况下，未受保护的意图意味着接收应用程序不检查发送意图的应用程序是否具有进行动作本身的必要权限——在这种情况下是*Android . permission . camera*。相机活动*com . Google . Android . Google camera/com . Android . camera . camera activity*也是一个导出的活动，这意味着其他应用程序可以调用它。因此，未受保护的意图和导出的活动会导致权限绕过漏洞。

因此，可以构建恶意应用程序，该应用程序不具有相机权限，但仍然能够通过这些相机应用程序路由某些相机功能，并利用其未受保护的意图和导出的活动来操作这些功能。

作为概念验证， *Checkmarx* 创建了一个虚拟的天气应用程序，它没有相机权限，但它有一个存储权限，对于天气应用程序来说，这个权限没有出现问题。在没有相机许可的情况下，天气应用程序能够触发谷歌相机和三星相机拍照和录制视频。存储权限在访问这个以及保存在/DCIM 的所有其他照片和视频时起作用——它不需要用于点击照片和录制视频的操作。

在最坏的情况下，这个漏洞可以被用来做一些事情，如在通话中记录用户的视频，如果相机应用程序中启用了位置标记，则从照片的 GPS 元数据中抓取位置信息(并有效地获取手机的当前位置)，等等。

诚然，用户界面确实会显示相机正在被访问，但这也可以通过利用接近传感器来测量手机显示屏何时关闭来解决，从而避开用户的注意。一个恶意的应用程序还可以静音手机的音量，并在拍照或录制视频时有效地静音设备。

Checkmarx 声称，这个名为 CVE-2019-2234 的漏洞也存在于其他智能手机供应商的相机应用程序中。但研究人员没有指出除了谷歌和三星之外，哪些厂商和设备受到了影响。如果其他相机应用程序已导出活动来启动照片捕捉和视频录制，并且具有不检查调用应用程序可用权限的未受保护的意图，它们也会受到影响。

由于这不是 Android 平台或 Linux 内核中的漏洞，因此它不能作为 [Android 安全公告](https://www.xda-developers.com/november-2019-android-security-patches/)的一部分包含和发布。2019 年 7 月，谷歌相机应用程序通过应用程序更新修复了该漏洞，三星相机应用程序也修复了该漏洞，尽管没有关于此更新何时推出的具体信息。

在未打补丁的 Google Camera 版本上，您可以通过运行以下 ADB 命令来强制通过此漏洞拍摄视频:

```
 adb shell am start-activity -n
com.google.android.GoogleCamera/com.android.camera.CameraActivity 
extra_turn_screen_on true -a android.media.action.VIDEO_CAMERA --ez
android.intent.extra.USE_FRONT_CAMERA true 
```

如果使用 Google Camera 或 Samsung Camera，请确保在设备上更新到最新的相机应用程序版本，并通过 Play Store 或 OTA(视情况而定)进行推广。