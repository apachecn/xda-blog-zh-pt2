# 谷歌在 Android 11 中测试双击手势以获取截图和最近事件

> 原文：<https://www.xda-developers.com/google-pixel-3-pixel-4-double-tap-gestures-android-11-screenshots-recents/>

当谷歌上个月发布 Android 11 开发者预览版 1 时，我们详细介绍了一套代号为“哥伦布”的[新手势，允许你双击设备后部来启动助手，打开相机应用程序，等等。当时，我们强烈怀疑该功能是针对 Pixel 手机而不是所有运行 Android 11 的 Android 手机的，但我们不知道该功能是否只针对较新的 Pixel 设备。现在随着](https://www.xda-developers.com/google-pixel-android-11-double-tap-rear-gestures/) [Android 11 开发者预览版 2](https://www.xda-developers.com/android-11-developer-preview-2-google-pixel-announcement-changelog/) 的发布，有迹象表明该功能正在 Pixel 3 XL、Pixel 4 和 Pixel 4 XL 上进行测试。此外，谷歌在“哥伦布”手势中增加了两个新动作:截图和打开最近的应用概述。最后，该公司还完善了实施，以减少误报。这是我们目前所知的。

新的“哥伦布”手势不需要任何特殊的硬件来工作；相反，他们使用设备的加速度计和陀螺仪的传感器数据来确定用户是否双击了设备的背面。为了减少功耗和/或不必要的触发，这些双击手势有“门”，防止它们在某些情况下工作，例如当屏幕关闭、锁屏可见或相机应用程序打开时。Android 11 开发者预览版 2 中的新功能是通过对加速度计和陀螺仪数据实施高通和低通滤波器来减少误报的代码。为此，SystemUIGoogle 中添加了几个新的类:Highpass1C、Highpass3C、Lowpass1C、Lowpass3C 等等。谷歌似乎还为 Pixel 3 XL、Pixel 4 和 Pixel 4 XL 优化了“哥伦布”手势，因为我们已经发现这三种设备参考了 [TensorFlow Lite](https://www.xda-developers.com/tensorflow-lite-mobile-machine-learning/) 机器学习模型。

在我之前的帖子中，我注意到“哥伦布”手势可以触发以下动作:

*   解散计时器
*   发射照相机
*   启动谷歌助手
*   播放/暂停媒体
*   折叠状态栏
*   静音来电
*   贪睡闹钟
*   取消固定通知
*   执行“用户选择的操作”

我还嵌入了一些视频，展示了我们如何控制媒体、启动谷歌助手，以及使用 Pixel 2 XL 背面的双击来启动谷歌相机应用程序。

现在，这里是我录制的视频，展示了 Android 11 开发者预览版 2 中添加的两个新手势:截图和打开最近的应用概述。这两个视频都显示了手势在我运行 Android 11 开发者预览版 2 的 Pixel 3a XL 上的工作情况。

https://gfycat.com/ifr/BigBrokenChanticleer

https://gfycat.com/ifr/FlawlessHollowBubblefish

请注意，虽然我在我的 Pixel 3a XL(以及更早的 Pixel 2 XL)上启用了这项功能，但没有证据表明当它们成为官方产品时，这两款设备都将支持这些手势。然而，Pixel 2 和 Pixel 3a 有必要的硬件来支持这些手势，所以我们可以看到谷歌未来对它们的支持。

**[谷歌像素 3 论坛](https://forum.xda-developers.com/pixel-3)**| | |**|[谷歌像素 3 XL 论坛](https://forum.xda-developers.com/pixel-3-xl)**| |**|[谷歌像素 4 论坛](https://forum.xda-developers.com/pixel-4)| |**|[谷歌像素 4 XL 论坛](https://forum.xda-developers.com/pixel-4-xl)****

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*