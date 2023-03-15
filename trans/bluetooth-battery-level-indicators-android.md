# 蓝牙电池电量指示器终于要来安卓了

> 原文：<https://www.xda-developers.com/bluetooth-battery-level-indicators-android/>

对于我们这些使用蓝牙耳机和其他设备的人来说，一个真正有用的功能终于来到了 AOSP:蓝牙电池电量指示器。这意味着谷歌、摩托罗拉、索尼和其他安装了 Android 软件的设备的用户应该能够在不需要第三方应用程序的情况下判断他们蓝牙连接设备的电池电量。目前还不知道这个蓝牙电池电量指示器在最终状态下会是什么样子，但这个新 API 在 AOSP 的存在意味着开发者可以随心所欲地实现蓝牙电池指示器。

现在，对于那些使用某些定制 rom(如 LineageOS)或使用某些制造商的设备(如三星、LG、华为、一加或小米)的人来说，这不是一个新功能。多年来，许多定制 rom 和第三方 OEM 设备都支持连接蓝牙设备的电池电量指示器，但 Android 开源项目(AOSP)明显缺少这样的功能，这意味着任何谷歌手机的固件都不支持它。

 <picture>![Samsung Bluetooth Battery Level Indicator](img/1e9287aafe9543b27be92e07a652e231.png)</picture> 

Samsung Bluetooth Battery Level Indicator

 <picture>![OnePlus Bluetooth Battery Level Indicator](img/27d38d2aeb4129af3d8d1d9f94e6e203.png)</picture> 

OnePlus Bluetooth Battery Level Indicator

 <picture>![LG Bluetooth Battery Level Indicator](img/0495c9af2f6d1395aed3dd660ca3333a.png)</picture> 

LG Bluetooth Battery Level Indicator

拥有蓝牙设备的用户，如果足够幸运，在谷歌 Play 商店上有一个配套的应用程序，就可以通过这种方式获取电池电量信息，但除此之外，几乎没有其他选择。Play Store 上一个名为 [BatON](https://play.google.com/store/apps/details?id=com.limi.baton) 的流行应用程序试图添加这一功能，但它在支持的设备范围方面非常有限(这不是它自己的错)，而且众所周知它存在很多问题(许多用户报告说经常断开蓝牙连接)。

如果谷歌能够提供一个在其他设备上已经存在多年的功能，而不是依赖于第三方应用程序，这些应用程序要么只能在你拥有的一个蓝牙设备上工作，要么只能支持少数设备。最后，看起来他们正在这么做。

* * *

## AOSP 的蓝牙电池级 API

蓝牙特别兴趣小组(Bluetooth SIG)是监督每一次蓝牙迭代标准的机构，它已经在 [GATT](https://www.bluetooth.com/specifications/gatt) (通用属性服务)中定义了电池服务(BAS)，但这取决于蓝牙对 BAS 的支持。根据我们在 AOSP 挖掘时发现的一些新提交，谷歌正准备添加新的[API](https://android-review.googlesource.com/#/q/topic:bt-feature-remote-battery-level-api+(status:open+OR+status:merged))来“获取远程设备的电池电量”他们特别提到了 AOSP 的以下新增内容:

**添加 API 以获取远程设备的电池电量**

*   添加 bluetooth device . getbatterylelevel()API 来检索远程设备的电池电量信息
*   添加蓝牙设备。ACTION_BATTERY_LEVEL_CHANGED 旨在通知用户远程设备的电池电量已更改
*   为 bluetooth device . getbatterylelevel()添加后端服务方法
*   用 getters 和 setters 在 DeviceProperties 中添加电池电量字段
*   在 RemoteDevices 中添加 updateBatteryLevel()方法
*   在 RemoteDevices 中添加 resetBatteryLevel()方法
*   当设备在 aclStateChangeCallback()中断开连接时重置设备的电池电量，以确保设备在连接后首次报告电池电量信息时具有 BATTERY_LEVEL_CHANGED 意图
*   为 updateBatteryLevel()和 resetBatteryLevel()添加测试

由此，我们可以看到 Google 将在 [BluetoothDevice](https://developer.android.com/reference/android/bluetooth/BluetoothDevice.html) 类中添加一个名为 getBatteryLevel()的新方法，该方法将在被调用时检索连接设备的当前电池电量。根据源[代码](https://android.googlesource.com/platform/frameworks/base/+/1d312bfa78c25e0e1d6ea25b2c027e2efdd5a418/core/java/android/bluetooth/BluetoothDevice.java)，这将返回一个 0 到 100 之间的值(如果蓝牙被禁用，设备被断开，或者不支持报告其电池电量，则返回-1)。因此，这意味着电池电量有可能以一种比简单的条形图更具信息性的方式显示。例如，开发人员可以显示带有确切百分比的通知或小部件。

但这还不是全部，订阅 ACTION_BATTERY_LEVEL_CHANGED 广播意图的应用程序将在连接设备的电池电量发生变化时得到通知。使用广播接收器，当电池电量发生变化时，正在监听所连接的蓝牙设备的电池状态变化的应用程序将得到通知，因此无需实施任何类型的持续后台轮询服务。该值通过 intent extra EXTRA_BATTERY_LEVEL 以 0 到 100%之间的整数形式发送，应用程序可以通过 intent extra EXTRA_DEVICE 过滤来区分连接的设备。

甚至某些以自己的方式发送电池信息的设备也将得到支持，如 Plantronics 的 XEvent 或苹果的 T2 VSC T3。还有关于蓝牙低能耗(BLE)电池电量报告的工作正在进行中，[支持](https://android-review.googlesource.com/#/c/429579/)，尽管目前这被列为“不能合并”。

* * *

## Android 8.1 可能的功能？

Android O 就快到了。第四个开发者预览版最近发布，主要是针对 bug 修复，尽管这里那里有一些小的 UI 调整。然而，谷歌宣布[第三次开发者预览版](https://www.xda-developers.com/android-o-developer-preview-3-rolling-out-with-final-android-o-apis/)展示了所有最终确定的 Android O APIs，开发者可以使用这些 API 为下一版本的 Android 做准备。因此，这意味着新的连接蓝牙电池水平报告 API 不会进入 Android O - Android 8.0 的第一个版本。

然而，这并不意味着它不会到来。随着 Android 8.1 的最终发布，谷歌可能会正式引入这个 API(当它真正完成的时候)。与此同时，他们甚至可能决定通过 Android [支持库](https://developer.android.com/topic/libraries/support-library/index.html)来支持这一功能，将其带到早期的 Android 版本中。如果这种情况最终发生，那么用户将不必等待数月来享受这样的功能(尽管我们总是鼓励用户尝试我们的牛逼论坛上提供的许多定制 rom 中的一个)。

尽管如此，对于手机上的股票软件的粉丝来说，这应该是一个令人兴奋的消息。希望你不会嫉妒苹果、三星、华为、LG 和其他设备的用户拥有这个很久很久以前就应该在 Android 中提供的漂亮功能。鉴于最近 Reddit 上对这个想法的支持，我们确信这将是一个受欢迎的功能——当它最终上市 Android 时。