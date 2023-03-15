# Android Automotive 通过蓝牙 HFP 增加了多设备连接

> 原文：<https://www.xda-developers.com/android-automotive-bluetooth-hfp/>

Android 8.0 奥利奥表面上看起来像是对 Android 7 牛轧糖的小更新。但是，一旦你深入研究各种变化，就会发现许多新功能和改进增强了各种硬件生态系统中的整体 Android 体验。本文讨论了基于 Android 8.0 Oreo 的 Android Automotive 的一些变化，这些变化增强了车载信息娱乐(IVI)系统上基于蓝牙的体验。

Android Automotive 是为车辆设计的基于 Android 的实际操作系统，不同于 Android Auto。Android Auto 是一个允许您将手机连接到汽车仪表板显示器以使用某些有用应用程序的系统，如地图、音乐或语音访问。Android Automotive 与您的汽车功能集成得更加紧密——根据设置，它甚至可以控制车辆中的各种传感器和开关。你可以[在这里](https://www.xda-developers.com/panasonic-automotive-to-build-android-automotive-in-vehicle-infotainment-system-into-fiat-chrysler-vehicles/)阅读更多关于 Android Automotive 的信息。

第一组改进来自蓝牙连接领域。Android Automotive 上的 Android 8.0 Oreo 在将设备连接到 IVI 系统时创建了更加无缝的蓝牙用户体验。IVI 现在可以监听特定事件，如打开车门或启动引擎，然后开始自动扫描范围内的蓝牙设备。

在以前版本的 Android Automotive 中，IVI 上的蓝牙只有在蓝牙适配器通电时才会扫描设备。如果 IVI 蓝牙打开，然后设备进入范围，用户将需要干预手动连接设备，因为在没有设备连接时没有自动扫描的规定。

在 Android 8.0 Oreo 到 Android Automotive 中，OEM 可以指定和自定义触发事件，这些事件可以导致蓝牙扫描范围内的设备以与之配对，前提是蓝牙适配器已打开且尚未连接到设备。这些触发引擎可以从解锁车门到启动引擎。在默认实现中，IVI 蓝牙将优先考虑最近连接的设备。

此外，IVI 现在可以支持通过蓝牙同时连接多个设备。多设备蓝牙电话服务允许用户连接不同的设备，如个人电话和工作电话，并从任一设备进行免提呼叫。该功能旨在通过减少分心和改善驾驶时的通话体验来提高驾驶安全性。蓝牙免提模式(HFP)允许两个并发连接，其中每个连接在 IVI 和 IVI 应用程序上注册为一个单独的电话帐户。默认情况下，呼出电话使用最后连接的设备，而拨号器应用程序不会故意指示呼入电话来自哪个设备。原始设备制造商可以通过定制拨号器应用程序来改变这种行为。

* * *

[**来源:安卓来源**](https://source.android.com/devices/automotive/ivi_connectivity)