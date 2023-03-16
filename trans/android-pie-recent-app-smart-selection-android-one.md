# Android Pie 最近的应用智能选择功能可能会出现在 Android One 智能手机上

> 原文：<https://www.xda-developers.com/android-pie-recent-app-smart-selection-android-one/>

# Android Pie 最近的应用智能选择功能可能会出现在 Android One 智能手机上

Android Pie 最近的应用智能选择功能目前是 Pixel 专有的功能，但它可能很快也会在 Android One 设备上提供！请继续阅读。

Android Pie 中引入的一个鲜为人知的功能是通过最近的应用概述进行的[智能选择。](https://www.xda-developers.com/android-p-smart-selection-app-actions-limited-google-pixel-2/)其默默无闻的原因可能是因为这一功能是谷歌 Pixel 系列独有的，即使在这些产品中，Pixel 2 和更新的产品也有这一功能。使用“智能选择”,您可以拷贝应用程序中的文本和图像，因为它们在“最近使用的应用程序”概览中是可见的，而无需再次打开这些应用程序来拷贝文本或图像。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

 <picture>![Android P Smart Selection](img/454da7321d1b1633a1db55ceb102aa9d.png)</picture> 

Smart Selection in Android P, as demonstrated by David Burke during Google I/O 2018\. Source:

智能文本选择功能由一个名为 ActionServices 的系统应用程序控制，该应用程序包含通过要求“ *PIXEL_EXPERIENCE* ”功能标志返回真值来检查设备是否为 Google Pixel 设备的代码。

然而，我们在 ActionServices APK 中发现的代码表明，该应用程序可能会被打开，以与 Android One 设备配合工作，正如功能标志*match maker _ _ enable _ match maker _ Android _ One*和 sysconfig 功能 *ANDROID_ONE_EXPERIENCE* 所证明的那样。

该功能尚未在 Android One 设备上上线，但谷歌已经考虑让 Android One 设备在未来使用该功能。这种未来何时到来，还有待观察。

*感谢 PNF 软件公司为我们提供了使用[反编译器](https://www.pnfsoftware.com/?aid=xdadev%22%3EJEB)的许可，这是一款针对 Android 应用的专业级逆向工程工具。*