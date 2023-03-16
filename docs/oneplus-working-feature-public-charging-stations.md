# [更新:更多图片]一加可能正在开发一个功能来帮助你找到公共充电站

> 原文：<https://www.xda-developers.com/oneplus-working-feature-public-charging-stations/>

**更新(06/15/2020 @ 05:00 AM ET):** 这篇文章发表后不久，推特用户@ UrAvgHomoSapien 分享了在机场发现的充电站的图片。滚动到底部了解更多信息。

这是令人兴奋的软件发布月，因为谷歌推出了针对 Pixel 设备的第一个 Android 11 测试版。其他原始设备制造商如 [Vivo、iQOO](https://www.xda-developers.com/download-iqoo-3-5g-4g-vivo-nex-3s-android-11-beta-1-build/) 和[一加](https://www.xda-developers.com/oneplus-8-oneplus-8-pro-android-11-beta-download/)已经发布了他们旗舰的第一组测试版，其他原始设备制造商如 [OPPO](https://www.xda-developers.com/oppo-find-x2-find-x2-pro-android-11-beta/) 、[小米、POCO](https://www.xda-developers.com/xiaomi-mi-10-pro-poco-f2-pro-android-11-beta-miui-11-12/) 和 [Realme](https://www.xda-developers.com/realme-x50-pro-android-11-beta/) 也承诺了他们旗舰的版本。这些软件版本是应用开发者在最新的 Android 版本上测试他们的应用的一个很好的媒介。但除此之外，他们也是一个很好的信息来源，可以了解在不久的将来手机会有什么样的功能。我们最近在一加发布的软件版本中发现了[新一加 8“冰蓝色”、65W Warp 充电功能](https://www.xda-developers.com/oneplus-8-ice-blue-color-65w-super-warp-charging-revealed-android-11-beta/)和[一加 Pods 真正无线耳机](https://www.xda-developers.com/oneplus-pods-truly-wireless-earbuds-android-11-beta/)。现在，我们了解到一加正在开发一个功能来帮助你找到公共充电站。

**[一加 8 XDA 论坛](https://forum.xda-developers.com/oneplus-8)**|**|[一加 8 亲 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro)**

**[从亚马逊](https://www.amazon.in/gp/product/B077PWK5BY/?tag=xdaportalin-21)购买一加 8 Pro**

XDA 资深会员*[Some _ Random _ Username](https://forum.xda-developers.com/member.php?u=8234677)*在一加 8 和一加 8 Pro 的 Android 11 Beta 1 的设置应用中发现了新的字符串。

```
 <string name="op_charging_Station_mute_notifications">Mute Notifications</string>
<string name="op_charging_station">Charging Stations</string>
<string name="op_charging_station_no_station">No charging stations nearby</string>
<string name="op_charging_station_summary">Notify when there is a charging station nearby</string>
<string name="op_charging_stations">Charging stations</string>
<string name="op_charging_stations_off_description">To find the charging stations, location permission is required to detect BLE beacons. Please provide access to location to start using this feature.</string>
<string name="op_charging_stations_off_header">To find the charging stations,location permission is required to detect BLE beacons. Please provide access to location to start using this feature.</string>
<string name="op_find_charging_stations">Find Stations</string> 
```

这些字符串中的描述表明，一加正在努力建设充电站网络，以帮助其用户快速为手机充电。这些充电站将配备 BLE 信标，这将让它们向附近的设备(在这种情况下是一加手机)广播它们的标识符，并向用户精确定位它们的位置。当然，当用户到达那里时，他们可以为他们的设备充电。

我们在 Settings 应用程序中发现了一个图形资产，让我们更好地了解会发生什么:

深入挖掘测试版，我们发现一加有几个与这个“充电站”功能相关的类。这些类别包括:

*   *充电站预控制器*
*   *OPChargingStationHeaderController*-其具有用于获取与充电站的距离的代码以及充电站的名称
*   *OPChargingStationSettings*-它有切换通知静音选项的代码，因此用户将不再受到充电站通知的困扰

测试版还多次引用了一个名为“*com . oneplus . charging pilar*的包名，这表明该功能需要一个配套应用程序才能工作。我们还发现了几个与此功能相关的设置首选项，包括:

*   *操作充电站功能开启*
*   *操作充电站信标名称*
*   *op _ 充电 _ 车站 _ 信标 _ 距离*
*   *op _ 充电 _ 电台 _ 静音 _ 通知*

这确实表明该功能也需要在应用程序中打开。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*

* * *

我们不知道一加何时会宣布其充电站网络，但一加 8T 的推出似乎是一个很好的时机。记住[一加也在研究 65W 翘曲充电](https://www.xda-developers.com/oneplus-8-ice-blue-color-65w-super-warp-charging-revealed-android-11-beta/)，充电站网络可以帮助巩固充电升级，作为即将到来的设备系列的一个亮点。

然而，我们不知道这些充电站将提供什么速度，也不知道它们是否会被限制在较新的智能手机上。由于我们假设这些是带有插头点和/或空 USB 端口的物理结构，因此任何拥有智能手机的人都可以走到这些站为他们的智能手机充电，这将是一个合理的假设。定位器可以简单地帮助一加用户通过他们的智能手机轻松定位这些。类似的装置已经存在于机场和商场等公共场所，因此人们可以认为一加将为它们的实施增加一些独特性。

测试版没有包含关于该功能可用区域的进一步线索，但图形中描绘的插头点看起来像[印度插头点(D 型)](https://www.worldstandards.eu/electricity/plugs-and-sockets/) -尽管这可能只是一个通用图像。

我们也不知道一加是否会在其手机上预装配套应用程序，或者是否会从 Play Store 为其手机和其他手机提供可选下载。

我们联系了印度一加公司进行评论。我们将根据他们的回应更新文章。

* * *

## 更新:一加充电站出现在印度班加卢鲁机场

在我们的文章发表后不久，Twitter 用户@UrAvgHomoSapien 告诉我们，一加充电站已经安装在印度班加卢鲁的国际机场。

一加充电站安装在肯佩戈达国际机场 Bengaluru 的出发航站楼，具有两个 USB Type-A 端口，支持一加设备的 30W 翘曲充电。还有一个其他设备的国际插头。

有了这些新信息，人们可以期待更多这样的充电站在印度出现。因此，一加正在开发的应用程序将帮助用户定位他们附近的车站。有可能一加也将更新这些充电站，以支持 65W 翘曲充电支持。

* * *

*感谢 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 的提示，感谢推特用户[@ uravghomospien](https://twitter.com/UrAvgHomoSapien)的图片！*