# Android 11 将不会有过度扫描的功能，严重影响导航手势应用

> 原文：<https://www.xda-developers.com/google-confirms-overscan-gone-android-11-crippling-third-party-gesture-apps/>

如今，手势导航已经成为大多数智能手机的主要功能。早些年，围绕谁的导航手势做得最好有过一些争论，但谷歌让这场讨论变得多余，因为他们[强制要求纳入 Android 10 的导航手势](https://www.xda-developers.com/android-q-navigation-gestures-mandatory/)，同时将 OEM 解决方案降级为可选的额外功能。还有像 [XDA 自己的导航手势](https://www.xda-developers.com/navigation-gestures-1-20-16-stable/)这样的应用，它引入了几个选项，比如 iPhone X 风格的手势和隐藏原始导航栏的能力。然而，Android 11 最近的一个[变化将很快削弱像我们这样的第三方手势应用，因为新的操作系统版本删除了 overscan，这正是我们用来隐藏药丸的方法。](https://issuetracker.google.com/issues/154803290#comment8)

过扫描是电视中常见的一种现象，其中图像的一部分超出了屏幕的可视范围。电视通常有一个选项来纠正这一点，通过缩小(以及扩展)屏幕的可见边界，以便整个画面能够适合显示器。由于 Android 也能够在电视和机顶盒上运行，该操作系统也支持过扫描功能。“WM overscan”shell 命令被许多开发人员巧妙地用来将部分 UI 移出可视屏幕区域。我们自己的应用，[导航手势](https://forum.xda-developers.com/android/apps-games/official-xda-navigation-gestures-iphone-t3792361)，[依靠 Android 的 Overscan API](https://www.xda-developers.com/navigation-gestures-1-11-7-changelog/) 隐藏原来的导航条，不需要 root 手机。

现在，[谷歌已经证实【Android 11 不具备过扫描功能。](https://issuetracker.google.com/issues/154803290#comment8)

> 状态:无法修复(预期行为)
> 
> 感谢您的反馈。Overscan 已被删除，因为它不再被任何产品使用。

随着 Overscan 被完全从 Android 中移除，第三方手势应用程序将不可能在不植根于手机的情况下隐藏导航栏。不过，手势应用也不是唯一使用过扫描的应用。一些应用程序，如 [SecondScreen](https://play.google.com/store/apps/details?id=com.farmerbb.secondscreen.free) ，可以让你在输出到外部显示器时控制各种显示选项，还可以让你调整过扫描。新版本的 Android 可能不再提供这一功能。

[XDA 所有 Android 11 新闻](https://www.xda-developers.com/tag/android-11/)

* * *

感谢 Hani Mohamed Bioud 的提示！