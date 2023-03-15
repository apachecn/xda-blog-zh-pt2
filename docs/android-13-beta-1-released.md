# Android 13 Beta 1 在这里有更好的媒体文件权限

> 原文：<https://www.xda-developers.com/android-13-beta-1-released/>

二月份发布了第一个 [Android 13](https://www.xda-developers.com/android-13/) 开发者预览版，随之而来的是世界上最大的操作系统的下一次迭代的基础。它带来了许多有益于开发者的变化，并对隐私、材料、语言控制等方面进行了改进。随后出现了第二个开发者预览版，它包含了通知权限请求和其他对开发者有益的变化。现在，随着 Android 13 Beta 1 的首次发布，我们正在退出“开发者预览”阶段。

与仅面向开发者的“开发者预览”版本不同，Android 13 的测试版面向希望尝试下一版本 Android 的普通用户。谷歌特别关注普通用户对新版安卓系统的普遍反馈。因此，虽然你可能仍然应该对在你的日常驱动中安装它保持警惕，但是这个版本应该比以前的版本更稳定一点。

Android 13 beta 1 最显著的特性包括:

*   更精细地访问媒体文件
*   更好的错误报告
*   预期音频路由

* * *

## Android 13 什么时候发布？

对于 Android 更新，谷歌通常会揭示一个“平台稳定性”里程碑，以便开发者可以知道谷歌打算何时交付最终的 SDK/NDK API，以及最终的内部 API 和面向应用的系统行为。谷歌打算在 2022 年 6 月达到平台稳定，在正式发布前至少计划几周。Android 12 于 2021 年 8 月达到平台稳定性，最终版本于当年 10 月发布[。谷歌发布了](https://www.xda-developers.com/android-12-launched/)[更多关于发布时间表](https://developer.android.com/about/versions/13/overview)的细节，你可以查看一下。

* * *

## Android 13 Beta 1 有什么新功能？

目前，当一个应用程序想要访问手机存储上的文件时，它需要请求 READ_EXTERNAL_STORAGE 权限。不过，该权限授予对所有类型的媒体文件的访问权限，这并不总是必要的。举个例子，为什么一个音频播放应用程序可以访问你的照片？在 Android 13 中，谷歌引入了三个新的权限:

谷歌表示，为了简化用户体验，如果一个应用程序同时请求 READ_MEDIA_IMAGE 和 READ_MEDIA_VIDEO，系统会显示一个对话框来授予这两种权限。

### Keystore 和 KeyMint 中更好的错误报告

对于生成密钥的开发人员来说，Keystore 和 KeyMint 提供了更好的错误。现在在 [java.security. <wbr>](https://developer.android.com/reference/java/security/ProviderException) 下有一个异常类层次结构

ProviderException，Android 特有的异常包括 [Keystore/KeyMint 错误代码](https://developer.android.com/reference/android/security/KeyStoreException)。用于密钥生成、签名和加密的方法也可以修改，以抛出那些新的异常。

### 预期音频路由

为了让媒体应用程序可以识别它们的音频将被路由到哪里，谷歌在 [AudioManager](https://developer.android.com/reference/android/media/AudioManager) 类中添加了一组新的音频路由 API。第一个是[getAudioDevicesForAttributes()](https://developer.android.com/reference/android/media/AudioManager#getAudioDevicesForAttributes(android.media.AudioAttributes))API，它允许您检索可能用于播放指定音频的设备列表。其次，Google 还增加了[getDirectProfilesForAttributes<wbr>](https://developer.android.com/reference/android/media/AudioManager#getDirectProfilesForAttributes(android.media.AudioAttributes))

()API，帮助你了解你的音频流是否可以直接播放。然后，这些新的 API 可以用于确定最佳的[音频格式](https://developer.android.com/reference/android/media/AudioFormat)以用于正在播放的音轨。

* * *

## 如何在你的谷歌 Pixel 设备上下载并安装 Android 13 Beta 1

你可以很容易地[下载 Android 开发者测试版 1](https://www.xda-developers.com/how-to-download-android-13/#beta1) ，如果你不确定如何安装 Android 13 ，请务必查看我们关于[如何安装 Android 13](https://www.xda-developers.com/how-to-install-android-13/)的指南。

谷歌正式发布了 Pixel 6 Pro、Pixel 6、Pixel 5a 5G、Pixel 5、Pixel 4a (5G)、Pixel 4a、Pixel 4 XL 或 Pixel 4 的测试版更新。您可以在 Android Studio 的 Android 模拟器中使用 64 位系统映像，也可以使用 GSI。

* * *

你对最新的测试版有什么想法？你会在你的设备上安装它吗？你的体验如何？请在下面的评论中告诉我们！