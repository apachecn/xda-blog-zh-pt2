# 以下是谷歌对原始设备制造商强制和不强制的 Android 11 功能

> 原文：<https://www.xda-developers.com/android-11-features-google-forcing-oems/>

谷歌刚刚开始向其 Pixel 系列设备推出 Android 11 的第一个稳定版本。该公司最新的软件版本带来了一系列面向用户的新变化，如气泡通知、内置屏幕录制支持、重新设计的媒体控制等等。除此之外，Android 11 还包括几个针对开发者的[更新](https://www.xda-developers.com/android-11-features-developers-new-apis/)和一系列我们在 Android 11 源代码中发现的[隐藏变化。但是，尽管这些变化中的大部分都将进入 Pixel 系列，谷歌并没有将一些 Android 11 功能强加给原始设备制造商。在本帖中，我们将看看谷歌要求和不要求原始设备制造商实现的所有 Android 11 功能。](https://www.xda-developers.com/hidden-changes-android-11-source-code/)

根据 Android 11 [兼容性定义文件](https://source.android.com/compatibility/android-cdd) (CDD)，谷歌不要求原始设备制造商实现 Android 11 的 3 个最大的功能。CDD [不按要求列出对话通知](https://source.android.com/compatibility/android-cdd#2_2_3_software:~:text=If%20Handheld%20device%20implementations%20support%20conversation%20notifications)，it [不要求 OEM 实现控制 API](https://source.android.com/compatibility/android-cdd#2_2_3_software:~:text=If%20Handheld%20device%20implementations%20include%20support%20for%20ControlsProviderService) ，身份凭证[也不是要求](https://source.android.com/compatibility/android-cdd#9_11_3_identity_credential)。我们第一次了解到这些需求是在今年早些时候[6 月](https://www.xda-developers.com/android-11-best-features-not-required/)，当时一份详细描述 CDD 变更的泄露文件与我们分享。

对于不知道的人来说，Android CDD 是设备制造商“必须”实现、只是“强烈建议”实现或“不应该”实现的软件和硬件功能的列表。如果一个功能被列为“必须”实现，那么原始设备制造商必须添加该功能，否则他们不能在他们的设备上发布谷歌应用程序。如果某个功能被列为“不应”实现，设备制造商就不能添加该功能。最后，如果一个特性被列为“强烈推荐”，那么就由原始设备制造商来决定是包含还是跳过这个特性。

由于 Android 11 CDD 将上述三个功能都列为“强烈推荐”，因此 OEM 厂商有可能在没有这些功能的情况下发布他们的 Android 11 更新。然而，这并不意味着所有的原始设备制造商将跳过这些功能，因为他们可能会发现这些功能对用户有益。也有可能谷歌针对 Android 11 更严格的谷歌移动服务授权协议要求 OEM 厂商实现这些功能，但我们不知道那些协议的条款。

既然我们已经讨论了不需要的功能，那么让我们来看看 Android 11 中明确需要的一些功能:

## 不允许面部外观改变

似乎谷歌正在[禁止原始设备制造商在图像处理过程中实施面部调整算法](https://source.android.com/compatibility/android-cdd#7_5_4_camera_api_behavior:~:text=%5BC%2D0%2D12%5D%20MUST%20ensure%20that%20the%20facial%20appearance%20is%20NOT%20altered)。这意味着，默认情况下，来自相机管道的所有图像都不会进行面部调整，但面部调整仍然可以通过相机应用程序在 post 中实现。因此，关闭美颜模式*实际上应该是*关闭，除非 OEM 相机应用程序没有让你完全禁用美颜模式，或者它有一个隐藏的 1 级美颜模式，永远无法关闭。虽然大多数 OEM 相机应用程序确实让你关闭它，但已知有一些设备即使在美颜模式关闭时也会应用美颜滤镜。例如，在 [Max 对 Vivo X50 Pro](https://www.xda-developers.com/vivo-x50-pro-camera-review/) 的评论中，他指出即使他禁用了美颜模式，相机也一直在改变他的脸。

## Roboto 作为默认字体

谷歌还要求 OEM 厂商将 [Roboto 作为 Android 11 中的默认字体](https://source.android.com/compatibility/android-cdd#3_8_6_themes:~:text=%5BC%2D1%2D3%5D%20MUST%20use%20the%20Roboto%20version,family%20for%20languages%20that%20Roboto%20supports)。然而，设备制造商仍然可以在设置期间或在设置中向用户提供他们自己的字体。谷歌指出*“目的是确保应用开发者的期望与他们应用的默认(例如，没有明确的用户同意)设备呈现保持一致，默认的无衬线字体是这种呈现的一个高度可见的方面。”*

## fs-verity 要求

使用 Android 11 的新设备将需要支持 fs-verity。根据 Google，*的说法，“fs-verity 类似于 dm-verity，但是是基于每个文件实现的...它有助于有效地验证或“评估”大型文件的真实性，这些文件中只有一小部分可以访问，例如 Android 应用程序(APK)文件...fs-verity 还提供了比提前哈希更好的针对恶意磁盘固件的保护，因为 fs-verity 会在每次分页时重新验证数据。”*