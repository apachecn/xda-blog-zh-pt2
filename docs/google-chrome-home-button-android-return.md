# Android 版谷歌浏览器的 Home 键正在回归

> 原文：<https://www.xda-developers.com/google-chrome-home-button-android-return/>

# Android 版谷歌浏览器的 Home 键正在回归

Android 版谷歌 Chrome 的 home 键正在回归。点击该按钮后，用户会很快回到主页。

谷歌不断为其 Chrome 浏览器尝试新功能和设计调整。通常情况下，界面的变化相当小，但有时它们相当大，例如实验性的 [Chrome Home](https://www.xda-developers.com/googles-experimental-chrome-home-gets-a-redesigned-new-tab-page/) 界面，该界面已被[弃用](https://www.xda-developers.com/google-deprecating-bottom-address-bar-chrome-home-chrome-duplex/)，取而代之的是新的分离工具栏“ [Chrome Duplex](https://www.xda-developers.com/hands-on-google-chromes-new-duplex-split-toolbar-ui-replaces-chrome-home/) 界面。另一个引起用户争议的界面变化是移除了工具栏中的主页按钮。

home 键是大多数网络浏览器的标准功能，甚至桌面上的谷歌 Chrome 也仍然有这个按钮。按下按钮启动用户指定的主页。这是一种快速返回经常查看的网页的便捷方式。我的主页设置为 XDA 开发者，因为我经常回来查看门户网站上的新文章和评论。不管出于什么原因，谷歌在早期版本的 Android 版 Chrome 中取消了 home 键，但似乎一个新的功能标志正在推出，允许你将其恢复。

在 Chrome 浏览器和 Chrome Canary 的最新夜间版本中，添加了一个名为“强制启用主页按钮”的新标志。通过将以下内容复制并粘贴到地址栏中，可以访问该标志:

```
 chrome: 
```

启用这个标志，然后重新启动 Chrome 两次，就会带回主页按钮，如上图截图所示。重新启动 Chrome 两次意味着你必须打开浏览器，然后在首次重新启动后修改标志时强制关闭浏览器。对于那些想念 home 键的人来说，这个新功能最终应该会进入测试版和稳定版，所以请密切关注。