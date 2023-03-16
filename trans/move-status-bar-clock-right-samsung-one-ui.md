# 如何在运行单一用户界面的 Samsung 设备上将状态栏时钟向右移动

> 原文：<https://www.xda-developers.com/move-status-bar-clock-right-samsung-one-ui/>

# 如何在运行单一用户界面的 Samsung 设备上将状态栏时钟向右移动

三星的 One UI 更新将状态栏时钟移到了状态栏的左侧。以下是如何将它恢复到右侧的方法。

三星的 [One UI](https://www.xda-developers.com/?tag=one-ui) 更新是三星自己的 UX 皮肤最好的更新之一。在 Android 2.1 艾克蕾尔上以 TouchWiz 开始的东西现在已经成为基于 Android 9 Pie 的一个用户界面，带来了多年来被用户采纳和喜欢的改进和功能。三星的 UX 不再像过去一样落后；虽然它可能仍然无法与现有的 Android 体验相比，但普通用户在较新的三星旗舰机上采用三星的 One UI 不会有任何问题。

然而，没有一个软件是完全完美的。出于不完全理解的原因，三星的 One UI 将状态栏时钟移到了设备的左上角。这种变化可能是在考虑到三星 Galaxy S10 上存在摄像头切口的情况下完成的，但这种变化会影响所有 One UI 设备，即使它们在设备的右上角没有摄像头切口。

如果你想将状态栏时钟恢复到它在设备右上角的原始位置，你可以使用 XDA 认可的开发者[za chare 1](https://forum.xda-developers.com/member.php?u=7055541)的 [SystemUI Tuner](https://forum.xda-developers.com/android/apps-games/app-systemui-tuner-t3588675) 应用来实现。

在运行单一用户界面的 Samsung 设备上，按照下述步骤进行操作:

1.  从谷歌 Play 商店下载并安装 [SystemUI Tuner](https://play.google.com/store/apps/details?id=com.zacharee1.systemuituner&hl=en_IN) 。注册测试版，并在注册后进行更新
2.  按照应用程序中写的说明，通过 ADB 授予它几个权限。这里有关于如何[设置和使用 ADB 的说明](https://www.xda-developers.com/install-adb-windows-macos-linux/)。
3.  打开应用，进入“TouchWiz”子菜单。
4.  导航到“杂项”下拉菜单，并将“时钟位置”设置为“右”

就是这样！该方法非常简单，不需要任何复杂的设置。在截图中，你也可以看到状态栏时钟已经改变了位置。

你可以在其[论坛主题](https://forum.xda-developers.com/android/apps-games/app-systemui-tuner-t3588675)中了解更多关于开源 SystemUI Tuner 应用的信息。