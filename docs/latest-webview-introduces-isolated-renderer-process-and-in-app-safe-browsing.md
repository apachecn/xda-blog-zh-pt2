# 最新的 WebView 引入了独立的渲染器流程和应用内安全浏览

> 原文：<https://www.xda-developers.com/latest-webview-introduces-isolated-renderer-process-and-in-app-safe-browsing/>

谷歌发布了一份关于 WebView 最新版本变化的简短回顾。Android WebView 是 Android 的一个系统组件，允许 Android 应用程序直接在应用程序中显示来自 web 的内容。

从 Android Lollipop 开始，谷歌决定将 WebView 作为独立的 APK 发布，每六周从 Play Store 更新一次。目标是迅速向用户提供关键的修复，因为该服务已经遇到了一些严重的安全难题。该应用的最新版本也带来了一些重要的安全增强。

谷歌将在今年夏天晚些时候发布 Android O。在发布的同时，WebView 将让渲染器在独立于主机应用程序的独立进程中运行，利用 Android 提供的进程间的隔离，这种隔离也可用于其他应用程序。

WebView 现在将提供两种隔离级别。

1.  渲染引擎被分割成一个独立的进程。这使主机应用免受渲染器过程中的错误或崩溃的影响，并使能够利用渲染器的恶意网站更难利用主机应用。
2.  To further contain it, the renderer process is run within an isolated process sandbox that restricts it to a limited set of resources. For example, the rendering engine cannot write to disk or talk to the network on its own.

    It is also bound to the same seccomp filter as used by Chrome on Android. The seccomp filter reduces the number of system calls the renderer process can access and also restricts the allowed arguments to the system calls.

最后，WebView 的最新版本允许第三方应用程序使用安全浏览功能。根据博客条目，可能是恶意网站的信息或通知警告每月显示超过 2.5 亿次。通过一个简单的 manifest 标签，您可以在您的应用程序中启用安全浏览。你可以通过访问 Android 开发者博客来了解你需要添加哪些代码。

最新版本的 WebView 应该很快就能在 Google Play 商店买到。

* * *

[**来源:安卓开发者博客**](https://android-developers.googleblog.com/2017/06/whats-new-in-webview-security.html)