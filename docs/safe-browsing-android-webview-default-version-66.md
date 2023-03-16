# 在版本 66 中，安全浏览将默认进入 Android WebView

> 原文：<https://www.xda-developers.com/safe-browsing-android-webview-default-version-66/>

恶意软件和网络钓鱼攻击继续威胁着在线安全。我们已经看到各种操作系统受到恶意软件攻击的影响，Android 就是其中之一。为了解决这个问题，谷歌已经将其 Android 安全功能整合到了 [Google Play Protect](https://www.xda-developers.com/google-play-protect-a-new-solution-to-keep-your-android-device-secure/) 中，该功能会定期扫描用户的应用程序以查找恶意软件。网络浏览是用户容易受到这些攻击的另一个领域，但谷歌的安全浏览自 2007 年发布以来一直因保护用户免受此类攻击而受到好评。

根据谷歌的说法，[安全浏览](https://www.xda-developers.com/latest-webview-introduces-isolated-renderer-process-and-in-app-safe-browsing/)保护超过 30 亿台设备免受“越来越多的威胁”，现在还包括桌面和移动平台上不需要的软件。现在，该公司宣布 Google Play Protect 正在默认为 WebView 带来安全浏览，从 2018 年 4 月 WebView 版本 66 的发布开始。

应用程序使用 WebView API 来显示 Android 中的 web 内容。2013 年，谷歌在 Android 4.4 KitKat 中用新的 Chromium 驱动的 WebView 取代了旧的 WebKit 驱动的 WebView。自 Android 5.0 Lollipop 以来，WebView 一直在谷歌 Play 商店上更新，自 Android 7.0 Nougat 以来，它由当前版本的谷歌 Chrome Stable 提供支持。

谷歌指出，自 Android 8.0 Oreo (API 级别 26)以来，WebView 中的安全浏览就已经存在，它使用了与 Android 版 Chrome 相同的底层技术。开发人员可以选择使用 WebView 在其 Android 应用程序中实现它，但现在，他们将不再需要进行任何更改来受益于这种保护。当触发安全浏览时，应用程序会显示警告并收到网络错误。谷歌补充说，为 API 级别 27 及以上构建的应用程序可以使用新的 API 定制这种行为，以实现安全浏览。

开发者现在可以使用安全浏览测试 URL(chrome://Safe-Browsing/match？type=malware)，同时使用当前的 WebView 测试版。他们还可以在 [Android API 文档](https://developer.android.com/reference/android/webkit/WebView.html)中了解更多关于定制和控制安全浏览的信息。

我们的观点:这意味着所有使用 WebView 的应用现在都可以安全浏览了。这有很大的潜力有利于用户的安全，这是一件好事。

* * *

[**来源:谷歌**](https://android-developers.googleblog.com/2018/04/protecting-webview-with-safe-browsing.html)