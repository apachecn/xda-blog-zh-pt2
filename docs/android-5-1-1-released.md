# Android 5.1.1 发布

> 原文：<https://www.xda-developers.com/android-5-1-1-released/>

# Android 5.1.1 发布

Android 5.1.1 已经发布。立即获取最新的工厂图片。

在过去的几周里，谷歌一直非常积极地发布各种更新。一个最意想不到的更新刚刚浮出水面，因为我们心爱的 Android 已经更新到版本 5.1.1。第一个更新到 Android 5.1.1 的设备是谷歌 Nexus 播放器，与 Lollipop 5.0 一起发布。编译系统所需的工厂映像和二进制文件已经在[相关网页](https://developers.google.com/android/nexus/images)上提供。其他受支持设备(希望包括 Nexus 9)的图片将在未来几天内发布。

Android 5.1.1，正如版本所暗示的，并不是一个主要版本。谷歌专注于提供漏洞修复，包括自 5.0 版本以来 Android 中臭名昭著的内存泄漏。我们没有太多的时间来查看日志，看看到底发生了什么变化，但 changelog 应该很快就会提供。

如果您是开发人员，迫不及待地想获得 OTA，您可以为支持的设备自己构建系统。

`repo init -b android-5.1.1_r1 && repo sync`

您也可以运行此命令从头开始同步 AOSP 源:

 ``repo init -u https://android.googlesource.com/platform/manifest -b android-5.1.1_r1 && repo sync`

您的设备已经更新了吗？请在下面的评论中告诉我们。`