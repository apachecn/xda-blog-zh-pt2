# 高通骁龙 865 支持安卓 11 中的 DSDS、驾照

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-865-spu-dual-sim-dual-standby-drivers-licenses-android-11/>

今天早些时候，高通公布了他们最新的高端 Snapdragon 800 系列 SoC 的全部规格和功能:高通骁龙 865 移动平台。在那篇文章中，我们涵盖了您需要知道的所有主要细节，但和往常一样，在主题演讲中也透露了一些更小的信息。在主题演讲中，高通产品管理高级主管 Jesse Seed 谈到了骁龙 865 中的一些新安全功能。值得注意的是，安全处理单元(SPU)是负责保护生物特征凭证、支付信息和 SIM 数据的片上安全元件，现在完全支持双 SIM、双待机和 Android 11 即将推出的 IdentityCredential API。

**集成双 SIM 卡，双待机**

带有 eSIMs 的 Android 智能手机仍然很少，尽管市场上有一些，包括 Pixel 2、Pixel 3、Pixel 3a、Pixel 4、Galaxy Fold 和摩托罗拉 Razr。存储 SIM 卡数据需要安全的硬件，这对于大多数设备来说意味着需要一个专用的芯片。对于 Pixel 2，根据 iFixit 的拆解，这是 ST Microelectronics ST33G1M2 32 位 MCU，配有 ARM SecurCore SC300。然而，[骁龙 855 上的安全处理单元具有智能卡等效的 EAL4+认证](https://www.xda-developers.com/qualcomm-snapdragon-855-secure-processing-unit-eal4/)，这意味着它被认为足够安全来处理 SIM 数据。高通与一家名为[金雅拓](https://www.businesswire.com/news/home/20180527005003/en/Gemalto-Announces-Collaboration-Qualcomm-Technologies-Integrate-eSIM)的公司合作，在骁龙的安全处理部门实现 eSIM 支持。

在这项工作的基础上，宣布骁龙 865 的 SPU 现在完全支持双卡双待(DSDS)。这意味着，SPU 不仅可以存储由多个运营商提供的 eSIM，而且第二个不活动的 eSIM 仍然可以接收呼叫和文本。

**支持 Android 11 的身份认证 API**

早在三月份，谷歌[就开始着手](https://www.xda-developers.com/google-android-digital-drivers-license/)一个新的身份认证 API。该 API 允许在设备上以电子方式存储凭证，如驾照或护照。[谷歌在 I/O 2019](https://www.xda-developers.com/android-q-security-privacy-features/) 上宣布，他们正在与 ISO 合作，以标准化移动驾照的实施，他们将开发一个 Jetpack 支持库，以便应用程序可以支持身份凭证的请求。现在，高通已经确认骁龙 865 的 SPU 支持谷歌的 IdentityCredential API。

更准确地说，这一声明很可能意味着骁龙 865 将支持谷歌在 IdentityCredential HAL 实现中提到的“直接访问”模式。这种模式允许证书被拉起，即使没有足够的电力来启动主要的 Android 操作系统。

**更新:**来自 Google 的 Shawn Willden 分享了一些关于如何支持直接访问模式的技术信息。[据他说](https://twitter.com/shawnwillden/status/1202648532840144896)，SPU 不太可能支持直接访问模式，因为它集成在 SoC 中。如果安全元件被集成到像 NFC 控制器这样的分立芯片中，它将更容易支持。然而，有一种可能性，高通可能已经发现或正在研究一种方法，使这项工作。

该 API 仍在开发中，但我们正在跟踪它在 AOSP 的进展。谷歌计划在下一个 Android 版本，也就是 Android 11 中发布这个 API 和 [Jetpack 库](https://android-review.googlesource.com/c/platform/frameworks/support/+/979252)。