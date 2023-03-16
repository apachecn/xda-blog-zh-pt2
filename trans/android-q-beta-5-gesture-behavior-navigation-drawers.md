# Android Q beta 5 改变了导航抽屉的手势行为

> 原文：<https://www.xda-developers.com/android-q-beta-5-gesture-behavior-navigation-drawers/>

# Android Q beta 5 改变了导航抽屉的手势行为

谷歌正在 Android Q 的第五个测试版中改变导航抽屉的行为。这些改变应该可以修复导航抽屉的复杂性。

我们离 Android Q 的[最终发布越来越近了。像每一个新版本的 Android 一样，也有一些有争议的变化。其中一个变化是全手势导航，幸好这是可选的，所以你可以随时退出。新手势控件的一个方面让许多用户和开发人员感到困惑。除了改变导航栏的行为，谷歌还增加了一个新的手势，让你从显示屏的任何一侧向内滑动即可返回。这与许多应用程序中的导航抽屉相冲突，因此谷歌建议应用程序开发者如果继续在应用程序中使用导航抽屉，就应该阻止向内滑动。今天，谷歌 Android 团队的一名开发人员发布了一个新的解决方案。](https://www.xda-developers.com/android-q-beta-release-schedule/)

据 Android 开发者关系成员 [Chris Banes](https://twitter.com/chrisbanes) 称，谷歌正在即将发布的 Android Q 第五个测试版中改变后退导航手势的行为，你将能够通过在抽屉附近“偷看”来打开导航抽屉。基本上，要打开抽屉，你只需轻按显示屏的边缘，然后短暂按住，直到它“弹出”来。然后，您可以继续拖动它打开。华为在装有 EMUI 系统的设备上使用类似的方法已经有一段时间了。由于这一变化，你将不必像一些用户建议的那样，从屏幕一侧进行奇怪的对角滑动。对于一些人来说，点击汉堡菜单按钮可能更好，但在较大的设备上很难将手指伸得那么远。

另一个变化是应用程序如何阻止侧手势。以前，如果开发者愿意的话，他们可以屏蔽整个页面。现在，应用程序将只能从边缘选择 200dp。对于请求退出更多的应用程序，只有底部的 200 dp 将被覆盖。

这些变化将扩展到所有版本的 DrawerLayout API，但谷歌建议开发者更新到 1.1.0-alpha02，以便在 Android Q 设备上获得最佳体验。这个 API 很有可能最终完成，并随着系统的最终发布转移到稳定的渠道。Android Q Beta 5 将在未来几周内发布。我们至少已经知道了最近 4 个测试版的大概发布日期，但是 Google [并没有透露 Beta 5、6 和最终版 Android Q 的预计发布时间。](https://developer.android.com/preview/overview#timeline)