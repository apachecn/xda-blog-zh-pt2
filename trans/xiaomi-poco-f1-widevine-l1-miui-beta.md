# 小米 POCO F1 在最新的 MIUI 测试版中获得了 Widevine L1 支持

> 原文：<https://www.xda-developers.com/xiaomi-poco-f1-widevine-l1-miui-beta/>

[POCOPHONE F1](https://www.xda-developers.com/xiaomi-pocophone-f1-launches-globally/) ，或在印度被称为[的 POCO F1](https://www.xda-developers.com/xiaomi-poco-f1-specs-pricing-availability-india/)，是 2018 年最好的智能手机之一，这要归功于它的可负担性、旗舰级硬件、[可接受的相机质量](https://www.xda-developers.com/xiaomi-poco-f1-blind-camera-comparison/)，以及[定制开发支持](https://www.xda-developers.com/poco-pick-developers-poco-f1/)。然而，与最接近的竞争对手 OnePlus 6 和一加 6T 不同，POCO F1 出厂时没有经过 Widevine L1 认证。当我们了解到以高清质量传输网飞和亚马逊 Prime 视频的必要性时，我们第一次介绍了 Widevine DRM。这一发现引发的争议促使一加向用户提供机会[亲自发送他们的设备](https://www.xda-developers.com/oneplus-5t-netflix-amazon-prime-video-hd/)以获得 Widevine L1 认证。在 POCO first [宣布](https://www.xda-developers.com/miui-10-global-stable-next-week-xiaomi-poco-f1/)他们将为 POCO F1 带来 Widevine L1 支持后，我们认为这意味着用户必须将他们的设备发送给小米。然而，我们后来了解到，设备在出厂后实际上可以配备 Widevine L1，并且[正如小米所承诺的](https://www.xda-developers.com/xiaomi-poco-f1-4k-60-fps-video-recording-update/)，POCO F1 终于在最新的 MIUI 10 9.2.25 测试版中获得了 Widevine L1 认证的更新。

正如你在上面使用 DRM Info 应用程序发布的截图中看到的，Widevine CDM 安全级别显示为 L1。这意味着，从理论上讲，小米 POCO F1 的所有者现在应该可以以 540p [以上的价格从网飞播放受 DRM 保护的内容，而不必使用被黑客攻击的 APK](https://forum.xda-developers.com/poco-f1/how-to/watch-netflix-hd-ultra-hd-poco-f1-t3840727) 。不过，仅仅因为一台设备通过了 Widevine L1 认证，并不意味着视频流媒体服务将自动允许他们播放受保护的内容。像网飞这样的服务提供商可以根据他们自己想要的参数[将设备列入白名单或黑名单](https://help.netflix.com/en/node/23939)。事实上，许多视频提供商[不愿意](https://twitter.com/atytse/status/1096690215190753281)认证已经推出的设备。~~我们尚未确认哪些视频提供商现在在 POCO F1 上使用高清技术，但我们会及时更新。~~

**更新:**POCO CM 向我们确认，现在支持 HotStar 和 Amazon Prime Video 的 DRM 内容。遗憾的是，网飞尚未认证 POCO F1 的高清流媒体功能。

[小米 POCO F1 论坛 ](https://forum.xda-developers.com/poco-f1)

如果你有兴趣下载 POCOPHONE F1 的最新 MIUI 10 全球测试版，你可以通过下载下面的恢复 ROM 来这样做，这是 XDA 公认的开发者 [yshalsager](https://forum.xda-developers.com/member.php?u=6084385) 提供的。

[**小米 POCO F1/POCOPHONE F1**](http://bigota.d.miui.com/9.2.25/miui_POCOF1Global_9.2.25_5dc5941802_9.0.zip) 下载 MIUI 10 全球 9.2.25

## 小米是如何用 Widevine L1 更新 POCO F1 的？

根据谷歌为 Widevine 提供的“[入门](https://storage.googleapis.com/wvdocs/Widevine_DRM_Getting_Started_Devices.pdf)”文档，keybox 在 TrustZone 中“必须用设备特有的密钥加密”。该密钥箱必须“在工厂安装”或使用经批准的安全交付机制交付给设备对于 OnePlus 5 和 OnePlus 5T，一加的一名社区经理表示，由于“更新设备涉及的安全流程”，用户必须亲自将他们的设备发送到一加，以便通过“经过身份验证的 PC”完成配置

一加的陈述与我们当时所知的唯一与 Widevine 相关的文档相匹配，因此社区普遍认为 OTA 供应是不可能的。因此，几个月来，我们预计小米将要求用户发送他们的设备，但即使这样也不可能，因为，POCOPHONE 全球负责人 Alvin Tse 表示，POCO 的 BSP 不像一加那样经过预先验证，因此 POCO 不可能走服务中心路线。BSP，即主板支持包，是由供应商(在本例中为高通)向 POCO 提供的一套软件和工具，用于支持特定芯片组上的特定 Android 版本，在本例中，他们指的是支持高通骁龙 845 移动平台的 Android 8.1 Oreo 版本的 BSP。(据我所知，高通的 bsp 已经通过了 Widevine 实施的预验证，所以我不完全确定 POCO 的情况如何。)

无论如何，很明显，小米无法在工厂为设备提供所需的设备专用密钥。这意味着他们唯一的选择是通过 OTA，而我们一直认为这是不可能的。相反，**至少从 2017 年中期**开始，Widevine L1 的 OTA 供应就已经成为可能。随着 Provisioning 3.0 模型的推出，Google 使通过 OTA 进行现场供应成为可能，该模型“使用 OEM 生成的设备信任根，该根可由 OEM 在工厂或通过无线方式安装。”然后，Widevine 可以使用该证书来“为设备提供特定于提供商的 DRM 证书”

 <picture>![Widevine DRM](img/06b0a5fbbb7136e75cfae24109b53cf1.png)</picture> 

Pre-requisites for Widevine L1 OTA provisioning. Source: [Widevine Level 1 Provisioning Models, version 1.2](https://storage.googleapis.com/wvdocs/Widevine_DRM_Device_Provisioning_Models.pdf).

 <picture>![](img/8eb7045c4e79bdb6092b40115c3e7ea0.png)</picture> 

An example flow for how an OEM can provision a device with Widevine L1 certification over OTA. Source: [Widevine Level 1 Provisioning Models, version 1.2](https://storage.googleapis.com/wvdocs/Widevine_DRM_Device_Provisioning_Models.pdf).

为了 OTA 供应设备，OEM 需要能够向 TEE(高通设备上的 QSEE)发布软件更新。)我相信大多数原始设备制造商使用高通对 QSEE 的默认实现 Widevine ，如果他们想更新它，他们需要提供源代码，他们可能会也可能不会由高通提供。因此，没有源代码，原始设备制造商将需要等待高通更新它。我不知道这是否发生在小米身上，但不管怎样，似乎该公司找到了如何将 Widevine L1 带到 POCO F1 的方法。现在他们只需要说服流行的视频提供商将他们的设备列入白名单。