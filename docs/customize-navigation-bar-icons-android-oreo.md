# 如何自定义 Android Oreo 上的导航栏图标

> 原文：<https://www.xda-developers.com/customize-navigation-bar-icons-android-oreo/>

自从谷歌随着三星 Galaxy Nexus 的发布抛弃了硬件电容按钮并转向软件导航键以来，人们一直在寻找定制导航条的方法。没有 root 访问权限或自定义 ROM，导航条的定制相当有限，直到人们发现 [Android Nougat 的隐藏导航条调谐器](https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/)不需要 root 就可以访问。同样的歌曲和舞蹈在 Android 8.0 中播放，在早期开发者预览版中添加了[，但在最终版本](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)中仍然可以访问[。然而，这些指南中缺少的是，虽然你可以添加、删除或重新排列导航条按钮，但是改变导航条图标有点棘手。](https://www.xda-developers.com/customise-the-navigation-bar-android-oreo/)

虽然使用 [ADB 方法](https://www.xda-developers.com/how-to-change-your-nav-bar-icons-or-re-arrange-the-buttons-without-root/)或[自定义导航条](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)应用程序来改变导航条图标是绝对可能的，但最终结果是你失去了长按按钮的能力。举例来说，这意味着你不能长按 home 键来调出谷歌助手。此外，出于安全考虑，另一个使用覆盖图在导航条图标[上绘制的变通方法](https://www.xda-developers.com/android-o-is-breaking-apps-that-overlay-on-top-of-the-status-bar/)不再有效，所以似乎没有 root 用户就没有办法改变导航条上的图标。

幸运的是，现在可以用底层主题引擎对 Android 的系统 UI 进行主题化。更好的是，它不需要 root 访问权限，也不会面临上面提到的任何问题。这个方法是导航条图标的真正替代品。在本教程中，我将向你展示如何**改变你的 Android Oreo 设备上的导航栏图标，而无需 root** 。

* * *

## 如何自定义 Android Oreo 上的导航栏图标

### 先决条件

我们将假设您已经[通读并设置了 Andromeda add-on for substrate](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)，它使您能够在没有 root 的情况下主题化您的手机。如果没有，请现在就去做，并确保在该教程的第 1 部分结束时停下来，因为这是您在继续本教程之前需要做的所有事情。

一旦你确认了 Substratum 在没有 root 用户的情况下也能工作，那就该开始了。继续下载 Substratum 主题应用程序，我们将使用它来定制我们的导航条，恰当地称为“导航条”

它的特点是从各种各样的设备上装载了大量不同的导航栏图标。有一些来自小米设备，HTC 设备，有 Pixel 导航条图标，甚至三星 Galaxy S8/S8+/ [Note 8](https://www.xda-developers.com/galaxy-note-8-835-rear-cameras-spen/) 的导航条图标。完整的列表是巨大的，所以一定要检查播放商店截图显示了完整的列表。

### 更改您的导航栏图标

这是一个如何使用导航条底层主题改变导航条图标的分步指南。

1.  打开底层主题管理应用程序。
2.  在已安装的底层主题列表中查找“zipalign cypher”的“Navbars”。
3.  轻按“系统用户界面导航”旁边的复选框
4.  现在让我们选择我们想要使用的导航条图标包。点击下拉框，显示“从列表中选择一个…”从导航条图标的大列表中进行选择。
5.  一旦你选择了你想看到的导航条图标，按下带有油漆滚筒图标的浮动按钮。
6.  在这里的选项列表中，选择“构建并启用”
7.  几秒钟之内，你的覆盖图就会编译、安装并立即应用到你的导航条上。
8.  现在，如果你不喜欢这个主题，或者你想尝试另一个，你需要禁用你应用的覆盖。要做到这一点，你只需再次点击勾号，选择你已经安装的覆盖，按下浮动按钮，这一次点击“禁用选择。”然后，您可以应用另一个覆盖。冲洗并重复，直到你对你得到的满意为止。

使用 Substratum 来为你的导航栏图标设置主题是一个非常简单的任务。最难的部分是首先设置底层+仙女座菌株，即使这也很简单，因为仙女座菌株不需要你太多的努力就能工作。

如果我们发现你可以用新的无根底层主题引擎做其他很酷的调整，你会第一个知道你是否关注我们的[底层论坛](https://forum.xda-developers.com/apps/substratum)或者你是否使用 XDA 实验室来关注 XDA 门户网站的新主页。

这篇文章是 Android Oreo 底层主题化系列教程的一部分。看看其他人: