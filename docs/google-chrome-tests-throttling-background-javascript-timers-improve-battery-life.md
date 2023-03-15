# 谷歌 Chrome 测试调节后台 JavaScript 定时器以延长电池寿命

> 原文：<https://www.xda-developers.com/google-chrome-tests-throttling-background-javascript-timers-improve-battery-life/>

为了减少谷歌 Chrome 对笔记本电脑电池寿命的影响，谷歌正在研究一种可以显著减少浏览器电池使用量的方法。根据最近来自 [*TheWindowsClub*](https://news.thewindowsclub.com/google-chrome-ships-a-new-feature-to-increase-the-battery-life-101417/) 的报道，该公司已经开始测试 [Chrome 86](https://www.xda-developers.com/chrome-64-bit-support-android-10/) 的一项实验性功能，该功能可以限制后台网页中的 JavaScript 定时器唤醒，并有可能将电池寿命延长两个小时。

该报告引用了谷歌的一份[技术文件，其中详细介绍了这项新功能，以及几个强调预期电池节省的实验。该文件透露，新的](https://docs.google.com/document/d/1sd9EVERCtRWKvnJXnP3iZ83fM3FLwDbjiyfMkaKWEYk/edit#) [Chrome 标志](https://www.xda-developers.com/tag/chrome-flags/)将 JavaScript 定时器唤醒限制为每分钟 1 次，很像苹果的 Safari 浏览器，并有助于在不破坏用户体验的情况下延长电池寿命。然而，节流将只针对那些不停止 visibilitychange 事件计时器的网页，以及那些没有切换到现代 API(如 MutationObserver、IntersectionObserver 或 requestAnimationFrame)的网页。

在使用 2018 款 MacBook Pro 15 英寸的测试中，谷歌 Chrome 开发者观察到，在没有启用标记的情况下，笔记本电脑在 Chrome 中浏览时放电 6.4 小时。同一台笔记本电脑在使用 Safari 时放电了 9.3 小时。然而，一旦启用了该标志，开发人员发现该笔记本电脑使用 Chrome 总共持续了 8.2 小时。在所有情况下，开发人员在前台打开一个空白标签，在后台打开 36 个标签。

在另一项实验中，开发人员用全屏播放的 YouTube 视频取代了空白标签，笔记本电脑在 Chrome 的当前状态下持续了 4.6 小时。启用 JavaScript 节流标志后，同一台笔记本电脑持续了 5.3 小时。

这个名为“在后台节流 Javascript 计时器”的实验性标志已经在谷歌 Chrome Canary 86 中可用，并且可以在 Windows，Mac，Linux，Android 和 [Chrome OS](https://www.xda-developers.com/tag/chrome-os/) 的 Chrome 上启用。根据[*bleeding computer*](https://www.bleepingcomputer.com/news/google/new-google-chrome-feature-to-drastically-reduce-battery-usage/)的消息，该功能计划在不久的将来与谷歌 Chrome 86 的稳定版本一起推出，并将默认启用。然而，Chrome Enterprise 用户将可以选择禁用该功能，一旦它成为默认行为。