# Wi-Fi 直接打印可能会在不久的将来出现在 Android 上

> 原文：<https://www.xda-developers.com/wi-fi-direct-printing-android/>

直到最近，Android 对打印机的支持还相当不稳定。[谷歌云打印](https://www.google.com/cloudprint/#jobs)，一个通过谷歌的服务器路由打印作业的半解决方案，2013 年来到安卓；Android KitKat 增加了原生打印；最新版本的 Android，Oreo，将互联网打印协议(IPP)合并到 Android 的默认打印服务中。Android 仍然无法使用 Wi-Fi Direct 直接打印到 Wi-Fi 连接的打印机，但这种情况可能会改变。

来自 AOSP Gerrit[Mopria](http://mopria.org/)移动打印联盟的开发者最近提交的一份承诺暗示 Android 将获得对 Wi-Fi 直接打印的支持，这将在无线设备和打印机之间直接创建一个点对点网络。新添加的代码包括一个管理 Wi-Fi 直接发现和连接的包 **com.android.bips.p2p** ，以及一个带有菜单的用户界面，用于添加打印机，从列表中选择已保存的打印机，并向它们发送打印作业。

 <picture>![](img/1e9773e864848c8ed49581a4665b01a6.png)</picture> 

Source: Android Open Source Project

如果 Wi-Fi Direct 听起来很熟悉，那是因为 Android 从冰淇淋三明治开始就支持它。这是由认证 Wi-Fi 产品和标准的全球行业协会 [Wi-Fi 联盟](https://www.wi-fi.org/)开发的协议，它不仅仅能够与打印机通信。Wi-Fi 直连是加密的，并使用两种服务-设备发现和服务发现-来识别附近的兼容 PC、电视、平板电脑和智能手机。一些支持 DLNA(数字生活网络联盟)的设备可以充当 Wi-Fi 直接媒体接收器，播放传输给它们的音频和视频。

无论如何，它是蓝牙的一个方便的替代品——不需要配对。与 Wi-Fi 热点不同，一些 Wi-Fi 直连设备不需要密码。

需要澄清的是，Android 上的 Wi-Fi 直接打印已经存在了一段时间——像三星的移动打印应用程序和[移动打印应用程序](https://play.google.com/store/apps/details?id=com.dynamixsoftware.printershare&hl=en)这样的应用程序支持它，正如[三星在较新的 Galaxy 系列智能手机上的打印服务](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=Wi-Fi+Direct+Printing+Might+Come+to+Android+in+the+Near+Future&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fwi-fi-direct-printing-android%2F&u1=UUxdaUeUpU19940&url=https%3A%2F%2Fwww.samsung.com%2Fus%2Fsupport%2Fmobile%2Fphones%2F&ourl=https%3A%2F%2Fwww.samsung.com%2Fus%2Fsupport%2Fanswer%2FANS00043266%2F)一样。但这些承诺表明，即将到来的 Android 版本，可能是 Android P，将原生支持它。

Wi-Fi Direct 已被惠普、爱普生和 Brother 等打印机制造商采用，所以如果你在过去几年里买了一台新的无线打印机，它很有可能支持它。预计运行 Android 下一个主要版本 Android P 的设备将会从中受益。

* * *

*本文于 2018 年 1 月 26 日修订，以反映 Mopria 移动打印联盟参与了此次提交。*