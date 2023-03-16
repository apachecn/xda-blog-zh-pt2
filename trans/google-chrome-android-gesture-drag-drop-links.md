# 谷歌正在测试一种在 Android 版 Chrome 中拖放链接的手势

> 原文：<https://www.xda-developers.com/google-chrome-android-gesture-drag-drop-links/>

# 谷歌正在测试一种在 Android 版 Chrome 中拖放链接的手势

一个新的 Chrome 提交引起了我们的注意，它的标题是“在旗帜后面实现触摸拖放链接元素”用户可以在 Android 浏览器中拖放链接。

有趣的事情总是在 Chromium Gerrit 上的提交中出现。跟踪提交是了解 Chrome 浏览器和 Chrome 操作系统可能会有哪些特性的好方法。我们最近看到了 Chrome 操作系统中的[触摸屏启动器和](https://www.xda-developers.com/chrome-os-fullscreen-launcher-tablet-mode/)[新标签切换器](https://www.xda-developers.com/google-chrome-testing-horizontal-tab-switcher/)的提交。一个吸引我们眼球的新提交是 [971764](https://chromium-review.googlesource.com/c/chromium/src/+/971764) ，标题为“在一个旗帜后面实现触摸拖放链接元素”的 Android 浏览器。阅读下面的全文。

*实现触摸拖放链接元素后的一个标志*

*这个 cl* 实现了*在旗子后面通过触摸拖动链接。* *这允许*用户*通过长按并移动*手指*来拖动链接或图像元素。*

*在 Android 上使用'-Enable-features = " TouchDragDropLink " '标志启用。当标志被禁用时，或者当*平台*不是 Android 时，行为没有变化。*

*暂时将标志设置为 true 以运行试用机器人。*

长按浏览器中的链接时，当前行为是弹出一些选项。你可以在一个新的标签中打开，匿名模式，复制链接，复制链接文本，下载链接，或分享它。这项新功能允许用户通过长按并移动手指来拖动链接或图像。基本上，就像你在 Chrome for desktop 中点击和拖动鼠标时的工作方式一样。我们不确定为什么这在手机浏览器中会是一个有用的功能。无论如何，这是一个有趣的补充，可能永远不会成为黄金时间。

* * *

[**来源:铬评**](https://chromium-review.googlesource.com/c/chromium/src/+/971764)