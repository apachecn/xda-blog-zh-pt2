# Android 版 Chrome 将很快更新到 WebGL 2.0

> 原文：<https://www.xda-developers.com/chrome-for-android-to-be-updated-with-webgl-2-0-soon/>

WebGL JavaScript API 使得在网站上显示硬件加速的 3D 图形成为可能，并且最近变得越来越流行。在 Chrome for Windows、macOS 和 Linux 的第 56 版中，那些拥有现代图形硬件的用户现在可以利用 WebGL 2.0。这是对 API 的一次重大升级，使网站显示各种新的图形功能以及一些高级渲染技术成为可能。

谷歌最近更新了 Chrome 桌面版 57，所以如果 Chrome 是你的桌面浏览器的选择，那么你可能已经拥有这个功能有一段时间了。这里的消息是，谷歌已经宣布 WebGL 2.0 将“很快”进入 Android 的 Chrome。在这篇具体的帖子中，谷歌没有透露任何关于这将在何时发生的细节，但谷歌也正在向 Android 用户推出 57 版本。

[谷歌强调了昨天更新中的一些变化](https://chromereleases.googleblog.com/2017/03/chrome-for-android-update.html)，而 WebGL 2.0 在帖子中根本没有提到。然而，谷歌也宣布安卓版 Chrome 浏览器的[测试版正在更新](https://chromereleases.googleblog.com/2017/03/chrome-beta-for-android-update.html)到版本 58。当[在他们巨大的 Git 日志中筛选更新](https://chromium.googlesource.com/chromium/src/+log/57.0.2987.0..58.0.3029.21?pretty=fuller&n=10000)时，我们确实注意到 [WebGL 2.0 在这个版本中被默认启用](https://chromium.googlesource.com/chromium/src/+/52d9483cb732e314990f93bc7291927b6369c4f0)。这并不意味着它将在 58 版本的稳定构建中可用，但这很可能会发生。

这次将 Chrome 升级到 WebGL 2.0 的新更新实际上将使它的功能与 OpenGL ES 3.0 不相上下。除了新的渲染功能，更新后的 API 还引入了一个大幅扩展的一致性测试套件，Chrome 通过了多个 GPU 供应商的 100%测试。谷歌提到的这些测试是在桌面平台上进行的，但他们没有提到是否能够在 Android 上取得同样的成功。

[**来源:铬博客**](https://blog.chromium.org/2017/03/faster-3d-rendering-with-webgl-20.html)