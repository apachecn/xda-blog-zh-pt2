# 谷歌 Chrome 80 稳定更新推出安卓和桌面

> 原文：<https://www.xda-developers.com/google-chrome-80-rolling-android-desktop/>

过去几周，谷歌一直在测试其流行浏览器 Chrome 的一系列新功能。我们已经看到了 Android 上 Chrome 新标签页全新用户界面的证据，Canary 中发现的自定义共享表，更少干扰的通知提示，等等。现在，谷歌已经开始在谷歌浏览器的最新更新中推出这些功能。根据来自*bleeding computer*的最新报告，Chrome 80 现在已经开始在 Android 和桌面上推出。此次更新带来了大量的安全修复、错误修复和一些新功能。以下是 Chrome 版本 80.0.3987.87 中包含的一些主要变化。

回到去年五月，谷歌[宣布了新的 cookie 控制](https://www.xda-developers.com/google-chrome-secure-cookie-controls-anti-fingerprinting-history-manipulation/)来改进谷歌 Chrome 管理 cookie 的方式。在最新的更新中，Chrome 正在实施默认安全的 cookie 分类系统，该系统旨在处理没有相同站点值的 cookie*same site = Lax*。谷歌声称只有 cookies 设置为*same site = None；Secure* 将在第三方环境中可用，条件是从安全连接访问它们。关于 SameSite cookie 变化的详细解释，您可以查看下面的视频。

### 

谷歌 Chrome 80 更新还通过重写 HTTPS 的网址来自动升级混合内容。浏览器不提供 HTTP 回退，如果网站无法通过 https://加载，就会阻止这些网站。我们[在去年 10 月](https://www.xda-developers.com/google-chrome-block-insecure-content-loading-https-pages/)了解到这个功能，根据 Chromium 博客上分享的时间表，Chrome 现在将自动更新混合音频和视频资源。然而，混合图像仍然允许加载，但是它们会在 omnibox 中显示“不安全”标签。

有了 Chrome 80，开发人员还可以将可缩放的 SVG 图像用作收藏夹图标。这反过来可以帮助他们减少任何网站或应用程序上此类资源的数量。此外，该更新还使作者和用户能够通过将页面中的文本片段添加到网站 URL 来链接网页的特定部分。当在浏览器中打开这样的 URL 时，添加的文本将在页面中高亮显示，Chrome 将自动滚动高亮显示的片段。

除了所有这些变化，最新的 Chrome 更新还带来了对 DevTools 的一系列[变化和改进，以及对浏览器中发现的 56 个漏洞的修复。](https://developers.google.com/web/updates/2019/12/devtools)

* * *

**来源:谷歌( [1](https://chromereleases.googleblog.com/2020/02/chrome-for-android-update.html) 、 [2](https://chromereleases.googleblog.com/2020/02/stable-channel-update-for-desktop.html) )、[铬博客](https://blog.chromium.org/2020/02/samesite-cookie-changes-in-february.html)**

**Via:[bleeding 电脑](https://www.bleepingcomputer.com/news/google/chrome-80-released-with-56-security-fixes-cookie-changes-more/)**