# OxygenOS 据称是数据挖掘个人身份信息进行分析

> 原文：<https://www.xda-developers.com/oxygenos-is-allegedly-data-mining-personally-identifiable-information-for-analytics/>

虽然一加手机在价格和开发开放性方面有着良好的声誉，但该公司本身在过去就如何处理用户数据做出了一些有问题的决定。当时，我们发现 OxygenOS 会在你的设备检查更新时将你设备的 IMEI 泄露到网络上。现在，根据安全研究员克里斯托弗·摩尔的说法，一加被指控收集更敏感的个人身份信息。

在去年参加的一次黑客挑战中，摩尔决定从他的 OnePlus 2 中探测互联网流量。他发现他的手机正在向域名 open.oneplus.net 发送 HTTPS 请求。他使用设备上的密钥解密了数据，并能够看到所有数据被发送回一加的 AWS 服务器。

然后，他分析了发送到该域的信息，发现一加正在收集屏幕打开、屏幕关闭、设备解锁事件、异常重启、序列号、IMEI、电话号码、MAC 地址、移动网络名称和 IMSI 前缀，以及无线网络 ESSID 和 BSSID。

但是数据挖掘并没有就此停止，因为 Moore 发现 OxygenOS 还在收集他打开和关闭应用程序的时间戳，甚至是正在打开的活动。

摩尔做了一些挖掘，发现负责这个数据收集的代码是一加设备管理器和一加设备管理器提供程序的一部分，它包含在系统应用程序 OPDeviceManager.apk 中

如果您的设备不是根设备，那么您可以运行以下 ADB 命令，在您的一加设备上禁用该系统应用程序:

```
 pm uninstall -k --user 0 net.oneplus.odm 
```

关于如何设置 ADB 和运行这个命令的教程可以在这里找到[。或者，如果你的设备是根用户，你可以安装](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)[这个 Magisk 模块](https://forum.xda-developers.com/oneplus-5/themes/magisk-oneplus-analytics-disabler-t3686636)。

所有这些信息都是通过 HTTPS 发送的，因此不会被任何人截获(前提是你在一个安全的网络上)。然而，人们想知道一加用这种信息做什么。在一份声明中，一加对他们正在收集的数据进行了如下解释:

> #### 我们通过 HTTPS 将两个不同的数据流安全地传输到亚马逊服务器。第一个流是使用分析，我们收集它是为了让我们根据用户行为更精确地微调我们的软件。可以通过导航到“设置”->“高级”->“加入用户体验计划”来关闭这种使用活动的传输。第二个数据流是设备信息，我们收集这些信息是为了提供更好的售后支持。

请记住，这种数据收集只发生在 OxygenOS 上，所以如果你安装了一个定制的基于 AOSP 的 ROM，如 LineageOS，那么你的手机就不会被数据挖掘。要了解更多的技术细节，我们建议你阅读摩尔先生在下面链接的原始博文。

* * *

[**来源:克里斯的安全和科技博客**](https://www.chrisdcmoore.co.uk/post/oneplus-analytics/)