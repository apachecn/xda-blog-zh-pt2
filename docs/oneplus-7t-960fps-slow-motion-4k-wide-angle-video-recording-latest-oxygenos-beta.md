# 一加 7T 在最新的 OxygenOS 测试版中悄悄地获得了 960fps 的慢动作和 4K 广角视频

> 原文：<https://www.xda-developers.com/oneplus-7t-960fps-slow-motion-4k-wide-angle-video-recording-latest-oxygenos-beta/>

# 一加 7T 在最新的 OxygenOS 测试版中悄悄地获得了 960fps 的慢动作和 4K 广角视频

正如之前承诺的那样，一加 7T 现在已经通过最新的公开测试版更新接收到了 960fps 慢动作和 4K 广角视频录制。

一加 7T 家族上周收到了他们的第三次 OxygenOS 公开测试版更新，其中引入了一个方便的相机镜头污垢检测功能以及 2020 年 4 月的安全补丁。然而，事实证明，该公司在这次更新中秘密地在普通的一加 7T 上启用了 960fps 慢动作视频录制支持，尽管该功能在 OTA 变更日志中根本没有提到。

**[一加 7T XDA 论坛](https://forum.xda-developers.com/oneplus-7t)**

一位网名为 *[u/sneakerspark](https://www.reddit.com/user/sneakerspark/)* 的 Redditor 首先注意到，随着 Open Beta 3 的推出，他们现在在股票相机应用程序上有了一个 [720p@960fps 慢动作选项](https://www.reddit.com/r/Android/comments/gjmeoo/oneplus_silently_pushed_960_fps_super_slowmo_mode/)。该人士还在后续回复中确认[他们有 4K@30fps 广角视频](https://www.reddit.com/r/Android/comments/gjmeoo/oneplus_silently_pushed_960_fps_super_slowmo_mode/fqmb8go)。这两个变化都没有出现在官方的变更日志中，这很令人惊讶。供您参考，一加确实在 2019 年 9 月告诉我们[他们正在开发这两个功能](https://www.xda-developers.com/oneplus-7t-960fps-slow-motion-4k-wide-angle-videos/)。也许在一加有足够的信心正式宣布它们之前，当前的实现需要再涂一层油漆。

请注意，一加 7T 上的相机传感器，包括主要的 48MP [索尼 IMX586](https://www.xda-developers.com/sonys-imx586-48mp-smartphone-camera/) 模块，都没有足够的马力来实际记录每秒 960 帧。它们缺乏专用的 DRAM 芯片，无法在将捕获的大量帧传递到图像缓冲区并最终写入存储之前临时存储这些帧。幸运的是，他们能够处理 720p@480fps，因此一加只需要结合某种帧插值算法。最终结果可能不如原生的 960fps 慢动作清晰，但对大多数人来说应该没什么关系。

关于广角视频录制，最初的[一加 7 Pro](https://forum.xda-developers.com/oneplus-7-pro) 也缺乏该功能，但该公司后来[通过 Android 10 更新为该设备启用了该功能](https://www.xda-developers.com/oneplus-7-pro-android-10-video-recording-wide-angle-telephoto-camera-open-beta-update/)。很高兴看到一加正试图在不同的后置摄像头之间实现功能对等，即使是在他们的旧款手机上。

* * *

**来源:[r/Android](https://www.reddit.com/r/Android/comments/gjmeoo/oneplus_silently_pushed_960_fps_super_slowmo_mode/)**