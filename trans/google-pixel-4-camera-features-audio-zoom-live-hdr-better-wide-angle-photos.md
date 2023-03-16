# 谷歌相机应用中透露的谷歌像素 4 相机功能

> 原文：<https://www.xda-developers.com/google-pixel-4-camera-features-audio-zoom-live-hdr-better-wide-angle-photos/>

对于谷歌 Pixel 智能手机的粉丝来说，过去的一周相当令人兴奋。[我们发现了](https://www.xda-developers.com/tag/google-pixel4/)谷歌 Pixel 4 的 LTE 连接、运动感应手势区域可用性、前后设计、90Hz 显示、变焦能力、RAM 容量、Pixel 主题应用程序和可能的新相机功能。如果 Pixel 智能手机擅长一件事，那就是它们的相机质量，所以毫不奇怪，很多注意力都集中在 2019 年底的 Pixel 相机硬件和软件上。在[*9 to 5 谷歌*泄露 Pixel 4 的新相机细节](https://www.xda-developers.com/google-pixel-4-night-sight-motion-mode/)后，我们得知谷歌相机应用程序包含许多隐藏信息，可能会泄露谷歌 Pixel 4 相机的关键功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

XDA 资深会员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 是我们社区的一员，他因修改谷歌相机应用程序以解锁旧款 Pixel 智能手机不支持的功能而闻名。例如，他是第一个在谷歌相机应用程序中启用夜视功能的[，该功能于去年广泛推广。他首先发现新的相机功能被添加到](https://www.xda-developers.com/google-pixel-night-sight-google-camera-review/)[谷歌相机 6.3](https://www.xda-developers.com/google-camera-6-3-android-q-beta-5-night-sight/) ，同样的 APK 版本暗示了 [Pixel 4 有一个长焦相机](https://www.xda-developers.com/google-pixel-4-telephoto-lens-google-camera/)(这一发现被证实了两次[而不是一次](https://www.xda-developers.com/google-pixel-4-xl-8x-zoom-6gb-ram-white-color/)。)我们检查了 7 月的第一个 6.3 APK 以及 8 月下旬的最新版本，并确认以下代码仍然存在。我们还检查了最近的 6.2 APK，并确认这些功能的代码是*而不是*存在的，这表明这些确实是新功能。此外，所有这些功能都标有“experimental2019”，因此只有 2019 年的 Pixel 智能手机才会拥有它们。我们知道像素 3a 不包括这些特征，所以像素 4 是可能的候选者。

### 音频缩放

首先是一个最近才进入智能手机领域的功能:音频缩放。音频缩放可能类似于[三星 Galaxy Note 10](https://www.xda-developers.com/samsung-galaxy-note-10-specs-features-price-availability/) 上的放大麦克风功能，该功能使用麦克风在放大或缩小时调整音频焦点。类似的功能在 HTC 和 LG 手机上已经存在多年，自从谷歌[收购了 HTC 的许多工程师和知识产权后，我们对这项技术出现在 Pixel 智能手机上并不感到惊讶。](https://www.xda-developers.com/google-completes-acquisition-htc-engineers-google-pixel-2/)

这是三星 Galaxy Note 10+的放大麦克风功能的演示，由我们在 [*PhoneArena*](https://phonearena.com) 的朋友提供。音频质量在远处不是很好，但肯定比几乎听不到任何人的声音要好。我希望谷歌能在 Pixel 4 上很好地实现这一功能，因为 Pixel 3 在发布时[在视频录制期间](https://www.xda-developers.com/google-pixel-3-pixel-3-xl-issues-problems-help-list/)出现了麦克风问题。

### 现场 HDR

谷歌相机应用程序正在开发的另一个新功能是“实时 HDR”，它可能使用麻省理工学院和谷歌研究人员米歇尔·加尔比、陈嘉文、乔纳森·t·巴伦、塞缪尔·w·哈西诺夫和弗雷多·杜兰德合作开发的“ [HDRNet](https://groups.csail.mit.edu/graphics/hdrnet/) ”算法，将 HDR 实时应用于相机取景器。(对 HDRNet 的引用存在于 Google Camera 6.3 的几个类中。)据 [*连线*](https://www.wired.com/story/googles-new-algorithm-perfects-photos-before-you-even-take-them/) 报道，HDRNet 还可以用来自动修饰照片——增加对比度，降低亮度等。—不到 20 毫秒。据 *Wired* 报道，在两年前发布时，这一自动编辑功能仍处于“研究阶段”，但谷歌可能已经完善了这一算法，现在有足够的信心将其应用于消费设备。

以下是 HDRnet 的实时演示，摘自 Khush Jammu 的[这篇 Medium 文章。能够在拍摄之前预览 HDR 的照片将是一个非常棒的功能，我希望它能搭载在谷歌 Pixel 4 上。](https://medium.com/the-artificial-intelligence-journal/understand-googles-cutting-edge-hdrnet-in-10-minutes-30ddc9e90288)

https://gfycat.com/ifr/BetterIllfatedDolphin

### 更好的广角自拍

接下来，cstark27 发现了一个“网格扭曲”功能的参考。

这似乎是参考了谷歌研究人员史义昌、赖伟生和贾梁凯开发的一种新算法，以纠正广角人像的失真。[算法](https://people.csail.mit.edu/yichangshih/wide_angle_portrait/)在不扭曲人脸或背景的情况下，从更宽的视野中校正失真。以下截图来自研究人员在 SIGGRAPH 2019 上的演示，由 [YouTube](https://www.youtube.com/watch?v=0g09DWYCGAU) 主办。它展示了他们的新方法如何在广角自拍中纠正失真，同时保持面部和背景的适当比例。

谷歌[已经证实](https://www.xda-developers.com/google-pixel-4-face-unlock-soli-gestures/)Pixel 4 不会像 Pixel 3 那样有第二个前置摄像头。Pixel 3 上的第二个摄像头是专用的广角镜头，所以听起来 Pixel 4 在自拍照片的灵活性上是一个降级。然而， [*9to5Google*](https://9to5google.com/2019/09/06/exclusive-pixel-4-camera-features-motion-mode/) 今天宣称前置摄像头“将是广角镜头”借助这种内容感知扭曲网格技术，Pixel 4 应该能够拍摄出出色、不失真的广角自拍，从而无需专用的第二个前置摄像头。该算法还解决了一个关于 Pixel 3 广角自拍质量的常见投诉。

值得注意的是，我们已经在一年前看到了广角失真校正功能的暗示[。虽然我们没有照片进行直接对比，但这种用于校正脸部广角失真的旧技术可能不如新技术复杂。旧功能的代号也不同于网格扭曲技术的代号，关于这项技术的论文也是今年才发表的。网格扭曲功能的代码只在 Google Camera 6.3 中出现，因此该功能对于 Google Camera 应用程序来说绝对是新的。](https://www.xda-developers.com/google-camera-distortion-correction/)

### 可能的夜视增强

最后， *9to5Google* 报道称，Pixel 4 将采用改进的夜视相机模式。具体来说，夜视将获得“一些速度相关的和其他一般的改进”，这应该允许 Pixel 4“拍摄星空的照片”夜视被广泛认为是最好的相机夜间模式之一，但[华为向我们展示了](https://www.xda-developers.com/huawei-p30-pro-camera-review/)移动弱光摄影是多么不可思议，因此谷歌正在努力增强其夜视算法以保持竞争力。

我们发现了一个暗示夜视零快门延迟(zsl_ns)的参考，尽管只有一个参考提到了这种增强，所以我们对这种解释不是很有信心。我们还发现了名为“camera.cuttle.sky”和“camera.cuttle.sky_gpu”的新标志，暗示通过使用 gpu(在这种情况下，是高通骁龙 855 中的 [Adreno 640)来改善天空摄影的夜视能力(代号为“乌贼”)。)这些代码参考本身并不令人信服，但它们与*9 to 5 谷歌*报道的一致。](https://www.xda-developers.com/qualcomm-snapdragon-855-snapdragon-845-kirin-980-cpu-gpu-ai-benchmarks/)

* * *

在本周接二连三的泄密事件之后，很明显，谷歌的锦囊妙计比他们最初透露的要多得多。像往常一样，我们将继续挖掘代码，尽可能找到所有关于谷歌 2019 年 Pixel 智能手机的信息。加入我们的论坛，了解最新消息。

[**谷歌 Pixel 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**谷歌 Pixel 4 XL 论坛**](https://forum.xda-developers.com/pixel-4-xl)

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*