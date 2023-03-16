# Chrome 测试了适用于 Android 10 黑暗模式的黑暗搜索结果

> 原文：<https://www.xda-developers.com/google-chrome-google-search-dark-theme/>

**更新 1(美国东部时间 05/26/2020 @ 01:30am):**让谷歌 Chrome 将谷歌搜索结果变暗的那面旗帜，现在已经活了，正在发挥作用。滚动到底部了解更多信息。下面保留了 2020 年 5 月 14 日发表的文章。

Android 10 中引入的全系统黑暗模式对许多 Android 应用程序的 UI 设计产生了巨大的影响。现在许多 Android 应用程序都内置了黑暗主题，其中许多应用程序还将其黑暗主题与 Android 10 的 toggle 同步。谷歌 Chrome 已经为其工具栏和设置页面提供了这一功能，但很快它还将与 Android 10 的黑暗模式切换同步暗化谷歌搜索结果。

谷歌首次在 Chrome 浏览器版本 74 中引入黑暗模式支持[作为功能标志。他们后来在 Chrome 的设置中引入了一个](https://www.xda-developers.com/google-chrome-android-dark-mode/)[专用的“主题”部分](https://www.xda-developers.com/google-chrome-dark-mode-darken-web-pages/)，他们还添加了一个功能标志，让[使用深色主题](https://www.xda-developers.com/google-chrome-forced-dark-mode-web-pages-android-windows-mac-linux/)呈现所有网络内容。虽然目前可以通过使用#enable-force-dark 功能标志以深色主题显示谷歌搜索结果，但这样做可能会破坏许多网站的体验，这些网站在设计时并没有考虑深色背景颜色。不过，有了新的 [#enable-android-dark-search 功能标志](https://chromium-review.googlesource.com/c/chromium/src/+/2186128)，只要 Chrome 的黑暗模式被启用，你就可以显示黑暗的搜索页面结果。由于 Chrome 的黑暗模式可以设置为与“系统默认”主题同步，这意味着黑暗的搜索结果可以与 Android 10 的全系统黑暗模式切换同步。

不过，这项功能仍在开发中，因为当我在 Android 10 的 Pixel 4 上运行的新开发的 Chromium APK 上启用该功能标志时，谷歌搜索结果并没有变暗。正如 [*9to5Google*](https://9to5google.com/2020/05/06/chrome-android-google-search-dark/) 上周在提交首次出现时指出的，Google 本可以通过“[偏好-配色方案](https://drafts.csswg.org/mediaqueries-5/#prefers-color-scheme)”媒体 CSS 特性来实现这个目标。然而，这似乎不是谷歌在这里采取的方法。

在相关的[提交](https://chromium-review.googlesource.com/c/chromium/src/+/2191209)中，谷歌详细说明了当用户启用 Android 10 的黑暗模式时，Chrome 浏览器将如何显示黑暗的搜索结果。描述中称，“当用户处于夜间模式并访问谷歌搜索(主页或结果)时”，谷歌 Chrome 将“附加一个额外的 URL 参数，以表明该用户应该获得网站的黑暗版本。”好像 Chrome 会追加？如果用户启用了黑暗模式，则任何 Google 搜索 URL 的 cs=1。下面是这个 URL 参数如何使谷歌搜索结果页面变暗的一个例子:

#enable-android-dark-search 特性标志目前在最新的 Chromium 版本中可用，但最终会在开发版、测试版和稳定版中使用。随着开发的进展，我们将跟踪这项功能。

* * *

## 更新:谷歌 Chrome 变暗搜索结果的标志现已启用

当我们在 2020 年 5 月 14 日首次发表我们的文章时，在 Chrome 中使谷歌搜索结果变暗的功能标志不起作用，我们不得不利用 URL 变通方法来展示该功能的样子。现在，flag 正在开发最新的 Canary 版本，允许 Chrome 改变结果 UX，与 Android 10 的黑暗模式设置保持一致，并在系统中同步。要在最近的 Chrome Canary 版本上启用该功能，请加载 chrome://flags 并将“在 Android 上显示深色搜索页面”选项设置为“已启用”。

**故事 Via: [安卓警察](https://www.androidpolice.com/2020/05/25/chrome-tests-dark-theme-for-mobile-google-search/)**