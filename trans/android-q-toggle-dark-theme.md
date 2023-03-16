# 如何切换 Android Q 隐藏的全系统黑暗主题

> 原文：<https://www.xda-developers.com/android-q-toggle-dark-theme/>

# 如何切换 Android Q 隐藏的全系统黑暗主题

谷歌 Pixel 智能手机的第一个 Android Q 测试版有一个隐藏的全系统黑暗主题，你可以通过简单的 ADB 命令来启用(或禁用)。

今天早些时候，谷歌[发布了第一个 Android Q 测试版，适用于所有三代 Pixel 设备:谷歌 Pixel/Pixel XL、Pixel 2/Pixel 2 XL 和 Pixel 3/Pixel 3 XL。这是我们将在最终发布前得到的 6 个测试版](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/)中的第一个[，还有一大堆](https://www.xda-developers.com/android-q-beta-release-schedule/)[新功能](https://www.xda-developers.com/android-q-new-features/)。谷歌为新的 Android 版本发布了很多文档，我们需要一些时间来浏览。我在 Pixel 3 XL 上闪现了 Q 测试版，以找到任何尚未被我们的泄露所覆盖的新功能，老实说，测试版中没有多少面向用户的功能是我们尚未发现的。然而，对许多人来说，Android Q 的一个主要特性——全系统黑暗模式——神秘地消失了。

有些人更新到 Q 时启用了它，而有些人(像我一样)更新时没有任何办法在设置中启用它。你可以通过打开电池节电模式来启用系统范围的黑暗主题，但是如果你依赖于及时获得通知，电池节电模式并不是你想要保持启用的。由于人们从 Android Pie 更新到 Android Q 时已经启用了黑暗主题，这让我想到:这是怎么发生的？我的结论是，这些用户在升级到 Q 之前，必须在开发者选项中启用强制夜间模式设置。该设置已经从 Q beta 中消失，但仍然可以通过 ADB 手动启用它。以下是方法。

## 切换安卓 Q 的隐藏黑暗模式

1.  1.  遵循本教程，从您的电脑上启用 ADB 。
    2.  将你的 Pixel 插入你的 PC，在你存储 ADB 二进制文件的同一个目录下打开命令提示符或终端窗口，输入以下命令:**启用黑暗模式:** `adb shell settings put secure ui_night_mode 2` **禁用黑暗模式:** `adb shell settings put secure ui_night_mode 1`
    3.  如果您使用的是 Windows PowerShell，那么您可能需要在命令前添加一个“.”。如果您使用的是 macOS 或 Linux，那么您可能需要在命令前添加一个. .。
    4.  重新启动你的像素和系统范围的黑暗模式应该切换。

我不完全确定为什么谷歌在 Android Q 测试版中取消了黑暗模式。最可能的解释是它仍在开发中。我希望它能在未来的测试版中启用，因为开发者需要时间来测试他们的应用。出于某种原因，这个开关不仅在设置、系统界面和框架中启用黑暗模式，而且还强制所有应用程序进入黑暗模式，这在 Google 相册中看起来很糟糕。在泄露的 Android Q beta 中，我能够为系统应用程序启用黑暗模式，但保持强制黑暗模式禁用——这在这里似乎是不可能的。我仍在研究这是否可能，但我相信我们将需要 root 访问权限，因为该标志与系统属性 debug.hwui.force_dark 相关联。

关注 [Android Q 标签](https://www.xda-developers.com/tag/android-q/)了解更多关于最新 Android 版本的新闻！