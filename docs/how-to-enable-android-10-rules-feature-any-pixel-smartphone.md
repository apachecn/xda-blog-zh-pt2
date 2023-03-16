# 如何在任何 Pixel 智能手机上启用 Android 10 的规则功能

> 原文：<https://www.xda-developers.com/how-to-enable-android-10-rules-feature-any-pixel-smartphone/>

# 如何在任何 Pixel 智能手机上启用 Android 10 的规则功能

Android 10 带有规则功能，允许你自动完成某些基本任务。查看如何在任何具有 root 用户的 Pixel 智能手机上启用它！

每年都会发布一个新的 Android 版本，谷歌会在 I/O 上展示一些最显著的操作系统变化。但是由于[缺少时间](https://www.xda-developers.com/google-pixel-4-what-you-missed/)，总是有很多[在](https://www.xda-developers.com/google-android-10-dsu-try-ota-updates-without-committing/)阶段没有涉及到的特性，这些特性最终在阶段[被发现。“](https://www.xda-developers.com/android-10-manifest-flag-developers-retain-app-data-before-uninstalling/)[规则](https://www.xda-developers.com/android-10-rules-automation-feature-rolls-out-some-pixel-devices/)”是 Android 10 的一个这样的功能，无论是在 Google I/O 2019 的 Android Q 主题活动上，还是在 [Google Pixel 4 发布会](https://www.xda-developers.com/google-pixel-4-specs-features-pricing-availability/)上，谷歌都没有强调。Rules 最初是作为[设置例程](https://www.xda-developers.com/google-pixel-android-q-settings-routines/)出现的，允许用户根据特定条件在设备上自动执行一些常见操作。奇怪的是。该功能在稳定的 Android 10 版本中从 surface 中缺失，在 Pixel 4 上也不可用。这个特性[突然出现在一些像素所有者的面前](https://www.xda-developers.com/android-10-rules-automation-feature-rolls-out-some-pixel-devices/)，但是没有办法全面启用它。现在，如果你愿意根你的设备，你可以在任何装有最新 Android 10 版本的 Pixel 设备上启用规则。

在 Android 10 上，规则允许符合条件的 Pixel 设备所有者设置条件，当满足条件时，可以启用勿扰模式，或将手机设置为静音、振动或铃声模式。这些条件包括连接到特定的 Wi-Fi 网络，或者当您在选定的位置附近时。当然，就功能而言，Rules 无法与专用自动化应用程序(如 [Tasker](https://forum.xda-developers.com/u/tasker-tips-tricks) 和 Automate)相媲美，但它提供了有用的基本功能。

如果您有 root 用户，但是被更复杂的自动化工具吓住了，您可以按照下面的步骤来启用该功能:

1.  1.  使用具有 root 访问权限的文件浏览器，然后转到*/data/data/com . Google . Android . settings . intelligence/shared _ prefs*
    2.  打开*settings Google intelligence sharedprefile . XML*
    3.  将所有名称中带有“*routine prototype*”的布尔值更改为“ *true*
    4.  强制关闭设置和设置建议。
    5.  通过终端模拟器在手机上运行以下命令:

        ```
         su
        pm enable com.google.android.settings.intelligence/.modules.routines.impl.settings.RoutinesSettingsActivity 
        ```

    6.  现在，你应该可以在设置中的“系统”下找到“规则”

无可否认，规则是其功能的基础。如果你有查找设备和执行上述指令的经验，你也应该能够用 Tasker 创建相同的任务(甚至更好)。但是安卓都是有选择的，多一些也是好的。

* * *

**故事 Via:[/r/Android](https://www.reddit.com/r/Android/comments/dr4r7k/enable_android_10_rulesroutines_on_any_rooted/)**