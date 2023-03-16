# Galaxy Buds Manager 是三星 Galaxy Buds 的开源非官方 Windows 客户端

> 原文：<https://www.xda-developers.com/samsung-galaxy-buds-manager-open-source-unofficial-windows-client/>

# 这个开源的 Galaxy Buds 客户端可以让你在 Windows PC 上管理你的 Buds

一名开发者在对三星的专有通信协议进行逆向工程后，发布了一款用于 Windows 的开源 Galaxy Buds 客户端。请继续阅读！

Galaxy Wearable 应用程序允许用户将三星可穿戴设备连接到他们的智能手机。人们还可以在安装[适当的](https://play.google.com/store/apps/details?id=com.samsung.accessory.fridaymgr) [插件](https://play.google.com/store/apps/details?id=com.samsung.accessory.popcornmgr)后，通过同一个应用程序管理 Galaxy Buds 系列无线耳塞。对于 PC 和 Mac 用户，三星提供了一个类似的配套应用程序，名为 [Galaxy Buds Manager](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=This+open+source+Galaxy+Buds+client+lets+you+manage+your+Buds+from+your+Windows+PC&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fsamsung-galaxy-buds-manager-open-source-unofficial-windows-client%2F&u1=UUxdaUeUpU28661&url=https%3A%2F%2Fwww.samsung.com%2Fau%2Fsupport%2Fmodel%2FSM-R175NZBAASA%2F%23downloads) ，以便检查软件更新和[在 Galaxy Buds/Buds+上安装新固件](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=This+open+source+Galaxy+Buds+client+lets+you+manage+your+Buds+from+your+Windows+PC&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fsamsung-galaxy-buds-manager-open-source-unofficial-windows-client%2F&u1=UUxdaUeUpU28661&url=https%3A%2F%2Fwww.samsung.com%2Fau%2Fsupport%2Fmobile-devices%2Fupdate-samsung-buds-firmware%2F&ourl=https%3A%2F%2Fwww.samsung.com%2Fau%2Fsupport%2Fmobile-devices%2Fupdate-galaxy-buds-plus-firware%2F)。三星在 buds 和配套应用程序之间利用了一种专有的通信协议，但一名开发者现在已经成功对其进行了逆向工程。蒂姆·施内伯格(Tim Schneeberger)也发布了一个非官方的开源 Galaxy Buds 客户端，它比官方应用程序更加通用。

非官方客户端的初始版本，也被命名为 **Galaxy Buds Manager，**是作为一个 Windows 专用应用程序发布的。你需要。NET Framework 4.7.2 或更高版本来运行它，这意味着使用 [Mono](https://www.mono-project.com/) 将应用移植到 Linux 和 macOS 可能在不久的将来成为可能。

该客户端提供以下功能:

*   在仪表板上显示详细的传感器统计数据，包括:
    *   两个耳塞的内置 ADC(模数转换器)的电压和电流
    *   两个耳塞的温度
    *   更精确的电池百分比(而不是 5 步)
*   对所有板载组件执行自检
*   显示各种(调试)信息，包括:
    *   硬件版本
    *   (触摸)固件版本
    *   两个耳塞的蓝牙地址
    *   两个耳塞的序列号
    *   固件构建信息(编译日期、开发人员姓名)
    *   电池类型
    *   其他传感器数据
*   均衡器:解锁“杜比优化”功能
*   触摸板:将音量调高/调低与其他选项相结合

这个非官方配套应用的初始版本是为[最初的 Galaxy Buds](https://www.xda-developers.com/samsung-galaxy-watch-active-galaxy-buds-galaxy-fit-official/) 设计的。然而，2020 年的[银河芽+](https://www.xda-developers.com/samsung-galaxy-buds-plus-wireless-earbuds-launch/) 目前不被客户支持，因为蒂姆没有一双，我们确认它们不兼容。我们希望 Galaxy Buds 社区将通过提供所需的日志和消息转储来帮助开发者扩展设备兼容性列表。

**非官方的银河芽管理器 Windows 版:[下载](https://github.com/ThePBone/GalaxyBudsClient/releases) || [源代码](https://github.com/ThePBone/GalaxyBudsClient)**

开发者还[分享了](https://github.com/ThePBone/GalaxyBudsClient/blob/master/GalaxyBudsRFCommProtocol.md)Buds 用来接收和发送二进制数据的定制 RFComm 串行协议的结构，这对其他修补者应该是有益的。

* * *

**来源:[r/galaxy buds](https://www.reddit.com/r/galaxybuds/comments/gzzj2o/pc_unofficial_buds_manager_for_windows_released/)**