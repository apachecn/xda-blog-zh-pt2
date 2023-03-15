# Android O 引入了对设备标识符的改变和改进

> 原文：<https://www.xda-developers.com/android-o-introduces-changes-and-improvements-to-device-identifiers/>

Android O 是 Android 的最新版本，仅提供开发者预览版，[带来了大量的变化](https://www.xda-developers.com/tag/android-o/)。开发者预览版旨在让应用和游戏开发者有机会体验新平台，并根据变化调整他们的软件产品，以便利用这些改进。

在一篇博客文章中，谷歌详细介绍了 Android O 带来的一些改进，让用户可以控制标识符的使用。

在 O 中，Android ID(设置。Secure.ANDROID_ID 或 SSAID)对于设备上的每个应用和每个用户都有不同的值。只要软件包名称和签名密钥保持不变，ANDROID_ID 值在软件包卸载/重新安装时也不会改变。只有当设备恢复出厂设置或签名密钥改变时，它才会改变。更新到 Android O 的早期 Android 版本将保留相同的 Android ID，除非卸载并重新安装该应用程序。

需要设备范围标识符的开发者被建议使用可重置的标识符，例如[广告 ID](https://developers.google.com/android/reference/com/google/android/gms/ads/identifier/AdvertisingIdClient) ，这给了用户更多的控制，因为它提供了一个面向用户的设置来限制广告跟踪*。*

Android O 还引入了一个新的 API build . get serial()，它取代了现在已经过时的 android.os.Build.SERIAL，以便与访问 IMEI 所需的运行时权限保持一致。除了建造。串行，其他系统属性在 Android O 中也变得不可用，比如:

*   **ro.runtime.firstboot** :毫秒——上次擦除或最近一次引导后第一次引导的精确时间戳
*   **htc . Camera . sensor . front _ SN**:相机序列号(部分 HTC 设备上有)
*   **persist . service . b droid . BD addr**:蓝牙 MAC 地址属性
*   **设置。Secure.bluetooth_address** :设备蓝牙 MAC 地址。在 O 中，这仅适用于拥有 LOCAL_MAC_ADDRESS 权限的应用程序。

Android O 还包含一个强大的 MAC 地址随机化系统，用于随机化 Wi-Fi 扫描流量。这些变化是针对谷歌 Pixel 和 Nexus 5X 上的芯片组固件进行的，Android O 将这些固件变化集成到 Android Wi-Fi 堆栈中，以便使用相同芯片组和运行 Android O 的其他设备也可以利用这些变化。一些变化简述如下:

*   在与接入点断开连接时，对于每次 Wi-Fi 扫描，手机都会使用一个新的随机 MAC 地址(无论设备是否处于待机状态)。
*   每次扫描的初始数据包序列号也是随机的。
*   删除了不必要的探测请求信息元素:信息元素限于 SSID 和 DS 参数集。

* * *

这些新变化旨在限制设备范围内不可重置标识符的使用。这些变化还提供了更多面向用户的控制，并改变了应用程序请求帐户信息的方式。你可以在[博客文章](https://android-developers.googleblog.com/2017/04/changes-to-device-identifiers-in.html)中看到所有的变化。