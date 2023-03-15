# 【更新:即将推出 Chrome 86】使用 bfcache 在谷歌 Chrome 中来回切换会快很多

> 原文：<https://www.xda-developers.com/back-forward-google-chrome-faster-bfcache/>

**更新 1(****07/24/2020****@****08:28am****ET):**。滚动到底部了解更多信息。下面保留了 2019 年 2 月 28 日发表的文章。

谷歌浏览器是世界上最受欢迎的网络浏览器，无论是在手机上还是在桌面上。多年来，它面临着相当多的批评，因为它占用了过多的内存，并且在大小和功能方面变得臃肿，但它也因其真实世界的速度和可用性而受到称赞。现在，谷歌宣布它正在开发一项新功能，使用 bfcache(向后-向前缓存)来改善网络浏览器中的向后-向前导航。

Google 声明，当导航离开一个页面时，后退/前进缓存(bfcache)会缓存整个页面，包括 JavaScript 堆。这样做是为了在用户向后导航时可以恢复页面的完整状态。该公司给出了一个用户离开时暂停页面，用户返回时播放页面的类比。它在向后导航和向前导航到先前访问的页面时都有效。

谷歌指出，这一功能在访问新网站时不会有帮助。但是，这并不意味着它没有用。据该公司称，在谷歌 Android 版 Chrome 浏览器上，有 19%的页面被浏览，在 PC 版 Chrome 浏览器上，有 10%的页面被浏览。据谷歌称，bfcache 将使导航“极快”。该公司指出，实现这一目标绝非易事。

谷歌指出，Mozilla Firefox 和 Apple Safari 对这种缓存技术的实现略有不同。然而，由于与 Chrome 的多进程架构不兼容，Chrome 选择不使用 WebKit 的 bfcache 实现。

Chrome 团队的工程经理 Addy Osmani 告诉*CNET*Chrome 的棘手之处在于重写浏览器的某些部分以保护隐私和安全。谷歌的网络浏览器必须确保它能阻止基于网络的 JavaScript 程序运行，即使这些程序还在内存中。他承认，在用户看来不存在的页面上运行 JavaScript 是“一个很大的潜在隐私问题”，因此，该公司将改变 Chrome 的架构，以确保隐私问题不会发生。

坏处呢？bfcache 不会很快出现在 Chrome 上。据奥斯马尼说，谷歌希望在 2019 年测试 bfcache，并在 2020 年将其内置到 Chrome 中。

另一个限制是保存网页状态以备后用会消耗内存，[这已经是 Chrome 面临的主要问题之一](https://www.xda-developers.com/site-isolation-roll-out-google-chrome-67/)。奥斯马尼表示，谷歌仍在试图找出最佳规则，以决定哪些页面应该保留，何时应该从内存中删除。他还表示，该功能可以帮助解决其他情况，例如当标签在后台时需要暂停的标签的更好性能，特别是在移动设备上。这种情况通常会节省内存，但它也有一个很大的缺点，因为页面在返回后必须重新加载。

Chrome 上的 bfcache 听起来肯定很有前景，但它目前还处于早期阶段。我们希望在接下来的几个月里了解更多信息。

**来源:[谷歌开发者](https://developers.google.com/web/updates/2019/02/back-forward-cache)**

**故事 Via:[CNET](https://www.cnet.com/news/chrome-should-get-extremely-fast-at-loading-a-whole-lot-of-web-pages/)**

* * *

## 更新:谷歌的“后退前进缓存”功能即将登陆 Chrome Android v 86

关于谷歌 Chrome 上的后退缓存功能的信息上一次成为新闻是在一年前，而即将推出的功能在此期间基本上被遗忘了。事实证明，随着 Android v86 版 Chrome 的推出，该功能已经越来越接近于在稳定发布渠道中发布。这可能会使在网站之间来回导航的速度更快。

**来源:[铬](https://groups.google.com/a/chromium.org/g/blink-dev/c/S9qRFx4ozXk/m/DNT8tiR3BAAJ?pli=1)**

**故事 Via:[Techdows](https://techdows.com/2020/07/chrome-android-back-forward-cache.html)**