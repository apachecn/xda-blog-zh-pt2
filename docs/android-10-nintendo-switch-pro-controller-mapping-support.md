# Android 10 为任天堂 Switch Pro 控制器带来了控制器映射支持

> 原文：<https://www.xda-developers.com/android-10-nintendo-switch-pro-controller-mapping-support/>

# Android 10 为任天堂 Switch Pro 控制器带来了控制器映射支持

Android 10 增加了对任天堂 Switch Pro 控制器的支持，允许用户在游戏中正确使用该控制器。继续阅读，了解更多信息！

在 Android 上玩游戏通常意味着在智能手机的触摸屏上玩游戏。虽然 Android 确实拥有非常多的触摸优化游戏，但当玩家使用游戏手柄和真正的硬件按钮和按键时，一些游戏的效果会更好。出于同样的目的，您可以找到一整套通用游戏配件，包括控制器，让您轻松升级游戏体验。例如，如果你有一台 PlayStation 4，你可以将 DualShock 4 控制器连接到智能手机上进行播放。不幸的是，这并不是在每个设备上都有效，原因通常归结为缺少关键布局文件。

如果你正在寻求重用你现有的游戏控制器，Android 已经逐渐增加了对各种流行控制器的支持，如 [Xbox One S 无线控制器](https://www.xda-developers.com/android-pie-controller-mapping-fix-xbox-one-s/)，以及 Xbox Elite 系列 1 控制器。对 AOSP 提交的一项研究显示，Android 10 还带来了使用任天堂 Switch Pro 控制器连接和正确播放 Android 的能力。

AOSP Gerrit 中的一个[提交](https://android.googlesource.com/platform/frameworks/base/+/94db68e0319b5c81aee0da8312f9638fc33b0727%5E%21/#F1)已经添加到任天堂 Switch Pro 控制器的按键布局文件中。按键布局文件使 Android 能够正确识别控制器上的按钮按压，并将其映射到游戏可以监听的适当 Android 动作。没有这个按键布局文件，游戏要么不能识别硬件按键，要么会启动错误的动作。

任天堂 Switch Pro 控制器与任天堂 Switch 一起推出，是 Joy-Cons 的更好选择。这个提交是在 2019 年 6 月添加的，所以你手机上的 Android 10 更新很可能已经包含了相同的内容。如果你身边有一个任天堂 Switch Pro 控制器，你可以检查并确认它是否可以在你的 Android 10 设备上无缝工作。

* * *

**来源:[AOSP·格里特](https://android.googlesource.com/platform/frameworks/base/+/94db68e0319b5c81aee0da8312f9638fc33b0727%5E%21/#F1)**