# 在根 Android 10 设备上启用 Pixel 4 的实时字幕功能

> 原文：<https://www.xda-developers.com/enable-pixel-4-live-caption-android-10/>

对于失聪或听力困难的用户来说，谷歌在 Android 10 中新推出的实时字幕工具可能会非常有用。这个工具是今年早些时候在 Google I/O 上发布的，它可以自动为你设备上播放的音频提供字幕。它适用于视频、播客、音频信息和其他支持的媒体(但不适用于电话或视频通话)。当谷歌推出这项功能时，他们把它变成了 [Pixel 4 独有的](https://www.xda-developers.com/google-pixel-4-specs-features-pricing-availability/)，尽管[说他们计划在本月的某个时候把它带到 Pixel 3 和 Pixel 3a 上。然而，](https://www.xda-developers.com/google-pixel-4-what-you-missed/)[我们已经展示了](https://www.xda-developers.com/android-10-live-caption-google-pixel-4/)它也可以在其他设备上运行，现在我将分享如何在您自己的设备上启用它。

你需要一个运行 Android 10 的根设备来实现这一功能，因为谷歌迄今为止打算让 Live Caption 只在最新的 Pixel 智能手机上运行。除了我用来在 Android 10 上启用实时字幕支持的方法，还有另一种方法，涉及到改变系统属性值，以欺骗设备个性化服务应用程序，使其认为它正在 Pixel 4 上运行。然而，在较旧的 Pixel 手机上这样做会破坏谷歌相机应用程序，所以我不会分享这种替代方法。我分享的方法不会触及任何系统属性；相反，它直接将控制实时字幕特性的所有值设置为真。因此，相机功能或任何其他功能都不会受到影响。不过，在像这样刷新任何模块之前，你应该准备好备份。

我在 Pixel 2 XL 和 Pixel 3 XL 上启用了实时字幕。我在 Twitter 上的一些粉丝说，它可以在 Pixel 3a、第一代 Pixel、Essential Phone 和运行定制 based ROM 的 Redmi K20 上工作。使用这种方法，直播字幕似乎无法在运行 OxygenOS 10 的一加 6T 或一加 7 Pro 上工作，但希望我们可以通过更多的调试让它工作。如果你想在你自己的设备上尝试一下，下面是你需要做的。

**要求:**

*   运行 Android 10 的 Android 智能手机或平板电脑。
*   使用 Magisk 进行 Root 访问。

**步骤:**

1.  前往“设置”>“应用”,然后轻按菜单以显示所有系统应用。查看是否安装了“设备个性化服务”。这款应用预装在 Pixel 设备上。它不应该出现在非像素设备上，但一些定制的 rom 可能已经捆绑了它。
2.  如果您的设备已经安装了“设备个性化服务”，那么您必须更新到从 Pixel 4 中提取的 APK 的最新版本。[具体来说，安装这个 APK](https://www.apkmirror.com/apk/google-inc/device-personalization-services/device-personalization-services-2-6-278396641-release/device-personalization-services-2-6-278396641-2-android-apk-download/#file) 。从像素 4 提取的 APK 具有用于实况字幕特征的代码。这个 APK 的其他版本将没有实时字幕。如果您的设备尚未安装设备个性化服务，则不要尝试安装它，只需继续下一步。
3.  打开 Magisk Manager 并从下载部分安装“SQLite for ARM aarch64 devices”模块。*注意:如果你已经有一个来自 TitaniumBackup 或 Termux 的 SQLite 二进制文件，那么我的 Magisk 模块安装程序脚本会检测到它，所以你不需要安装这个单独的 SQLite 二进制文件。*
4.  重启你的手机。
5.  下载我制作的以下 Magisk 模块之一，并将其安装在 Magisk 管理器中。如果您的设备安装了“设备个性化服务”，并且您按照步骤#2 更新到最新版本，则安装这个名为“ [LiveCaption_Pixel.zip](https://www.androidfilehost.com/?fid=4349826312261651123) ”的模块。如果你的设备没有安装“设备个性化服务”并且你跳过了第 2 步，那么安装这个名为“ [LiveCaption_nonPixel.zip](https://www.androidfilehost.com/?fid=4349826312261651122) 的模块。_Pixel 和 _nonPixel 模块的区别在于 _nonPixel 模块捆绑了“设备个性化服务”应用程序。这是一个系统应用程序，所以如果你没有安装它，它不能像任何普通的 APK 一样安装。
6.  重启你的手机。
7.  检查实时字幕设置的设置>声音或设置>辅助功能。启用该功能，并通过观看带有英语音频的 YouTube 视频来查看它是否有效。如果它不起作用，尝试重新启动一次。

希望你能在你的 Android 10 设备上运行实时字幕。我已经在我的 Pixel 2 XL 上启用该功能两个多月了，没有出现任何问题。不过，给你个警告。**不要通过谷歌 Play 商店更新设备个性化服务应用程序。**谷歌为不同的设备提供不同版本的应用程序——如果你安装的版本不是为 Pixel 4 设计的，你将失去实时字幕功能。在 Play Store 中禁用此应用程序的自动更新，并检查以确保您通过 APKMirror 安装的任何更新的 APK 都来自 Pixel 4。

* * *

这个方法是我自己发现的，但是我要感谢 XDA 论坛版主 [Didgeridoohan](https://forum.xda-developers.com/member.php?u=4667597) 和 XDA 公认开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 帮我调试我的脚本。我还要感谢 XDA 的高级成员 [73sydney](https://forum.xda-developers.com/member.php?u=9317193) 、jcmm11、adpoliak 以及所有参与 [GPay-SQLite-Fix](https://github.com/stylemessiah/GPay-SQLite-Fix/tree/master/common) Magisk 模块的其他人，因为我借用了代码来检查 SQLite 二进制文件。