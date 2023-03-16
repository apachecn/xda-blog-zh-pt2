# Android Pie 增加了一个功能，可以防止意外退出时杀死大量内存的游戏

> 原文：<https://www.xda-developers.com/android-pie-ram-heavy-games-exit/>

今天早些时候，谷歌[正式宣布了谷歌 Pixel 和谷歌 Pixel 2 的](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/) Android Pie。紧接着， [Essential 发布了](https://www.xda-developers.com/essential-phone-android-pie-android-9/)Essential 手机的 Android 9 更新。[其他参与了](https://www.xda-developers.com/android-p-beta-program-is-now-available/)Android P beta 计划的设备应该很快就会收到更新，所以跳过开发者预览版的用户现在有很多事情要做。随着我们深入研究最新版本，包括 AOSP 上的[源代码和最新的兼容性定义文档(CDD)，我们将定期向您更新我们发现的任何新信息。我们在 CDD 中发现了一个有趣的现象，那就是有一个“重量级”(RAM-heavy)应用和游戏区，如果用户意外退出，Android Pie 会优先将这些应用保存在 RAM 中。](https://www.xda-developers.com/android-pie-source-code-aosp/)

## 安卓派中的“重量级”应用和游戏

在 [CDD](https://source.android.com/compatibility/cdd) 中增加了一个新的章节来概述这一特性。它是这样说的:

### 3.17.重量级应用

如果设备实现声明了特征 FEATURE_CANT_SAVE_STATE，那么它们:

*   [C-1-1]一次只能安装一个指定 cantSaveState 的应用程序在系统中运行。如果用户在没有明确退出的情况下离开这样的应用程序(例如，通过在离开系统的活动时按 home，而不是在系统中没有剩余活动的情况下按 back)，则设备实现必须在 RAM 中优先考虑该应用程序，就像它们为预期将保持运行的其他事情所做的那样，例如前台服务。虽然这样的应用程序在后台，但系统仍然可以对其应用电源管理功能，例如限制 CPU 和网络访问。
*   [C-1-2]必须提供一个 UI 启示，以便在用户启动另一个声明了 cantSaveState 属性的应用时，选择不参与正常状态保存/恢复机制的应用。
*   [C-1-3]不得将策略中的其他更改应用于指定 cantSaveState 的应用，如更改 CPU 性能或更改调度优先级。

如果设备实现没有声明特性FEATURE _ CANT _ SAVE _ STATE，那么它们:

*   [C-1-1]必须忽略 apps 设置的 cantSaveState 属性，并且不得基于该属性更改 appbehavior。

基本上，这意味着，如果一个设备支持 [FEATURE_CANT_SAVE_STATE](https://developer.android.com/reference/android/content/pm/PackageManager#FEATURE_CANT_SAVE_STATE) 功能，那么他们必须优先在 RAM 中保留指定 [cantSaveState](https://developer.android.com/reference/android/R.attr#cantSaveState) 属性的运行应用。如果用户通过按下 home 按钮退出应用程序或游戏，或者在没有明确退出的情况下离开应用程序或游戏(如按下 back 按钮或 quit 按钮),则 RAM 优先化开始。)此外，系统仍然可以通过限制这些应用程序的 CPU 和网络访问来节省电力，但除非必要，否则他们无法通过杀死它们来释放 RAM。最后，请注意，只允许运行一个定义了 cantSaveState 属性的应用程序。如果你试图在另一个应用程序运行时启动另一个定义了该属性的应用程序，Android Pie 会要求你选择你想要继续运行的游戏。

您可以通过 ADB 运行以下两个命令来检查您的设备是否支持 FEATURE_CANT_SAVE_STATE:

```
 adb shell
dumpsys package | grep "cant_save_state" 
```

要检查应用程序是否指定了 cantSaveState 属性，需要反编译应用程序并查看其清单，或者在 ADB shell 中使用`dumpsys package package.name.here`命令。请记住，这个属性只是刚刚在 API level 28 (Android 9 Pie)中添加的，所以还不太可能有很多应用程序或游戏会利用这一点。

这项功能对于内存容量小的设备和/或消耗大量内存的应用程序来说非常有用。例如，安卓系统上的堡垒之夜移动[需要至少 3gb 的内存](https://www.xda-developers.com/minimum-requirements-fortnite-mobile-on-android/)，因为它消耗了大量的内存(甚至没有启动游戏，堡垒之夜移动就在我的谷歌 Pixel 2 XL 上保留了 1.6GBs 的内存。)如果堡垒之夜的目标是 SDK level 28 并使用该功能，那么这意味着如果你的设备空闲内存不足，意外退出游戏将有望防止它立即被杀死。不幸的是，堡垒之夜[目前只针对 SDK 级](https://www.xda-developers.com/fortnite-mobile-on-android-samsung-galaxy-note-9-exclusive/)(Android 5.0 Lollipop)，所以它没有利用谷歌在 Android Pie 中提供的最新 API，更不用说 Android 奥利奥、Android 牛轧糖或 Android 棉花糖了。希望其他游戏也能利用这一特性。明年，谷歌[将要求他们](https://www.xda-developers.com/developers-new-app-play-store-api-level-26/)更新，如果他们想继续在谷歌 Play 商店上提交更新的话。