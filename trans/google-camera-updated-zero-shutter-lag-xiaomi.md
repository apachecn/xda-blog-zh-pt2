# 谷歌摄像头端口更新了 ZSL 和更多小米设备支持

> 原文：<https://www.xda-developers.com/google-camera-updated-zero-shutter-lag-xiaomi/>

[正如我们在本月早些时候](https://www.xda-developers.com/google-camera-hdr-ported/)报道的那样，谷歌相机**被移植到任何使用 Snapdragon 820/821 或 835 芯片的设备**(根据其他用户的报告，中兴 Axon 7 除外)。据报道，它也可以在**某些骁龙 4XX 或 6XX 设备**上工作，如小米 Redmi Note 3 和小米 Redmi Note 4，尽管这需要设备具有启用的[camera 2 API](https://www.xda-developers.com/camera2api-magisk-module-enables/)。自最初发布以来，谷歌相机端口已经收到了修复主要错误的更新，带来了更多的小米设备，并为自动 HDR+模式引入了零快门延迟。

谷歌摄像头端口似乎在这些骁龙 SoC 中使用了 Hexagon 680 DSP，因此没有等效的 Exynos 或麒麟 SoC 将能够使用该端口(抱歉，国际三星或华为/Honor 用户！)这一功能不仅显著改善了大量设备在特定条件下的照片，还使某些手机成为最佳手机摄影师的主要竞争者。配有这个摄像头的 OnePlus 3 在使用这个端口时，在拍照能力上可以打出远超自身重量的拳，在我看来。

自从本月早些时候首次发布以来，谷歌摄像头端口已经有了**次重大更新**。来自 4pda 论坛的乌克兰开发者 [B-S-G](https://4pda.ru/forum/index.php?showuser=243055) 一直在不知疲倦地提供最好的相机应用。随着版本 4.4.020.163412804 的新基础和他如何实现 HDR+的一些主要变化，改进是全面可见的。

我们报道的最初的谷歌摄像头端口在 OnePlus 3T 上有一个损坏的前置摄像头，损坏的突发火灾模式，损坏的 60FPS 视频记录，损坏的慢动作视频记录和偶尔崩溃的错误的 HDR+模式。现在 B-S-G 已经**修复了所有这些问题**并且也增加了一些改进。如果慢动作或 60FPS 对你不起作用，看看[这个线程](https://forum.xda-developers.com/oneplus-3/how-to/modded-google-camera-hdr-60fps-video-t3658552)。这是一个 Magisk 模块方法，使它能够工作，但它对我来说是开箱即用的。更重要的是，另一个开发人员已经开始对原来的端口进行改进。

在最近的更新中有一个回归，那就是当使用“无 HDR”模式时，图片有时需要很长时间才能保存。**我们建议始终使用自动 HDR+****。在当前版本中，你也可能会遇到罕见的崩溃，但是比以前的版本要少得多。**

 *** * *

## 对谷歌相机 HDR+端口的改进，现在零快门延迟

*上面所有的图片都是在 OnePlus 3 上拍摄的，带有最新的谷歌相机 HDR+端口上的 aHDR+*

谷歌相机端口在过去两周内经历了许多变化，改变了 HDR+的工作方式，并添加了 ZSL。

### ZSL、HDR+和 aHDR+

B-S-G 增加了 ZSL，但是**只针对自动 HDR+** 。自动 HDR+使用比强制更轻的算法，更轻的算法使用更少的照片缝合在一起。这就是为什么它可以使用 ZSL，否则将没有足够的时间来拍摄足够的照片。如果你使用强制 HDR+，那么你不能受益于 ZSL。

这是一件好事，但是，自动 HDR+是你真正需要的。使用强制 HDR+会导致图像看起来不自然，没有阴影。这也是谷歌 Pixel 所做的，因此该端口再次实现了其目标，即将类似 Pixel 的相机功能带到其他设备上。这是对原始端口的巨大改进，原始端口在所有情况下都需要强制 HDR+。这样，相机应用程序自己计算它需要做什么，而不是“一刀切”的方法。许多新端口的用户都认为这是一个巨大的进步。

### 与小米 Mi5s 的兼容性

由于糟糕的相机处理，这个相机端口最初是为 Mi5s 准备的，尽管它可以在大量设备上工作。如果使用小米 Mi5s，这个端口是完整的，除了上面提到的非 HDR+问题，应用程序应该可以完美地工作，零崩溃。如果你使用的是其他 Snapdragon 820/821 设备，那么请看下面。

### 骁龙 4xx/6xx 设备-小米

在最初的帖子之后，似乎这个端口实际上可以在许多小米设备上工作，包括红米 Note 4x，红米 4 和红米 Note 3。如果你想使用它，你需要把它添加到你的建造道具中。

```
 persist.camera.HAL3.enabled=1 
```

或者，您可以刷新这个 [Magisk 模块](https://www.xda-developers.com/camera2api-magisk-module-enables/)。来看看吧！这可能只在小米设备上工作，因为该端口最初是为 Mi5s 准备的，它可能使用小米特定的硬件/专有 blobs。

### 下载并安装

零快门延迟(ZSL)已经成为谷歌相机在 Nexus 5X 和 6P 用户中的一种[流行模式，因为它增加了谷歌像素在这些设备上拍摄优质快速照片的能力。B-S-G 不知疲倦地改进相机，解决了许多崩溃问题，更重要的是，推出了更好的 HDR+解决方案。你可以从我们的 AndroidFileHost 页面下载他的 1.4 版本，或者你](https://forum.xda-developers.com/nexus-6p/themes-apps/mod-camera-nx-v4-google-camera-zsl-hdr-t3494435)[也可以在俄罗斯论坛 4pda 上注册，下载他的新相机更新。](https://4pda.ru/forum/index.php?s=&showtopic=782469&view=findpost&p=64478110)

[**下载 B-S-G 的谷歌相机 v4.4 Mod 用 HDR+和 ZSL**](https://www.androidfilehost.com/?fid=817550096634795524)

* * *

## Snapdragon 820/821 设备的优化

XDA 成员 Ivanich 已经开始着手解决 B-S-G 的一些相机接口问题。我联系了他以确认他所做的更改，如下所示。他有效地优化了 OnePlus 3 和 OnePlus 3T 的摄像头端口，从而也优化了其他非像素、非小米 Mi5s Snapdragon 820/821 设备。我强烈建议 Axon 7 用户也尝试一下，看看它是否能解决他们的问题。

> #### 我只做了一些小的改动，为了修复 op3 上坏了的一些东西。我还添加了 60fps 的录制，所以基本上我是这样做的:
> 
> -增加了 60 帧/秒，感谢阿米尔[https://github.com/amirzaidi/gcam/commits/full](https://github.com/amirzaidi/gcam/commits/full)
> 
> -修复了视频模式下的暗视频问题
> 
> -并禁用导致我们设备上的相机 FC 的爆发

Ivanich 还允许我们在我们的 AndroidFileHost 上重新托管他的修改。看看下面吧！

[**下载针对骁龙 820/821 设备优化的 HDR+谷歌相机 v 4.4 Mod**](https://www.androidfilehost.com/?fid=817550096634795525)

* * *

## 跟上时代

如果你没有最新的版本，我强烈建议你升级到上面链接的选项之一。有了更好的 HDR+，ZSL 工作慢动作和工作 60FPS 视频的方法，绝对没有理由不升级！**