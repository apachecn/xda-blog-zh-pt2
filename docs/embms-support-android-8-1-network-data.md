# Android 8.1 中增加了 eMBMS 支持，以减少移动网络拥塞

> 原文：<https://www.xda-developers.com/embms-support-android-8-1-network-data/>

Android 8.1 中已确认支持 eMBMS，这将允许通过提供商采用的新技术来减少移动网络拥塞，这些提供商在您的设备中使用高通硬件。这一点已经被谷歌 Pixel 2 XL 和 Nexus 5X 上发现的新许可所证实，如下所示，以及我们在 8 月份对 AOSP 的[监控中的发现。](https://www.xda-developers.com/embms-google-support-multicast/)

```
<permission android:name="android.permission.SEND_EMBMS_INTENTS" android:protectionLevel="privileged|signature"/>
```

当许多用户试图访问相同或相似的内容(如视频)时，eMBMS 工作得最好，因为它避免了将信息单独发送给每个客户端(单播)。相反，相同的数据通过多播发送给每个人。例如，在现场活动中，视频可以直接发送给一次扫描中连接的所有客户端，而不是单独发送给每个用户。

这一增加在很大程度上是因为我们有意愿应对我们最终将面临的'[1000 倍数据挑战](https://www.qualcomm.com/invention/1000x)。对于那些不熟悉 1000 倍数据挑战的人来说，它只是描述了一个场景，其中我们所有的设备加起来将需要 1000 倍于当前带宽所能处理的数据量。[在思科](https://www.cisco.com/c/en/us/solutions/collateral/service-provider/visual-networking-index-vni/complete-white-paper-c11-481360.html#_Toc484531491)最近提供的一项研究中，预计 82%的互联网流量将由视频流构成。eMBMS 非常适合视频流，将是应对 1000 倍数据挑战的重要一步。这是比不断增加消费者可用带宽更有效的解决问题的方法。目前带头发起这一倡议的主要供应商是美洲的威瑞森、亚洲的 Kt 和 Reliance 以及欧洲的 EE 和 Vodafone。

如上所述，这项新技术利用了高通硬件，因此那些使用麒麟、Exynos 或联发科设备的用户无法使用 eMBMS。希望现在 Android 8.1 正式发布支持，我们会看到越来越多的提供商支持这个平台。

* * *