# 如何隐藏 EMUI 5.0 中的导航栏【无根】

> 原文：<https://www.xda-developers.com/how-to-hide-the-navigation-bar-in-emui-5-0/>

随着大屏幕手机继续席卷智能手机市场，曾经被认为是小众的类别现在实际上已经成为主流。

华为最新的旗舰智能手机[华为 Mate 9](https://forum.xda-developers.com/mate-9) 采用了 6.0 英寸的大屏幕，如果不是由于华为巧妙实现了单手模式，自然会使单手使用手机更加困难。

但是，尽管华为很容易缩小屏幕，以轻松触及所有 UI 元素，但他们没有提供相反的方法。一些用户更喜欢能够利用 Mate 9 漂亮的 6.0 英寸屏幕上更多的屏幕空间，华为甚至似乎乐于提供包含所有标准导航键的“浮动码头”功能。不幸的是，当这个浮动码头被激活时，他们没有提供隐藏导航栏的本地方法。

如果您熟悉 build.prop 编辑，您可能会看到将 qemu.hw.mainkeys=1 添加到 build.prop 的建议，以便只隐藏导航栏。这是一个相当古老的技巧，但是它需要您拥有 root 访问权限才能实现。即使你有超级用户权限，EMUI 5.0 目前也有一个错误，如果你把这一行添加到你的 build.prop 中，会导致你启动到黑屏。

但是有一个简单的技巧可以用来**只隐藏 EMUI 5.0** 上的导航栏，最棒的是它不需要 build.prop 编辑(这意味着它没有根**)。这样，你仍然可以显示状态栏，但使用你喜欢的任何其他导航方法(如华为的浮动码头)。**

 *** * *

## 在 EMUI 5.0 上隐藏导航栏

要实现这个技巧，你只需要一台装有 [ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)和适合你的华为设备的驱动程序的电脑(下载 [HiSuite](http://consumer.huawei.com/minisite/HiSuite_en/index.html) 以方便安装驱动程序)。一旦设置好 ADB(并在开发人员选项中启用 USB 调试)，只需输入以下命令:

`adb shell settings put global navigationbar_is_min 1`

重启，你手机的导航条会完全隐藏。如果没有导航条，你会希望使用第三方应用程序或华为的浮动基座来实际使用你的手机。

由于这是**而不是沉浸式模式**(我们稍后会制作一个关于如何使用无根沉浸式模式的教程)，导航栏将**保持隐藏**，直到你**撤销这个命令**。如果您希望撤销该命令，只需输入以下命令即可:

`adb shell settings put global navigationbar_is_min 0`

我们希望你喜欢这个为你的非根华为设备的俏皮把戏！如果我们遇到更多这样的把戏，我们一定会很快让我们的读者知道。**