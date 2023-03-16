# 谷歌发布 Android 11 开发者预览版 1.1 修复部分 bug

> 原文：<https://www.xda-developers.com/android-11-developer-preview-1-1-fix-bugs/>

# 谷歌发布 Android 11 开发者预览版 1.1 修复部分 bug

今天，谷歌发布了 Android 11 开发者预览版 1.1，以解决最初版本中存在的一些错误。查看变更日志！

整整两周前，谷歌发布了 Android 11 的第一个开发者预览版。公司[计划在第三季度稳定发布之前再发布](https://www.xda-developers.com/android-11-2-more-developer-previews-3-betas-before-stable/)两个开发者预览版和三个公开测试版。然而，今天 Google 发布了开发者预览版 1.1 来解决最初版本中出现的一些错误。查看下面的变更日志。

**隐私**

*   针对 Android 11 的应用程序不再会在试图请求前台位置权限(如 ACCESS_COARSE_LOCATION 或 ACCESS_FINE_LOCATION)以及同时请求任何其他权限时收到错误的安全异常。

**Android Studio 和工具**

*   armeabi-v7a 应用程序不再导致 x86 模拟器映像崩溃。针对 Android 11 的 NDK 应用不再因为 Android Gradle 插件的问题而被阻止构建。此修复包含在 Android Studio 4.0 Beta 2(或更高版本)和 Android Studio 4.1 Canary 1(或更高版本)中。

**非 SDK 接口限制**

*   对 OkHTTP 和广泛使用的相关 SDK 使用的少数方法的灰名单限制已经暂时放宽。在开发者预览版中恢复这些限制之前，这将为应用开发者提供更多时间来测试和更新他们的库。

**应用程序**

*   修复了 com.android.phone 抛出致命异常的问题。

**GSI**

*   修复了在 Pixel 3 设备上使用 gsi_gms_arm64-userdebug build 无法引导的问题。
*   修正了在 Pixel 4 XL 设备上运行时设置向导会崩溃的问题。

更新后的 Android 11 DP 系统映像现可用于 Pixel 4、Pixel 4 XL、Pixel 3a、Pixel 3a XL、Pixel 3、Pixel 3 XL、Pixel 2、Pixel 2 XL 和 GSIs。这些版本必须手动刷新。你可以在这里找到已知问题的列表。

**[下载像素手机 Android 11 开发者预览版 1.1 系统图片](https://developer.android.com/preview/download)**

**[下载 Android 11 开发者预览版 1.1 GSI 图片用于项目高音设备](https://developer.android.com/preview/gsi-release-notes)**