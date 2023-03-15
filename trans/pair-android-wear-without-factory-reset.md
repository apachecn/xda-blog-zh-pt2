# 将 Android Wear 手表与新手机配对，无需工厂重置

> 原文：<https://www.xda-developers.com/pair-android-wear-without-factory-reset/>

Android Wear 作为一款智能手表操作系统并不是没有缺点，但遗憾的是，尽管越来越多的技术爱好者可能会使用它，但这些人也可能会在手机上安装定制的 rom。在大多数情况下，这意味着每当你在设备上切换到另一种版本的 Android 时，都必须清除你的智能手表。然而，当你买了一部新的智能手机或在你的设备上闪存一个新的定制 rom 时，有一个简单的方法可以绕过从头开始设置你的智能手表。这种方法**不需要手机或手表上的 root** ，但它需要一些 Android 调试桥(ADB)命令。这已经在 Android Wear 1.5 和 Android Wear 2.0 上的华为手表上进行了测试，不过它也应该可以将 Android Wear 手表与任何新的智能手机配对。如果由于某种原因，你的手表已经根了，你可以忽略这个教程，只需使用[重置穿戴客户端](https://forum.xda-developers.com/android-wear/development/app-reset-wear-client-switch-phones-t3058962)来配对 Android Wear，而无需直接从你的智能手表进行工厂重置。

* * *

## 无需擦拭即可将 Android Wear 与新手机/同一部手机配对

首先，您需要下载亚行工具。我个人使用的是在 XDA 找到的“ [Minimal ADB 和 Fastboot Kit](https://forum.xda-developers.com/showthread.php?t=2317790) ”，但是如果你愿意，也欢迎你使用来自谷歌的[官方二进制文件。接下来，你需要在智能手表上启用 ADB 调试(有线或 WiFi 调试都可以，不过我觉得 WiFi 更方便)。这是通过智能手表上的开发者选项实现的，您也需要启用它。要做到这一点，只需在你的手表上进入设置→系统→关于，然后点击标有“内部版本号”的字段，直到你看到一条提示信息，说明“你现在是一名开发人员”。](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)

一旦你完成了这些步骤，你就可以开始了！

### 启用 ADB 调试

打开开发者选项并启用“ADB 调试”或“通过 wifi 调试”,如果你想无线调试的话。将 Android Wear 同步到智能手机的过程两种方式都可以正常工作，但它们需要的命令略有不同。

同步 Android Wear 的初始设置将需要不同的命令，无论您是否通过 WiFi 进行同步。请打开 adb 工具，要么在 Windows 搜索栏中搜索 adb，要么导航到包含 adb 的文件夹，按住 shift，然后右键单击并选择“在此打开命令窗口”。然后输入以下命令。

### 通过 WiFi

在我的例子中，我会键入:

```
 adb connect 192.168.1.100:5555 
```

来连接我的 Android Wear 手表。你需要输入的 IP 地址位于“通过 WiFi 调试”下，如上图截图所示。接受手表上的提示，允许电脑调试。如果成功，它将简单地返回到命令提示符，在那里您可以键入。现在有文本输出。

### 有线的

命令简单得多，只需将设备连接到计算机，然后键入:

```
 adb devices 
```

如果您的设备出现，您就没事了。确保您接受了手表上的提示，允许它进行调试。

### 发送命令

要继续，首先**禁用手机上的蓝牙**，然后在电脑上键入:

```
 adb shell “pm clear com.google.android.gms && reboot” 
```

你的手表会重新启动，但不会发生 Android Wear 工厂重置。当它重新启动时，它应该不会再显示一个划叉的云形图标，表示它无法连接到你的手机。你现在想在手机上安装 Android Wear 应用程序(如果你还没有的话)，**但是不要启用蓝牙**。

接下来，按照与之前完全相同的步骤，通过 ADB 再次连接到智能手表。但是，这一次您想要运行的命令是:

```
 adb shell “am start -a android.bluetooth.adapter.action.REQUEST_DISCOVERABLE” 
```

然后在你的手表上允许它被其他设备发现，这样你就可以将 Android Wear 与智能手机同步。现在，您可以通过打开 Wear 应用程序、启用蓝牙和搜索设备，从智能手机连接到 Android Wear。您的 Android 手表应该会显示出来，您的手机将与它同步。如果应用程序在“检查更新”时挂起，只需重新启动应用程序，它应该会开始连接到 Android Wear。

* * *

## 说明

关于这一点的简单解释是，所有智能手机和智能手表的配对数据都包含在 Google Play 服务中。该数据是特定于手机的，因为密钥存储在智能手表上的 Play Services 数据中。这就是为什么你不能简单地从智能手机上备份 Android Wear 应用程序的原因，因为你需要的密钥存储在智能手表上。当你试图配对一部新手机时(或者已经安装了一个新的定制 ROM，手表认为这是一部新手机)，通常会通过 Android Wear 工厂重置来擦除按键。

解决这个问题的唯一方法是删除关键数据，这样你就可以将 Android Wear 与新设备配对，而无需进行工厂重置，因为将它与手机配对的关键数据也会被清除。然后，我们请求通过 adb 发送的意向使智能手表的蓝牙可被发现，这将创建您需要接受的提示。这意味着您的手机现在可以找到您的手表，然后与设备创建新的配对密钥。