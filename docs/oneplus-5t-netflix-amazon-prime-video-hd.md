# OnePlus 5 和 OnePlus 5T 获得了播放网飞和亚马逊 Prime 视频高清版的更新，但有一个问题

> 原文：<https://www.xda-developers.com/oneplus-5t-netflix-amazon-prime-video-hd/>

回到 12 月，当一加论坛上的一些用户报告说 OnePlus 5 和 OnePlus 5T 无法播放来自网飞或亚马逊 Prime Video 的高清视频时，引起了一场轩然大波。然而，这个问题影响的不仅仅是两款最新的一加旗舰，因为它还影响了 OnePlus 3、OnePlus 3T、中兴 Axon 7、Axon M，可能还有更多设备。问题？这些手机都不支持谷歌的 Widevine DRM 的最安全级别:Widevine Level 1。

但在承诺研究它之后，一加终于准备好更新 OnePlus 5/5T，支持 Widevine Level 1。只有一个问题:没有 OTA 更新，也没有你可以下载的 ROM。

[据大卫 Y](https://forums.oneplus.net/threads/important-oneplus-5t-does-not-support-hd-viewing-for-netflix-google-play-movies-etc.704333/page-23#post-17864514) 。作为一加社区经理之一，由于“更新设备涉及的安全流程”，更新只能通过**认证的 PC** 完成这意味着用户将不得不**亲自把他们的设备发送到一加**来接收更新，因为唯一被授权处理更新的个人电脑大概在一加的办公室里。

如果你住在北美、欧洲、印度或中国，你不需要支付任何费用，因为一加会支付运费。该公司表示，如果您选择发送您的设备，您应该在 5 个工作日内收到它。感兴趣的用户应该[联系一加客户支持团队](https://oneplus.net/support)获取更多关于设置退货的信息，尽管一加承诺他们已经尽可能简化了流程。

对于那些希望看到这个问题得到解决的人来说，我们确信你们中的绝大多数人都希望看到一个能够支持 Widevine 级的 OTA 更新。不幸的是，由于 Widevine DRM 的处理方式，这似乎是不可能的。就个人而言，这似乎是为了能够看到网飞或亚马逊的高清视频而付出的巨大努力，但如果这些服务缺乏高清视频真的让你感到困扰，那么你可能想接受一加的这一提议。我们只是希望这件事能从一开始就处理好，特别是因为谷歌不需要任何授权费用来获得 1 级认证。

* * *

## 更新:你必须把手机送进去的原因

一加要求你提交 OnePlus 5 或 5T 的原因是因为 Widevine Level 1 的工作方式。根据[文档](https://storage.googleapis.com/wvdocs/Widevine_DRM_Getting_Started_Devices.pdf):

> #### Widevine 密钥箱必须使用设备独有的密钥进行加密，该密钥对于 TrustZone 之外的软件或探测方法是不可见的。Widevine 钥匙盒必须在工厂安装，或使用经批准的安全交付机制交付给设备。

*感谢[米奇福利](https://www.xda-developers.com/oneplus-5t-netflix-amazon-prime-video-hd/#comment-3774633407)*