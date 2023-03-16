# 【更新 3:设置切换直播标志】谷歌 Chrome 的黑暗模式也可能使网页变暗

> 原文：<https://www.xda-developers.com/google-chrome-dark-mode-darken-web-pages/>

**更新 3(美国东部时间 9/24/19 @ 12:05PM):**Android 用户将很快获得 Chrome 网页黑暗模式的切换。

**更新 2(美国东部时间 8/28/19 @上午 10:50):**Android 强制黑暗模式的 Chrome 将在设置的新“主题”部分提供。

**更新 1(2019 年 2 月 20 日@美国东部时间下午 1 点 54 分):**这篇文章发表几个小时后，负责变更的提交被合并，我们抓取了一些截图。

谷歌的[材质主题革新](https://www.xda-developers.com/material-design-redesign-gmail-google-photos/)一直以亮白色为主，并不是每个人都喜欢随处可见的炫目白色。他们花了几年时间，但谷歌最终意识到，许多用户确实在寻找一个更黑暗的 UX。[几个谷歌应用](https://www.xda-developers.com/youtube-dark-mode-android-roll-out/)已经采用了黑暗主题，谷歌 Chrome 正在迎头赶上。据[报道，用于 macOS 的谷歌 Chrome 获得了原生黑暗模式](https://www.xda-developers.com/google-chrome-dark-mode-macos/)，用于 Windows 10 的谷歌 Chrome 也在金丝雀发布频道获得了黑暗模式。谷歌 Android 版 Chrome 也在测试 Chrome 73 Beta 的夜间模式，但这一设置仅限于浏览器 UI。

Chromium 的 Gerrit 发布了一条[新代码变更](https://chromium-review.googlesource.com/c/chromium/src/+/1478106)(via[*9 to 5 Google*](https://9to5google.com/2019/02/19/android-chrome-webview-web-dark-mode/))，这表明 Chrome for Android 计划做的不仅仅是主题化自己的 UI 元素。当用户在浏览器中选择深色主题时，该应用的未来版本会将网页重新着色为更深的颜色。提交添加了*# enable-Android-we b-contents-dark-mode*标志，该标志启用了允许浏览器使用其内置高对比度设置的其他首选项。高对比度设置通常用于辅助功能，因此这不会影响浏览器或网页的性能。但是，由于这确实会以开发人员不希望的形式显示网站，因此可能会导致网站内的视觉不匹配，这取决于网站的构建方式。

旗帜背后的潜在变化也指向 Android 内置的 WebView 浏览器获得夜间模式功能。这两者，Android 的 Chrome 和 Android WebView 将来都可以使网页变暗。Chrome 针对网络内容的实验性黑暗模式应该会在未来几天内进入金丝雀发布渠道，而 WebView 的测试版需要更多时间才能获得这一功能。

* * *

## 更新 1:提交合并，所以这里是截图

这篇文章发表几个小时后，负责变更的提交被合并。我们决定下载一个新编译的 Chromium APK 来看看网页中新的黑暗模式是什么样子的。这里有一个前后对比。正如你所看到的，它仍然是一个正在进行的工作，因为它只是颠倒了大部分页面内容，包括图像。

* * *

## 更新 2:进入设置

 <picture>![](img/a2ef8093e4f9164eebfe34caf3d19e8a.png)</picture> 

Current Themes settings

Android 版 Chrome 的强制黑暗模式设置正在转向面向消费者的位置。根据最近的一次提交，以前可以通过在所有平台上切换 Chrome 标志来获得，现在可以在设置的新“主题”部分获得。主题设置包括“系统默认，亮”和“暗”当选择系统默认或黑暗时，会出现一个复选框来启用强制黑暗模式。

**来源:[铬革里特](https://chromium-review.googlesource.com/c/chromium/src/+/1762543)**

* * *

## 更新 3:设置标志切换实时

Chrome 网页的黑暗模式现在可以在 Android 10 的 Chrome Canary 中切换。可以使用上面显示的“主题设置中的暗化网站复选框”标志来启用此切换。当这个标志被启用时，你会在 Chrome 的主题设置中看到一个复选框“使网站变暗”这似乎也出现在 Android Pie 中，但不尊重系统默认设置。事实上，这是现在在金丝雀的意思是，它应该很快就会成为稳定的版本。