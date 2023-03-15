# Chrome 操作系统上的 Android 应用程序将很快能够从 USB 驱动器中读取文件

> 原文：<https://www.xda-developers.com/chrome-os-android-apps-usb-drive/>

# Chrome 操作系统上的 Android 应用程序将很快能够从 USB 驱动器中读取文件

根据 Chrome OS Gerrit 最近的承诺，Chrome OS 上的 Android 应用程序将很快能够从 USB 驱动器中读取文件。

Chrome OS 的一大优点是它可以原生运行 Android 应用程序，这使它成为移动中 Android 智能手机的一个很好的补充。你可以在笔记本电脑上玩你最喜欢的 Android 游戏或运行你最喜欢的 Android 应用程序，同时保留谷歌应用程序套件的所有生产力功能。

然而，Chrome 操作系统上的 Android 应用程序并不完美，一个可能让用户恼火的问题是 Android 应用程序无法访问设备上的 USB 驱动器。鉴于 USB-A 端口并不普遍，这种限制在 Android 手机上可能是可以理解的，但这可能会令人沮丧，因为 Chromebooks 通常有一两个 USB-A 端口。

然而，现在 Chrome OS Gerrit 中的一项承诺表明，谷歌可能很快就会纠正这个问题。[提交](https://chromium-review.googlesource.com/c/chromium/src/+/854990)添加了一个新的 ARC 标志，以“允许 Android 应用程序在 ChromeOS 设备上使用 USB 主机功能。”这应该意味着，在下一个 Chrome OS 开发版本中，只要可用，Android 应用程序就可以访问插入 Chromebook 的 USB 设备上存储的文件。

这一变化将有利于媒体播放器、生产力应用程序或任何其他你可能想在 Chrome OS 上运行的 Android 专用应用程序，这些应用程序应该可以访问外部 USB 驱动器。无论如何，这都不是 Chrome OS 上 ARC 的主要补充，但这是我们在各种 Chrome OS 论坛上看到用户抱怨的事情，所以很高兴看到该功能被包括在内。在接下来的几个月里，你会在 stable 频道上看到这个新功能，所以如果对你有帮助的话，请留意 Chrome flags 页面。