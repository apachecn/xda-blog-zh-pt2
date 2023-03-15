# 如何查看您的安卓牛轧糖或安卓奥利奥设备的启动次数

> 原文：<https://www.xda-developers.com/boot-count-android-nougat-oreo-device/>

我们热爱统计。即使是平凡的或者基本上无用的统计数据也会引起人们极大的兴趣。与 adb，或根和一个终端应用程序，有可能查看你的手机启动计数，这是多少次你已经启动了你的设备！显然，这个计数器只有在你的手机最后一次恢复出厂设置后才会被记录。该数据存储在设置数据库中，因此在工厂重置中擦除数据意味着该启动计数器丢失。如果遵循下面的根方法，您将需要 Magisk 或 SuperSU。读取的值[“BOOT _ COUNT”](https://developer.android.com/reference/android/provider/Settings.Global.html#BOOT_COUNT)仅在 SDK24 或 Android Nougat 中添加，因此 Android Nougat 或 Android Oreo 上的任何设备都将具有该计数器。**安卓棉花糖或更低版本不能使用本教程，因为字符串不存在。**

不过，你也没错过什么。

* * *

## 在任何 Android 7.0 以上设备上查看您的启动计数(无 Root)

首先，按照本教程在你的设备上设置 adb。它拥有您在 Windows、Mac 或 Linux 上启动和运行所需的一切！一旦您完成了所有的设置，您将需要通过 adb 运行以下两个命令。您可以检查您的设备是否也与“adb 设备”连接。右图向您展示了它应该是什么样子。

```
 adb shell 
```

```
 settings get global boot_count 
```

这应该会给你一个整数值，也就是你的设备已经启动了多少次。

## 查看您在任何 Android 7.0 以上设备上的启动次数(Root)

您需要 root 用户，因此在 [Termux](https://play.google.com/store/apps/details?id=com.termux) (或任何终端应用程序)中键入以下命令。右图向您展示了它应该是什么样子。

```
 su 
```

接受授予超级用户访问权限的提示。

```
 settings get global boot_count 
```

仅此而已！

* * *

用安卓牛轧糖，增加了字符串“BOOT_COUNT”。这是一个记录设备启动次数的字符串。如上所述，如果您恢复出厂设置，该字符串将被清除。如果您关心这个次要的引导统计，我建议不要擦除/data 分区。但你可能真的不在乎。也许吧。

你的靴子数是多少？下面就让我们知道吧！