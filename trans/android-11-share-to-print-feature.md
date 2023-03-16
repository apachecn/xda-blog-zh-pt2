# Android 11 将包括共享打印功能，以简化图像/PDF 打印

> 原文：<https://www.xda-developers.com/android-11-share-to-print-feature/>

# Android 11 的“共享打印”功能将使打印图像和 pdf 更加容易

Android 11 将包括一个新的“共享打印”功能，这将使从智能手机打印图像和 PDF 文件变得更容易。

早在 2017 年，谷歌为支持互联网打印协议(IPP)的打印机推出了 Android Oreo 上的[内置打印服务。在此之前，用户必须在 Play Store 上搜索第三方打印服务，才能从他们的 Android 设备上打印一些东西。这一变化是由佳能、惠普、三星和施乐成立的 Mopria 联盟为 AOSP 贡献的技术带来的。自](https://www.xda-developers.com/android-oreo-print-service-ipp/)[以来，Mopria 联盟在改善安卓设备](https://www.xda-developers.com/wi-fi-direct-printing-android/)上的[打印方面发挥了重要作用](https://www.xda-developers.com/history-of-printing-in-android/)，为安卓 Pie 中的 [WiFi 直接打印提供了支持。现在，Mopria 联盟的一名工程师向 AOSP 提交了代码，表明 Android 11 可能会包括一个新的“共享打印”功能，这将简化图像和 PDF 文件的打印。](https://www.xda-developers.com/android-pie-wifi-direct-printing/)

谷歌刚刚向 Android 开源项目(AOSP)合并了一项新的承诺，以支持“共享打印”——这一功能将使开发者能够向打印服务发送意图，以直接打印图像或 PDF 文件，而无需用户从共享菜单中手动选择打印服务。截至目前，这一代码变化似乎不会在共享菜单中添加一个专用的打印按钮，因为在目前的形式下，该功能只是一种绕过共享菜单的方式，使应用程序能够直接将图像/pdf 发送到默认的打印服务。

该代码表明，在 Android 11 中，开发者将能够在他们的应用程序中添加一个“打印”按钮，直接将图像或 PDF 发送到用户的默认打印服务。此“打印”按钮应构造为发送指向活动“com . Android . bips . imageprintactive”或“com . Android . bips . PDF print activity”的意图，并带有操作“android.intent.action.SEND”、类别“Android . intent . category . default”以及图像或 PDF 文件的数据。

根据 commit 的描述，该功能“使应用程序通过正常的共享意图更容易打印到任何支持的打印机上。”PrintManager 处理以适当的分辨率发送内容，以便打印到任何已安装并启用的打印服务。该提交进一步揭示了图像内容“被缩减到良好的 DPI 以用于预览(屏幕 DPI)或交付(300 DPI)。”“适合”或“填充”选项“由用户的横向和纵向打印属性选择激活”，照片“默认为特定于语言环境的默认照片媒体大小”截至目前，谷歌还没有关于此事的官方信息，但我们希望在第一个 Android 11 公开测试版发布前的几周内了解更多信息。

* * *

**来源:[AOSP](https://android-review.googlesource.com/c/platform/packages/services/BuiltInPrintService/+/1227541)**