# Chrome OS 80 可以让你在没有开发者模式的情况下下载 Android 应用

> 原文：<https://www.xda-developers.com/chrome-os-80-sideload-android-apps/>

Chrome OS 现在支持 Android 应用程序对任何人来说可能都不是秘密。事实上，已经有一段时间了。在 Chrome OS 中引入 Android 应用支持之前，它实际上非常局限于 web 应用，但 Android 应用支持为 Chromebook 用户打开了许多可能性，包括社交媒体、生产力应用甚至一些游戏的更好的原生体验。起初，这种体验相当有限，但进一步的更新使它变得更加自然和无缝。不过，一个值得注意的遗漏是，除非你启用了开发者模式，否则你无法在 Chromebook 上下载 Android 应用。从 Chrome OS 80 开始，[如之前宣布的](https://www.xda-developers.com/google-chrome-os-80-easier-android-app-sideload/)，这种情况将会改变。

现在，请注意，这个过程仍然不像在 Android 手机或平板电脑上那样简单。这是因为谷歌打算让用户只通过谷歌 Play 商店将安卓应用安装到他们的 Chromebooks 上:据谷歌称，侧装 apk 的过程是为了让开发者测试他们的应用。这可能是为了确保与他们的 Chrome OS 系统兼容，但对于想要下载 apk 的高级用户来说，这仍然是一个障碍。不过，一旦你在 Chromebook 上运行了 Chrome OS 80，这个过程如下:

1.  在你的 Chromebook 上下载谷歌的 Android SDK 平台工具，并将内容提取到一个容易访问的位置。这将允许你通过 Linux 控制台在 Chromebook 中使用 adb 和 fastboot 命令。关于如何让 adb 和 fastboot 运行的更多信息，请参考本教程[的 Linux 部分。](https://www.xda-developers.com/install-adb-windows-macos-linux/)
2.  在 Chrome OS 的 Linux 设置下的开发 Android 应用程序部分启用 ADB 调试。确认对话框后，设备将重新启动。
3.  打开一个 Linux 控制台，运行*ADB connect 100.115.92.2:5555*命令，在您的设备中设置一个 ADB-over-WiFi 服务器。
4.  将要安装的应用程序拖到您正在使用的平台工具文件夹中。
5.  从这里开始，您可以在同一个 Linux 控制台中使用 *adb install* 命令来下载 Android 应用程序。例如，如果我想安装 fortnite.apk，那么你应该运行 *adb install fortnite.apk* 。
6.  此时，应用程序应该已经正确安装。

这远不是一个简化的过程，但它不需要你在 Chromebook 上启用开发者模式，也不会损害它的安全性。不过，你会在锁屏上看到一条警告，提示你设备上可能正在运行非 Google Play 应用。

Chrome OS 80 目前在 Dev 分支中可用，所以如果你想将应用程序下载到 Chromebook 中，这也是你应该记住的事情。我们希望谷歌最终放松他们的政策，以便我们可以像你一样在 Android 手机上下载应用程序，因为包括堡垒之夜在内的几个热门应用程序在 Play Store 上不可用。

* * *

**Via: [关于 chrome books](https://www.aboutchromebooks.com/news/chrome-os-80-how-to-sideload-android-apps-to-a-chromebook/)**