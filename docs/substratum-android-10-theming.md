# Substratum 现在支持 Android 10 主题化

> 原文：<https://www.xda-developers.com/substratum-android-10-theming/>

# Substratum 现在支持 Android 10 主题化

如果 Android 10 中内置的主题选项对你的口味来说不够强大，Substratum 现在支持谷歌最新和最棒的 Android 版本。

对于那些觉得 Android 10 的[内置主题化](https://www.xda-developers.com/google-pixel-themes-customize-android-10/)选项和[全系统黑暗模式](https://www.xda-developers.com/android-q-beta-changes-google-pixel/)有点简陋的人来说，最新的 Substratum 测试版现在支持谷歌最新最棒的，前提是有问题的手机是[根](https://www.xda-developers.com/magisk-v20-stable-release-android-10-support/)。我已经在我的备用手机上进行了测试，这是一部 OnePlus 5T，通过 [AOSiP](https://forum.xda-developers.com/oneplus-5t/development/rom-unofficial-aosip-aka-derpfest-t3978357/post80525525#post80525525) 运行 Android 10，并使用 [Liv Dark](https://play.google.com/store/apps/details?id=liv.substratum.theme) Substratum 主题。我也有机会与 Substratum 背后的 Projekt 开发团队的一些成员交谈，并深入了解 Android 10 支持是如何实现的。

为了利用 Substratum 的 Android 10 支持，你需要使用 [Substratum Lite](https://play.google.com/store/apps/details?id=projekt.substratum.lite) 或者加入主 [Substratum](https://play.google.com/store/apps/details?id=projekt.substratum) 应用的 Play Store 中的测试频道。你还必须是根用户，这可以通过最新稳定的 [Magisk](https://www.xda-developers.com/magisk-v20-stable-release-android-10-support/) 构建在支持的设备上，带有解锁的引导加载程序和适当的自定义恢复来实现。此外，你要确保你使用的底层主题支持 Android 10。根据 Projekt 开发团队成员和 XDA 资深成员伊万·伊斯坎达尔( [iskandar1023](https://forum.xda-developers.com/member.php?u=4880721) )的说法，大多数主要底层主题已经提供了所需的支持，尽管你应该首先阅读你选择的主题的 Play Store 描述以确保安全。

在我对 Substratum 的测试中，我使用了主应用程序的测试版，该应用程序最后一次更新是在 10 月 15 日。正如我之前提到的，我通过定制的 ROM 在运行 Android 10 的 OnePlus 5T 上测试了它，并通过 [Magisk 20](https://forum.xda-developers.com/apps/magisk) 让它扎根。你可以在下面的图片中看到我选择的主题。

在我对 Substratum 开发负责人 Nicholas Chum([Nicholas Chum](https://forum.xda-developers.com/member.php?u=3605033))和 XDA 资深成员伊万·伊斯坎达尔( [iskandar1023](https://forum.xda-developers.com/member.php?u=4880721) )的采访中，我了解到更新 Substratum 应用程序本身以支持 Android Q 并没有我想象的那么困难，尽管谷歌在 Android 10 中对 UI 主题的改变需要主题者做出一些重大改变。例如，虽然主题使用者仍然可以为他们希望包含在主题中的应用程序的/res (resources)文件夹中的项目设置主题，但他们不能再为应用程序资产设置主题(如 Gboard 中的键盘背景，或特定于应用程序的表情符号资产)。根据 Nicholas 和 Ivan 的说法，除了 Gboard 之外，最终用户不会特别注意到这种差异。