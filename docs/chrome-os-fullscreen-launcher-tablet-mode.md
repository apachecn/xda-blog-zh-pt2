# Chrome OS 正在测试平板模式下的全屏启动器

> 原文：<https://www.xda-developers.com/chrome-os-fullscreen-launcher-tablet-mode/>

# [更新:截图] Chrome OS 正在测试平板模式下的全屏启动器

谷歌一直在慢慢地为 Chrome OS 添加更多触摸友好和 Android 功能。现在，谷歌正在测试更多的触摸屏功能。

**2018 年 4 月 23 日**更新:根据 Francois Beaufort 的说法，现在可以在`chrome://flags/#enable-home-launcher`、[访问特征标志。我们已经改变了上面的特征图像来展示它的样子。](https://plus.google.com/+FrancoisBeaufort/posts/1a98yD6wwbr)

Chrome OS 越来越倾向于触摸屏优化的界面，这并不奇怪。在过去的几个月里，谷歌一直在慢慢增加更多的触摸屏和安卓功能。我们已经看到他们对[的发射器](https://www.xda-developers.com/pixelbooks-launcher-more-chrome-os/)做了一些改动，以使其更好地触摸。现在，谷歌正在测试更多的触摸功能。

目前，Chrome OS 应用程序启动器看起来像左边的图像。轻按主屏幕按钮时，会出现搜索栏和一行最近使用的应用程序。点击箭头会弹出全屏启动器，如右图所示。Chromium Gerrit 中的一个新的 commit 添加了一个特性标志来启用平板模式下的全屏启动器。它也改变了主页按钮的行为。点击它将最小化所有窗口，而不是打开启动器。

```
 Add home launcher feature flag

Home launcher is a feature to show fullscreen launcher in tablet mode. And home button will minimize all windows instead of opening/closing the launcher. 
```

[宏碁上个月宣布了首款 Chrome OS 平板电脑](https://www.xda-developers.com/acer-chromebook-tab-chrome-os-tablet/)，这使得触摸优化更加中肯。Chrome OS 有望成为谷歌事实上的平板电脑操作系统。[安卓应用和功能](https://www.xda-developers.com/chrome-os-67-android-p-system-tray/)的加入使其成为全功能安卓平板电脑的可行替代品。Chrome 操作系统的网络体验当然更好，它有足够的 Android 功能来填补空白。2018 年可能是谷歌基于网络的平板电脑之年。

* * *

[**来源:铬评**](https://chromium-review.googlesource.com/c/chromium/src/+/996177)