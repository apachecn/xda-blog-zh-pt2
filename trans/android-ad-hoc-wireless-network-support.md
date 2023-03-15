# Android Ad-hoc 无线网络支持

> 原文：<https://www.xda-developers.com/android-ad-hoc-wireless-network-support/>

你们中的一些人可能知道，Android 不显示临时网络。更准确地说，引用 AOSP 的话——Android 使用 wpa_supplicant 作为 Wi-Fi 设备的平台接口。除了添加到请求者的扩展外，您的 Wi-Fi 驱动程序必须与标准 wpa_supplicant 兼容。

然而，XDA 论坛成员 [blackplatypus](http://forum.xda-developers.com/member.php?u=797810) 发现了一个修改过的 wpa _ supplicant】确实显示了 adhoc 网络，并在 XDA 论坛发布了补丁和信息。

> *修补程序修改了外部/wpa_supplicant AOSP 报告中的 wpa_supplicant 代码，以使临时网络显示为带有(*)前缀的常规接入点。*

最初由名为“szym”的开发人员修改，blackplatypus 应用了该补丁并为 Froyo 编译了它，并提供了带有修改后的 wpa_supplicant 的签名 update.zip。

更多信息和下载文件，请查看[修改线程](http://forum.xda-developers.com/showthread.php?t=754961)。