# 渐进式网络应用程序现在可以在桌面 Chrome 上启用——下面是方法

> 原文：<https://www.xda-developers.com/progressive-web-apps-chrome-how-to/>

Chrome 上的应用程序通常提供良好的用户体验，但对于必须浏览浏览器专有 API 的开发人员来说，它们可能是噩梦。幸运的是，谷歌正在采用一个平台- [渐进式网络应用](https://www.xda-developers.com/progressive-web-apps-replace-google-chrome-apps/) -这消除了许多复杂性，并且在最新稳定版本的 Chrome 中得到支持。

在 Chrome 中启用渐进式网络应用很容易。假设您的客户端是最新的，您所要做的就是切换三个开发标志: **[应用横幅](chrome://flags/#enable-app-banners)** 和 **[实验性应用横幅](chrome://flags/#enable-experimental-app-banners)、**，它们启用让您安装 web 应用的提示；以及 [**桌面 PWAs**](chrome://flags/#enable-desktop-pwas) ，增加了对 PWAs 的窗口和横幅支持。

如果链接对您不起作用，请尝试将这些 URL 复制并粘贴到地址栏中:

 <picture>![](img/95b9760b7fa8df7f710a89e4d9335c77.png)</picture> 

Progressive Web App flags in Chrome.

从那时起，事情就变得容易了。一旦你启用了相关标志并输入了 PWA 的网址，你会在 Chrome 的下拉菜单中看到一个**安装到桌面**选项。

然后你会得到一个**安装到桌面**弹出提示。点击**添加**会将 PWA 保存到你电脑的桌面上，在那里你可以像启动任何 Chrome 应用程序一样启动它。

如果你还没听说过，PWAs 是在考虑桌面应用灵活性的基础上设计的网络应用。它们从图标和快捷方式启动，就像本地应用程序一样，但它们对 CSS3、JavaScript 和其他开放 web 框架的依赖使它们可以跨浏览器和平台工作，只需最少的移植。通过使用插件、web APIs 和脚本的组合，他们能够处理网络请求、推送通知、内容获取等任务。

PWAs 有很多让人喜欢的地方。他们有潜力[减少加载时间和数据使用](https://www.xda-developers.com/case-study-progressive-web-apps-reduce-load-time-improves-ux/)，有些甚至有[比他们的本地对手更好的用户界面](https://www.thinkwithgoogle.com/intl/en-gb/advertising-channels/mobile/settled-reduces-mobile-page-load-times-nearly-3x/)。但它们并不完美。例如，Chrome 缺乏 PWA 的第一方店面——要找到应用，你必须搜索像 [PWA.rocks](https://pwa.rocks/) 这样的社区展示。PWAs 还不能充分利用 Chrome。在去年年底的一份声明中，谷歌表示，它一直在“研究为依赖独家 Chrome 应用程序 API 的开发者简化过渡的方法。”

不管喜欢与否，谷歌正在全力推进 PWAs。2017 年，这家搜索巨头宣布，它将在“2018 年年中”之前逐步取消对 Windows、Mac 和 Linux 上的 Chrome 应用程序的支持，转而支持 PWAs。