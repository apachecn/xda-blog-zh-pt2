# 隐藏的像素启动器设置揭示了 Android Q 中 iPhone 风格的手势

> 原文：<https://www.xda-developers.com/android-q-iphone-navigation-gestures/>

当谷歌第一次在 Android Pie 中引入手势控制时，许多爱好者觉得谷歌的实现是半生不熟的。例如，您只能单向快速切换应用程序，向上推送手势以显示最近的应用程序概述通常会导致应用程序抽屉显示。此外，任务之间的转换动画感觉不到无缝，并且后退按钮的存在受到了激烈的竞争。幸运的是，我们知道谷歌正在努力调整 Android Q 中的导航手势控制。我们已经看到谷歌[如何用手势取代后退按钮](https://www.xda-developers.com/android-q-gestures-back-button/)以及快速切换的过渡动画如何改变，但我们现在发现了更多的手势控制调整，这要归功于 Pixel Launcher 中的隐藏标志。

与你可以通过 ADB[访问来修改](https://www.xda-developers.com/android-q-navigation-gesture-controls/)[第一个 Android Q beta](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/) 中的手势的隐藏偏好相反，我们发现的新手势只能通过修改股票 Pixel Launcher APK 来访问，以暴露其“开发者选项”XDA 资深会员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) ，一个开发过[无根 Pixel Launcher ports](https://www.xda-developers.com/download-pixel-launcher-google-assistant-search-bar-pixel-3/) 、[一加 Launcher mods](https://www.xda-developers.com/oneplus-launcher-recent-apps-interface-android-pie/) 和 [Lawnchair launcher app](https://www.xda-developers.com/lawnchair-android-pie-recent-apps-integration-root/) 的开发者，修改了 Pixel Launcher app 来显示这些隐藏的标志。下面的截图显示了 Pixel Launcher 设置中新的“开发者选项”菜单。当你打开这个菜单时，你可以访问大量的新设置来控制 QuickStep，这是 Android Pie 和 Android Q 中手势和最近应用组件的名称。

当你启用这些标志时，Android Q 中的手势行为会立即改变。我用最新的 [Magisk Canary build](https://www.xda-developers.com/root-android-q-beta-google-pixel-pixel-2/) 在运行 [Android Q beta](https://www.xda-developers.com/android-q-beta-changes-google-pixel/) 的谷歌 Pixel 2 XL 上测试了这些标志。下面嵌入的第一个视频展示了带有这些隐藏像素启动器标志的改进手势。以下是这些变化的摘要:

*   在药丸上向右滑动现在在改变任务时使用更无缝的过渡动画。
*   在导航栏上向左滑动现在可以切换到你刚刚离开的任务。这里的过渡动画是一个正在进行中的工作。
*   吃了药就回家了。为这个手势制作了一个新的动画。
*   向上滑动并按住药丸会显示最近的应用程序概览。
*   在启动器上向上滑动导航栏，现在只显示应用程序抽屉。
*   在主页的任何地方向下滑动，现在会带来通知面板。

总的来说，这些变化让 Android Q 的手势更像 iPhone。最大的区别就是后退键还在。

这些标志带来的另一个变化是，在最近的应用程序概览中，你有更多的时间来“撤销”意外的任务取消。

我们不确定这些新的手势，或者我们之前发现的那些，是否会形成 Android Q 改进后的手势控制的基础。显然，谷歌正在对手势进行大量的幕后实验，所以我期待手势的重大变化将在 [Google I/O 2019](https://www.xda-developers.com/google-io-2019-may-7-9/) 期间公布。如果你想自己尝试这些新手势，你可以遵循下面的简短指南。请注意，这些手势目前的形式存在一些缺陷。例如，你会经常看到一些看不见的任务，它们不能被利用。

## 如何在 Android Q 中启用 Pixel Launcher 的隐藏开发者选项

**要求:**

*   谷歌 Pixel，Pixel XL，Pixel 2，Pixel 2 XL 运行 Android Q beta。
*   使用 Magisk 进行 Root 访问。(发稿时，Pixel 3 和 Pixel 3 XL 还没落地生根。)

1.  如果你在 Q Beta 1 上，从 AndroidFileHost 下载[这个 Magisk 模块](https://www.androidfilehost.com/?fid=1395089523397919287)，或者如果你在 Q Beta 2 上，下载[这个模块](https://www.androidfilehost.com/?fid=1395089523397939746)..我在 paphonb 的许可下制作了这个模块，并在我的 rooted Pixel 2 XL 上进行了测试。它所做的只是替换/product/priv-app 中的 NexusLauncherRelease.apk。
2.  Open Magisk Manager.
3.  点击菜单。
4.  点击“模块”
5.  点击+图标。
6.  找到并选择您下载的 Magisk 模块。
7.  安装完成后，重启你的手机。
8.  一旦你启动备份，打开像素启动器设置，你应该看到开发者选项菜单。

* * *

更多安卓 Q 新闻，关注我们专属的[标签](https://www.xda-developers.com/tag/android-q/)。如果我们发现更多隐藏的功能，我们一定会让您知道。

*2019 年 4 月 11 日更新:本文更新为 Android Q beta 2 添加了一个工作像素启动器 mod。*