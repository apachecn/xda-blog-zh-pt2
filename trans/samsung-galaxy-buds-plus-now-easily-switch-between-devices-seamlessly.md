# 三星 Galaxy Buds+现在可以轻松地在设备之间切换

> 原文：<https://www.xda-developers.com/samsung-galaxy-buds-plus-now-easily-switch-between-devices-seamlessly/>

三星 Galaxy Buds+ 是三星目前的旗舰 TWS 解决方案，它们在很大程度上相当成功。三星甚至更进一步，发布了新的颜色变体，如[光环红](https://www.xda-developers.com/samsung-galaxy-buds-plus-wireless-earbuds-launch/)、[光环蓝](https://www.xda-developers.com/samsung-galaxy-buds-sale-aura-blue-color-u-s/)，该公司还计划发布紫色 BTS 版。尽管耳塞本身非常好，但在如何处理与多种设备的连接方面还存在一些困惑。在发布时，三星提到了对使用蓝牙 5.0 的设备的“多点”(多设备)支持，但[这是一种误导，因为该功能仅限于](https://www.xda-developers.com/samsung-galaxy-buds-multi-device-feature-galaxy-phones-smartthings/)安装了三星 [SmartThings](https://www.xda-developers.com/samsung-smartthings-new-virtual-home-feature-at-a-glance-dashboard-connected-devices/) 应用程序的 Galaxy 手机。幸运的是，现在情况正在好转，因为三星 Galaxy Buds+现在可以在设备之间无缝切换。

三星 Galaxy breads+Plugin[v 1 . 3 . 20061151](https://www.apkmirror.com/apk/samsung-electronics-co-ltd/galaxy-buds-plugin-2/galaxy-buds-plugin-2-1-3-20061151-release/galaxy-buds-plugin-1-3-20061151-android-apk-download/)已经开始推出，并且附带了对 Galaxy breads+的 r175 Xu 0at f 2 固件更新的更新提示。我们发现了一些与 APK 无缝连接相关的新字符串，并发现所描述的功能已经在推出。

```
 <string name="seamless_connection_desc">"You can switch your earbuds quickly to nearby devices without disconnecting them or turning on pairing mode. This works with any nearby device that's signed in to your Samsung account, even if it never paired with your earbuds before, and also with other devices if they've paired with your earbuds previously. In some rare cases, this may allow unknown devices to connect to your earbuds and control them. You can turn this off in settings."</string>
<string name="settings_seamless_connection">Seamless earbud connection</string>
<string name="settings_seamless_connection_desc">"Switch quickly to nearby devices without disconnecting your earbuds or turning on pairing mode. This works with any nearby device that's signed in to your Samsung account, even if it never paired with your earbuds before, and also with other devices if they've paired with your earbuds previously. In some rare cases, this may allow unknown devices to connect to your earbuds and control them."</string> 
```

## 三星 Galaxy Buds+上的无缝连接是什么？

为了了解这个功能的作用，我们需要后退一步，了解在这次更新之前，Buds+是如何连接多个设备的。

### 先前行为

此前，三星 Galaxy Buds+只能在两台运行 Android 7.1.1 和更高版本的三星设备之间进行多设备切换，前提是这两台设备上都安装了 SmartThings 应用程序。SmartThings 将使用户能够在每台设备的媒体面板内点击，以移动两台设备之间的 Galaxy Buds+连接。

对于非三星手机，用户必须关闭当前连接的设备(设备 A)的蓝牙，在 Buds+上进入配对模式(轻按一次，然后轻按 plus hold)，然后连接第二个设备(设备 B)。要回到设备 A，您需要关闭设备 B 上的蓝牙，并再次进入 Buds+上的配对模式，依此类推。

可以想象，这不太方便。

### 新行为

通过这一新的更新，设备之间的切换变得非常方便，因为您不再需要关闭任何设备上的蓝牙，也不需要在 Buds+上进入配对模式。

假设两个设备之前已经配对，您只需选择设备上预先存在的 Buds+连接进行连接和切换。因此，如果您连接到设备 A，您需要打开设备 B 上的蓝牙连接页面，并选择 Buds+。这将切换您的连接。要从设备 B 返回到设备 A，只需打开设备 A 上的蓝牙连接页面并选择 Buds+连接。

* * *

我尝试了这款设备在戴尔 XPS 13 2in1 (7390)和一加 7 Pro 之间切换，体验要方便得多。这不是真正的“多点”连接，Buds+会自动切换到活动音频源。我也不会称之为“无缝”，因为你确实需要摆弄源设备。但它无疑消除了仅仅为了在设备之间切换而反复配对的痛苦。考虑到 Buds+在语音通话方面的出色表现，在设备之间切换时，拥有这一功能确实非常方便。