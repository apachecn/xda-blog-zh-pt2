# Android-x86 项目发布 Android 6.0 稳定版

> 原文：<https://www.xda-developers.com/android-x86-project-releases-stable-version-of-android-6-0/>

# Android-x86 项目发布 Android 6.0 稳定版

Android-x86 项目已经收到了它的第一个稳定版本，修复了错误并为我们带来了安全补丁。请继续阅读，了解更多新内容！

如果你是在笔记本电脑或台式机上运行 Android 的人，你可能听说过 Android-x86 项目。对于那些还没有的人来说，Android-x86 计划是由志愿者开发人员发起的，旨在将 Android 移植到运行 AMD 或 Intel 处理器的台式机和笔记本电脑上。

在 6 月推出 Android 6.0 棉花糖和一个月前的第二个候选版本 T1 之后，Android-x86 项目向公众推出了 Android 6.0 T3 的第一个稳定版本 T2。这个版本是基于 AOSP 的 Marshmallow MR2 版本(6.0.1_r66)以及所有的安全补丁。

下面看一下此版本的主要功能，这些功能是对 RC2 版本功能的补充:

*   将内核更新到 4.4.20，添加更多来自 AOSP 的补丁。
*   将 [Mesa](http://www.mesa3d.org/) (图形库)更新到 12.0.2。
*   初步的 HDMI 音频支持。
*   添加 F2FS 支持。
*   将触控板光标从圆形改为普通鼠标指针(从 Android N 移植回来)。
*   改善由 wifi 驱动程序引起的挂起/恢复问题。

稳定版本可以在官方网站上找到[，有 32 位和 64 位处理器的图片。这些映像可以从 BIOS 和 UEFI 固件启动。您还可以加载映像来创建可引导的 USB 记忆棒。](http://www.android-x86.org/download)

该版本有几个已知问题。具体来说，Skylake GPU 可能会在内置浏览器应用程序上出现渲染问题。此外，挂起和恢复功能在某些设备上不起作用，因此您的里程数可能会有所不同。

如果你想在桌面系统上安装 Android，Android-86 是一个不错的选择。现在你可以得到稳定格式的棉花糖和更新的安全补丁。

你对这个来自 Android-x86 项目的稳定版本有什么想法？你试过释放吗？请在下面的评论中告诉我们你的想法！