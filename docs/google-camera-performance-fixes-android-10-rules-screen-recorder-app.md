# 谷歌摄像头性能修复，Android 10 规则，和屏幕录制应用程序透露

> 原文：<https://www.xda-developers.com/google-camera-performance-fixes-android-10-rules-screen-recorder-app/>

几天前，我们从 Pixel 4 上拿到了[新的谷歌相机 7.0 APK](https://www.xda-developers.com/google-camera-7-0-google-pixel-4-leak-hands-on/) 。我们展示了用户界面，也是第一个[展示我们在 APK 发现的像素 4 相机功能](https://www.xda-developers.com/google-pixel-4-camera-features-google-camera-leak/)，以及神秘再现的“针鱼”2019 像素。在检查 APK 时，我们看到了一些关于谷歌相机应用程序启动缓慢的字符串，这表明谷歌正在努力解决应用程序启动性能的任何问题。我们没有想太多，因为这听起来像标准的开发工作，但 Philip Chang (@ [m4au312](https://twitter.com/m4au312) )给我们发了一个有趣的提示，指向 Google 相册上的一个指导页面。[页面](https://photos.google.com/share/AF1QipMtdAPdeQHidVNaQO9EH18tXuXgcXNgnqaZY3P4uGKsE7mGyVpRTqykDn3cvecp4g?key=OVlnbC0wcUN0ZG1leUpfR1FST1p2Vll2XzcyOHVB)概述了谷歌跨团队努力使谷歌相机应用更快，页面上包含的屏幕记录展示了一些我们很少看到的 Android 10 功能以及一些引起我们兴趣的内部应用。

**提高谷歌相机性能**

尽管 Pixel 3 拥有 2018 年最好的相机之一，但它的相机体验并不完美。例如，有人抱怨相机应用程序不能正确保存照片。谷歌通过改进内存管理的后续更新解决了这些问题，但损害已经造成了。在页面中，谷歌提到，提高性能是 2019 年“团队的最高优先事项之一”，因为“它如何侵蚀对产品的信任。”然而，提高性能并不像“扳动开关或修复一两个错误”那么简单，因为它需要“相机团队以外的重大努力，如 Android 系统和 Android 性能团队。”例如，Android 团队之前创建了 [PinnerService](https://android.googlesource.com/platform/frameworks/base/+/master/services/core/java/com/android/server/PinnerService.java) ，Pixel 团队使用它将谷歌相机 APK、ODEX 和 VDEX 文件固定在内存中(在我的 Pixel 2 XL 上，那大约是 183MB。)经过谷歌“执行领导层”的批准，谷歌相机团队今年“把重点放在‘快’上”，有“人们积极调查所有问题。”

正在测试的主要性能问题是一些用户可能遇到的相机应用程序偶尔启动缓慢的问题。你希望总是能够快速启动相机应用程序，以防你需要立即拍摄照片或视频，但一些用户可能已经注意到，偶尔“在最初的大约 10 秒钟内，点击快门键不会做任何事情，相机的其他部分可能会看起来像是完全加载了一样”，而加载应用程序只需不到 2 秒钟。这个页面显示给狗粮用户(即内部 Google beta 测试人员)，他们在 Google Camera 应用程序启动期间经历了这样的“缓慢启动”，通知他们如何捕获系统跟踪并发送错误报告。

```
 <string name="dogfood_slow_launch_toast_send_feedback">go/be-faster</string>
<string name="dogfood_slow_launch_toast_text">That launch seemed slow.</string>
<string name="dogfood_toast_learn_more">Learn more</string> 
```

点击“了解更多”按钮会将他们带到 Google 相册页面，正如我们在 Google Camera 7.0 的代码中确认的那样。我们的情报提供者很可能是在他们自己经历缓慢启动时看到这个页面的。

该页面创建于 2019 年 5 月 3 日，就在[谷歌 I/O 2019](https://www.xda-developers.com/google-io-2019-may-7-9/) 之前，该公司在那里发布了 [Pixel 3a 和 Pixel 3a XL](https://www.xda-developers.com/google-pixel-3a-3a-xl-specs-features-price/) 。鉴于该页面发布的时间与 Google I/O 的开始日期非常接近，该团队不太可能在 Pixel 3a 发布前及时收集并实施所有这些反馈。因此，我们很可能会看到提到的相机改进进入稳定的谷歌相机 7.0 更新，我们预计下个月将与 Pixel 4 一起发布。

**安卓 10 规则**

在 Android Q beta 3 中，[我们发现](https://www.xda-developers.com/google-pixel-android-q-settings-routines/)谷歌正在研究一种方法来自动化你手机上的一些设置。我们后来[激活了这个功能](https://www.xda-developers.com/google-pixel-android-q-rules-ramping-ringer-now-playing-album-art/)，透露它将被称为“规则”，当你连接到某个 Wi-Fi 网络或你在某个位置附近时，你将能够自动改变声音模式。此功能出现在两个屏幕录像中显示的设置应用程序中。由于屏幕录制是在 Pixel 3a 上进行的，因此谷歌可能会在旧款 Pixel 智能手机上启用该功能。

**谷歌内置屏幕录制应用**

Android 10 有一个非常简单的屏幕录制应用程序，目前隐藏在稳定版本中，但谷歌可能会为[Android 11 R](https://www.xda-developers.com/android-q-ama-summary/)或 [Pixel 4 版本](https://www.xda-developers.com/google-pixel-4-hands-on-video-ambient-eq-screen-attention-pixel-themes-recorder-app/)开发一个合适的录制应用程序。有趣的是，我们在谷歌照片页面上发布的屏幕录像中发现了一个新的记录器应用程序。这款应用名为“召回”，它有一个我们从未在任何现有谷歌应用上见过的应用图标。我们认为它用于屏幕录制，因为当 MediaProjection API 被应用程序使用时，会在状态栏中显示“Cast”图标，并且通知会提到 Recall 应用程序正在录制。此外，我们可以在状态栏和通知中看到“隐私芯片”，它可以显示应用程序何时正在使用摄像头或麦克风。这个功能出现在我们早期的 Android Q 泄漏中，但在公开测试版和稳定版中被删除了。

我们不知道这个应用程序是什么样子的，也不知道它提供了什么设置。有可能这只是打算供谷歌内部使用，而不会在谷歌之外公开。我们希望情况不是这样，因为用户想要一个预装的屏幕记录器已经有一段时间了。Android 10 甚至允许屏幕记录器记录来自其他应用程序的音频，但目前，你需要使用第三方屏幕记录器来完成。

**Volta App？**

最后，我们发现了一个以前从未见过的“Volta”应用程序的图标。这或许与 Android 5.0 Lollipop 的 [Project Volta](https://www.xda-developers.com/android-5-0-rollout-begins/) 旨在提高电池寿命的举措有关。这款应用可能是一款测试应用电量或分析设备电池历史的工具。

* * *

我们期待 Pixel 4 智能手机发布日期的公告。我们很高兴看到新手机将带来什么样的相机改进，特别是在我们使用[改装的谷歌相机应用](https://www.xda-developers.com/google-pixel-4-astrophotography-preview-google-camera-7-0/)对其夜视功能进行了改进之后。如果我们对这两款智能手机有更多了解，我们会通知您。

[**谷歌 Pixel 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**谷歌 Pixel 4 XL 论坛**](https://forum.xda-developers.com/pixel-4-xl)

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*