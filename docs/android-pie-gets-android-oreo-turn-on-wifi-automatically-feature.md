# Android Oreo 的“自动打开 WiFi”功能适用于 Android Pie 中的所有用户

> 原文：<https://www.xda-developers.com/android-pie-gets-android-oreo-turn-on-wifi-automatically-feature/>

# Android Oreo 的“自动打开 WiFi”功能适用于 Android Pie 中的所有用户

Android Oreo 增加了一个“自动打开 WiFi”功能，当你靠近一个高质量的保存网络时。Android Pie 中的所有人都可以使用该功能。

谷歌 Nexus 5X 和 Nexus 6P 用户会记得当获得官方 Android 8.0 Oreo 更新，而没有获得夜灯和自动 Wi-Fi 唤醒等功能时的失望。谷歌 Pixel 和 Pixel XL 的 Android Oreo 更新引入了后一个功能。它所做的是自动打开 Wi-Fi 连接到高质量的存储网络。该功能并不适用于所有 Android Oreo 设备，因为原始设备制造商必须选择启用它，但它将适用于所有运行 Android Pie 的设备！

**2018 年 8 月 9 日**更新:标题已更新，以阐明该功能现在对所有人都可用，而不必默认为所有人启用。它仍然是可选的，可以由用户启用或禁用！

## 所有 Android Pie 设备的 Wi-Fi 自动唤醒

随着 Android Pie 的[发布和](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/) [AOSP](https://www.xda-developers.com/android-pie-source-code-aosp/) 的代码下降，我们发现了两个变化，为所有使用或升级到 Android 9 Pie 的设备启用了该功能。第一次提交只是通过将 AOSP 框架中`config_wifi_wakeup_available`的值从 0(假)更改为 1(真)来在所有设备上启用它。后续提交会完全删除此标志，因为它现在在 Android Pie 中默认启用。

如果您将 android-8.1.0_r43 标签的 Android frameworks/base 分支中的 config.xml 与 android-9.0.0_r3 标签中的 config . XML 进行比较，您会看到“自动打开 Wi-Fi”标志不再存在。即使是基于 Android Pie 的定制 rom 也将启用该功能，而无需进行任何更改。

为了快速复习一下这项功能在 Android Oreo 中是如何工作的，它利用定位服务中的“Wi-Fi 扫描”功能来检测后台的 Wi-Fi 网络。它会根据谷歌的推荐服务检查这些 Wi-Fi 网络，如果推荐服务确定 Wi-Fi 网络是可信的(保存的网络)和高质量的(基于连接质量、网络速度等)。)，那么你的 Android 设备就会完全打开 Wi-Fi，自动连接网络。如果你住在一个有大量 Wi-Fi 接入点的地区，这实际上最终会节省电池，因为另一种选择是让 Wi-Fi 开着，这会导致你的手机不断连接和断开低质量的开放 Wi-Fi 网络。我们不确定这项功能在 Android Pie 中是如何工作的，因为它不再使用网络推荐服务。

如果你的设备在 Android Oreo 中有这个功能，你会在设置->网络&互联网- > Wi-Fi - > Wi-Fi 偏好设置->自动打开 Wi-Fi 中找到它。要使用此功能，您还需要在“设置”->“位置”->“扫描”中启用“Wi-Fi 扫描”。如果你的设备没有这个功能，你必须等待 Android Pie (Android 9)更新推出或者[自己手动启用](https://www.xda-developers.com/turn-on-wifi-automatically-nexus5x-nexus6p/)(尽管我们应该注意，只有当你使用覆盖来启用框架中的值时，这种方法才可能真正有效。)