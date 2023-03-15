# 如何在 Android 上降级应用程序——不需要 Root 用户

> 原文：<https://www.xda-developers.com/downgrade-an-app-android-no-root/>

有时应用程序更新来了，你希望你停留在旧版本。有时候，这并不像卸载你当前的应用程序并再次安装旧的 APK 那么简单，因为也许你想保留应用程序中的数据，或者它是一个系统应用程序，而你不想完全卸载它。谢天谢地，由于 Android Debug Bridge (ADB)的功能，可以在不需要 root 和**保存所有数据**的情况下，降级应用版本**。**

一个主要的例子是 WhatsApp，使用底层主题通常需要一定的版本要求。而不是必须卸载 WhatsApp，经历重新登录账号的痛苦，你可以简单地用这个教程再次降级，只用 adb。Root 用户可能更喜欢在 Play Store 上使用类似于 [App 降级器](https://play.google.com/store/apps/details?id=com.alessandro193a.appdowngrader&hl=en)的东西。如果你想继续，首先获取[最小 ADB &快速启动](https://forum.xda-developers.com/showthread.php?t=2317790)或者包含 ADB 的[官方 Google 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)。

当你降级一个应用程序时要小心。应用程序可以升级数据库，降级可能会导致旧版本的应用程序无法读取这些文件。在极少数情况下，如果旧版本的应用程序试图修改数据库，数据库可能会完全崩溃。

* * *

## 如何降级 Android 上的应用程序

找到要降级到的应用程序版本的 APK。我建议在 XDA 实验室或 APKMirror 上寻找。打开包含 adb 工具的文件夹，打开命令提示符并导航到包含 adb 的文件夹。将您希望降级到的 apk 文件复制到与 adb 文件相同的文件夹中。

通过输入开发者选项，在您的设备上启用 USB 调试。如果你没有看到开发者选项，那么进入“设置”中的“关于手机”,点击“内部版本号”7 次，直到出现一个祝酒词。接下来，按 back 按钮，你应该会看到一个开发者选项部分。检查 USB 调试在这里，然后连接您的手机到您的电脑。

准备好降级应用程序时，在命令窗口中运行以下命令。

```
 adb push app.apk /sdcard/app.apk 
adb shell pm install -r -d /sdcard/app.apk 
```

其中“app.apk”是您已经下载并想要降级到的 apk 文件。如果这是你第一次在手机上运行 adb，允许你的手机在屏幕上的提示下被调试。然后，应用程序应该降级，您的数据保持不变。

* * *

## 说明

亚洲开发银行对你的设备有很多控制，你通常无法访问。我们首先将文件推送到我们的内部存储器。然后我们使用“pm”来调用你的设备上的包管理器，“install”当然会安装应用程序。标志“-r”和“-d”分别表示“保留数据”和“降级”。这可以确保您的手机在降级时不会清除属于该应用程序的文件夹。