# 如何在没有 Root 的 Android Oreo 中自定义锁屏快捷键

> 原文：<https://www.xda-developers.com/customize-lockscreen-shortcuts-android-oreo/>

[Android Oreo 终于推出了](https://www.xda-developers.com/android-8-0-oreo-google-released/)，和[很像导航栏](https://www.xda-developers.com/customise-the-navigation-bar-android-oreo/)，我们也可以自定义锁屏快捷键！它甚至比导航栏教程更容易，因为你需要的只是 adb。随着 Android Oreo 的推出，我们还将寻找许多其他调整，像你们这样的 XDA 用户可以从中受益，所以请关注我们的新闻提要。

这里需要一点背景知识。锁屏快捷方式是那些在左下角和右下角的小图标，当你唤醒手机时，你可以从键盘进入。以前你可以从 Android O 开发者预览版开始定制它们，但是在 DP3 中他们移除了这个选项。不过，手动定制锁屏快捷方式是可能的，因为谷歌只是取消了面向用户的 GUI，而不是完全取消该功能。

要获得 adb，安装“ [Minimal ADB & Fastboot](https://forum.xda-developers.com/showthread.php?t=2317790) 或[Google](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)的官方二进制文件，并启用 USB 调试。要启用 USB 调试开放设置，请转到“关于”，轻按“内部版本号”七次，然后按返回键。现在，您将看到一个“开发人员选项”菜单，您可以进入该菜单并在其中启用调试。

本指南需要 Android Oreo，它只在 Nexus 6P、Nexus 5X、Google Pixel、Google Pixel XL、Nexus Player 和 Google Pixel C 上提供。如果您还没有出厂映像，您可以现在[安装它](https://www.xda-developers.com/android-oreo-download-pixel-nexus/)！

* * *

## 如何在 Android Oreo 中自定义锁屏快捷键

编辑锁屏快捷方式的功能也存在于系统 UI 调谐器中，就像导航栏一样。在这种设置下，你不仅可以更改特定应用程序的锁屏快捷方式，还可以选择一项活动。它已经和其他选项一起被删除了，提交消息声明“它们还没有完全完成”。幸运的是，我们仍然可以在这里做到这一点，但比谷歌过去提供的优雅的解决方案要多做一点工作。要启动 adb，按住 shift +右键单击包含 adb 的文件夹，并确保您的手机连接到您的 PC 并启用调试。虽然编辑快捷方式很容易，但您需要使用以下命令来编辑它们。

对于左侧:

```
 settings put secure sysui_keyguard_left "COMPONENT/NAME" 
```

对于右侧:

```
 settings put secure sysui_keyguard_right "COMPONENT/NAME" 
```

其中“组件”是应用程序的包名，“名称”是活动的名称。

例如，如果我想通过从左侧滑动来启动 Google Hangouts 左窗格，我将输入如下 adb 命令。

```
 settings put secure sysui_keyguard_left "com.google.android.talk/com.google.android.apps.hangouts.phone.BabelHomeActivity" 
```

这适用于任何应用程序和活动。要查找应用程序包名称和活动，您可以使用 Play Store 上的 Activity Launcher 来查找活动的名称。您可以在该应用程序中试验各种活动，并找到您想要的活动。

接下来，如果你想让快捷方式解锁设备，你也可以这样做。只需使用以下命令:

```
 settings put secure sysui_keyguard_left_unlock 0/1
settings put secure sysui_keyguard_right_unlock 0/1 
```

其中 0 表示当快捷键激活时设备保持锁定，1 表示解锁设备。

* * *

就是这样！没有太多的方法来进一步定制这些快捷方式，但这是一个很好的方法来加快启动一些你最喜欢的应用程序。玩一玩，看看你能做什么，然后告诉我们！