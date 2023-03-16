# Android 11 可能会取消 Android 对视频录制的 4GB 文件大小限制

> 原文：<https://www.xda-developers.com/android-11-unlimited-video-recording-file-size/>

**更新(美国东部时间 6/12/20 @下午 4:00):**官方消息:Android 11 终于摆脱了视频录制的 4GB 文件大小限制。

2019 年，智能手机品牌在相机质量方面有了巨大的飞跃，特别是在变焦和低光方面。另一方面，视频质量没有得到同等的重视。这可能会在 2020 年随着高通骁龙 865 的改进 ISP 而改变。然而，尽管 Android 智能手机配备了更大的内部存储容量，更快的调制解调器，并且现在支持 5G 网络，但一个旧的限制阻止了大多数手机保存大于 4GB 的视频文件。然而，这可能会在 Android 11 中发生变化，Android 的下一个主要版本将于 2020 年发布。

我将尝试总结这种限制背后的原因，而不会深入到技术方面。基本上，Google 决定 Android 的 MediaMuxer 和 MPEG4Writer 类(分别负责多路复用(组合)视频文件并将其保存为 MP4 文件)应该支持输出最大大小为 2^32 - 1 字节的 MP4 文件，大约为 4GB。这个决定[是在 2014 年初](https://android.googlesource.com/platform/frameworks/av/+/1f1f2b1678fd0d038dfc501252dd2b65ecf10cae%5E%21/)做出的，当时最大内存为 32GB 的谷歌 Nexus 5 仍在市场上销售，SD 卡仍在广泛使用，第一款具有 4K 视频录制功能的手机刚刚上市(Galaxy Note 3)。因此，没有太多的需求来保存大小超过 4GB 的视频文件:大多数手机没有足够的存储空间，FAT32 格式的 SD 卡无论如何都不支持它，很少有手机录制的质量足够高，甚至满足这一限制。一晃 5 年过去了，很多事情都发生了变化:现在有 1TB 存储空间的手机，SD 卡现在是例外而不是标准，4K 视频录制无处不在，8K 视频录制很快就会到达设备。

今天，如果你在 Pixel 4 上录制一段 4K 视频，你的视频将在大约 12 分钟内达到 4GB 的大小；这是默认的质量设置，帧速率为 30fps，比特率为 48Mbps。在大约 12 分钟的录制后，相机应用程序将保存视频，并立即开始录制另一个视频-而用户不会注意到。当你查看手机的 DCIM 文件夹时，你会注意到原本应该是一个连续的视频记录被分割成了多个视频文件。例如，我的 Pixel 4 上的一个 73 分钟的视频记录被分成 7 个不同的文件——所有这些在 Google 相册中都是单独的记录。在上传到谷歌照片之前，对这些 MP4 文件进行多路复用并不困难，但如果你想这样做，你必须使用第三方应用程序。我可以想象，大多数人不会费心或者不知道如何去做。

 <picture>![](img/702a296c3a3afbb25733b7fe38a3bf32.png)</picture> 

A 73 minute 4K30 video recording from my Pixel 4 split up into 7 different files.

多年来，开发人员一直在寻找一种录制大于 4GB 的视频文件的方法，现在看来，这种变化最终将在 Android 11 中出现。根据 AOSP gerrit 的[新承诺](https://android-review.googlesource.com/c/platform/frameworks/av/+/1198379)的描述，谷歌正在更新 Android 的媒体类，以取消 32 位文件大小的限制。具体来说，Android 现在将“在 mpeg4writer 中使用[a]64 位偏移”，这允许 Android“合成/多路复用大于 4GB 的文件”在测试中，谷歌成功地编写了一个大约 32GB 大小的文件，在另一次测试中，甚至用一段录音就填满了手机的整个存储容量。2^64 -1 字节的最大文件大小是滑稽的大，永远不会真正达到，所以我们希望谷歌限制 MediaRecorder API 或原始设备制造商限制他们的股票相机应用程序，以支持更合理的最大文件大小。然而，像 OpenCamera 这样使用 Camera2API 的应用程序应该仍然能够任意设置他们想要的任何最大文件大小，而不必担心 32 位文件大小的限制。

 <picture>![](img/76575969ff37a02f1251454ab26c4cc8.png)</picture> 

OpenCamera's Video Recording Settings

提交尚未合并，但当它合并时，我们预计这一变化将反映在 Android 11 中，因为这是 Android 的下一个主要版本。第一个 Android 10 测试版于今年 3 月上线，因此预计将在 2020 年 3 月看到 Android 11 测试版，然后在 2020 年 8 月的某个时候发布稳定版。随着来自[小米](https://www.xda-developers.com/miui-camera-xiaomi-8k-30fps-video-recording-smartphone/)和[三星](https://www.xda-developers.com/samsung-camera-app-8k-video-209-aspect-ratio-108mp/)的手机有望支持 8K 视频录制，这一变化是受欢迎的——尽管早该如此。

*感谢 XDA 公认的开发者 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 的提示！*

* * *

## 更新:已确认

摄像师们欢欣鼓舞，Android 11 正式摆脱了视频录制的 4GB 文件大小限制。Android 11 Beta 1 最终取消了这一限制，但你需要使用支持它的相机应用程序。目前，甚至谷歌自己的相机应用程序也不支持它。流行的应用程序 [Open Camera](https://play.google.com/store/apps/details?id=net.sourceforge.opencamera) 似乎已经支持它了，我们应该会看到更多的应用程序，包括谷歌相机，也增加了支持。

**来源:[谷歌](https://issuetracker.google.com/issues/155575514#comment5) | Via: [安卓警察](https://www.androidpolice.com/2020/06/12/android-11-will-finally-lift-the-idiotic-4gb-cap-on-video-recordings/)**