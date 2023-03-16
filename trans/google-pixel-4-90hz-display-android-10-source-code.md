# Android 10 源代码证实谷歌 Pixel 4 拥有 90Hz 显示屏

> 原文：<https://www.xda-developers.com/google-pixel-4-90hz-display-android-10-source-code/>

2019 年 IFA 正在进行中，因此我们看到大量智能手机设备制造商推出了他们的最新产品。到目前为止，已经公布的新智能手机都没有高刷新率显示屏。仅在今年，我们就已经看到努比亚 Red Magic 3、ROG Phone II 和一加 7 Pro 推出了 90Hz 或更高的刷新率。我将一加 7 Pro 评为 2019 年上半年最佳智能手机，很大程度上是因为它的 90Hz 显示屏。传言即将发布的谷歌 Pixel 4 智能手机也有 90Hz 显示屏，我们现在可以确认这一点，这要感谢一位谷歌人在 Android 10 源代码中留下的评论。

前几天，谷歌完成了[上传](https://www.xda-developers.com/android-10-source-code-aosp/) [Android 10 版本](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/)的源代码，我花了一些时间在源代码中挖掘，寻找谷歌没有公布的幕后变化。在检查对 Android 的 SurfaceFlinger(一个负责将应用程序和系统表面合成到显示控制器的单个缓冲区中的系统服务)所做的更改时，我发现了几个与显示刷新率有关的提交。例如，一个提交描述了[基于内容的 fps 检测](https://android.googlesource.com/platform/frameworks/native/+/93bc83d7d196da49db17110694f16cc4d6b331da%5E%21/#F0)，而另一个[描述了覆盖](https://android.googlesource.com/platform/frameworks/native/+/03b02dda62e8d1dc8a07eb927b2f47189c2a926d%5E%21/#F1)的实现，以显示设备何时运行在 60Hz 与 90Hz 之间。鉴于谷歌一直在对 AOSP 进行修改，以适应来自原始设备制造商的越来越多的设备——智能手机推出高刷新率面板肯定有上升趋势——这些对 Android 10 源代码的承诺并不能证明下一个 Pixel 将拥有 90Hz 的显示屏。然而，直到我偶然发现了提交中留下的一个注释，这个注释已经被删除了，但是仍然可以通过查看提交历史来查看。

让我解释一下你在看什么。这段代码添加了一个启用/禁用标志来切换 90Hz，根据提交[描述](https://android.googlesource.com/platform/frameworks/native/+/bd6654bdab3bdf9b6c50d24ff23f603f76e37f31%5E%21/#F0)，它只是打算暂时使用，直到实现正确的解决方案(不到一个月后[实现](https://android.googlesource.com/platform/frameworks/native/+/97d0423a1af70ac6520213bdb26cab5735d0007d%5E%21/#F0))。if 上面的注释...else 声明揭示了切换到 90Hz 的开关“应该只对 P19 设备可用”，其中 P19 几乎肯定是像素 2019。由于 Pixel 3a 系列已经发布，但没有 90Hz 显示屏，这意味着谷歌肯定是指即将到来的 Pixel 4 系列。

由于我们了解到这些与刷新率相关的代码变化主要是针对谷歌 Pixel 4 的，所以我们回去检查了 SurfaceFlinger 的其他变化，看看我们是否可以了解更多。我们发现谷歌打算在 Android 10 中公开刷新率覆盖作为开发者选项。覆盖图将显示在状态栏中时钟的下方，它将显示为一个细长的矩形，对于 60Hz 为“红色”，对于 90Hz 为“绿色”。最后，我们还了解到，谷歌正在准备检测视频播放的时间，以便 Pixel 4 可以自动调整刷新率。

上个月，[一位消息人士告诉*9 to 5 谷歌*](https://www.xda-developers.com/google-pixel-4-90hz-smooth-display-6gb-ram/) 谷歌 Pixel 4 将采用 90Hz 的“平滑显示屏”较大的 XL 型号预计将有 6.3 英寸 1440p 90Hz 有机发光二极管显示屏，而非 XL 型号预计将有 5.7 英寸 1080p 90Hz 有机发光二极管显示屏。XL 型号预计将有 3700 毫安时的电池，而非 XL 型号则有 2800 毫安时的电池。使用 90Hz 显示模式时，较小的 2019 像素是否会有体面的电池寿命仍有待观察，但我们要等到手机发布后才能知道。

据传，谷歌 Pixel 4 还有 6GB 内存和双后置摄像头，其中一个是 16MP 长焦摄像头。我们有确凿的证据证明 [Pixel 4 的长焦摄像头](https://www.xda-developers.com/google-pixel-4-telephoto-lens-google-camera/)，所以很可能谷歌不会像一些人希望的那样添加专用的超广角镜头。谷歌证实，2019 年底的 Pixel 将拥有类似 Face ID 的硬件和一个用于“运动感应”空中手势的 [Soli 雷达](https://www.xda-developers.com/google-pixel-4-face-unlock-soli-gestures/)(尽管这些手势只在选定国家的[有效)。由于新的 Android 操作系统已经达到稳定状态，这两款智能手机都将推出 Android 10。我们现在也确切地知道了 Pixel 4 智能手机的设计，这要归功于](https://www.xda-developers.com/pixel-4-soli-gestures-select-countries/)[谷歌自己](https://www.xda-developers.com/google-pixel-4-teaser/)和[过去一周的两次](https://www.xda-developers.com/google-pixel-4-sprint-leak/) [单独的](https://www.xda-developers.com/google-pixel-4-xl-leaked-hands-on-video/)实践泄露。谷歌的 2019 款 Pixel 智能手机预计将于下月发布，随着发布日期的临近，我们势必会揭开更多细节。

[**谷歌 Pixel 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**谷歌 Pixel 4 XL 论坛**](https://forum.xda-developers.com/pixel-4-xl)