# Chrome 72 增加了可信的网络活动，允许网络开发者在 Play Store 上发布渐进式网络应用

> 原文：<https://www.xda-developers.com/chrome-72-trusted-web-activities-pwa-play-store/>

# Chrome 72 增加了可信网络活动，让网络开发者在 Play Store 上发布渐进式网络应用

Chrome 72 for Android 现在允许网络开发者在 Play Store 中发布他们的网站作为渐进式网络应用，使用一种称为可信网络活动的功能。

由于 Chrome for Android all things 的更新，谷歌的 Play Store 正在获得一个全新的应用类别。现在，Android 版 Chrome 的稳定频道更新到了 72 版，[渐进式网络应用](https://www.xda-developers.com/progressive-web-apps-replace-google-chrome-apps/)现在可以发布到 Play Store，这要归功于谷歌[在 2017 年宣布的一项名为可信网络活动](https://www.xda-developers.com/google-trusted-web-activities-full-screen-activities-web-content/)。

正如谷歌 Chromium 博客中所描述的，“可信网络活动(TWA)在没有浏览器用户界面的 Android 应用程序中显示全屏 Chrome 浏览器。”“可信”的名字意味着谷歌验证活动(发布到 Play Store 的渐进式 Web 应用程序)及其相应的网站都属于同一开发商。例如，由于我没有开发网站[allmusic.com](http://www.allmusic.com)，我不能发布一个 AllMusic Progressive Web App (PWA)到 Play Store。

虽然这可能会与通过 Chrome 自定义标签或 Android 系统 WebView 或其他方式使用网络内容的应用程序混淆，但最明显的区别是受信任的网络活动没有浏览器 UI。此外，与 WebView 实现不同，TWAs 允许独特的 Chrome 功能，如网络推送通知、后台同步和表单自动填充(例如，如果 Chrome 存储了您的联系信息，TWA 可以为您填充该信息)。

虽然使用 Chrome 72 的可信网络活动将渐进式网络应用发布到 Play Store 并不像在 Google Play 开发者控制台中键入 URL 并点击“发布”按钮那样简单，但现在开发者应该更容易将网站转换为用户可以从 Play Store 下载的 Android 应用。就个人而言，我很乐意看到 allmusic.com 的开发者利用这个特性。

* * *

[**来源:谷歌(Chromium Blog)**](https://blog.chromium.org/2019/02/introducing-trusted-web-activity-for.html)[**Via:Maximiliano Firtman**](https://medium.com/@firt/google-play-store-now-open-for-progressive-web-apps-ec6f3c6ff3cc)