# 指南:如何在 Android 上获得类似 iPhone X 的手势

> 原文：<https://www.xda-developers.com/iphone-x-gestures-android-guide/>

iPhone X 是一款两极分化的智能手机，但苹果做对的一件事是放弃了物理 Home 键，代之以一系列基于软件的滑动手势。

虽然 Android 已经有软件导航多年了，但大多数原始设备制造商并没有像苹果公司在 iPhone X 上那样利用它。如果你像我一样拥有或使用 iPhone X，你可能会有兴趣学习如何复制 iOS 的手势，这是一种非常自然和流畅的方式来导航带有小边框的 18:9 高显示屏上的应用程序。

如果你足够幸运，拥有一台注册了 Oxygen OS Open Beta 计划的 OnePlus 5T，那么升级到最新固件并启用导航手势就像[一样简单。对于我们其他人来说，还需要几个步骤。这里有一个在你的 Android 手机上设置类似 iPhone X 的滑动手势的指南——这比你想象的要简单！](https://www.xda-developers.com/oxygenos-open-beta-5-3-oneplus-5-5t/)

* * *

有三种方法可以在 Android 设备上设置滑动手势。一个需要 [Magisk](http://xda-developers.com/tag/magisk) ，另一个需要[底层](http://xda-developers.com/tag/substratum)，后者可以与[仙女座结合使用，实现无根方法](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)，但最简单的方法是使用我们的导航手势应用 。(注意仙女座是付费附加。)

由于 Android 的安全措施，操作系统的一些部分会干扰自定义手势应用程序。例如，设置菜单中的权限屏幕和 toast 消息都会破坏使用 Android“在其他应用上绘制”权限的手势应用。

万一自定义手势不起作用，了解你在 Android 周围的方式是有帮助的。例如，您可以使用通知阴影中的设置按钮(齿轮图标)退出 toast，或者点击应用程序设置页面中的**应用程序详细信息**按钮切换到不同的应用程序。

* * *

## 选项 1

**步骤 1 -下载导航手势应用**

我说过这很容易，不是吗？你所需要做的就是使用这个链接去[谷歌 Play 商店并安装我们简单的应用程序。 ***你需要一台电脑在*** 附近，通过一个简单的 ADB 命令来启动应用程序，但是一旦你完成了，你就可以开始了。关于导航手势最好的部分是你不需要有根，你也不需要使用底层来隐藏导航条——这在 Oreo 上似乎不太可靠。此外，导航条从手机的功能中消失了，这意味着从底部向上滑动不会显示半隐藏的导航条。](https://play.google.com/store/apps/details?id=com.xda.nobar)

我们还包括了一系列可选的命令，您可以运行，并通过一个高级选项来增强，您可以控制音乐播放(对于大多数应用程序)等。我强烈建议使用这个应用程序，而不是下面列出的删除导航栏的方法，就我个人而言，我将这个应用程序与 Edge 手势结合使用，以使我的设置完全符合我的喜好。

如果您对更多细节感兴趣，请查看[这个门户网站发布的](https://www.xda-developers.com/navigation-gestures-iphone-x-app-xda/?preview=true)更多细节和我们的视频评论！

[**从谷歌 Play 商店**下载导航手势](https://play.google.com/store/apps/details?id=com.xda.nobar)

* * *

## 选项 2

### 步骤 1 -设置手势控制

你可以自己决定滑动手势的工作方式。在 Play Store 中快速搜索“edge 手势”(不带引号)( T1 ),你会看到许多可供选择的应用程序——有些是付费的，有些是免费的，有些可以让导航条完全看不见，还有一些模仿 iPhone X 的滑动手势，一直到药丸形状的手柄。请随意尝试，找出最适合你的方式，不要担心性能影响——自从安装手势叠加功能后，我没有注意到明显的电池消耗，我同时运行了两个手势叠加功能。

就我个人而言，我使用向上滑动手势回家，向左滑动手势调出多任务菜单，向右滑动手势启动最后打开的应用程序，向内滑动手势返回。

不言而喻的一点是，在隐藏导航栏之前，您需要设置手势应用程序。你还需要确保在启用手势之前，你已经为 USB 调试配置了你的电脑，否则你必须进入 Android 的辅助功能菜单，暂时禁用你的自定义手势应用程序。由于这些应用程序使用 Android Accessibility API 的“Draw over other applications”，你将在 Android Oreo 上获得一个持久的通知，可以通过点击它并切换应用程序的警告通知来删除。

* * *

### 步骤 2 -删除导航栏

为什么不直接使用沉浸式模式？

Android 的沉浸式模式很棒，可以让你轻松隐藏导航栏。([下面介绍如何在没有 root](https://www.xda-developers.com/how-to-enable-system-wide-immersive-mode-without-root/) 的情况下启用全系统沉浸式模式。)但它也有缺点。

如果你设置了一个向上滑动的手势来带你回到主屏幕，每次你从屏幕底部向上滑动，它都会带回来导航栏。此外，每当应用程序调用键盘时，导航栏就会出现，这可能会变得很烦人。

**非根(需要付费的 Andromeda 附加软件用于底层)**

如果你有一个与 Substratum 兼容的非根设备，Andromeda 为隐藏导航栏提供了一个很好的解决方案。(在三星设备上，你可以使用[三星插件，但要知道它目前只与基于牛轧糖的固件兼容。)从 XDA 论坛下载](https://play.google.com/store/apps/details?id=projekt.sungstratum&hl=en)[导航条高度改变器 v4](https://forum.xda-developers.com/nexus-6p/themes-apps/mod-navbar-height-changer-android-nougat-t3447956) 应用程序，通过 Substratum 启用它，并将导航条高度设置为零——这非常简单，如果出错，撤销起来也很容易。

**根**

如果你的手机已经安装了 Magisk，隐藏导航条就更容易了。你需要做的就是通过 Magisk 管理器下载并安装**隐藏导航栏** Magisk 模块。重启手机后，你将看不到导航栏。不过，需要预先警告的是，包括 [Essential PH-1](http://forum.xda-developers.com/essential) 在内的一些手机并不完全兼容这种方法，可能是由于 SystemUI 的修改。我个人在运行奥利奥 beta 2 的基本手机上经历过随机的系统界面崩溃。

无论你使用哪种方法来隐藏导航栏，你一定会遇到一些奇怪的问题，就像任何一种模式一样。不过，在使用新系统一段时间后，你可能会比普通 Android 更喜欢它——我更喜欢去掉导航条带来的额外屏幕空间。

mods 在运行接近库存版本的 Android 的手机上工作得最好，如谷歌 Pixel 2、Essential Phone 和 OnePlus 5T。我也强烈建议有一个后备计划，以防出现问题。

关于这些模块最好的部分是它们是高度可定制的。在我的手机上，我使用一个手势控制应用程序，允许我从屏幕的右侧滑入，并上下移动手指来调整媒体音量。您还可以设置手势来打开通知阴影或一个喜爱的应用程序。

手势控制是一个我真的希望谷歌带到股票 Android 的功能。一个合适的内置解决方案将解决诸如与“其他应用程序不兼容”的怪癖，并为应用程序省去必须使用 Android 辅助功能 API 的麻烦。不管是哪种方式，第三方解决方案让你制作满足你独特需求的定制手势，或者至少将 iPhone X 风格的手势带到你的手机上，这太棒了。

* * *

***你喜欢手势控制吗？你在手机上用吗？如果是，请在下面评论你最喜欢的应用和控制方案。***