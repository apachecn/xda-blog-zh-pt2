# 谷歌在 Chrome 中增加了谷歌镜头作为反向图片搜索选项

> 原文：<https://www.xda-developers.com/google-chrome-google-lens-reverse-image-search/>

**更新 2 (11/19/19 @美国东部时间下午 4:10):**通过 Google Lens 进行反向图片搜索现已在所有 Google Chrome 频道提供。

**更新 1(美国东部时间 8/22/19 @ 8:43PM):**谷歌已经合并了负责显示“用谷歌镜头搜索”上下文菜单项的提交。这个新选项的屏幕截图显示在下面的更新中。

多亏了像 Google Lens 这样的服务，曾经只是互联网侦探的工具现在已经相当主流了。反向图像搜索，或在网络上搜索图像的来源，在 Google Images 上很容易做到，但 Google Lens 更进一步，让你可以分离图像的部分或识别图像中的文本、条形码和其他关键项目。通过谷歌助手和谷歌照片应用程序中的快捷方式可以使用 Lens，但如果你在手机上浏览，也可以通过网络上的[谷歌图片](https://www.xda-developers.com/google-lens-launches-for-google-image-search-on-mobile/)使用它。现在，谷歌似乎将在 Android 版谷歌浏览器中添加 Lens 的快捷方式。

前几天，我在 Chromium Gerrit 中发现了一个名为“从上下文菜单中添加对 Google Lens 意图的支持”的[提交](https://chromium-review.googlesource.com/c/chromium/src/+/1761662)一旦合并，在 Android 版谷歌浏览器中打开任何图片的上下文菜单，都会显示“使用谷歌镜头搜索”选项，而不是“在谷歌上搜索该图片”。点击新选项会将所选图像发送到镜头。你现在可以通过点击“共享图像”，然后在共享表中选择镜头来实现这一点，但这一新功能将使镜头选项更加突出，因此你可以保留共享按钮用于其他操作。

基于 Chromium 的浏览器 Kiwi Browser 中显示的谷歌 Chrome 图片的上下文菜单。

一旦提交被合并，我们将能够在最新的 Chrome Canary 版本中看到这个特性的运行。

## 更新 1:“用谷歌镜头搜索”现已推出

今晚提交被合并了，所以我抓取了带有新选项的更新后的上下文菜单的截图。这是它的样子。

要启用，只需在 chrome://flags 中搜索“Lens”即可，只要该标志在您的特定 chrome 频道中可用。目前，它只在 Chromium 夜间版本中可用。

* * *

## 更新 2:在 Stable 中可用

Google Lens for Chrome 终于在所有稳定版本中上线了。不过，默认情况下该特性是不启用的，所以您必须切换一个标志来获得它。这个标志叫做“谷歌镜头的上下文菜单搜索”在你的浏览器中进入 chrome://flags 并搜索该标志。启用后，当长按图像时，你会看到一个“用谷歌镜头搜索”的选项。以前，谷歌只会搜索相同的图片，但有了镜头，它就聪明多了。

**Via: [安卓警察](https://www.androidpolice.com/2019/11/19/google-lens-is-now-integrated-in-chromes-image-search/)**