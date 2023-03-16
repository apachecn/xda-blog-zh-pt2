# Android Studio 现已推出 Chrome OS 模拟器

> 原文：<https://www.xda-developers.com/chrome-os-emulator-available-android-studio/>

Chrome 操作系统越来越受欢迎，这在一定程度上要归功于众多新增功能，这些功能使它成为一款可以推荐给各种使用场合的操作系统。在过去的几个月里，我们已经看到了一些值得注意的新增功能，例如 [Linux 应用支持](https://www.xda-developers.com/chrome-os-linux-app-support-google-pixelbook/)、[平板模式下的全屏启动器](https://www.xda-developers.com/chrome-os-fullscreen-launcher-tablet-mode/)、[视频录制支持](https://www.xda-developers.com/chrome-os-video-recording/)、[用于概览屏幕的滑动手势](https://www.xda-developers.com/chrome-os-overview-swipe-gesture/)、[应用快捷方式](https://www.xda-developers.com/android-app-shortcuts-better-bluetooth-chrome-os/)、 [GBoard 甚至 PiP 支持](https://www.xda-developers.com/chrome-os-gboard-app-shortcuts-android-p/)—所有这些功能要么已经添加，要么即将上线。

依靠这种日益增长的受欢迎程度，谷歌现在已经在 Android Studio 中发布了一个 Chrome OS 模拟器。这将允许开发人员在 Chrome OS 设备(如谷歌 Pixelbook)上开发和测试他们的应用程序，而不需要手头有物理硬件。

要使用 Chrome OS 模拟器，你需要先下载并安装 Android Studio。然后，通过在 Android Studio >工具> SDK 管理器> SDK 更新站点中添加以下名称和 URL 来安装 Chrome OS SDK 插件:

`Chrome OS Repository: https://storage.googleapis.com/chrome_os_emulator/addon2-1.xml`

Chrome OS 系统映像:https://storage . Google APIs . com/chrome _ OS _ emulator/sys-img 2-1 . XML

一旦下载并安装了系统映像，您就可以使用 AVD 管理器创建一个 Chrome OS 虚拟设备，在本例中是一个 Pixelbook。

请注意，在您使用有效的 Google 帐户登录之前，在模拟器上运行 Android 应用程序的功能是禁用的。由于这是一个模拟器，你可以预期它会比实际的 Chrome OS 设备运行得慢。谷歌还建议将 AVD 的内存从默认的 1536 MB 增加到 2048 MB。模拟器还有一些已知的问题，你可以在 Android 开发者的网页上阅读。

有一个模拟器来测试真的有助于开发人员制作高质量的应用程序，因为它提供了一个额外的媒介来测试他们的应用程序。对于较小的开发项目，它甚至可以消除购买单独硬件的成本，使整个过程更便宜，更有利可图。看到谷歌是如何推动 Chrome 操作系统的，这可能是开发者赶时髦的最佳时机。

[**来源:安卓开发者**](https://developer.android.com/topic/arc/emulator)