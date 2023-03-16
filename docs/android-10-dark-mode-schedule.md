# Android 10 黑暗模式:如何为其设置时间表

> 原文：<https://www.xda-developers.com/android-10-dark-mode-schedule/>

稳定的 Android 10 现在可用于所有代的 Pixel 智能手机和 Essential 手机，它带来了大量备受欢迎的功能，如改进的手势导航和全系统黑暗模式。后一个功能可能是最有影响力的，因为它导致许多应用程序添加了黑色主题，如 [Gmail](https://www.xda-developers.com/google-gmail-dark-mode-android/) 、[谷歌 Play 商店](https://www.xda-developers.com/google-play-store-dark-theme-android-10/)等等。在早期的 Android Q betas 中，你可以根据一天中的时间来安排黑暗模式的切换，就像夜间照明一样。然而，谷歌[取消了](https://www.xda-developers.com/android-q-ama-summary/)这个选项，因为它可能会在你使用应用程序时突然重启它们，从而对用户体验产生负面影响。谢天谢地，有了第三方应用，你可以带回 Android 10 黑暗模式调度。

我确认这个应用程序可以在我运行稳定的 Android 10 版本的 Pixel 2 XL 上运行。我所要做的就是安装它并运行一个 ADB 命令来授予它更改控制系统范围黑暗模式切换的设置的权限。ADB，即 Android Debug Bridge，是一款开发者工具，可以用来控制手机上的各种选项；它主要用于开发，但也可以用来授予 Android 操作系统不允许授予的权限。只要你小心你授予权限的应用程序，你将是安全的。哦，运行这个命令不会以任何方式使保修无效。

在您授予应用程序适当的权限后，应用程序将根据您选择的时间表处理黑暗模式的更改。最好的部分是，它还有一个选项，只改变手机锁定时的活动主题。这样，当你在使用某个应用时，它不会突然重启。现在，这里是如何设置它。

【Android 10 自动黑暗主题截图，从应用的 Play Store 列表中检索。

**要求:**

*   **Android 10(稳定版、测试版或定制 ROM):** 目前在所有 Pixel 智能手机和 Essential 手机上提供稳定版，但也在[华为 P30 Pro](https://www.xda-developers.com/emui-10-huawei-p30-pro-android-q-hands-on/) 、[小米 Mi 9](https://www.xda-developers.com/android-q-miui-xiaomi-mi-9-video/) 、红米 K20 Pro (“稳定版测试版”)和许多其他手机上提供测试版。[自定义 ROM 用户](https://www.xda-developers.com/tag/android10/)也可以利用这个 app。
*   **ADB 安装在您的电脑上。**如何在你的 Windows、macOS 或 Linux 电脑上设置它的说明[可以在这里找到](https://www.xda-developers.com/install-adb-windows-macos-linux/)。

**步骤:**

1.  安装来自谷歌 Play 商店的“Android 10 自动黑暗主题”应用程序。您可以点击上方方框中的链接，或者点击此处的。
2.  将您的手机插入 PC，在下载 ADB 二进制文件的同一目录下打开命令提示符或终端窗口。
3.  打开手机上的应用程序。
4.  运行以下命令: **Windows 10 命令提示符:**

    ```
     adb shell pm grant com.cannic.apps.automaticdarktheme android.permission.WRITE_SECURE_SETTINGS 
    ```

    **Windows 10 PowerShell:**

    ```
     .\adb shell pm grant com.cannic.apps.automaticdarktheme android.permission.WRITE_SECURE_SETTINGS 
    ```

    **MAC OS/Linux 终端:**

    ```
     ./adb shell pm grant com.cannic.apps.automaticdarktheme android.permission.WRITE_SECURE_SETTINGS 
    ```

5.  享受使用应用程序的乐趣！您可以通过更改是否希望应用程序仅在手机锁定时切换黑暗模式来稍微定制应用程序的行为。还可以隐藏应用发布的通知；这个通知对于应用程序在后台运行是必要的，这样它就可以按计划改变黑暗主题，而不会被 Android 操作系统杀死。

这款应用的开发者[表示](https://www.reddit.com/r/androidapps/comments/d2pzdl/dev_automatic_dark_theme_for_android_10/)他们计划增加基于日出和日落时间表的黑暗模式调度，以及从应用抽屉中隐藏应用图标的选项。这是一个相当简单的应用程序，它的工作做得很好，但这些增加的功能将使 Android 10 黑暗模式调度感觉像一个原生功能。

* * *

*注意:虽然你可以使用像 [Tasker](http://xda-developers.com/tag/tasker) 这样的自动化应用程序在技术上自动化 Android 10 中的黑暗模式，但这个应用程序是免费使用的，并且只有一个目的。如果你对自动化感兴趣，我强烈推荐你学习如何使用像 Tasker 这样的应用。*