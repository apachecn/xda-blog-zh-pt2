# 谷歌 Chrome 应用不再是 Android 10 中的 WebView 提供商

> 原文：<https://www.xda-developers.com/google-chrome-no-longer-webview-provider-android-10/>

Android 的 WebView 功能经历了一段坎坷的历史，在过去几年中经历了数次演变。Android 4.4 KitKat 在 2013 年首次推出了基于 Chromium 的 WebView 组件。当时，它内置于系统中，但后来随着 Android 5.0 Lollipop 的推出，它成为了一个单独更新的组件。然而，使用 Android 7.0 牛轧糖，所有与 WebView 相关的任务都由[谷歌 Chrome](https://www.xda-developers.com/google-chrome-grid-tab-layout-tab-hover-previews-themes/) 处理，以简化事情。对于谷歌来说，这似乎是合乎逻辑的前进道路:将 WebView 转移到 Chrome 意味着少了一个需要更新或关心的应用程序(尽管他们仍然更新了应用程序:它仍然在那里，只是没有被使用)，但随着最新的 Android 版本，他们似乎正在逆转路线，再次兜了一圈。

在 Android 10 中，谷歌已经恢复到牛轧糖之前的行为，WebView 现在再次由一个单独的应用程序处理。根据谷歌工程师的说法，这种更新的实现被称为“三色”。这似乎和牛轧糖之前的 WebView 实现没什么区别；它与谷歌 Chrome 分开更新，仍然使用 Chromium 基础，这意味着如果你是一个普通用户，你应该不会注意到任何不同。

*“Chrome 在 Q+中不再作为 WebView 实现使用。我们已经转向在 Chrome 和 WebView 之间共享公共代码的新模式(称为“Trichrome”)，这种模式同样有利于减少下载和安装规模，同时减少奇怪的特例和错误。”*

然而，有一个关键的区别，那就是事实上，就像 Chrome 一样，这个 WebView 组件现在也将在 Play Store 中有 4 个独立的发布渠道:Stable、Beta、Dev 和 Canary，它们应该与 Chrome 的对应产品保持一致。您还可以通过下载它们，进入“开发者选项”中的“WebView 实现”部分，并更改您的 WebView 提供商，在这些发布渠道之间进行切换。

正如我们之前所说的，这对最终用户来说无关紧要，因为他们不应该注意到。但简而言之，这意味着谷歌 Chrome 又回到了仅仅是一个浏览器的状态，独立的 WebView 组件现在可以处理所有与 WebView 相关的任务。

你怎么看待这种变化？请在评论中告诉我们。

* * *

**来源 1: [Google Issue Tracker](https://issuetracker.google.com/issues/140572934) |来源 2:[Chromium Project](https://chromium.googlesource.com/chromium/src/+/HEAD/android_webview/docs/channels.md)| Via:[Android Police](https://www.androidpolice.com/2019/09/19/android-10-no-longer-uses-chrome-app-to-render-pages-inside-apps/)**