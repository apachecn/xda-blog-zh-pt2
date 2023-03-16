# 谷歌相机 7.0 大部分确认了谷歌像素 4 相机功能

> 原文：<https://www.xda-developers.com/google-pixel-4-camera-features-google-camera-leak/>

今天早些时候，我们发表了一篇文章，详细介绍了 Google Pixel 4 在 Google Camera 7.0 中的所有 [UI 变化和新的面向用户的设置](https://www.xda-developers.com/google-camera-7-0-google-pixel-4-leak-hands-on)。这个版本的谷歌相机应用程序是由我们的线人哈尼(@ [哈尼 _4K](https://twitter.com/HANI_4k) )发给我们的，他从越南 YouTube[ReLab](https://www.youtube.com/channel/UC7MGCyKDw8iQX7Vs0-BH9uA)那里获得了 APK。最新版本的 Pixel camera 应用程序的用户界面有很多变化，但也有大量代码揭示了 Pixel 4 的相机功能。

上周末，我们分析了谷歌相机应用程序的最新公开版本 6.3，揭示了谷歌[一直在开发几个新功能](https://www.xda-developers.com/google-pixel-4-camera-features-audio-zoom-live-hdr-better-wide-angle-photos/)，我们认为这些功能将出现在 2019 年的 Pixel 智能手机上。我们发现了音频缩放、实时 HDR、网格扭曲以纠正广角自拍失真以及可能的夜视改善等功能。泄露的谷歌相机应用 7.0 版本继续致力于这些功能，并证实了它们在 Pixel 4 上的存在。泄露的 APK 还透露了几个先前未披露的功能，以及 Pixel 4 相机功能的可能列表。

## **像素 4 上的运动模糊**

虽然这感觉像是一个永恒的过去，但就在上周，我们第一次听说 Pixel 4 将在谷歌相机应用程序中拥有“运动模式”。据消息人士透露，新的相机模式将是 Pixel 4 的主打功能之一。据说它可以让你拍摄前景中的移动物体，同时模糊背景，非常适合体育赛事的照片。

这项“运动模式”功能没有在最近的任何泄露中出现，但这很可能是因为该功能仍然隐藏在预发布设备上的谷歌相机应用程序中。我们发现了一个新相机模式的字符串，虽然字符串本身只列出了模式的代号:“paneer。”

```
 <string name="mode_paneer">Paneer</string> 
```

作为参考，夜视内部叫“墨鱼”，延时内部叫“猎豹”。我们不确定为什么选择“paneer”这个代号，但很明显这是为了谷歌相机应用程序中的一个新的“运动模糊”功能。“运动模式”可能是这种“运动模糊”功能的营销名称。

## 测试零快门延迟夜视和天文摄影

谷歌的消息来源还声称，谷歌[著名的夜视功能](https://www.xda-developers.com/google-pixel-night-sight-google-camera-review/)，使用计算摄影算法在低光照条件下产生详细的图像，不仅速度更快，而且能够拍摄星空。一个泄露的宣传视频证实了 [Pixel 4 的天文摄影能力](https://www.xda-developers.com/google-pixel-4-leaked-promo-video/)，但我们在谷歌相机 6.3 中发现的新夜视代码没有达到我们的预期。然而，有了谷歌相机 7.0，我们更有信心谷歌像素 4 的夜视能力将得到改善。我们在一个狗粮配置类中发现了多个标志，显示了谷歌是如何测试夜视的主要改进的。

尽管在之前的 APK 中，我们只模糊地提到了夜视零快门延迟(zsl_ns)，但最新的 APK 让事情变得非常清楚。ZSL 夜视证实，谷歌正在测试一种更快的夜视系统，可能用于 Pixel 4。另一方面，对于天体摄影，谷歌将使用 GPU(高通骁龙 855 中的 [Adreno 640)来加速天空的分割，然后通过“找到”星星并使它们变亮来优化图像。三脚架检测也有所改进，因为它现在将快门按钮改为停止按钮，并在倒计时时将帧数添加到中间。](https://www.xda-developers.com/google-pixel-4-xl-launch-october-15-2019-qualcomm-snapdragon-855/)

## 实时 HDR、HDRNet 和网格变形

在我们拆卸谷歌摄像头 6.3 的过程中，我们发现了一个“直播 HDR”模式的参考资料，似乎与麻省理工学院和谷歌研究人员开发的“ [HDRNet](https://groups.csail.mit.edu/graphics/hdrnet/) ”算法有关。这种算法可以用来将 HDR 实时应用到相机取景器中，也可以用来在拍摄照片后几毫秒内自动修饰照片。网格扭曲很可能是指谷歌研究人员开发的一种[新技术](https://people.csail.mit.edu/yichangshih/wide_angle_portrait/)，用于纠正广角前置摄像头的失真。谷歌相机应用程序中网格扭曲的存在与 Pixel 4 拥有广角前置摄像头的传言相符。

我们再次在谷歌相机 7.0 中发现了对实时 HDR、HDRNet 和网格扭曲的引用，尽管这一次这些引用没有那么模糊。这些功能仅限于 2019 年的 Pixel 智能手机(不包括 Pixel 3a 和 Pixel 3a XL，因为谷歌在代码中将 Pixel 3a 系列称为“Pixel _ 2019 _ middle ”),因为它们需要新的相机库。

## 谷歌 Pixel 4 的音频缩放

当摄像头放大时，一些智能手机使用麦克风来聚焦主要的音频源。LG 和 HTC 已经这样做了好几年，三星最近在几代人之前淘汰了它之后，在 [Galaxy Note 10](https://www.xda-developers.com/samsung-galaxy-note-10-specs-features-price-availability/) 上又把它带了回来。新的苹果 iPhone 11 也有自己的音频缩放功能，所以我们并不奇怪谷歌 Pixel 4 也可能会配备该功能。毕竟，谷歌确实[获得了 HTC 的大部分知识产权和人才。2019 年像素的配置将“AUDIO_ZOOM_SUPPORTED”列为真，因此它很可能会在 Pixel 4 上推出。](https://www.xda-developers.com/google-completes-acquisition-htc-engineers-google-pixel-2/)

## 动态深度格式支持

Android 10 增加了对名为[动态深度格式](https://developer.android.com/training/camera2/Dynamic-depth-v1.0.pdf) (DDF)的新文件模式的支持。根据谷歌的说法，DDF 文件包含照片的深度数据，允许应用程序在后期处理中使用这些数据来改变模糊，而无需接触原始图像。Pixel 4 相机配置将“EMBED_DYNAMIC_DEPTH_REAR”和“EMBED_DYNAMIC_DEPTH_FRONT”都列为 true，这表明设备将支持将深度数据保存为 DDF 文件。值得一提的是，我们还注意到 Google Photos 应用程序正在测试对处理动态深度格式的支持。

## 可能的照相亭与游乐场 AR 贴纸的集成

[Photobooth](https://www.xda-developers.com/google-camera-photobooth-motion-tracking-google-lens-pixel-2/) 是谷歌 Pixel 3 上推出的谷歌相机功能。该功能在检测到相框中的微笑或滑稽面孔时会自动拍照。虽然我们不知道会对该功能进行什么样的改进，但看起来谷歌可能会引入一些底层的变化。在整个代码中，我们发现检查是否支持“Photobooth2019”，而不是只支持“Photobooth”，这意味着这是对现有 Photobooth 功能的更新。

一种特别的方法是在激活“Photobooth2019”之前检查是否在设备上找到“com . Google . VR . apps . corrupt . fun shot . Activity . funshot Activity”活动。运行 Android 10 的 Pixel 2 XL 或 Pixel 3 XL 上不存在此活动。鉴于“com . Google . VR . apps . orange”是 [Playground](https://www.xda-developers.com/download-playground-2-0-ar-stickers-marvel/) (之前称为 AR 贴纸)的包名，我们有可能会看到一些 AR 贴纸与 Photobooth 的集成。自从将该功能更名为 Playground 以来，谷歌使 AR 贴纸更具表现力和互动性，然而，我们不知道升级后的 Photobooth 是否会根据 AR 角色的表情来拍摄照片。

## 测量模式、倒带模式和“洛奇”

早在 4 月份，[我们发现了证据](https://www.xda-developers.com/google-camera-ar-measure/)表明谷歌正准备将其由 [ARCore 驱动的](https://www.xda-developers.com/tag/arcore/)增强现实测量应用 Measure 整合到谷歌相机应用中。这项功能的代码仍然存在于谷歌相机 7.0 中，但尚不清楚谷歌是否计划与 Pixel 4 一起推出这项功能。

接下来，谷歌相机应用的过去几个版本已经暗示了一种代号为“小飞侠”的倒带模式(在回到未来主角之后。)我们不太确定它是如何工作的；我们能确定的是它的图标是一个倒带符号。

另一个更不为我们所知的特征是“洛基”我们在 ViewfinderEffectElement 和“MultiCropModule”中发现了对它的引用，但我们还不知道它应该做什么。

## 根据谷歌相机配置，谷歌像素 4 相机的所有功能

最后，dogfood 配置类列出了 Google Pixel 4 的基本所有相机功能。还有一些论点列出了 2016 年，2017 年，2018 年和 2019 年中期像素的更新相机配置，但为了简洁起见，我们将只关注新设备。摄像机配置表明以下情况属实:

*   谷歌 Pixel 4 支持音频缩放
*   谷歌像素 4 支持使用新的动态深度格式(DDF)保存深度数据
*   Pixel 4 有一个长焦镜头(这个发现已经被[证实了无数次](https://www.xda-developers.com/google-pixel-4-xl-8x-zoom-6gb-ram-white-color/))。)
*   这些设备支持更长的夜视曝光时间。
*   这些设备支持 HDRNet 算法。
*   Google Lens suggestions 可以检测并推荐文档扫描(确实有一个新的“扫描文档”建议芯片的字符串。)

...除了别的以外。相比而言，2018 款 Pixel 3 支持的功能列表要短得多。

## 额外收获:神秘的 2019 像素“针状鱼”再次出现

[早在四月](https://www.xda-developers.com/google-pixel-4-xl-mysterious-third-device-codename/),《AOSP 时报》的一篇评论提到了据信属于 2019 款 Pixel 智能手机的代号。另外，提到了 3 个代号，而不是 2 个代号:“珊瑚”、“火焰”和“针鱼”。我们现在知道“火焰”是较小的 Pixel 4，而“珊瑚”是较大的 Pixel 4 XL，但自 4 月以来，我们没有看到提到“针鱼”，也没有看到谷歌正在为 2019 年底开发第三个 Pixel 的证据。嗯，“针鱼”又回来了，我们还是和四月份一样迷茫。

Google Camera 7.0 中的“DeviceProperties”类区分像素设备，因此可以加载正确的相机配置。我们注意到，在 isPixel2019()中，“珊瑚”和“火焰”旁边是“针鱼”，这表明它确实是 2019 像素。然而，它究竟是什么仍然是个谜。测试设备？统一内核的代号是什么？谁知道呢。除了 Pixel 4 和 Pixel 4 XL 之外，几乎没有证据表明存在另一个 2019 年的像素，所以这是我们现在必须提出的一个谜。

* * *

这就是我们从预发布的 Pixel 4 中泄露的谷歌相机 7.0 版本中挖掘出的所有信息。如果我们了解更多关于 2019 年像素的信息，我们会努力让你知道，即使这些泄露变得令人疲惫不堪。

[**谷歌 Pixel 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**谷歌 Pixel 4 XL 论坛**](https://forum.xda-developers.com/pixel-4-xl)

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*