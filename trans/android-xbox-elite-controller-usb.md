# Android 通过 USB 为 Xbox Elite 控制器添加了控制器映射

> 原文：<https://www.xda-developers.com/android-xbox-elite-controller-usb/>

# Android 通过 USB 为 Xbox Elite 控制器(系列 1)添加了控制器映射

谷歌为 Xbox Elite 控制器添加了一个关键布局文件，这意味着当连接到 Android 智能手机或平板电脑时，它可以通过 USB 工作。

如果你想在 Android 智能手机或平板电脑上玩游戏，你可能需要通过 USB 或蓝牙连接游戏手柄或控制器。有大量的通用游戏配件可以在您的设备上运行，但你们中的许多人可能会对使用您已经拥有的游戏控制器感兴趣。例如，如果你有一台 PlayStation 4，你可以将 DualShock 4 控制器连接到智能手机上进行播放。不幸的是，这并不是在每个设备上都有效，原因通常归结为缺少关键布局文件。如果你通过 USB 将 Xbox Elite 无线控制器(系列 1)连接到大多数 Android 设备，它将无法工作，但这可能会在未来的 Android 版本中发生变化。

AOSP Gerrit 最近的一次[提交](https://android-review.googlesource.com/c/platform/frameworks/base/+/1105183)为 1698 型 Xbox Elite 控制器添加了一个按键布局文件。这意味着控制器上的按钮按压将被映射到游戏可以监听的的[适当的 Android 动作。如果没有这个按键布局文件，Android 上的按键将无法识别，或者会执行不希望的操作。遗憾的是，Xbox Elite 控制器不能无线连接到您的 Android 设备，因为它不能通过蓝牙操作。](https://developer.android.com/training/game-controllers/controller-input.html)

谷歌还为更多 Xbox One 控制器添加了[的关键布局文件(USB 的型号为 1537，USB 和蓝牙的型号为 1708)。一年前，谷歌去年为](https://android-review.googlesource.com/c/platform/frameworks/base/+/1105184/1) [Xbox One S 无线控制器](https://www.xda-developers.com/android-pie-controller-mapping-fix-xbox-one-s/)添加了控制器映射。随着这些关键布局文件的加入，更多的 Android 设备将能够连接到微软的 Xbox 控制器。我们不确定这个关键布局文件是否会出现在所有运行 Android Q 的设备上，但可以肯定的是，如果 OEM 厂商在明年之前不手动添加它，它会出现在 Android R 中。事实上，如果 OEM 费心自己添加这样的关键布局文件，你的 Android 设备可能比大多数设备支持更多的控制器。

*特色图片:Xbox Elite 无线控制器(系列 1)——鸣谢:微软*