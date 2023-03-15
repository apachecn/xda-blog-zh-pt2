# Google Chrome 现在支持延迟加载 iframes 来加速页面加载

> 原文：<https://www.xda-developers.com/google-chrome-now-supports-lazy-loading-iframes-speeding-up-page-loads/>

# Google Chrome 现在支持延迟加载 iframes 来加速页面加载

在去年为 Chrome 添加了原生图像延迟加载功能后，谷歌现在让开发者延迟加载繁重的 iframes。继续阅读，了解更多信息！

来自全球移动用户和连接能力有限的人的 web 流量的增加，促使公司和开发者大力优化网站加载速度。传统上，当您导航到一个 web 页面时，它会下载并显示所有可用的内容:图像、图标、gif、样式、脚本等等。你可以想象，加载所有这些东西会导致网站启动延迟，尤其是对于网速较慢的用户。一段时间以来，谷歌一直在试图消除这个问题。就在去年，他们在谷歌 Chrome 76 中添加了[图片延迟加载功能](https://www.xda-developers.com/google-chrome-image-lazy-loading-speed-up-page-loading-mobile/)。现在，Google 给 iframes 带来了同样的功能。

延迟加载按需加载网页的内容，这意味着它们不会被下载和显示，直到你向下滚动并在视图中看到它们，从而降低了网站的初始启动速度。如前所述，自去年以来，Chrome 就提供了图像的延迟加载，但现在开发者也可以在 iframes 上使用相同的方法。要在您自己的网站上实现它，您所要做的就是为您的图像和/或 iframe 元素添加 *loading="lazy"* 属性。像 Firefox 和 Safari 这样的浏览器已经实现了原生图像延迟加载特性。至于 iframes，他们仍在努力修复一些错误。谷歌还提到，Chrome for Android 在 Lite 模式下会自动延迟加载屏幕外图像和 iframes。

具有讽刺意味的是，在测试 YouTube 视频嵌入(基于 iframe)在延迟加载时如何影响网页加载速度的过程中，Chrome 团队发现，他们“*将我们的页面在移动设备上的交互速度缩短了 10 秒。*“不用说，与传统的一访问网页就下载整个网页内容的方法相比，惰性加载具有真正的优势。

* * *

**来源:[web . dev](https://web.dev/iframe-lazy-loading/)**

**Via:[Techdows](https://techdows.com/2020/07/chrome-supports-iframes-lazy-loading.html)**