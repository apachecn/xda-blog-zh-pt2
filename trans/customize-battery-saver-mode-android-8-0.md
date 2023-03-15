# 安卓 8.0 奥利奥如何自定义省电模式

> 原文：<https://www.xda-developers.com/customize-battery-saver-mode-android-8-0/>

Android 上的电池节电模式可以通过限制后台服务、禁用动画和执行各种其他调整来有效延长电池寿命。然而，它采用了一些额外的措施，有些措施可能显得过分或不必要。例如，振动真的需要足够的能量来证明关掉它是正确的吗？禁用振动的代价是你可能会错过重要的信息。在电池保护程序中，屏幕也会变暗，但仅仅因为我的电池已经达到 15%并不意味着我不需要使用最大亮度才能看到。这些都是你在使用电池节电器时不得不忍受的事情，直到现在你都没有办法选择你想要的东西。我们将向您展示如何在 Android 8.0 Oreo 中**定制电池节电模式。要学习本教程，你不需要 root 权限，但你需要[使用 adb](https://www.xda-developers.com/install-adb-windows-macos-linux/) 。**

* * *

## 在 Android 8.0 Oreo 中自定义电池节省模式

Android Oreo 的另一个改进是可以编辑电池节电器的功能！这些命令需要 adb，但是您所做的更改会保持不变。首先，观察下面的图片，取自 Android Oreo 的源代码。

因此，这些值中的每一个都应该相当简单，以便理解它们的作用，但是我们还是会解释它是如何工作的。每个设置都采用一个布尔值、一个整数或一个浮点值。boolean 是“真”或“假”，integer 只是标准的整数，float 是可以包含小数的数字。

那么这有哪些用例呢？以下是一些例子:

### 启用振动

为了在省电模式下启用振动，我们需要将 vibration_disabled 设置为“false”。

### 启用动画

要在电池保护程序中启用动画，我们需要将“animation_disabled”设置为“false”。

### 禁用亮度变暗

要禁用亮度变暗，请将“adjust_brightness_disabled”更改为“true”。

## 如何更改电池节电设置

因此，在您选择了想要更改的值之后，我们可以提出我们想要运行的 ADB 命令，以对节电模式执行这些更改。例如，每当我打开电池保护时，我想启用振动、启用动画和禁用屏幕亮度变暗。打开命令提示符/终端，键入“adb devices ”,以确保您的计算机能够识别您的设备。

一旦有了类似上面的输出，输入“adb shell ”,就可以继续了！

例如，在我的例子中，我会键入以下内容。

```
 settings put global battery_saver_constants "vibration_disabled=false,animation_disabled=false,adjust_brightness_disabled=true" 
```

如您所见，我将我想对电池保护模式所做的更改放入一个以逗号分隔的 key=value 列表中。您可以根据需要向该命令添加或移除任意数量的操作数。任何保持不变的值都不会改变，并将保留其原始默认值。

发送上述命令后，断开手机与电脑的连接。启用电池保护，看到你的手机现在振动，动画打开，亮度不再变暗。

### 对设备上的电池节电程序进行更改(Root)

如果你有 root 用户，实际上可以从你的设备上编辑这些设置！如果您的设备是通过 Magisk 或 SuperSU 启动的，您只需从 Termux 等终端应用程序运行与上述相同的命令。按照上面的语法，像往常一样运行命令。

* * *

## 说明

看起来谷歌正在努力增加许多提高生活质量的功能。随着主题化、[锁屏快捷键](https://www.xda-developers.com/customize-lockscreen-shortcuts-android-oreo/)命令的加入，谷歌无疑正在努力完善操作系统，允许调整许多设备区域。希望我们能找到更多像这样可修改的设置！