# 奇异果浏览器的最新更新为 Android 带来了谷歌 Chrome 扩展

> 原文：<https://www.xda-developers.com/kiwi-browser-google-chrome-extensions-android/>

谷歌的开源 Chromium 浏览器是许多非谷歌开发的网络浏览器的基础。[微软 Edge for Windows](https://www.xda-developers.com/microsoft-chromium-based-browser-replace-edge/) 、 [Brave Browser](https://www.xda-developers.com/brave-browser-blocks-ads/) 和 [Opera](https://www.xda-developers.com/opera-touch-new-mobile-browser-optimized-one-handed-use/) 只是运行在 Blink 浏览器引擎(Chromium 的浏览器引擎)上的一些主要网络浏览器。)尽管这些浏览器都运行在相同的引擎上，但它们支持的功能却大相径庭。几乎所有基于 Chromium 的 Android 浏览器都缺少的两个功能是书签和与谷歌的历史同步以及对 Chrome 扩展的支持。前者可以通过桌面扩展来解决，这就是 Brave Browser 和[三星互联网](https://www.xda-developers.com/samsung-internet-92-beta-one-ui-night-mode-smart-anti-tracking/)提供 Chrome 同步功能的方式。然而，后者要复杂得多，因为谷歌官方的 Android 版 Chromium 不支持谷歌 Chrome 扩展。这并没有阻止 XDA 资深会员 arnaud 42 [, Kiwi 浏览器的开发者，在他最新版本的浏览器中加入 Chrome 扩展支持。

Kiwi 是一个快速的基于 Chromium 的浏览器，去年出现在我们的论坛上。该浏览器由 arnaud42 开发，具有[内置黑暗主题、广告拦截器](https://www.xda-developers.com/kiwi-chrome-browser-dark-theme-ad-blocker/)、[底部地址栏](https://www.xda-developers.com/kiwi-browser-chrome-home-bottom-address-bar/)、[边缘历史滑动手势](https://www.xda-developers.com/kiwi-browser-edge-history-swipe-gestures/)、[可达性按钮](https://www.xda-developers.com/kiwi-browser-update-reachability-button/)，以及许多其他改进。现在，浏览器的最新更新增加了对导入任何不依赖于 x86 二进制代码的谷歌 Chrome 扩展的支持。这意味着并不是所有的扩展都能工作，但是许多现有的 Chrome 扩展应该可以正常工作。据开发者称，像 Stylus、 [YouTube 黑暗主题](https://chrome.google.com/webstore/detail/youtube-dark-theme/icgoeaddhagkbjnnigiblfebijeinfme?hl=en)、[绕过付费墙](https://github.com/iamadamdev/bypass-paywalls-chrome)，甚至[uBlock](https://www.ublock.org/)/[u matrix](https://chrome.google.com/webstore/detail/umatrix/ogfcmafjalglgifnmanfmnieipoejdcf?hl=en)这样的扩展都在工作。你甚至可以从 TamperMonkey/ViolentMonkey 安装脚本。继去年 Yandex 浏览器增加支持后，Kiwi 现在是第二个支持桌面 Chrome 扩展的 Chrome 浏览器。

你可以从 XDA 实验室下载奇异果浏览器。虽然该应用程序也可以在 Google Play 上使用，但开发者正在以 XDA 独家 24 小时的形式发布最新版本。

[**从 XDA 实验室下载奇异果浏览器**](https://labs.xda-developers.com/store/app/com.kiwibrowser.browser)

如果你从 XDA 实验室下载它有问题，你可以从[开发者的 GitHub 页面这里](https://github.com/kiwibrowser/android/releases/tag/Upsilon)下载最新版本。

## 如何在奇异果浏览器中安装谷歌 Chrome 扩展

一旦您安装了最新版本的 Kiwi 浏览器，您首先需要启用扩展支持:

1.  打开奇异果浏览器，在地址栏输入 chrome://extensions。
2.  启用开发人员模式。(如果没有显示，您可能需要重新加载选项卡。)

然后，你可以用两种方法之一安装 Chrome 扩展:

### 更容易的

1.  在桌面模式下导航到 [Chrome 商店](https://chrome.google.com/webstore/category/extensions)。
2.  选择您选择的扩展名。
3.  安装它。就是这样！

### 更坚固的

1.  安装[总指挥官文件管理器](https://play.google.com/store/apps/details?id=com.ghisler.android.TotalCommander)。其他文件管理器可能会工作，但 Kiwi Browser 需要一个其他文件管理器(如默认应用程序)在选择文件时可能不会提供的文件 URI。
2.  下载一个 Chrome 扩展文件。CRX 格式。这个网站会帮你解决这个问题。
3.  将文件的文件扩展名从。CRX 到。活力
4.  打开包装。使用像 [RAR](https://play.google.com/store/apps/details?id=com.rarlab.rar) 这样的应用压缩到一个文件夹。其他存档管理器应用程序可能会工作，但我没有成功使用 MiXplorer 的取消存档工具。
5.  点按“载入解压缩的扩展”
6.  使用 TotalCommander (TotalCmd file://)选择 manifest.json 文件。扩展应该会加载，但是它可能不会显示在 chrome://extensions 中，直到你刷新标签。如果您遇到一个错误，说明文件开头的 _ 字符不被接受，请尝试从解压缩的扩展名中的元数据文件夹的开头删除 _ 字符。

* * *

随着 Kiwi 浏览器的最新更新，它已经成为谷歌 Chrome 的近乎完美的替代品。唯一缺少的是浏览器同步，正如我们已经看到的，通过变通方法已经可以实现。如果你还没有使用奇异果，现在是一个很好的转换时机。如果你这样做了，请务必访问[开发者的 XDA 论坛主题](https://forum.xda-developers.com/android/apps-games/app-kiwi-browser-chromium-adblock-caf-t3797252)以给出反馈。