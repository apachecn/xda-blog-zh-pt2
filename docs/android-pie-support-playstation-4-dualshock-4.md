# Android Pie 增加了对索尼 PlayStation 4 的 DualShock 4 的支持

> 原文：<https://www.xda-developers.com/android-pie-support-playstation-4-dualshock-4/>

# Android Pie 为索尼 PlayStation 4 的 DualShock 4 添加了控制器映射

Android Pie 终于为索尼 PlayStation 4 的 DualShock 4 控制器添加了控制器映射支持。所有 Android 9 设备都将识别 DS4！

Android Pie 终于增加了一个备受期待的功能:索尼 PlayStation 4 的 DualShock 4 的控制器映射。PlayStation 4 是市场上最受欢迎的当代游戏主机，所以难怪有很多人想用 DualShock 4 控制器在 Android 上玩手机游戏。在 Android 上使用 PlayStation 4 控制器的问题是，您的设备上可能没有按键映射。因此，虽然您可以通过蓝牙连接到 PlayStation 4 控制器，但您可能无法实际使用控制器来导航 UI 或玩任何游戏。索尼 Xperia 设备可以使用开箱即用的 DualShock 4 控制器，但对其他设备的支持取决于设备制造商。幸运的是，谷歌终于在 AOSP 添加了正确的[键映射，因此所有 Android 9 Pie 设备都应该可以使用 PlayStation 4 控制器。](https://android.googlesource.com/platform/frameworks/base/+/master/data/keyboards/Vendor_054c_Product_05c4.kl)

## Android Pie 中的 PlayStation 4 控制器支持

虽然你的 Android 智能手机可以通过蓝牙无线连接到你的 DualShock 4 控制器，但你的智能手机需要一个按键布局文件，让 Android 知道如何将控制器上的按钮按压转换为 Android 中的标准按键事件。然后，开发人员可以在他们的应用程序中监听这些关键事件，以确定在他们的应用程序中采取什么行动。例如，如果用户按下“X”键，那么射击游戏可以解释为执行射击动作，或者移动平台玩家可以用跳跃动作来响应。如果没有告诉 Android 如何翻译按键的按键布局文件，应用程序就不会知道用户按的是什么按钮。

如果您有 root 访问权限，您可以手动添加索尼在其 Xperia 设备上包含的键布局文件。如果你真的想的话，你甚至可以[设置远程播放](https://www.xda-developers.com/how-to-enable-ps4-remote-play-on-any-android-and-play-dualshock-4-tips-opinion/)。然而，如果你没有 root，你只能希望设备制造商足够关心添加对 DualShock 4 控制器的支持。有了 Android Pie，你再也不用担心这个问题了，因为默认情况下，所有 Android Pie 设备都会包含这个关键映射文件。索尼工程师一直在努力让 DualShock 4 键布局支持最早于 2017 年 4 月进入 AOSP，但那些提交不再是必要的，因为谷歌在[将代码推向 AOSP](https://www.xda-developers.com/android-pie-source-code-aosp/) 之前就在他们的内部主分支中包含了支持。由于这一变化，Android 现在支持无线 DualShock 4 控制器以及[无线 Xbox One S 控制器](https://www.xda-developers.com/android-pie-controller-mapping-fix-xbox-one-s/)。