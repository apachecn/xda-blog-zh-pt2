# 如何在任何 Android 10 设备上获得带有概述文本和图像选择的 Pixel 启动器

> 原文：<https://www.xda-developers.com/pixel-launcher-overview-text-image-selection-rooted-android-10-device/>

# 如何在任何 Android 10 设备上获得带有概述文本和图像选择的 Pixel 启动器

通过 Magisk 模块和一些其他技巧，你可以在 Android 10 设备的 Pixel Launcher 概览屏幕上选择文本和图像。

当谷歌在 Android P 中切换概览屏幕时，他们引入了一个名为“[智能选择](https://www.xda-developers.com/android-p-beta-3-google-pixel-2-xl/)的新功能基本上，将 Pixel Launcher 概览切换到具有高分辨率预览的水平滚动卡允许 OCR(光学字符识别)在其上工作。你可以从应用程序最后状态的截图中选择文字和图片。不幸的是，谷歌[将这一功能](https://www.xda-developers.com/android-p-smart-selection-app-actions-limited-google-pixel-2/)限制在 Pixel 2 和更新的 Pixel 设备上。

当然，如果你愿意做一点修改，这些限制很容易被打破。通过 QuickSwitch Magisk 模块和其他一些技巧，你可以在任何 Android 10 设备的 Pixel Launcher 概览屏幕上选择文本和图像。感谢 XDA 资深会员 [remewer](https://forum.xda-developers.com/member.php?u=9101454) ，如果你已经有了一台安装了 Magisk (20.1+)的 ARM64 Android 10 设备，设置过程相当简单。

**注意:安装设备个性化服务可能无法在您的设备上运行，并可能导致引导循环。您的里程可能会有所不同。如果发生这种情况，可以在/data/adb/modules 中删除该模块。**

1.  安装像素启动器 APK ( [在这里找到](https://www.apkmirror.com/apk/google-inc/pixel-launcher/))但是*不要*设置它为你的默认启动器。
2.  打开 Magisk 管理器，搜索由 Lawnchair 团队创建的[快速切换模块](https://forum.xda-developers.com/apps/magisk/module-quickswitch-universal-quickstep-t3884797)。
3.  安装模块并重启手机。
4.  打开 QuickSwitch 并选择 Pixel Launcher 作为 Recents 提供程序。重启你的手机。
5.  将 Pixel 启动器设置为默认启动器。
6.  安装设备个性化服务 Magisk 模块[在这里找到](https://forum.xda-developers.com/showpost.php?p=81023021&postcount=16)，由 XDA 资深会员 paphonb 创建并由我们修改。重启你的手机。
7.  打开像素启动器设置，选择建议并启用这两个选项。
8.  就是这样！

*OnePlus 6 上带有概览选择的像素启动器*

**[在 OnePlus 6 论坛](https://forum.xda-developers.com/oneplus-6/how-to/pixel-launcher-overview-selection-t3997955)** 了解更多关于这个 mod 的信息