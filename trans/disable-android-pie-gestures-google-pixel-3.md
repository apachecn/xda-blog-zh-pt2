# 如何在谷歌 Pixel 3 上禁用 Android 饼图手势

> 原文：<https://www.xda-developers.com/disable-android-pie-gestures-google-pixel-3/>

如果你在谷歌 Pixel 3 之前使用过 Android 智能手机，你可能会熟悉后退、主页和最近应用概述的 3 按钮导航栏布局。在 Android Pie 中，谷歌引入了手势导航，允许你向上滑动以查看最近的应用程序，向右滑动以切换到上一个应用程序，向右滑动并按住以在最近的应用程序之间滚动，按下后退按钮或按下 home 按钮。谷歌让这种新的导航风格对所有升级到 Android Pie 的设备都是可选的，如谷歌 Pixel 和谷歌 Pixel 2，但在谷歌 Pixel 3 上是强制性的。如果你一直想知道如何在 Pixel 3 或 Pixel 3 XL 上禁用新的 Android Pie 手势，有一种非官方的方法可以做到这一点。

### 背景

在 Android 9 Pie 中，谷歌将新的导航风格与经过改进的横向最近应用概述集成到预装的启动器应用中。在谷歌 Pixel 3 上，这是 Pixel 启动器。在之前的 Android 版本中，最近的应用概述与 SystemUI 绑定在一起。如果由于某种原因，预装的启动器应用程序在 Android Pie 设备上被卸载，那么系统将退回到使用旧的最近应用程序风格，手势将不再工作。因此，如果我们能以某种方式卸载谷歌像素启动器，我们将禁用手势导航。我们的最后一步是重新启用旧的 3 按钮导航栏布局。以下是如何做到这一切，没有根。

**注意:如果你想在谷歌 Pixel 3 上禁用 Android Pie 手势，你将无法使用原来的谷歌 Pixel 启动器。然而，如果你决定回到手势导航，你可以很容易地再次加载 Pixel Launcher。或者，你可以使用类似于[无根像素发射器](https://www.xda-developers.com/rootless-pixel-launcher-google-play-store-pixel-bridge/)的东西，它是股票发射器的增强版本。**

### 如何在谷歌 Pixel 3 上禁用 Android 饼图手势

1.  安装您选择的任何第三方启动器。这是必须的，因为否则，一旦我们完成了这个教程，你就不会有一个启动器程序了！
2.  在您的电脑上设置 ADB。这里有一个我们之前写的教程，你应该通过这个过程。
3.  将您的 Pixel 3 连接到您的 PC，并在您下载 ADB 二进制文件的目录中打开命令提示符/终端。根据你的 OS 输入以下命令: **Windows 命令提示符**

    ```
     adb shell 
    ```

    **Windows Power Shell**

    ```
     .\adb shell 
    ```

    **MAC OS/Linux 终端**

    ```
     ./adb shell 
    ```

4.  现在，输入以下命令从当前用户卸载 Pixel 启动器。

    ```
     pm uninstall -k --user 0 com.google.android.apps.nexuslauncher 
    ```

5.  现在，输入这个命令在重启后重新启用股票导航栏。[这个](https://android.googlesource.com/platform/frameworks/base/+/pie-dr1-release/core/java/android/provider/Settings.java#7732)是您将通过发出以下命令来更改的设置。

    ```
     settings put secure system_navigation_keys_enabled 1 
    ```

6.  重启你的 Pixel 3。
7.  一旦你启动备份，你应该看到原来的 3 按钮导航栏布局和原来的垂直堆叠卡最近的应用概述。

### 如何在谷歌 Pixel 3 上重新启用 Android 饼图手势

如果你想重新使用新的手势，你需要重新安装 Pixel Launcher。只需从[这里](https://www.apkmirror.com/apk/google-inc/pixel-launcher/pixel-launcher-9-4902955-release/pixel-launcher-9-4902955-android-apk-download/)下载它，然后像加载其他应用程序一样加载它。它是由谷歌签署的，所以它是安全的。侧加载后，你必须重启来修复崩溃并恢复旧的手势。

* * *

旁注:如果你有 root 权限，有办法在不禁用 Pixel 启动器的情况下恢复旧的导航栏布局。一旦 Magisk 更新到与 Pixel 3 兼容，我们将继续跟进。