# 以下是 iOS 15.4 和 macOS 12.3 中 Safari 的所有新功能

> 原文：<https://www.xda-developers.com/safari-15-4/>

苹果周一发布了 MAC OS Monterey 12.3 T1 和 T2 iOS 15.4 T3，两者都包含了 Safari 网络浏览器的最新更新版本 15.4。除了两个操作系统通常的变更日志之外，苹果还发布了一篇博客文章，披露了最新 WebKit 引擎更新的所有变化，该引擎为所有平台的 Safari 提供动力。

Safari 15.4 增加了对<dialog>元素和::background 伪元素的支持，这些元素也包含在最近的 [Firefox 98 更新](https://www.xda-developers.com/firefox-98/)中。这些特性使得网站可以更容易地创建符合页面设计的对话框/弹出框，只需较少的自定义 JavaScript 和 HTML 代码。现在支持 web 开发人员的其他 CSS 功能，包括新的:has()伪类、层叠层、CSS 包容、新的视口单位和更多 calc()数学函数。这些新功能将使网络开发变得更容易，更重要的是，帮助 Safari 赶上 Chrome 和基于 Chrome 的浏览器(这反过来意味着使用 Safari 的人会有更少的坏网站)。</dialog>

Safari 更新也有一些新的 Web APIs。现在支持 BroadcastChannel，因此来自同一来源的选项卡、窗口、框架和服务人员都可以相互通信——对于跨多个选项卡和窗口运行的 web 应用程序来说，这是一个非常有用的功能。文件系统访问 API 提供了新功能，允许 web 应用程序访问本地文件和文件夹(经过许可)，并且添加了 Web Locks API。

苹果并没有强迫 Manifest V3 做出有争议的改变

苹果去年增加了对 WebExtensions API(本质上是 Chrome 的扩展 API 的克隆)的支持，Safari 15.4 也做了一些改进，以保持与 Chrome 的变化保持一致。随着 Chrome 88 的发布，谷歌去年推出了更新的 Manifest V3 API，Safari 现在支持新标准中的一切(如后台页面的服务工作者和新的动态/会话规则)。然而，苹果并没有强迫 Manifest V3 做出有争议的改变，这是针对网络请求的 [API 改变，限制了一些内容/广告拦截扩展的能力。苹果可能会决定在未来追随谷歌的脚步，但目前，新旧网络请求 API 都将得到支持。](https://www.xda-developers.com/google-chrome-manifest-v3-ad-blocker-extension-api/)

Safari 15.4 中还有一些其他更改，包括对 Web 检查器的更新、新的字体选项等等。如果你是一名网络开发人员，或者只是对 Safari 的内部工作方式感兴趣，我强烈建议你查看下面的源代码链接。

**来源:** [WebKit 博客](https://webkit.org/blog/12445/new-webkit-features-in-safari-15-4/)，[苹果](https://developer.apple.com/documentation/safari-release-notes/safari-15_4-release-notes)