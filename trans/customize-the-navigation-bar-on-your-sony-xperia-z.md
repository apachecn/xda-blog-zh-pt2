# 自定义索尼 Xperia Z 上的导航栏

> 原文：<https://www.xda-developers.com/customize-the-navigation-bar-on-your-sony-xperia-z/>

我们几乎都已经习惯了标准的 Android 导航条设置，它通常是后退、主页和最近应用按钮的任意组合。这通常以 home 键在另外两个中间为特色。但是电源和菜单按钮呢？当然，它们被频繁访问以保证在方便的导航栏上占有一席之地，对吗？

XDA 高级议员拉吉耶夫似乎也这么认为。因此，他写了一篇很棒的教程，教我们如何在[索尼 Xperia Z](http://forum.xda-developers.com/xperia-z) 的导航栏上同时添加电源和锁定按钮。这个过程非常简单，包括对 *SystemUI.apk* 进行反编译，将提供的图像移动到指定的文件夹，在两个 XML 文件中添加和删除代码行，最后将它们重新组合到一个 apk 文件中并签名。

默认情况下，你最终会看到一个导航栏，里面有五个按钮，按后退、主页、菜单、锁定和最近应用的顺序排列，但是改变顺序很简单。正如 Rajeev 在帖子中进一步解释的那样，你所要做的就是按照你喜欢的方式重新排列这些按钮的代码顺序。

任何在设备上运行官方 Android 4.1.2、4.2.2 或 4.3 固件的 Xperia Z 用户都可以遵循该教程，尽管类似 Xperia 设备的所有者也可能这样做。如果你想了解更多，查看[原始线程](http://forum.xda-developers.com/showthread.php?t=2553416)获取更多信息。