# 修改后的谷歌 Chrome 浏览器为移动设备带来了开发者工具

> 原文：<https://www.xda-developers.com/modded-google-chrome-browser-developer-tools-mobile/>

# 修改后的谷歌 Chrome 浏览器为移动设备带来了开发者工具

XDA 初级成员 Alcatraz323 已经成功地将谷歌 Chrome 开发者工具集成到他为 Android 定制的 Chromium build 中。继续阅读，了解更多信息！

开源 Chromium 项目是谷歌 Chrome 的支柱，因此开发者可以自由定制浏览器的特性并添加额外的功能。山景城巨人决定不在 Android 版本中包括桌面版 Chrome 的几个功能，但由于 Chrome 源代码的可用性，售后开发社区成功移植了少量这样的组件(如[在 Android](https://www.xda-developers.com/at-least-3-chromium-based-browsers-enable-extensions-support-thanks-kiwi-browser/) 上引入了 Chrome 扩展支持)。XDA 少年成员 [Alcatraz323](https://forum.xda-developers.com/member.php?u=10682425) 现在已经做了类似的工作，他成功地将开发者工具集成到他为 Android 定制的 Chromium build 中。

对于那些不熟悉谷歌 Chrome 开发工具(通常被称为 [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools) )的人来说，这是一套内置于浏览器中的 web 创作和调试工具。与桌面环境不同，谷歌基本上强迫用户从 PC/Mac 上选择[“远程调试”选项](https://developers.google.com/web/tools/chrome-devtools/remote-debugging)，以便检查运行在 Android 设备上的页面。不仅感觉相当笨拙，而且这个设计也大大低估了现代 Android 设备*(以及它们越来越大的屏幕)*的能力。

像 Eruda 这样的现有项目通过注入远程托管的脚本，在任何 Android 浏览器上提供了一套工作的 DevTools。另一方面，Alcatraz323 的解决方案非常独特，因为它以最小的开销将 Chrome 的原生开发工具带回了浏览器。他的 Chromium fork 是开源的，没有与谷歌账户相关的 API。

如果您不想深入研究代码，那么只需抓取 APK 并将其加载到您的设备上。注意，Chromium fork 不支持基于 Intel 的 x86 Android 设备。

**Chromium for Android with DevTools:[从 GitHub 下载](https://github.com/Alcatraz323/F12Browser/releases) || [XDA 讨论线程](https://forum.xda-developers.com/android/apps-games/chrome-android-devtools-t4115763)**

最初的版本缺乏智能手机相关的 UI 优化(例如，在检查页面元素时没有浮动窗口)，尽管我们希望开发者在未来几天内实现这些功能。Alcatraz323 还发布了另一款应用，本质上是作为 Chrome Desktop 远程调试功能的替代品，可以从 Play Store 下载[。](https://play.google.com/store/apps/details?id=io.alcatraz.f12)