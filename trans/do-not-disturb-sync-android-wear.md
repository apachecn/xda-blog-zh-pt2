# 在 Android Wear 2.0 和你的手机之间同步免打扰模式

> 原文：<https://www.xda-developers.com/do-not-disturb-sync-android-wear/>

Android Wear 2.0 是一个期待已久的更新，Moto 360 Sport 等手表现在才获得它，而华为 Watch 的更新是在 5 月[发布的](https://www.xda-developers.com/android-wear-2-0-arrives-for-the-original-huawei-watch/)。Wear 2.0 的更新带来了许多改进，包括设备现在可以直接在你的手表上安装应用程序和一个键盘来回复信息。这一更新的一个缺点是，请勿打扰模式不再在智能手表和手机之间同步。在本教程中，我们将向您展示如何在您的两台设备之间同步勿扰模式。早在五月份，我们就给了这个应用程序一个[喊出](https://www.xda-developers.com/do-not-disturb-sync-for-wear-2-0-regain-lost-functionality/)，今天我们将向您展示如何设置它！

* * *

## Android Wear 2.0 免打扰同步

我们将在手机和手表上设置这个应用程序。您需要[在您的手表](https://www.xda-developers.com/install-adb-windows-macos-linux/)上设置 adb。Android Wear 的步骤基本相同，但流程截图如下所示。

你实际上没有**可以通过 Wi-Fi 调试**，但是我发现这非常方便。完成后，使用以下命令将手表连接到电脑。

```
 adb connect 192.168.1.100:5555 
```

您连接的 IP 取决于您的设备在“通过 Wi-Fi 调试”下显示的地址。一旦你的电脑连接上，就会出现一个提示，允许你的手表被调试。一旦连接完毕，就可以开始了。如果您不使用 Wi-Fi，不需要任何初始设置命令。

### 设置电话

要设置手机，请先从谷歌 Play 商店下载下面的“佩戴免打扰同步”应用程序。

现在您已经安装了它，打开应用程序，并在应用程序中启用“请勿打扰”权限。你现在完成了电话方面的事情。

### 设置手表

一旦你在手机上安装了“佩戴免打扰同步”，你的 Android Wear 手表应该会通知你建议在手表上安装该应用程序。轻按通知并安装它。如果您没有收到通知，请打开谷歌 Play 商店并向下滚动到“手机上的应用程序”。如果还是看不到，那就自己去搜吧。你只需在谷歌 Play 商店上搜索包名“rkr.weardndsync”就能找到你手表上的应用。

安装完成后，打开连接的 adb 并运行以下命令。

```
 adb shell settings put secure enabled_notification_listeners com.google.android.wearable.app/com.google.android.clockwork.stream.NotificationCollectorService:rkr.weardndsync/rkr.weardndsync.HackService 
```

然后你就完事了！将手机上的“请勿打扰”改为手表上的“请勿打扰”。这可能会对那些为 Android Wear 2.0 的勿扰功能而烦恼的人有用。

* * *

## 说明

安装的应用程序只是为了将“请勿打扰”的当前状态传达给手表。我们通过 adb 为手表运行的命令与上面的切换功能完全相同，只是在 Android Wear 上没有用于启用通知监听器的 GUI(这是管理勿扰模式所必需的)。这就是为什么我们需要亚洲开发银行的手表，而不是手机。如果我们在电话上启用了通知监听程序，但没有在手表上启用，禁用手表上的勿扰模式将会在电话上禁用它，但反之亦然。