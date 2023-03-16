# 如何在一加 7 Pro 上启用 960fps 慢动作和微距模式

> 原文：<https://www.xda-developers.com/enable-960fps-slow-motion-video-recording-macro-mode-oxygenos-camera-oneplus-7-pro/>

# 如何在一加 7 Pro 的 OxygenOS 相机中启用 960fps 慢动作和微距模式

修改者已经知道如何为一加 7 Pro 启用 960fps 慢动作视频录制以及 OxygenOS 相机中的微距模式。请继续阅读！

一加 7T 最近通过 OxygenOS Open Beta 3 更新获得了一个“秘密” [960fps 慢动作视频录制选项](https://www.xda-developers.com/oneplus-7t-960fps-slow-motion-4k-wide-angle-video-recording-latest-oxygenos-beta/)。该功能基于基于软件的帧插值技术，因此摄影专家可能不认为它是“真正的”960fps 实现。然而，由于整个处理过程是由 OxygenOS 的摄像头堆栈完成的，理论上可以将这一功能应用到配备类似摄像头传感器和内部硬件的老式一加手机上。XDA 资深成员 [elmarian756](https://forum.xda-developers.com/member.php?u=7328026) 也基本做到了这一点，他已经成功在一加 7 Pro 上启用了 960fps 慢动作支持。最重要的是，它也可以用类似的模式解锁期待已久的宏模式。

**[一加 7 场职业 XDA 论坛](https://forum.xda-developers.com/oneplus-7-pro)**

事实证明，一加 7 Pro 实际上能够利用这些功能，但在一些隐藏的参数背后，它们被禁用了。根据 XDA 资深会员 [docnok63](https://forum.xda-developers.com/member.php?u=4967345) 的发现，XDA 资深会员 elmarian756 随后通过修改股票相机应用程序的`CameraInfo_0.xml`和`CameraInfo_5.xml`偏好设置文件，并添加一个名为`Video960FpsSizes`的新字符串，值为`1280x720`，在一加 7 Pro 上启用了 960fps 慢动作录制。一旦你保存它们并重新启动相机，你就可以在慢动作模式上找到第三个 960fps 的选项，就像在[一加 7T](https://forum.xda-developers.com/oneplus-7t) 上一样。

谈到相机中的微距模式，一加确实在 Android Q beta 测试阶段在一加 7 Pro [上简要介绍了它。然而，这个特性并没有进入稳定版。现在您可以通过将`CameraInfo_3.xml`文件中的`IsUWMacroSupported`变量的值从`false`切换到`true`来解锁它。这个特别的实验是由 XDA 资深成员](https://www.xda-developers.com/oneplus-camera-3-8-13-focus-tracking-macro-mode/) [gohan040](https://forum.xda-developers.com/member.php?u=4096435) 进行的。请记住，虽然 7 Pro 和 7T Pro 一样，使用超广角相机来拍摄微距照片，但 7 Pro 缺少 7T Pro 所具有的附加微距电机。您的里程可能会有所不同，以及这个模块的工程。

你必须在你的一加 7 Pro 上安装一加相机的最新测试版( [v3.10.17 或更高版本](https://www.apkmirror.com/apk/oneplus-ltd/oneplus-camera/))才能解锁这些功能。虽然可以在 OxygenOS 的稳定渠道版本上手动加载相机应用的测试版，但建议安装最新的公开测试版[以确保完全兼容。Root 访问是一个强制性的先决条件，用户可以使用像](https://www.xda-developers.com/oneplus-7-oneplus-7t-series-oxygenos-open-beta-14-4-ambient-display-clocks-may-2020-patches/)[偏好管理器](https://forum.xda-developers.com/showthread.php?t=2490022)这样的应用来执行上述更改。

**[一加 7 Pro 相机改装— XDA 讨论线程](https://forum.xda-developers.com/oneplus-7-pro/themes/guide-enable-960fps-slow-motion-7t-pro-t4101389)**