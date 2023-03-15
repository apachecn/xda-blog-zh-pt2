# 谷歌正在为 AOSP 的所有设备添加 AAC 蓝牙音频编解码器

> 原文：<https://www.xda-developers.com/google-aosp-aac-bluetooth-audio-codec/>

# 谷歌正在为 AOSP 的所有设备添加 AAC 蓝牙音频编解码器

合并到 AOSP 的新提交表明，谷歌正在为所有 Android 智能手机和平板电脑添加 AAC 蓝牙音频编解码器支持。

过去，Android 一直因蓝牙在谷歌移动平台上的整体表现而受到批评。有些人在让蓝牙设备正确连接方面有问题，有些人遇到过音频播放跳跃，还有人抱怨音频质量本身。随着 Pixel 2 和 Pixel 2 XL 取消了 3.5 毫米耳机插孔，谷歌似乎正在做更多的工作来改善蓝牙音频体验，我们刚刚注意到他们正在通过 AOSP 为所有设备添加 AAC 蓝牙音频编解码器。

就在这个月，我们看到了 Android 操作系统平台上蓝牙发生的两大变化，这是许多人多年来一直在问的问题。我们首先分享了一些我们发现的承诺，表明你将很快能够在具有蓝牙免提模式(HFP)的设备上[启动与谷歌助手的对话，并完全用你的声音结束对话](https://www.xda-developers.com/hands-free-bluetooth-google-assistant-conversation/)。可悲的是，当设备处于高负载下时，一些人还经历了蓝牙播放期间的音频跳过。为了缓解这个问题，谷歌正在努力让[授权蓝牙音频播放](https://www.xda-developers.com/android-oreo-bluetooth-audio-real-time-cpu-scheduling/)的实时 CPU 调度。

这两个变化对改善 Android 上的蓝牙音频体验大有帮助，但谷歌的工作似乎并未就此停止。一些合并到 AOSP 的新提交显示，谷歌正在为所有设备添加 AAC 蓝牙音频编解码器。当然，这并不意味着它会出现在每一台运行新版本 Android 的设备上，但它应该有助于让 OEM 更容易做出实施它的决定。

例如，OnePlus 5 只有在 aptX、aptX HD 和 SBC 之间选择的选项。然后，当我们查看谷歌的 Pixel 手机(第一代和第二代都运行 Android 8.0 Oreo)时，我们可以看到我们可以在 SBC、AAC、aptX、aptX HD 和 LDAC 蓝牙音频编解码器之间进行选择。

* * *