# 快速配对正在获取位置跟踪、电池通知和新设置

> 原文：<https://www.xda-developers.com/fast-pair-location-tracking-battery-notifications-new-settings/>

回到 2017 年，谷歌[宣布了 Fast Pair](https://www.xda-developers.com/fast-pair-quick-bluetooth-pairing-headphones/) ，这是一项旨在改善蓝牙配件首次配对体验的功能。第一个支持快速配对的蓝牙配件是与谷歌 Pixel 2 和 Pixel 2 XL 一起推出的第一代谷歌 Pixel Buds。从那以后，来自许多不同制造商的许多其他蓝牙配件增加了对 Fast Pair 的支持。支持 Fast Pair 的最新设备是今天早些时候宣布的第二代真正无线[谷歌 Pixel Buds](https://www.xda-developers.com/google-pixel-buds-2-available-now/) 。除了这个产品发布，谷歌还宣布了一些新的快速配对功能来选择蓝牙配件。

在去年的谷歌 I/O 2019 上，[谷歌悄悄宣布【Fast Pair 将获得一些有用的新功能。他们提到的第一个功能“查找我的配件”，将让用户在“](https://www.xda-developers.com/android-q-bluetooth-revamp-fast-pair-find-my-accessories/)[查找我的设备](https://play.google.com/store/apps/details?id=com.google.android.apps.adm)”应用程序中 ping 其蓝牙配件的最后已知位置。接下来，谷歌表示，用户无论何时打开或关闭充电盒，都会在手机上收到通知，显示配对配件的电池电量。最后，谷歌展示了一个经过改进的蓝牙设置页面，用户可以控制快速配对设备上支持的所有设置，这样用户就不必仅为该配件打开一个专用应用程序。

自从去年 I/O 开发者大会上的早期声明以来，我们不知道这些新功能何时会推出，尽管过去几个月里我们已经在 APK 的拆卸活动中瞥见了它们的身影。然而今天，[谷歌终于宣布](https://www.blog.google/products/android/fast-pair-easier-bluetooth/)推出这些功能中的大部分。

**找到我的配件**

如果您的蓝牙耳机或头戴式耳机已连接到手机，但您不知道它们在哪里，现在您可以通过在“设置”中响铃来定位它们。对于真正的无线耳塞，您可以独立响铃左右耳塞。在未来几个月的更新中，您将能够通过“查找我的设备”应用程序找到丢失的附件，即使它们没有连接到您的手机。不过，你需要启用位置历史。

**电池通知**

接下来，谷歌宣布，当你打开真正无线耳塞的外壳时，你会收到关于每个组件(右耳塞、左耳塞和外壳，如果支持的话)电池电量的电话通知。当耳塞和外壳电池电量低时，您也会收到通知。

**修改后的设备详情页面**

如果您有运行 Android 10+的设备和支持快速配对的蓝牙配件，您将能够从蓝牙设备详细信息页面调整配件的所有设置。目前，只有[哈曼卡顿飞](https://www.harmankardon.com/true-wireless-headphones/FLYTWS-.html)和新[谷歌像素芽](https://store.google.com/us/product/pixel_buds)支持在设备详情页面显示这些附加设置。鼓励蓝牙配件制造商通过使用[切片 API](https://developer.android.com/guide/slices) 来集成他们专用应用程序的选项，在设备详情页面中显示这些设置。

最后，谷歌宣布，在通过蓝牙与手机配对后，你的配件名称将包括你的名字。重命名蓝牙设备已经是可能的，但是这自动化了一个许多用户从不费心去做的步骤。

* * *

除了“查找我的设备”集成之外，这些功能现已面向受支持的快速配对蓝牙配件推出。Fast Pair 是 Google Play 服务的一部分，Android 版本支持。