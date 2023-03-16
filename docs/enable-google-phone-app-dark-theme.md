# 如何启用谷歌手机应用程序的新黑暗主题[根]

> 原文：<https://www.xda-developers.com/enable-google-phone-app-dark-theme/>

# 如何启用谷歌手机应用程序的新黑暗主题[根]

谷歌手机 25 测试版包括一个黑暗的主题，所以我们找到了一种无需等待就能启用它的方法。您将需要 root 用户来执行这些操作。

自从新材料主题工具[发布](https://www.xda-developers.com/material-design-revamp-material-theming-tool/)以来，谷歌一直在用他们自己的谷歌材料主题设计更新他们的每个第一方应用。一些应用程序甚至获得了官方的黑暗主题！ [Android Messages](https://www.xda-developers.com/android-messages-redesign-dark-mode/) 和 [YouTube](https://www.xda-developers.com/youtube-dark-mode-android-roll-out/) 已经有了一个，很快谷歌手机应用程序也将有一个。我们听说 Pixel 和 Android One 设备上的股票拨号器应用程序将在一个月前[获得更新](https://www.xda-developers.com/google-phone-app-dark-theme/)。现在，谷歌手机版本 25 最近开始在测试频道推出，这是第一个没有半破的黑暗主题版本。因此，我们最终能够与您分享如何启用它的说明。对于本教程，您需要 root 用户，因为处理共享的首选项文件需要 root 用户访问权限。说完了，让我们开始吧。

1.  请确保您是 rooted 用户，并且安装了最新版本的应用程序 Google Phone 25。你可以通过找到正确的链接[找到你的设备的根](https://www.xda-developers.com/magisk-hub-2/)。要加入谷歌手机应用的测试频道，请前往[谷歌 Play 商店列表](https://play.google.com/store/apps/details?id=com.google.android.dialer)，寻找测试选项。你也可以从这里下载 APK [并手动侧装。](https://www.apkmirror.com/apk/google-inc/google-phone/google-phone-25-0-218361296-release/)
2.  下载任何支持 root 的文件浏览器，如 [FX 文件浏览器](https://forum.xda-developers.com/showthread.php?t=1253399)或 [MiXplorer。](https://forum.xda-developers.com/showthread.php?t=1523691)
3.  打开浏览器，从左侧导航菜单导航到根目录。
4.  导航到`/data/data/com.google.android.dialer/shared_prefs`并寻找名为`dialer_phenotype_flags.xml`的文件。
5.  查找`G__enable_dark_mode_settings`并将值从“假”更改为“真”。您可以使用文本编辑器中的查找功能。
6.  查找`__data_rollout__DarkMode.EnableDarkModeRollout__launched__`并将字符串从“false”更改为“true”。
7.  点击顶部的保存图标保存文件。
8.  关闭编辑器/文件管理器，打开谷歌手机应用程序。
9.  点击右上角的三点菜单，进入设置>显示选项
10.  你现在会看到一个黑色主题选项，启用它。
11.  就是这样！这里有一些谷歌手机应用程序在黑暗主题下的截图。

不幸的是，谷歌联系人应用程序尚未更新黑暗主题。这意味着当你点击任何联系人卡片时，你仍会在谷歌手机应用中看到浅色卡片。我们已经有了如何在谷歌联系人中启用黑暗主题的想法，但实际的主题还没有准备好，所以我们必须等待更新的测试版 APK。

截图归功于 XDA 成员 FlavioV。