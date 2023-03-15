# 谷歌新的 Chrome 功能可以链接到页面上的特定文本

> 原文：<https://www.xda-developers.com/google-chrome-extension-link-to-text-fragment/>

**更新 1 (09/29/2020 @ 05:31 PM ET):** 谷歌正准备将链接到文本片段扩展的功能原生集成到谷歌 Chrome 中。滚动到底部了解更多信息。下面保留了 2020 年 6 月 18 日发表的文章。

谷歌很少发布自己的新 Chrome 扩展，但今天它做到了(通过 [*The Verge*](https://www.theverge.com/2020/6/18/21295300/google-link-to-text-fragment-chrome-extension-chromium-highlight-scroll-down) )。该公司最新的扩展被称为“链接到文本片段”，它允许你链接到网页上特定的文本部分。除了链接到整篇文章，您还可以共享一个链接，直接链接到您希望他人阅读的页面上的某个部分。

文本片段扩展的链接使用起来非常简单。一旦安装在 Chrome 或基于 Chrome 的支持扩展的浏览器中，你需要做的就是突出显示网页上的一些文本，然后右键单击。你会看到“复制链接到选定的文本”作为菜单中的一个选项，它会自动将链接复制到您的剪贴板。当有人访问 Chrome(或其他基于 Chrome 的浏览器，如 [Microsoft Edge](https://www.xda-developers.com/chromium-based-microsoft-edge-browser-windows-10-update/) )中创建的链接时，您选择的文本将以黄色高亮显示。它在 Android 上也能工作。

该扩展使用了最近添加到 Chromium 中的一个特性，名为“[文本片段](https://wicg.github.io/scroll-to-text-fragment/)”它的[基本上是](https://web.dev/text-fragments/#browser-compatibility)将额外的信息添加到网址的“#”之后，以导航到特定的部分。谷歌已经在使用这项技术从谷歌搜索链接到网页的特定部分[。使用 Link to Text Fragment 扩展创建的链接可以在基于 Chromium 的浏览器版本 80 及更高版本中工作。如前所述，这包括 Android 浏览器的 Chrome。](https://www.xda-developers.com/clicking-featured-snippets-in-google-search-will-now-take-you-directly-to-the-result/)

你可以现在就在 Chrome 网上商店下载文本片段扩展[的链接，或者在这里](https://chrome.google.com/webstore/detail/link-to-text-fragment/pbcodcjpfjdpcineamnnmbkkmkdpajjg)查看它的源代码[。诚然，这可能是一个小众的扩展，但对于经常分享长文章的人来说，它可能极其有用。它非常容易使用，直到你需要它的时候你才会意识到它的存在。看看这个。](https://github.com/GoogleChromeLabs/link-to-text-fragment)

* * *

## 更新 1:自带 Chrome

*更新由[米沙拉赫曼](https://www.xda-developers.com/author/mishaalrahman/)*

据 [*Techdows*](https://techdows.com/2020/09/copy-link-to-text-chrome.html) 报道，谷歌正在努力将文本片段链接扩展的功能烘焙到 Chrome 中。在 Mac、Window、Linux 和 Chrome OS 上的 Chrome Canary 频道中，您可以启用一个名为“复制文本链接”的标志，该标志“将一个项目添加到上下文菜单，以允许用户复制指向突出显示所选文本的页面的链接。”这个特性目前正在开发中，但是一旦推出，你将不再需要使用链接到文本片段扩展。