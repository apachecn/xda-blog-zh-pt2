# 用 Xposed 模块在 Android 牛轧糖上添加锁屏小工具

> 原文：<https://www.xda-developers.com/lock-screen-widgets-xposed-module/>

自从我们在本周早些时候宣布牛轧糖官方 Xposed 框架的到来，XDA 社区的许多成员一直在想他们应该尝试哪些模块。今天，我们要提到一个这样的模块，它最近刚刚用 Xposed 更新了 Android 牛轧糖支持:“[锁屏小工具](https://forum.xda-developers.com/xposed/modules/app-lock-screen-widgets-t3167027)”

锁屏小部件，顾名思义，是一个 Xposed 模块，允许你在锁屏上添加小部件。XDA 成员 [SergioSanchezR](https://forum.xda-developers.com/member.php?u=6374995) ，负责锁屏小工具的开发者，捆绑了应用程序的某些标准锁屏修改，以及一些“额外”修改。

## 标准修改

标准的修改包括改变锁定屏幕上显示的通知的顶部填充，隐藏日期和/或时钟，隐藏状态栏，以及隐藏“即将到来的警报”列表。

此外，用户可以向锁定屏幕添加任意数量的小工具。这些部件也是可以添加到主屏幕启动器的部件，不过要注意你的锁屏空间要小得多。每个小工具都有自己的水平空间，所有小工具都垂直平铺在锁屏时钟的正上方。

一旦你添加了一个部件，每个部件都有几个选项供你选择。例如，您可以使小部件成为可点击的实例，编辑和更改大小，更改重力，以及更改填充。

## “额外”修改

你可以利用本节中的模块来改变通知的背景颜色，完全隐藏锁定屏幕的底部栏，并为容器的重力设置一个自定义值——将其移动到顶部或底部。

鉴于有这么多选项，这款应用乍一看可能有点令人不知所措，但是社区已经在我们的论坛上整合了一些教程(例如 Zooper Widgets 的[教程，每行添加两个 Widgets](http://forum.xda-developers.com/showpost.php?p=64222888&postcount=145)的[教程，以及激活 Widgets 列表滚动的](http://forum.xda-developers.com/showpost.php?p=65422468&postcount=208)[教程](http://forum.xda-developers.com/showpost.php?p=65422594&postcount=209))。你可能不想错过它们。

我们自己确认了这个模块在 Android 牛轧糖官方 Xposed 上工作。具体来说，我们在运行 OxygenOS 的 OnePlus 5 上进行了测试。

过去你对 Xposed 的模块增强有什么体验？让我们知道你对“锁屏小工具”的看法吧！