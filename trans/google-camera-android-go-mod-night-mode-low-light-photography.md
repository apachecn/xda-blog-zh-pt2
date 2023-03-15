# 谷歌相机 Go 中的夜间模式:民主化弱光摄影

> 原文：<https://www.xda-developers.com/google-camera-android-go-mod-night-mode-low-light-photography/>

如果谷歌的 Pixel 智能手机有一个领域保持不败，那肯定是在相机软件领域。谷歌相机应用程序的大部分魔力发生在软件方面。尽管自 Pixel 2 以来，这家科技巨头继续在其智能手机上使用相同的 1220 万像素主摄像头，但支持谷歌摄像头惊人的“计算摄影”的软件算法随着每款新的 Pixel 智能手机而不断改进。谷歌令人难以置信的相机处理能力启发了开发者，包括 XDA 开发者论坛上一些最著名的人物，他们修改了谷歌相机应用程序，以便在非谷歌智能手机上运行。同样，对于低端和预算设备，开发人员也移植了[谷歌相机 Go](https://www.xda-developers.com/google-camera-go-portrait-mode-android-go-budget-smartphones/) ，这是谷歌用于 Android (Go Edition)设备的相机应用的轻量级版本，最近[更新了夜间模式](https://www.xda-developers.com/google-camera-go-adds-night-mode-hdr-better-budget-phone-photography/)。

正如你所料，夜间模式类似于完整的谷歌相机应用程序中的夜视。我们试用了 Camera Go 的夜间模式，使用了开发者和 XDA 高级成员 [mickey36736](https://forum.xda-developers.com/member.php?u=5059016) 提供的应用程序的修改版本，在 GCam modding 社区中更好地称为 Wichaya。最新的谷歌相机 Go(版本 1.8.332394960) APK 是由 XDA 资深会员 [RKBD](https://forum.xda-developers.com/member.php?u=7544065) 从谷歌 Play 商店提取的，但是如果你侧装这个版本的话，夜间模式就不会显示出来。威查亚改装了 APK 来激活夜间模式，这就是我们用来测试的。

**注意:谷歌相机 Go 应用程序中的夜间模式目前只适用于[诺基亚 1.3 安卓 Go 智能手机](https://www.xda-developers.com/nokia-8-3-5g-nokia-5-3-nokia-1-3-announced/)，但我们正在诺基亚 5.3 上使用该模式。这篇文章是为了演示 Camera Go 的夜间模式功能，而不是回顾诺基亚 1.3 的相机质量，因为我们手头没有这方面的资料。**

## 谷歌相机 Go 中的夜间模式

今年早些时候，谷歌相机 Go 应用程序与诺基亚 1.3 一起首次推出。它是为配有单个摄像头的低端设备设计的[，因此它配备了一个简单的界面，具有基本功能，如面部增强、照片、视频、人像模式和内置的视觉翻译器。该应用程序的最新更新增加了夜间模式，尽管谷歌也在](https://www.xda-developers.com/google-camera-go-hands-on-gcam/)[准备为该应用程序](https://www.xda-developers.com/google-testing-hdr-photography-camera-go-budget-android-smartphones/)增加 HDR 支持。

Wichaya 的应用程序修改版本中还没有启用 HDR(可能是因为谷歌自己还没有完成)，但夜间模式可以在我们尝试的大多数设备上运行——尽管我们不能确保在所有现代设备上支持。新的 APK 只有 16MB 大小，非常适合存储空间有限的低端设备。国防部似乎也有夜间模式处理库，名为“ *libNightMode_jni.so* ”，大小为 7.1MB，位于 APK 内部。

昨晚，我带着诺基亚 5.3 版谷歌相机出去兜了一圈，并在不同的弱光条件下测试了它的表现。以下是一些例子:

*夜间模式关闭(左)与开启(右)*

非常明显，谷歌相机 Go 的夜间模式在所有场景下都显著改善了照明。除了照亮场景，夜间模式也有助于提高图像的清晰度。尽管如此，在一些亮度相当低的情况下，Camera Go 应用程序可能无法对焦。所有的照片都有相当多的噪点，主要是因为高 ISO 值。

值得注意的是，虽然没有夜间模式的图像是在 12MP 拍摄的，但有夜间模式的图像仅在 2MP 拍摄，这可能是为了保持图像尺寸较小。此外，阅读 EXIF 数据显示，使用夜间模式的曝光时间比不使用夜间模式的曝光时间长 3-4 倍。

虽然谷歌相机 Go 的夜间模式产生的图像并不令人难以置信，但我们必须保持我们的期望——谷歌相机 Go 的夜间模式并不意味着与普通谷歌相机的[夜视](https://www.xda-developers.com/google-pixel-4-night-sight-motion-mode/)不相上下，这样的期望只会让自己失望。当单独考虑它们时，结果是令人兴奋的，因为该应用程序是为价格比 T2 低得多的设备设计的。

你可以在下面分享的 Flickr 图库中找到以上所有图片和更多图片。

**你对 Google Camera Go 上的夜间模式有什么想法？请在下面的评论中告诉我们！**