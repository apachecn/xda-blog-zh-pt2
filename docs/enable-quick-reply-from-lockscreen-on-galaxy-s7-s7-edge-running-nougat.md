# 如何在运行牛轧糖的三星 Galaxy 设备上启用锁屏快速回复

> 原文：<https://www.xda-developers.com/enable-quick-reply-from-lockscreen-on-galaxy-s7-s7-edge-running-nougat/>

Android 牛轧糖对传统 Android 体验的粉丝来说是一个巨大的更新。除了官方的多窗口支持和一系列其他变化，更新还带来了一个新的快速回复功能，允许你在不打开有问题的应用程序的情况下从通知阴影中回复消息。

在第五版 Android N 开发者预览版之前，用户甚至可以在安全锁屏后快速回复通知。然而，谷歌从 Android N 的后续版本中删除了该功能，但 Android 的 UX 总监承诺团队会尽快恢复该功能。嗯，我们现在有了我们的[第一个 Android O 开发者预览版](https://www.xda-developers.com/google-announces-android-o-developer-preview-1-available-for-supported-devices/)，但是这个功能仍然遥遥无期。

不过幸运的是，如果你有一台运行 Android 7.0 牛轧糖官方版本的三星 Galaxy 设备(如三星 Galaxy S7 和 Galaxy S7 Edge)，那么你可以手动启用该功能。默认情况下，该功能在三星体验软件中是隐藏的，但是我们可以使用简单的 ADB 命令来启用它。

注意:我已经在运行官方 Android 7.0 牛轧糖的美国电话电报公司三星 Galaxy S7 上测试了这一点，但我没有任何理由相信这不应该在所有运行基于 Android 7.0 的三星体验软件的设备上工作。此外，这个技巧可能也适用于其他制造商的设备，但是我无法在我的华为 Mate 9 或 OnePlus 3T 上使用它。

* * *

## 启用锁屏快速回复

正如我们之前提到的，我们将向我们的设备发出 ADB 命令，以便能够从锁屏中快速回复。如果您尚未启用 ADB 访问，请遵循以下步骤。如果有，请跳到下一部分。

### 建立亚洲开发银行

首先，[直接从 Google](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/) 为您的特定操作系统下载 ADB 二进制文件，并将其解压缩到您计算机上的一个单独目录中。接下来，[为你的手机安装合适的驱动](https://developer.android.com/studio/run/oem-usb.html)。然后，在设置- >开发者选项中启用“USB 调试”。如果你看不到开发者选项，那么你需要进入设置- >关于手机，然后点击 7 次内部版本号来启用它。最后，通过在与 ADB 二进制文件相同的目录中启动命令提示符(右键单击->“open command prompt here”)并运行以下命令，确保 ADB 正在工作:

```
 adb devices 
```

如果你看到你的设备的序列号(它没有说未经授权)，你是黄金。如果你在手机上看到一个弹出窗口，要求你授予你的计算机 ADB 访问权限，那么就说是。如果你看不到这两种情况，那么试着重启你的电脑/手机，并重新连接到你的电脑上。否则，请尝试重新安装驱动程序。

### 发送 ADB 命令

确认 ADB 访问正常后，打开命令提示符并输入以下命令:

```
 adb shell settings put secure lock_screen_allow_remote_input 1 
```

这个设置更改应该立即生效，不需要重启，至少对我来说是这样。如果应用程序支持的话，你现在应该可以在锁屏状态下回复通知了。Telegram 和 Hangouts 等应用程序支持通知快速回复，以及大多数现代短信客户端，所以试试吧！

让我们知道这一招是否适用于您的三星 Galaxy 设备！如果它能在你的非三星设备上运行，也请告诉我们！