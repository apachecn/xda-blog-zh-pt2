# 阻止飞行模式关闭 Android 上的 WiFi、蓝牙或 NFC

> 原文：<https://www.xda-developers.com/customize-radios-airplane-mode-android/>

人们一直担心手机的无线电频率会导致飞机设备出现问题。在智能手机时代之前，飞机上的乘客被要求关掉所有电子设备，以防万一。智能手机引入了飞行模式，因此我们仍然可以使用它们做其他事情，如玩游戏或看视频。一些用户甚至在旅行之外使用飞行模式来节省一点电池寿命，或者作为一种从互联网上彻底戒除毒瘾的方式。当您启用飞行模式时，它会禁用设备上的所有无线电，如蜂窝、WiFi、NFC 和蓝牙。然而，在飞机上通常允许使用蓝牙，有些甚至允许使用 WiFi。这里有一个教程，教你在打开飞行模式时，如何防止 WiFi、蓝牙或任何其他无线电被禁用。

* * *

## 如何防止飞行模式禁用某些无线电

1.  为你的设备制造商安装 USB 驱动程序(谷歌在这里提供了一些[通用 USB 驱动程序的列表)。](https://developer.android.com/studio/run/oem-usb.html)
2.  为你的操作系统下载 [ADB 二进制](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)([Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)、 [Mac](https://dl.google.com/android/repository/platform-tools-latest-darwin.zip) 、 [Linux](https://dl.google.com/android/repository/platform-tools-latest-linux.zip) )。这些链接将始终指向亚行的最新版本。
3.  将 ADB 二进制 ZIP 文件的内容解压缩到您电脑上的文件夹中。
4.  启动设备上的设置应用程序，然后点击关于电话选项。
5.  找到内部版本号并轻按 7 次，这样我们就可以启用开发人员模式。
6.  回到设置主菜单，进入开发者选项，然后打开 USB 调试。
7.  将手机插入电脑，从“仅充电”模式切换到“文件传输(MTP)”模式。在允许 ADB 工作之前，一些设备需要这一步骤作为安全措施。
8.  回到 PC，调出您解压 ADB 二进制文件的目录。
9.  在您的 ADB 目录中启动命令提示符或终端。对于 Windows 用户，这可以通过按住 Shift 并右键单击然后选择“在此打开命令提示符”选项来完成。(部分 Windows 10 用户可能会看到“PowerShell”而不是“命令提示符”。)
10.  一旦进入命令提示符或终端环境，执行以下命令:`adb devices`
11.  这将启动 ADB 守护进程(如果它还没有启动的话)。你甚至可以在手机上看到一个提示，要求你授权与电脑的连接。在这里允许 USB 调试访问。
12.  现在，如果您从步骤 10 重新运行 adb 设备命令，命令提示符/终端将打印您的设备的序列号。如果是这样，那么你已经准备好继续前进了。如果没有，那么 USB 驱动程序可能没有正确安装。
13.  在命令提示符或终端中执行以下命令:`adb shell`
14.  然后运行以下命令阻止飞行模式关闭 WiFi: ``settings put global airplane_mode_radios cell,bluetooth,nfc,wimax``
15.  或者，您可以执行此命令来阻止飞行模式关闭 WiFi 和蓝牙:`settings put global airplane_mode_radios cell,nfc,wimax`
16.  我们从列表中删除的每一项都告诉 Android 在打开飞行模式时让收音机开着。
17.  如果您想恢复原状，可以在 ADB shell 提示符下执行以下命令:`settings delete global airplane_mode_radios`

* * *

## 说明

正如你从上面的步骤中看到的，我们使用 ADB 命令来手动定制当我们点击飞行模式按钮时关闭的无线电。通常情况下，飞行模式会关闭蜂窝、WiFi、NFC、蓝牙和 WiMAX(如果存在)无线电，但使用步骤 14 中所示的 ADB 命令从列表中删除一个或多个无线电会使其被忽略。在我上面第 15 步给出的例子中，当我启用飞行模式时，我选择让 WiFi 和蓝牙都开着。

这就是该命令只包含蜂窝、NFC 和 WiMAX 选项的原因。由于我们在步骤#15(在这种情况下，WiFi 和蓝牙)的 ADB 命令中没有这两个无线电，当你打开飞行模式时，Android 将不会处理这些无线电。你可以通过省略这些选项来使用任何组合，甚至可以让蜂窝无线电在你打开飞行模式时保持开启。只是要确保你知道你在做什么，因为开着手机可能会给你带来航空公司的麻烦。

如上所述，你可以在打开飞行模式后重新打开一些无线电。我知道，在我关闭所有其他我不经常使用的设备的无线电后，我会经常打开 WiFi 和蓝牙。

因此，您可能想知道，当启用飞行模式时，还有一种方法可以阻止设备打开其中一个无线电。通过更改全局首选项“飞机模式可切换无线电”中的值来控制首选项。例如，如果您选择输入以下命令，您可以将其设置为无法重新打开 WiFi:

```
 settings put global airplane_mode_toggleable_radios bluetooth,nfc 
```

默认情况下，此命令的选项为 WiFi、蓝牙和 NFC。但是如果你在执行上面的命令时漏掉了其中一个，那么你就阻止了设备重新打开收音机。这对于儿童的智能手机或平板电脑来说是一个好主意，甚至可以用作自动防故障装置，以确保在飞行模式打开时收音机不会打开。这个特性可能没有上面的大指南中详细介绍的那个有用，但是这是你可能想要知道的。