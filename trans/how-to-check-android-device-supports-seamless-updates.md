# 如何检查你的 Android 设备是否支持无缝更新

> 原文：<https://www.xda-developers.com/how-to-check-android-device-supports-seamless-updates/>

Android Nougat 引入了对 A/B 分区系统无缝更新的支持。支持新分区系统的设备有两组分区，a_slot 和 b_slot。使用术语“无缝更新”是因为所有更新现在都下载到非活动插槽。当用户重启以完成安装时，设备会无缝切换到非活动插槽，从而消除停机时间。用户数据在分区之间共享。

A/B 分区有其优点和缺点。这里的第一个优点是，如果没有正确安装更新，设备可以简单地切换到另一个插槽(例如，如果更新是在后台安装到 b_slot，则设备将切换回 a_slot ),从而避免启动错误。第二个好处是，用户不再看到“Android 正在升级...”屏幕。更新安装完成后，设备会正常重启。

另一方面，A/B 分区系统有明显的缺点。它增加了设备的已用存储空间，因为现在有两组分区。在具有大量内部存储的设备上，存储增加可能不是主要的，但是它确实存在。这里更主要的问题是，A/B 分区已被证明是几款设备开发的障碍，包括第一代谷歌像素、 [Moto Z2 Force](https://www.xda-developers.com/moto-z2-force-ab-seamless-updates/) 和[小米 Mi A1](https://www.xda-developers.com/xiaomi-mi-a1-android-ab-partition/) 。

截至目前，很少有 Android 设备制造商选择使用 A/B 分区系统。除了谷歌的第一代和第二代像素，使用分区系统的设备包括 Moto Z2 Force、Essential Phone 和小米 Mi A1。

* * *

## 如何检查设备是否支持 A/B 无缝更新

### 终端方法

用户可以通过在 [ADB shell](https://www.xda-developers.com/install-adb-windows-macos-linux/) 或终端模拟器应用程序中运行以下命令，轻松检查他们的 Android 设备是否支持无缝更新。

```
 getprop ro.build.ab_update 
```

如果设备支持双分区，这将返回 true。

### App 方法

或者，您也可以使用谷歌 Play 商店上的高音检查应用程序。除了通知用户[是否支持 Project Treble](https://www.xda-developers.com/project-treble-android-oreo/)之外，该应用还会通知用户他们的设备是使用 A-only 系统分区还是 A/B 分区系统进行无缝更新。