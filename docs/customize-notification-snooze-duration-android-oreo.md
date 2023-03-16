# 如何在没有 Root 的 Android 8.1 Oreo 上更改通知暂停持续时间

> 原文：<https://www.xda-developers.com/customize-notification-snooze-duration-android-oreo/>

随着[安卓 P](https://www.xda-developers.com/tag/android-p/) [即将到来](https://twitter.com/mishaalrahman/status/958428092669874176)，大部分用户可能最近才更新到[安卓 8.0 奥利奥](https://www.xda-developers.com/tag/android-oreo/)，更不用说[安卓 8.1](https://www.xda-developers.com/nokia-8-android-oreo-update-2/) 了。Android Oreo 带来了大量有用的功能，如更好的电池寿命/内存使用，这要归功于[严格的后台应用限制](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)，画中画模式[，通知通道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)，[更快的启动时间](https://www.xda-developers.com/android-o-to-cut-reboot-time-in-half-significantly-improve-app-performance/)，以及用于密码管理器的自动填充 API 。另一个有用的功能是[通知休眠](https://www.xda-developers.com/android-8-0-oreo-google-released/)，这个功能最终允许你暂时关闭通知来清理你的状态栏。默认情况下，你只能暂停 15 分钟、30 分钟、1 小时或 2 小时的通知，但如果你运行的是 Android 8.1 Oreo，没有 root 用户也可以自定义这些数字。以下是方法。

*默认奥利奥通知暂停持续时间*

* * *

## 如何在 Android 8.1 Oreo 上自定义通知暂停持续时间

虽然 Android 8.0 Oreo 引入了通知打盹，但直到 Android 8.1 Oreo，谷歌才引入了一种定制打盹持续时间的方法。因此，本教程将只适用于 Android 8.1 设备，如谷歌 Nexus 5X、谷歌 Nexus 6P、谷歌 Pixel、谷歌 Pixel XL、谷歌 Pixel 2、谷歌 Pixel 2 XL、诺基亚 8，以及任何运行定制的基于 AOSP 的 Android 8.1 ROM 的设备。

我们使用的方法包括通过 Android 调试桥(ADB)改变一个隐藏的设置。由于这并不涉及解锁你的引导程序或下载你的设备，你可以通过 OTA 更新或通过 Android Pay 支付。你所需要的只是你的设备、你的电脑和一个由 XDA 论坛主持人开发的名为 T2 系统界面调谐器的应用程序。这款应用在谷歌 Play 商店上是免费的，但请确保你运行的是**248**版本，否则你将无法使用这项新功能。

下面是一个关于如何使用这个应用程序在 Android 8.1 Oreo 上更改通知暂停持续时间的分步教程:

1.  按照我们的教程[在这里](https://www.xda-developers.com/install-adb-windows-macos-linux/)设置 ADB。
2.  打开命令提示符或终端，输入以下内容:`adb shell pm grant com.zacharee1.systemuituner android.permission.WRITE_SECURE_SETTINGS`
3.  启动 SystemUI Tuner 应用程序并浏览设置屏幕。
4.  点击“调整”
5.  接受弹出的警告。
6.  点击“杂项”
7.  向下滚动到“通知休眠”部分。
8.  对于“默认”,选择通知暂停持续时间的默认时间**,单位为分钟**。
9.  对于“时间 A”到“时间 D”，选择通知暂停持续时间应该设置为的 4 个时间**(以分钟**为单位)。例如，如果我想要 30 分钟、1 小时、2 小时和 6 小时，我将从 A 到 D 分别输入 30、60、120 和 360。
10.  确保“默认”小睡持续时间**与您在第 9 步中选择的数字**相匹配。
11.  最后，为了让它在重启时保持不变，点击应用右上角的菜单按钮，选择“设置”然后，切换“**安全模式**，允许应用程序在重启时恢复这些值。

你完了！需要记住的是，启用“安全模式”会在状态栏中显示一个烦人的通知，但你可以通过长按它并禁用其通知通道来轻松隐藏该通知。此外，您的新通知暂停持续时间**将不会出现在状态栏中的任何现有通知**上——只有在您进行此更改后出现的新通知。

 <picture>![How to change the Notification Snooze Durations on Android 8.1 Oreo without Root](img/408e8b980e57d4b6bb684d92869c8573.png)</picture> 

Snooze Button on Notifications in Android 8.1 Oreo

作为奖励，因为你已经经历了设置 SystemUI Tuner 的麻烦，你可以使用应用程序中提供的任何其他功能！这里和那里有许多小的调整，可能会使你的用户界面看起来更舒服一点！

* * *

## 这是如何工作的

好的，所以你们中的一些人可能想知道这到底是怎么回事。这很简单，谷歌增加了一个[开发者选项](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/provider/Settings.java#10975)，允许改变通知暂停选项。该选项只能通过 ADB 访问，因为它位于设置表中。您可以直接通过 ADB 更改此选项，或者像我们上面所做的那样授予应用程序 WRITE_SECURE_SETTINGS 权限，以便应用程序可以访问该表。

可以通过在 ADB 中发出如下命令来更改此选项:

```
 adb shell settings put global notification_snooze_options "default=60,options_array=30:60:120:360" 
```

这正是 Zacharee1 的 SystemUI Tuner 应用程序的工作方式。我自己发现了这个小技巧，并要求 Zacharee1 将其添加到他的应用程序中，以便让你们更容易使用它，所以享受这个调整吧！