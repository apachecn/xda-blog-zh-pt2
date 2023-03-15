# joo Dias 设计的旁路放大器链接

> 原文：<https://www.xda-developers.com/bypass-amp-links-deampify/>

早在 2015 年末，谷歌[推出了](https://googleblog.blogspot.com/2015/10/introducing-accelerated-mobile-pages.html)[加速移动页面](https://www.ampproject.org/) (AMP)项目，以彻底改变移动网络用户消费网络内容的速度。从那以后，许多网络出口(包括[我们自己的门户](https://www.xda-developers.com/accelerated-mobile-pages-what-are-they-and-how-do-i-implement-them/))都集成了 AMP，这样用户就可以通过有限或较慢的数据连接快速访问他们的内容。虽然有些人对谷歌向出版商推行 AMP 的方式感到不安，但其他人则哀叹这种新标准被强加到他们的移动设备上。对于那些使用快速连接的用户来说，加载一个 AMP 页面与加载原始页面在速度上没有明显的差别，但仍然会导致屏幕上显示的内容减少。然而，除非您使用的特定移动应用程序有一个选项禁止加载其 AMP 版本的页面，否则检索原始 URL 的唯一方法是[手动执行](https://www.xda-developers.com/google-to-make-it-easier-to-share-the-original-url-on-an-amp-site/) -添加两个额外的点击。多亏了我向 AutoApps 开发者 joo Dias 提出的一个想法，终于有了一种完全绕过放大器链接的方法。

这款应用名为 **DeAMPify** ，它的工作速度非常非常快。这是我做的一个样本屏幕记录。请注意，从我点击 DeAMPify 打开 URL 到原始 URL 在浏览器中打开之间的时间有多短。

* * *

## 它是如何工作的

应用程序将自己注册为 AMP 样式 URL 的默认 URL 处理程序。当用户选择在 DeAMPify 中打开一个链接(或者选择它作为默认处理程序，绕过对话框)时，应用程序会抓取 AMP 页面的 HTML 源代码来查找文章的原始 URL。一旦找到了原始的 URL，它就会获取该 URL 并将其传递给默认的浏览器应用程序。这个过程非常非常快，即使从技术上来说，您仍然在下载 AMP 页面的 HTML 源代码，但是在足够快的连接上，这几乎没有区别，因为 AMP 页面需要解析的数据量相对很小。然而，对于最终用户来说，结果是 AMP 链接被完全绕过，而是在该 URL 的默认应用程序中打开，无论是你的浏览器还是其他应用程序，如官方的 Reddit 应用程序或 XDA 实验室。

更详细地说，该应用程序专门通过查找 HTML 链接标签来抓取 AMP 页面中的“规范”(原始)文档，如下所示:

```
 <link rel="canonical" href="https://www.example.com/url/to/canonical/document.html"> 
```

每个 AMP 页面都在它的 HTML 源代码中嵌入了这个标签，作为官方规范的一部分。这使得 AMP pages 能够首先检测并向最终用户显示原始 URL，但我们可以利用这种嵌入式链接来绕过向用户显示移动优化页面的需要。这种方法击败了我们在网上找到的所有其他重定向工具，它们只是试图通过对 AMP URL 执行 regex 操作来检索原始内容 URL。由于 AMP 页面没有一致的 URL 方案，这种方法对于很多很多奇怪的页面来说都会失败。但这不会。

我们在制作这个应用程序时发现的一个警告是，当通过移动用户代理检索源时，规范链接没有嵌入到 HTML 源中，因此 DeAMPify 作为桌面浏览器用户代理运行。这对最终用户(你)来说并没有什么影响，但是对于任何想知道这个应用程序如何工作的人来说，这是一件有趣的事情。

* * *

## 带去放大器的旁路放大器链接

实际的应用程序本身。DeAMPify 做的比*多一点，只是*旁路放大器链接。我的意思是，这是 95%的应用程序，但它不会有趣，如果它*只有*这样做，不是吗？为了让这款应用更有用，迪亚斯给它增加了一些额外的功能(不过要使用它们，都需要在应用内购买):

*   网址例外:黑名单网址，你总是想打开的 AMP 网页，可以使用正则表达式进行这项工作
*   Tasker 集成:选择何时运行 bypass AMP 服务

Tasker 集成是我确信许多用户会发现有用的部分，例如，只有当连接到您的家庭 WiFi 时，您才能自动绕过 AMP 链接。如果有一两个特定的网站，你总是想加载链接，URL 例外可能是有用的，但就我个人而言，我还没有真正使用过这个功能。

从今天开始,[在谷歌 Play 商店](https://play.google.com/store/apps/details?id=com.joaomgcd.deampify)可以买到 DeAMPify。对于那些讨厌网络上无处不在的 AMP 页面膨胀的用户，你终于有了一个对 AMP 说不的解决方案。今天就摧毁你的网站！

如果你尝试在 Chrome 浏览器中打开谷歌搜索的 AMP 链接，这个应用将无法运行。不过，这并不是这款应用的错，因为当你在谷歌搜索中点击一个链接时，谷歌 Chrome 不会发送你的意图。