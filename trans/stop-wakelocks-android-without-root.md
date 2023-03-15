# 如何在没有 Root 用户的情况下停止任何 Android 应用程序的唤醒锁

> 原文：<https://www.xda-developers.com/stop-wakelocks-android-without-root/>

你有没有在晚上带着充满电的手机睡觉，醒来时却发现电池电量很低？别担心，我们每个人都遇到过。即使有了[瞌睡模式](https://www.xda-developers.com/xda-external-link/doze-mode-an-in-depth-look/)和所有[谷歌努力提高安卓系统的电池寿命](https://www.xda-developers.com/how-android-n-will-improve-battery-and-memory-management/)，空闲电池寿命并不完全理想。尤其是当你安装了很多应用的时候。罪魁祸首很可能是脸书、Messenger、Snapchat 等应用程序的不当唤醒锁。幸运的是，您可以使用简单的 shell 命令轻松停止这些唤醒锁。你甚至不需要根！今天，我们将向你展示如何在不使用 root 的情况下**阻止任何安卓应用**的唤醒锁。这在每一部安卓手机上都可以做到，只要你拿到了 ADB。

* * *

## 停止任何 Android 应用程序的唤醒锁

*我们 YouTube 频道的视频教程，以防你喜欢视觉辅助工具*

在开始任何操作之前，你需要在你的手机和电脑上设置 ADB。如果你还没有做，请参考[本教程](https://www.xda-developers.com/install-adb-windows-macos-linux/)以便设置自己。

除非你完全确定是什么耗尽了你的电池，我们将使用一个叫做“更好的电池统计”的小工具来找到罪魁祸首。开发者活跃在我们的论坛上，所以你可以在这里找到应用程序。然而，如果你想支持开发者，你也可以从谷歌 Play 商店下载，这是一个付费应用。它提供了许多其他统计数据，如 CPU 状态、应用程序唤醒和网络信息。

它需要在安装了 Android KitKat 和更高版本的设备上安装 root，但是，有一个针对非 root 设备的 ADB 命令变通方法。通过 USB 调试或 WiFi 调试将设备连接到计算机。使用以下命令确保它已连接:

```
 adb devices 
```

然后，我们将使用以下命令启动 Android shell:

```
 adb shell 
```

之后，我们将授予刚刚安装的 BetterBatteryStats BATTERY _ STATS 权限:

```
 pm grant com.asksven.betterbatterystats_xdaedition android.permission.BATTERY_STATS 
```

搞定了。现在 BBS 可以在你的非根设备上运行了。

注意:如果您从谷歌 Play 商店购买了更好的电池状态，那么在上面的 ADB 命令中将“com.asksven.betterbatterystats _ xd edition”更改为“com . ask sven . betterbatterystats”。

### 找到罪犯

你的手机上有很多应用程序，所以没有简单的方法来确定是什么在消耗你的电池。这就是为什么我们使用更好的电池状态来找到负责任的唤醒锁。设置好应用程序后，给你的手机充电，然后拔掉插头，让它离开屏幕至少 30 分钟。这应该给应用程序足够的时间来注册一切。一旦进入应用程序，选择部分唤醒锁，看看哪个应用程序造成的损害最大。

### 停止唤醒锁

现在我们知道是什么在消耗你的电池，我们可以停止它。在我们的例子中，它是 Snapchat。无论你的罪魁祸首是什么，一定要使用 Package Name Viewer 从 Play Store 找到应用程序的包名，因为我们下面的 ADB 命令需要它。

因为你显然断开你的手机使用更好的电池状态，插回你的电脑再次使用 ADB。再次检查它是否与正确连接

```
 adb devices 
```

并使用以下命令进入 shell:

```
 adb shell 
```

现在，使用您的目标应用程序的包名，发送以下命令:

```
 cmd appops set com.android.application WAKE_LOCK ignore 
```

当然，您将使用应用程序的包名来切换“com.android.application”。就我而言:

```
 cmd appops set com.snapchat.android WAKE_LOCK ignore 
```

如果你已经正确地完成了所有的步骤，Android 系统将会忽略应用程序的所有唤醒请求。恭喜你！

* * *

## 说明

一个 wakelock，通俗地说，就是一个 app 为了执行一个特定的后台任务，在手机空闲的时候，让 CPU/屏幕/其他东西保持清醒的一种方式。一些应用程序确实需要唤醒锁才能正常工作，但当一些应用程序重复持有唤醒锁，长时间持有而不丢弃它们，或者利用这些唤醒锁执行过多/不必要的网络和 CPU 任务时，问题就来了。

例证:Snapchat、脸书、Messenger 或其他社交媒体应用程序都包含行为不端的唤醒锁。本教程只是一个简单的方法来阻止这些唤醒锁再次发生，而无需卸载应用程序。但是，如果您注意到在使用此 ADB 命令后应用程序停止正常运行，您可以通过重新运行该命令并将“忽略”更改为“允许”，或者通过简单地卸载然后再次重新安装应用程序，将事情恢复到原来的样子。