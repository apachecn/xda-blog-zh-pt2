# Android P 增加了将手机用作蓝牙键盘或鼠标的支持

> 原文：<https://www.xda-developers.com/android-p-bluetooth-keyboard-mouse/>

据传闻称，我们已经接近第一个 Android P 开发者预览版的发布日期[。就面向用户的功能而言，对即将发布的版本知之甚少，尽管我们已经尽最大努力](https://twitter.com/MishaalRahman/status/969822517002211328)[将我们能够找到的所有零碎信息](https://www.xda-developers.com/tag/android-p/)进行了分类。传闻中 Android P 的两个最大变化包括支持[非典型显示器类型](https://www.xda-developers.com/android-p-atypical-display-types-material-design-2/)(例如带有“[凹口](https://www.xda-developers.com/android-display-notch-discussion/)”)和改进的[材料设计界面](https://www.xda-developers.com/chromium-gerrit-material-design-2-colors/)。今天，我们也相信 Android P 将最终添加对蓝牙 HID 设备配置文件服务的支持，这将允许您的智能手机被用作蓝牙键盘或鼠标。

早在 2014 年，高通 CodeAurora 论坛的一名成员提交了一个补丁，添加了对蓝牙 HID 设备角色的支持。该补丁于 2016 年 12 月提交，但该功能在后续 Android 版本中仍处于禁用状态。随着 Android P 的发布，这种情况似乎正在改变，因为我们收到了 XDA 成员 [500 内部服务器错误](https://forum.xda-developers.com/member.php?u=5924703)的提示，即[两次提交](https://android-review.googlesource.com/#/q/topic:hid-device-support+(status:open+OR+status:merged))最终启用了蓝牙 HIDD。

我们自己证实了这个蓝牙 HID 配置文件是最近才添加的，因为在 Android 8.1 Oreo(分支 [oreo-mr1-release](https://android.googlesource.com/platform/packages/apps/Bluetooth/+/oreo-mr1-release/res/values/config.xml) )与[最新主](https://android.googlesource.com/platform/packages/apps/Bluetooth/+/master/res/values/config.xml)中支持的蓝牙配置文件的比较显示，启用 HIDD 的布尔值已被翻转为真。

此外，供开发人员使用的[相关](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/bluetooth/BluetoothHidDevice.java)[API](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/bluetooth/BluetoothHidDeviceCallback.java)已经[取消隐藏](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/)，这意味着应用程序将能够在运行 P 版本的 Android 设备上利用这一功能(从谷歌 Pixel 和 Pixel 2 设备开始)。

那么这一切到底意味着什么呢？

## Android P 蓝牙 HID 设备配置文件服务

支持蓝牙的设备可以支持所谓的“蓝牙模式”您可能熟悉一些更常见的模式，如免提模式(HFP)和高级音频分配模式(A2DP)，它们通常分别用于语音通话和音乐流。实现人机接口设备(HID)蓝牙配置文件允许诸如鼠标、键盘、操纵杆等输入设备工作。

默认情况下，Android(Android 开源项目的基础版本)不支持蓝牙协议栈中的 HIDD。这意味着应用程序开发人员不能利用该服务来创建应用程序，以使您的智能手机能够被用作基本的键盘/鼠标输入设备。Play Store 上有支持 root 的应用程序，如 Bluetooth+,它为蓝牙框架打了补丁，以支持 HIDD，当与另一个应用程序如 True Mouse/KB 结合时，你可以将智能手机用作输入设备。

然而，AOSP 的原生支持意味着所有运行 Android P 的设备都可以通过蓝牙作为输入设备使用。我们可以看到这可能有助于潜在控制工作场所的演示，或者在您没有更好的解决方案时作为媒体遥控器。三星(Samsung)和华为(Huawei)等公司一直在兜售将你的智能手机用作移动工作站的方法，尽管这一功能与这两家公司提供的生态系统相比相形见绌，但这是你的 Android 设备和其他设备之间互联互通的一个很好的进步。