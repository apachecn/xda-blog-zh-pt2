# 采用英特尔芯片的 Chromebooks 很快将最终能够通过 HDMI 播放高清 Vudu 和网飞

> 原文：<https://www.xda-developers.com/chromebooks-intel-play-hd-vudu-netflix-hdmi-hdcp/>

为了防止盗版，网飞和 Hulu 等平台使用加密和数字版权管理方案来限制某些设备上的内容播放。然而，由于一些要求的严格性，一些野生设备无法从这些服务中输出高清视频。原因可能各不相同- [我们已经报道过](https://www.xda-developers.com/android-netflix-hd-amazon-prime-video-hd-drm/)一加和中兴这样的制造商的手机是如何缺乏必要的 [Widevine L1 DRM](https://www.xda-developers.com/android-netflix-hd-amazon-prime-video-hd-drm/) 。但对于采用英特尔处理器的 Chromebooks，高带宽数字内容保护(HDCP)是罪魁祸首。

HDCP 是英特尔开发的一种版权保护形式，用于加密通过 HDMI 和 DisplayPort 连接传输的数字音频和视频信号。它使用一个认证密钥来防止不符合 HDCP 标准的显示器、电视、个人电脑和其他硬件发送或接收信号，这对英特尔驱动的 Chromebooks 构成了一个真正的问题。它们缺乏 HDCP 支持，因此无法传输来自网飞、Vudu 和其他服务的高清视频。

 <picture>![](img/c4b551e59fcba448e0201bfdf21e13b0.png)</picture> 

A comparison of HD and SD resolutions. // [Source: Wikimedia](https://upload.wikimedia.org/wikipedia/commons/e/e0/HD_vs_SD_resolutions.png)

不过，对这些 Chromebooks 的修复正在进行中。Chromium Gerrit 源代码审查页面中的新提交表明，谷歌正在为 Chrome OS 内核添加 HDCP 支持。

事实上，有三个与 hdcp 相关的新提交:两个补丁通过实现 **intel_hdcp_shim** 添加了对 HDMI 和 DisplayPort 连接器的支持，一个补丁添加了在英特尔连接器上支持 HDCP 所需的框架。如果一切按计划进行，Chrome OS 的未来版本将合并这些变化，并因此为基于英特尔的 Chromebooks 带来通过 HDMI 播放高清视频的支持。

目前还不清楚 Chrome OS 多久会支持 HDCP，但对于那些将 Chromebooks 连接到电视屏幕的人来说，这肯定是一个受欢迎的变化。如果你想自己看看代码，你可以在这里查看所有与 HDCP 相关的提交[，在这里](https://chromium-review.googlesource.com/#/c/chromiumos/third_party/kernel/+/849084/)查看[，在这里](https://chromium-review.googlesource.com/#/c/chromiumos/third_party/kernel/+/849085/)查看[。](https://chromium-review.googlesource.com/#/c/chromiumos/third_party/kernel/+/849081/)