# 谷歌 Pixel 手机 Android 11 开发者预览版 3 现已上线

> 原文：<https://www.xda-developers.com/android-11-developer-preview-3-announced/>

回到 2 月份，谷歌发布了针对 Pixel 智能手机的[首个 Android 11 开发者预览版](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel/)(2016 款 Pixels 除外)。该公司的目标是在开放非像素设备的测试版之前，再发布两个开发者预览版。谷歌在三月份发布了[第二代 Android 11 DP](https://www.xda-developers.com/android-11-developer-preview-2-google-pixel-announcement-changelog/) ，今天，他们又发布了 Android 11 开发者预览版 3。第三个开发者预览版增加了一个主要特性，并对早期 DPs 中引入的现有特性进行了一些调整。以下是发生的变化。

## Android 11 开发者预览版 3 的新功能

**App 退出原因更新**

在 Android 11 中，应用程序可以使用 ActivityManager 类中新的[gethistoricalprocessextreasons](https://developer.android.com/reference/kotlin/android/app/ActivityManager#gethistoricalprocessexitreasons)方法来检索最近应用程序死亡背后的原因记录。新的 [ApplicationExitInfo](https://developer.android.com/reference/android/app/ApplicationExitInfo) 类详细描述了应用程序可以检索的历史退出原因的信息，其中包括系统内存不足、本机代码崩溃、运行时权限更改、过度资源使用等因素。这些 API 已经在开发者预览版 3 中根据开发者的反馈进行了更新，这是[谷歌正在积极寻求的](https://google.qualtrics.com/jfe/form/SV_9HOzzyeCIEw0ij3?Source=process-terminations)。

**GWP-阿桑堆分析**

早期的 Android 11 开发者预览版增加了许多工具，帮助开发者找到并修复内存安全问题。最新的是 GWP-阿桑(也以其递归 backronym“GWP-阿桑将提供分配健全性”而闻名)，这是一个“采样分配工具，以最小的开销或对性能的影响来检测堆内存错误。”在 Android 11 开发者预览版 3 中，GWP-阿桑在平台二进制文件和系统应用中默认启用，但开发者也可以在他们的应用中启用它。如果你的应用程序使用库的原生代码，谷歌建议这样做。

**亚行增量**

谷歌想让开发者更快地安装大型 apk，所以他们引入了一个新的 [ADB 增量](https://developer.android.com/preview/features#incremental)功能。这项功能可以使从 PC 到手机安装大型 apk(2GB 以上)的速度比以前快 10 倍。在 Android 11 开发者预览版 3 中，开发者可以使用最新 adb 二进制中的“adb install - incremental”命令安装增量 APK。APK 必须使用新的 [APK 签名方案 v4](https://developer.android.com/preview/features#signature-scheme-v4) 格式进行签名，这将在一个单独的文件中生成签名。该功能还要求设备支持新的[增量文件系统](https://www.xda-developers.com/google-incremental-file-system-android-big-games/)，目前只有 Pixel 4 和 Pixel 4 XL 支持。谷歌表示，所有 Android 11 发布设备都将支持增量文件系统，因此也支持 ADB 增量文件系统。

**无线调试**

无线 ADB 现在在 Android 11 中比以往任何时候都更容易，开发者选项中新增了“无线调试”选项。我们第一次[在 Android 11 开发者预览版 2](https://www.xda-developers.com/android-11-developer-preview-2-changes/) 中看到这个功能，但谷歌从未强调过它的存在。你目前可以使用配对代码工作流将手机与 PC 配对，但谷歌表示，他们计划在未来的 Android Studio 版本中添加二维码扫描工作流。

 <picture>![Wireless debugging in Android 11 Developer Preview 3](img/7e999be53318b5570cb017b759a6c226.png)</picture> 

Wireless debugging in Android 11 under Settings > Developer options

**数据访问审计更新**

最后，谷歌在 Android 11 开发者预览版 3 中更新了新的[数据访问审计 API](https://developer.android.com/preview/privacy/permissions#data-access-auditing)。具体来说，谷歌已经重命名了几个 API，所以如果你正在使用它们，请确保更新你的应用程序。一个示例应用程序[可以在这里找到](https://github.com/android/permissions-samples/tree/master/DataAccessAuditingKotlin)。反馈可以在这里[给出。](https://google.qualtrics.com/jfe/form/SV_9HOzzyeCIEw0ij3?Source=data-access-auditing)

## 下载 Android 11 开发者预览版 3

你可以[到这里](https://android.google.com/sdk/api_diff/r-dp3-incr/changes.html)查看 Android 11 DP2 和 DP3 之间的完整 API 差异，但我们当然会留意谷歌没有公布的任何显著变化。你可以在这里阅读[发行说明](https://developer.android.com/preview/release-notes)，我们建议你在下载和刷新更新之前阅读。最后，请务必[到这里](https://issuetracker.google.com/issues/new?component=190602&template=1407746)提交任何错误报告，并[到这里](https://www.reddit.com/r/android_beta/)讨论最新版本。

我们将链接下载谷歌 Pixel 设备的最新系统图像，并在此页面上投影 Treble 兼容设备[。您可以手动刷新构建，也可以使用 Android Flash 工具来完成。如果没有兼容设备，可以在 Android Studio 的 Android 模拟器中运行预览版。](https://www.xda-developers.com/how-to-download-android-11-developer-preview-for-google-pixel-and-other-android-devices/)

* * *

这是第三个也是最后一个开发者预览版。将会有 2 个测试版发布，包括非像素设备，然后在第三季度的某个时候发布稳定版。

对于所有最新的 Android 11 新闻，请将此标签设为书签:

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**