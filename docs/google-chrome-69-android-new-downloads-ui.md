# Android 上的谷歌 Chrome 69 增加了重命名下载和更改文件夹

> 原文：<https://www.xda-developers.com/google-chrome-69-android-new-downloads-ui/>

# Android 上的谷歌 Chrome 69 带来了新的下载用户界面，可以重命名和更改下载文件夹

Chromium Gerrit 的最新活动表明，谷歌 Chrome 将很快让你重命名文件并选择下载文件夹。

谷歌的移动网络浏览器 Chrome 可以完成大多数浏览网站的功能。山景城的工程师认为该应用程序还可以进一步改进，我们社区中的许多人都同意这一点。去年，我们发现[谷歌正在试验一个新的“Chrome Home”](https://www.xda-developers.com/googles-experimental-chrome-home-gets-a-redesigned-new-tab-page/)功能，该功能将重新设计新的标签页，[今年继续发展](https://www.xda-developers.com/hands-on-google-chromes-new-duplex-split-toolbar-ui-replaces-chrome-home/)。尽管如此，谷歌 Chrome 的 Android 版本要达到与桌面版同等的功能，还有很长的路要走。Chromium Gerrit 中的[最新活动表明，该应用程序将很快让你重命名文件并选择下载文件夹。](https://chromium-review.googlesource.com/c/chromium/src/+/1137841)

去年 12 月，我们的主编米莎尔·拉赫曼透露了一些他用谷歌浏览器发现的信息。首先，我们了解到 Google 正在通过他们的 Google Chrome 应用程序增加对并行下载的支持。这被安排在应用程序的版本 64 中发布，但是它只在应用程序的测试版本中进行测试。该特性是创建 3 个并行作业来加快下载过程，这已被证明可以提高从支持它的源的下载速度。

同一个月，我们还发现谷歌 Chrome 浏览器的标准下载程序正在进行改进。目前，当你点击自动下载的链接时，它会在未经你同意的情况下进入“下载”文件夹。也许你想重命名那个文件，或者你想把它放到另一个文件夹里。当时它要求你在谷歌 Chrome 的夜间分支上启用隐藏的*Chrome://flags # enable-downloads-location-change*标志，但现在该功能已经有所进展。

这些通过 Google Chrome 下载的新选项目前在开发者和金丝雀版本的网络浏览器中可用，并且实际上是默认启用的。它可以通过*download home modem*标志禁用。然而，目前看来，改变下载文件夹的功能似乎还没有发挥作用。你可以在下面的截图中看到新的选项。