# 旧版本 Android 上的 Gmail 中的黑色主题，带有这个暴露的模块

> 原文：<https://www.xda-developers.com/enable-gmail-dark-theme-older-android-versions-xposed/>

# 使用这个暴露的模块在旧的 Android 版本上启用 Gmail 的黑暗主题

如果你已经暴露了，如果你还没有 Android 10，有一个简单的方法让 Gmail 的黑暗主题运行起来:安装这个模块！

Android 10 的全系统黑暗主题是最受期待的功能之一，允许用户通过一个开关将应用程序设置为完全黑暗或黑色。然而，这项功能的一个大问题是，它只在 Android 10 上受支持，尽管某些应用程序确实包括独立于系统值打开和关闭黑暗模式的手动开关，但大多数应用程序都没有。 [Gmail 支持黑暗模式](https://www.xda-developers.com/google-gmail-dark-mode-android/)，但只有 Android 10 用户才能看到切换。除非你已经曝光了。

**[x 曝光框架 XDA 论坛](https://forum.xda-developers.com/xposed)**

这个被曝光的模块名为 Gmail Dark Theme Enabler，它只做一件事:不管你有没有 Android 10，它都会让主题切换可见。它应该在 Android Pie 和更低版本上运行得很好，同样，只要你安装了 Xposed 或 EdXposed。如果你不熟悉 EdXposed，这是一个非官方版本的 Xposed 框架，可用于较新的 Android 版本和手机，你可以[参考这篇文章](https://www.xda-developers.com/xposed-framework-unofficial-port-android-pie/)了解更多信息。

您现在就可以从 Xposed 存储库中下载这个模块。看看吧！

**[下载 Gmail 黑暗主题启用程序！](https://repo.xposed.info/module/com.alex193a.gmdtenabler)**