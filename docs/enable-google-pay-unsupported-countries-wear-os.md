# 如何在 Wear OS 上不支持的国家启用 Google Pay

> 原文：<https://www.xda-developers.com/enable-google-pay-unsupported-countries-wear-os/>

# 如何在磨损操作系统不支持的国家启用谷歌支付

如果你曾经想在 Wear OS 上使用非接触式支付，但你的国家不支持 Google Pay，现在你可以通过永久代理使用它。

非接触式支付是智能手表的最佳功能之一，但许多地区的用户没有使用它的奢侈。这是因为世界上仍有很多国家没有正式支持 Google Pay。不过，如果你有一个 Wear OS 智能手表，并且生活在一个不支持该功能的国家，你现在可以使用 XDA 资深会员 [Humpie](https://forum.xda-developers.com/member.php?s=b464018083ff4848ea30452f2645ac69&u=3372705) 的解决方案。他的应用程序，[永久代理，](https://forum.xda-developers.com/android/apps-games/app-enable-google-pay-unsupported-t3980625)是为 Wear OS 设备设计的，允许任何人在通常被屏蔽的地区使用 Google Pay。

为此，应用程序使用 Android 内置的 http_proxy 服务。唯一的警告是，运行服务的命令只能通过 ADB shell 执行，这本身就需要一台计算机。永久代理使用 ADB over Bluetooth 作为解决此问题的方法。这样，你只需要智能手表和一个代理就可以使用这项服务。网上有很多代理，所以一定要找一个值得信赖的，可靠的，不经常换地址的。如果你找到一个为代理提供静态 IP 地址的提供商，你甚至可以在永久代理中启用自动启动选项，以便在设备启动时运行应用程序。

事不宜迟，让我们解释一下如何让它工作。

1.  首先，你必须在你的 Wear OS 智能手表上启用开发者选项。进入**设置>系统>关于**点击**构建号** 7 次
2.  导航到**设置>开发者选项**并启用 **ADB 调试**和**蓝牙调试**选项
3.  现在，你必须从 [XDA 实验室](https://labs.xda-developers.com/store/app/nl.jolanrensen.permanentproxy)或[谷歌 Play 商店](https://play.google.com/store/apps/details?id=nl.jolanrensen.permanentproxy)下载应用程序并打开它
4.  点击**总是允许这台电脑**
5.  输入您选择的代理地址和端口，并可选地启用**启动时启用**选项

这种方法的明显缺点是，您必须信任代理提供商，面临可能的电池耗尽问题，并处理设备上潜在的慢速连接。无论如何，你现在可以在你的 Wear OS 设备上使用 Google Pay，即使它在你的国家不受支持。

[appbox xda nl . jolanrensen . permanent proxy]

* * *

**[在 XDA 论坛](https://forum.xda-developers.com/android/apps-games/app-enable-google-pay-unsupported-t3980625)** 阅读更多关于永久代理的信息