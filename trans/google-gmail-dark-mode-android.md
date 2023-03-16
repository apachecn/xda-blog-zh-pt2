# 【更新:官方消息】谷歌终于开始在 Android 10 的 Gmail 应用中推出黑暗模式

> 原文：<https://www.xda-developers.com/google-gmail-dark-mode-android/>

**更新(美国东部时间 2019 年 9 月 24 日上午 11 点 15 分):**谷歌宣布，他们正式推出 Gmail 的黑暗模式。

Android 10 中最受欢迎的新功能是全系统黑暗主题。内置的黑暗模式开关使设置、系统用户界面和框架呈现更暗的材质设计颜色，但它也可以在受[支持的第三方应用](https://www.xda-developers.com/reddit-for-android-android-q-dark-mode/)中启用黑暗模式。谷歌[表示](https://www.xda-developers.com/android-q-ama-summary/)他们将在稳定的 [Android 10](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/) 发布之前更新他们所有主要的 Android 应用程序，以拥有黑暗主题，虽然他们已经更新了许多应用程序，但仍有一些保留。值得注意的是，谷歌 Play 商店和 Gmail 应用程序在 Android 10 发布前未能接收黑暗模式，但在发布一周后，后者终于获得了其承诺的黑暗主题更新。

正如多名用户在 Reddit 上首次提到的那样，Android 版 Gmail 应用程序的最新版本 2019.08.18.267044774.release 具有全功能的黑暗模式。我们手动激活了该功能，以确认它正在工作。下面是我在运行 Android 10 的 Pixel 2 XL 上拍摄的一些截图。你可以看到现在在常规设置中有一个主题选项，让你在亮、暗和系统默认选项(即遵循 Android 10 设置中的黑暗模式切换。)启用深色主题后，背景颜色会变成深灰色，出现在收件箱的所有文件夹和大多数电子邮件中。

微软在电子邮件应用中推出了黑暗模式，勉强击败了谷歌，但我们很高兴看到谷歌并没有花很长时间赶上来。一旦 Gmail 黑暗模式更广泛地推出，我们会让你们都知道。

Gmail 应用程序的黑暗模式版本正在谷歌 Play 商店上推出，但你也可以从 APKMirror 下载。如果你想手动启用黑暗模式，你需要 root 权限，这样你就可以在`/data/data/com.google.android.gm/shared_prefs/FlagPrefs.xml`中将`DarkThemeSupport__dark_theme_support`布尔标志设置为真。将此标志设置为 true 后，保存文件，然后强制关闭 Gmail 应用程序。我试图在运行 Android 9 Pie 自定义 ROM 的华硕 ZenFone 6 上启用此标志，但我无法让黑暗主题工作。如果你在早于 10 的 Android 版本上使用 Gmail 黑暗模式，请在下面的评论中告诉我们！

* * *

## 更新:官方

谷歌正式为 Android 和 iOS 用户推出黑暗主题。从今天开始，它将向 Android 10 用户推出，可能需要超过 15 天才能到达所有设备。该主题将自动遵循 Android 10 中的系统设置，但你也可以从 Gmail 应用程序手动打开它。黑暗主题也适用于所有 G 套件版本。

**来源:[谷歌](https://gsuiteupdates.googleblog.com/2019/09/dark-theme-android-ios.html?m=1)**