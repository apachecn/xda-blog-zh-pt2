# 非官方的 LineageOS Fork with microG 让你避开谷歌服务

> 原文：<https://www.xda-developers.com/unofficial-lineageos-built-in-microg-avoid-google-services/>

MicroG 是 Google Play 服务的替代产品，几乎可以在所有安卓设备上找到。它允许你在设备上避开对谷歌专有软件的需求，同时通过开源软件保留几乎全部的功能。

以前，设置 microG 有点复杂，因为它需要签名欺骗形式的 ROM 支持以及用户端的许多其他准备工作。[Magisk 模块的发布有助于简化流程](https://www.xda-developers.com/xda-external-link/nanomod-magisk-module-automates-microg-pseudo-debloat-f-droid-and-more/)，但它仍然需要 ROM 端的支持和一些准备工作，而 stock LineageOS 无法满足这些要求。

现在，XDA 成员 [Simon94](https://forum.xda-developers.com/member.php?u=4316015) 已经通过创建一个[非官方分支简化了多种设备的流程，该分支内置了 MicroG](https://lineage.microg.org) 和 F-Droid，后者是自由/开源软件应用程序的 Play Store 替代品。

microG 的好处包括能够根据你的需要和喜好启用或禁用谷歌服务。例如，如果您愿意，您可以禁用安全网或 GSM 并启用设备注册。定位服务也被两个开源软件所取代(一个是 Mozilla 的，一个是 Nominatim 的),可以选择安装其他软件。更何况你还会收到 OTA 更新！

如果你想从 LineageOS 切换，建议清除 flash [microG LineageOS](https://lineage.microg.org) 因为密钥不同，它不会像 OTA 更新一样覆盖其他 LineageOS 版本。您可以更改密钥，但出于稳定性原因，强烈建议您只清理闪存。一旦安装完毕，你将不得不在 microG 应用程序中授予一些设备权限，所以打开它并检查“自检”部分。您可以启用所有功能，或者在那里查看您还需要做什么。请记住，由于您所使用的软件的非官方性质，任何东西都不能保证正常工作，并且随时可能崩溃。

* * *

[**检出 microG 支持的 LineageOS！**](https://lineage.microg.org)

*感谢 XDA 资深会员 [kurtn](https://forum.xda-developers.com/member.php?u=8031265) 的提示！*