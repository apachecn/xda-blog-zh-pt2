# 如何在任何 Android 设备上获得 Android P 的旋转建议功能

> 原文：<https://www.xda-developers.com/how-to-android-p-rotation-suggestion/>

尽管它安装在如此少的设备上，以至于没有在[安卓最新版本发布统计](https://www.xda-developers.com/android-oreo-android-nougat-april-distribution-statistics/)，[安卓 P](https://www.xda-developers.com/android-p-developer-preview-1-google-pixel-xl-pixel-2-xl/) 上注册，却得到了所有安卓粉丝的大量关注。一旦今年晚些时候全面发布，它最终会转向其他非谷歌 Android 设备，但如果你没有谷歌 Pixel/XL 或谷歌 Pixel 2/2 XL，那就要等很长时间了。虽然许多 Android 设备制造商已经实现了 Android P 中的功能(如[自动记住蓝牙设备音量](https://www.xda-developers.com/android-p-automatically-remember-bluetooth-device-volume-levels/))，但还有一些像令人敬畏的新“[旋转建议](https://www.xda-developers.com/everything-new-android-p-developer-preview/)”功能并不存在于任何设备上。

旋转建议是我们给这个新的 Android P 特性起的名字。在以前的 Android 版本中，设备可以处于两种方向状态:锁定到纵向模式或自动旋转，在纵向和横向模式之间切换。对于 Android P，如果你禁用自动旋转，你仍然会被锁定到纵向模式，但是，如果你调整设备的方向，就好像你试图切换到横向模式一样，导航栏中会出现一个新按钮，当按下该按钮时，会将方向锁定到横向模式。当然，你可以通过相反的动作回到纵向模式，或者你可以通过启用自动旋转模式来完全关闭它。

下面是这项新功能的视频短片:

与其等待 Android P 在今年晚些时候或明年推出到你的设备上，不如现在就告诉你如何在任何 Android 设备上复制这一功能！我将提供两种方法来做到这一点。第一个可以在任何运行 Android 4.1+的 Android 设备上工作，但它不是该功能的完美复制，因为它没有在导航栏中添加旋转建议按钮。第二种方法可以在任何运行 Android 7.0+的 Android 设备上工作，实际上像 Android P 一样将按钮添加到导航栏，但这种方法需要在应用内购买一个名为自定义导航栏的应用。

* * *

## 方法 1 —动态旋转控制(Android 4.1 以上)

这是一个非常简单的应用程序，只有一个目的:它允许你在不启用自动旋转的情况下在旋转锁定模式之间切换！只要打开应用程序，按下右下角的“开始”按钮。它会要求你授予它两个权限:“在其他应用上绘图”和“系统设置”正如对话框所解释的，这两者都是必要的，尽管如果您通过 Play Store 安装了应用程序，则会自动授予“绘制其他应用程序”权限，因此您只需手动授予“系统设置”权限。

一旦你做到了这一点，你就可以调整灵敏度，按钮大小和显示时间，分别调整方向检测对按钮显示的准确性，按钮的大小，以及它在屏幕上停留的时间。顺便说一下，这是按钮在屏幕上的样子(记住，你必须禁用自动旋转，否则这不会显示):

* * *

## 方法 2 —自定义导航栏(Android 7.0 以上)

以上是我的 OnePlus 5 运行在基于[安卓 8.1 奥利奥](https://www.xda-developers.com/android-8-1-oreo-final-release-imminent/)的最新 [OxygenOS 5.1.0 稳定版](https://www.xda-developers.com/oxygen-os-5-1-0-oneplus-5t-android-8-1-oreo-april-security/)上的导航栏截图。正如你所看到的，旋转建议按钮是由于自定义导航栏应用程序。目前，该功能仅在自定义导航栏应用程序的测试版中可用，它也需要专业版才能解锁。你可以[在这里](https://play.google.com/apps/testing/xyz.paphonb.systemuituner)注册测试版。完成后，从 Play Store 下载应用程序。

**注意:这款应用并不能在每一款 Android 7.0+设备上运行。请参考[XDA 官方论坛帖子](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)中的列表，了解它在哪些设备上工作的详细信息。**

按照设置过程授予它修改导航栏的必要权限。一旦你这样做了，只需在设置中启用“旋转建议”选项，你就可以开始了！

该功能仍处于测试阶段，因此预计在某些应用程序中可能会出现一些问题。开发人员正在快速更新应用程序，以修复您可能遇到的任何错误。如果您有任何反馈，请在官方论坛帖子上留下您的反馈[。](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)