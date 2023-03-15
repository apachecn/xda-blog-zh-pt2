# Native Alpha 可以让你将任何网站转换成 Android 上的原生全屏网络应用

> 原文：<https://www.xda-developers.com/native-alpha-lets-you-transform-any-website-into-a-native-fullscreen-web-app-on-android/>

# Native Alpha 可以让你将任何网站转换成 Android 上的原生全屏网络应用

Native Alpha 是一个开源的 Android 应用程序，由 XDA 初级成员 cylonid 创建，它可以帮助你将任何网站转换为原生全屏 web 应用程序。

由于可以访问更多的 API，本机应用程序可以提供与底层操作系统的更丰富的集成，但运行基于 web 的应用程序也有其自身的好处。[渐进式网络应用](https://web.dev/progressive-web-apps/) (PWAs)不仅可以[改善移动体验](https://www.xda-developers.com/case-study-progressive-web-apps-reduce-load-time-improves-ux/)，而且由于有了 [WebAPK](https://developers.google.com/web/fundamentals/integration/webapks) 标准，还可以表现得与常规 Android 应用程序非常接近。虽然许多浏览器允许你把你最喜欢的网站转换成一个网络应用程序，但是制作一个合适的 PWA 也需要网络开发者做一些工作。此外，超级用户几乎没有自定义 PWA 生成过程的自由。

XDA 少年成员[赛昂 id](https://forum.xda-developers.com/member.php?u=10954689) 创建了一个有趣的应用程序，名为**原生阿尔法**(风格化为**原生阿尔法**)，允许你在 PWA 创建过程中修改不同的参数。这个应用程序最有用的功能是它可以在一个原生的、无边框的全屏窗口中显示任何网站——甚至是那些没有有效的渐进式 Web 应用程序清单的网站。如果您想在每个站点的基础上修改 cookies 或 JavaScript 相关的设置，您可能会发现 *Native Alpha* 非常方便。默认情况下，该应用依赖于内置的 Android WebView，但如果你有 root 权限，它允许你选择不同的 WebView 提供商。例如，您可以使用*原生 Alpha* 设置一个 AdBlock Plus 自定义 WebView，以便生成的 PWA 没有广告。

下面是由 *Native Alpha* 提供的功能的概要:

*   使用 Android 系统 WebView 在无边框全屏窗口中显示任何网站。
*   提供创建主屏幕快捷方式和检索合适分辨率的图标。
*   可以为每个 web 应用单独设置各种设置(JavaScript、cookie、第三方 cookie、缓存)
*   浏览时使用多点触控手势导航。
*   使用 adblock Plus 自定义 webview 选择加入 AdBlock。
*   与本机应用程序相比，内存占用更少，没有侵犯隐私的应用程序权限
*   Android 10+的黑暗模式

由于使用了现代快捷方式 API，该应用程序需要 Android Oreo 或更高版本，但开发者计划稍后添加传统快捷方式支持。Native Alpha 本身是开源的，源代码[可在开发者的 GitHub 简介](https://github.com/cylonid/NativeAlphaForAndroid/)上获得。

**安卓原生 Alpha:[下载](https://github.com/cylonid/NativeAlphaForAndroid/releases)| |[XDA 讨论线程](https://forum.xda-developers.com/android/apps-games/app-native-alpha-transform-website-t4132849)**