# Android Oreo 增加了对 WiFi Passpoint 的支持，但对原始设备制造商来说是可选的

> 原文：<https://www.xda-developers.com/android-oreo-supports-wifi-passpoint/>

# Android Oreo 增加了对 WiFi Passpoint 的支持，但对原始设备制造商来说是可选的

Android Oreo 增加了对 WiFi Passpoint 功能的支持，但没有强制 OEM 厂商支持相同的功能。请继续阅读了解更多信息！

WiFi Passpoint 由 WiFi 联盟于 2012 年推出，是一个全行业的解决方案，旨在简化对热点的网络访问。它旨在消除用户每次连接到网络时查找和验证网络的需要。在不支持 Passpoint 的网络中，用户每次从一个热点移动到下一个热点时，都需要搜索并选择一个网络，并请求连接到接入点。他们甚至可能需要重新输入他们的身份验证凭据或重新接受使用条款和条件。

[Passpoint](https://www.wi-fi.org/discover-wi-fi/wi-fi-certified-passpoint) ，通常被称为 Hotspot 2.0，解决了大型热点网络的这一痛点。它允许用户在网络上登录一次，然后当他们请求时，将您的凭证传递到网络支持的所有其他热点。这允许您的移动设备以更无缝的方式从一个热点跳到另一个热点，因为它不需要再次登录。

Android Oreo 现在正式增加了对 WiFi Passpoint 的支持。但是[根据 Android 8.0 的兼容性文档](https://source.android.com/compatibility/8.0/android-8.0-cdd#7_4_data_connectivity)，它留给原始设备制造商去实现，而不是强制添加。

如果软件包含对 WiFi Passpoint 的支持，OEM 就必须履行一些强制性义务，以确保预期的功能。必须实现 [SDK 文档](http://developer.android.com/reference/android/net/wifi/WifiManager.html)中描述的与 Passpoint 相关的*wifi manager*API。OEM 还必须支持 IEEE 802.11u 标准，具体涉及[网络发现和选择](https://en.wikipedia.org/wiki/IEEE_802.11u#Network_discovery_and_selection)，如通用广告服务(GAS)和接入网查询协议(ANQP)。相反，如果设备实现不支持 WiFi Passpoint，OEM 必须确保 *WifiManager* API 抛出一个`UnsupportedOperationException`。

官方对 WiFi Passpoint 的支持无疑是对 Android 体验的一个净积极因素，即使没有给 OEM 厂商提供强大的动力来支持它。我们希望原始设备制造商出于对最终用户的有用性主动支持该功能。