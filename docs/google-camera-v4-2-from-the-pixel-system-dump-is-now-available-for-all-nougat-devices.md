# 来自 Pixel 系统转储的 Google Camera v4.2 现在可用于 Nexus (7.0+)设备

> 原文：<https://www.xda-developers.com/google-camera-v4-2-from-the-pixel-system-dump-is-now-available-for-all-nougat-devices/>

# 来自 Pixel 系统转储的 Google Camera v4.2 现在可用于 Nexus (7.0+)设备

我们已经将谷歌相机应用从 Pixel 系统转储移植到运行 Nougat 的 Nexus 设备上。包括曝光/聚焦和 UI 增强。

**(06:15PM CST)更新:我们了解到该端口仅适用于 ARM64 设备。对不起 Nexus 5 和 Nexus 6 的机主！**

* * *

随着 Pixel 手机即将向预购用户发货(或者如果你是 Telstra 的用户，你可能已经[拿到了设备](https://www.reddit.com/r/Android/comments/5789l8/telstra_australia_has_sent_out_the_pixel/))，我们不必等待太久，开发者就可以将新的 Pixel 功能移植到其他手机上。多亏了我们论坛上一些狡猾用户的工作，我们已经在其他手机上尝到了谷歌[“像素专属”助手](http://forum.xda-developers.com/android/software/guide-how-to-enable-google-assistant-t3477879)的味道。由于 [@LlabTooFer 的 Pixel/Pixel XL 系统映像](http://www.xda-developers.com/llabtoofer-leaks-system-images-for-pixel-and-pixel-xl/)的转储，许多其他将与新 Pixel 设备一起推出的更新应用程序已经被泄露。一个尚未移植到 Nougat 设备的应用程序是更新的谷歌相机应用程序，版本 4.2。这是因为该应用要求设备运行最新版本的 Android Nougat，即 7.1 版，Pixel 随附了该版本，其他 Nexus 设备将在不久的将来收到该版本。但是如果你不想等着试用最新版本的谷歌相机应用程序，那么我们已经将该应用程序移植到 Android 7.0 设备上。到目前为止，我们已经确认这可以在谷歌 Nexus 5X 和谷歌 Nexus 6P 上运行。

[**下载谷歌相机 4.2 版**](https://labs.xda-developers.com/store/app/com.google.android.GoogleCameraMOD)

请记住，由于这是谷歌相机应用程序的修改版本，它不会安装在您现有的相机应用程序上。此外，谷歌相机应用程序仍然无法在非 Nexus 设备上运行，所以不要试图在运行非官方牛轧糖的设备上安装它。最后，这个 mod 不需要您以任何方式更改 build.prop 文件，这可能会导致 Pixel 系统转储中的其他应用程序中断。除了修改 APK 以强制应用程序在 7.0 上运行，我们没有以任何其他方式更改相机应用程序。我们已经向 [VirusTotal](https://www.virustotal.com/en/file/401f647d28eaa5b927a11ba3ad32aae56bb2fc465f5a9bfb8ebb612e013e2e95/analysis/1476379692/) 和 [NVISO 的 APKScan](https://apkscan.nviso.be/report/show/c912086b7982ba3a76df0a198142906b) 上传了 APK 的安全扫描报告，以向您保证该应用是干净的，因为我们不得不删除我们论坛上关于谷歌摄像头 4.2 端口的一个帖子，因为用户担心该应用是恶意的。现在我们已经解决了这个问题，下面是这个应用的一些截图:

正如你所看到的，谷歌相机应用程序的所有最新增强功能似乎都存在。最重要的是，你已经有了**长按锁定曝光/对焦、** **手动曝光、**和新的 **UI 网格选项。**旋转应用程序，让我们知道您的想法！