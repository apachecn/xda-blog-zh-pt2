# 独家:Android 11 的 3 个最好的功能不会出现在每台设备上

> 原文：<https://www.xda-developers.com/android-11-best-features-not-required/>

谷歌每年都会发布新版本的 Android 操作系统。谷歌在 2 月份发布了第一个 Android 11 开发者预览版，随后在过去的几个月里发布了第二、第三和第四个开发者预览版。本月早些时候，谷歌发布了第一个 Android 11 测试版(T1 ),并深入讨论了用户享受和开发者实现的最佳功能。然而，我们现在已经了解到，Android 11 中的三个顶级功能不会在每个 Android 设备上可用。

为了理解这是如何可能的，我们必须简要解释一下 Android 操作系统是如何从谷歌分发给智能手机设备制造商的。Android 是一个在 Apache 2.0 下授权的[开源操作系统](https://android.googlesource.com/)，这意味着任何人，从独立开发者到大公司，都可以在自己的设备上自由修改和分发该操作系统。谷歌为 Android 11 推出的大多数新操作系统功能都将是 Android 开源项目(AOSP)的一部分，智能手机设备制造商基于该项目开发自己的软件，但正如我之前提到的，Apache 2.0 许可证允许任何人根据自己的意愿修改软件。为了保持 Android 设备之间 API 和平台行为的一致性，谷歌将谷歌移动服务(包括谷歌 Play 商店和 Google Play 服务等应用程序和框架)的分发与许可协议捆绑在一起，强制设备遵守谷歌“ [Android 兼容性计划](https://source.android.com/compatibility/overview)”下的规则(以及其他要求)。Android 兼容性计划由多个自动化测试套件和 Android [兼容性定义文档](https://source.android.com/compatibility/cdd) (CDD)中列举的一组规则组成。

在 CDD 中，谷歌列出了设备制造商“必须”实现、仅“强烈建议”实现或“不应该”实现的软件和硬件功能。如果一个功能被列为“必须”实现，那么设备制造商必须添加该功能，否则他们不能在自己的设备上发布谷歌应用程序。如果一个功能被列为“不应该”实现，那么设备制造商就不能添加该功能，或者他们不能捆绑谷歌应用程序。最后，如果一个特性被列为“强烈推荐”，那么它取决于设备制造商是否想要实现这个特性。CDD 是一个不断变化的文档，甚至在每年公开发布新的 Android 版本后发布之前也是如此。谷歌经常更新文档以删除功能，更改语言以更加清晰，并根据合作伙伴的反馈放松要求。然而，一旦谷歌为某个特定的 Android 版本公开了 CDD，那些要求将会为运行该 Android 操作系统版本的谷歌认证设备而定。

Android 11 CDD 要到今年晚些时候才会公开，可能是在 9 月初。然而，开发者@ [deletescape](https://twitter.com/deletescape) 分享了一份预发布文件，详细介绍了 CDD 的变化，让我们提前了解了谷歌如何在整个生态系统中塑造 Android 11。CDD 的 60 多项变化中的绝大多数对用户来说都不是很有趣——它们描述了设备制造商必须如何实现某些 API、声明某些功能以及实现某些内核功能。然而，CDD 的 3 个变化引起了我们的注意，因为它们涉及到 Android 11 中一些最有趣的功能。这是我们发现的。

**设备控制**

设备控制是 Android 11 中的一项功能，允许智能家居自动化控制显示在电源菜单中。你可以关掉灯，打开车库门，启动吸尘器，改变家里的温度，以及做更多事情，而无需打开十几个不同的智能家居应用程序。谷歌增加了 API，智能家居应用程序的开发者可以使用这些 API 来显示电源菜单中的控件。我们认为这是一个很好的功能，最终将您的智能手机带入智能家居。不幸的是，没有要求原始设备制造商实际实施它。如果 OEM 认为该功能很差劲，或者他们想走不同的路线(例如只允许来自他们自己生态系统中的设备的智能家居控制)，那么他们可以简单地禁用对设备控制的支持。

当谷歌在 2020 年 2 月 25 日首次将设备控制添加到 CDD 时，他们通过在第 2.2.3 节-手持软件要求中添加“必须”要求来强制将其包含在内。然而，2020 年 5 月 20 日，谷歌更新了文本，删除了提议的“必须”。新的第 3.8.16 节-设备控制概述了必须如何实现该功能，但实际上并不要求首先实现它！我们希望原始设备制造商不会禁用这个漂亮的功能，但我们没有办法知道他们是否禁用了它，直到他们准备好推出他们自己的基于 Android 11 的 Android 版本，这要到几个月后才会发生。

### 提议的第 3.8.16 节(新)-装置控制(2020 年 5 月 20 日更新)

**3.8.16 设备控制**

Android 包括 ControlsProviderService 和 Control APIs，允许开发人员发布设备控件，以便为用户提供快速状态和操作。

**3.8.16.1 设备控制用户可见性**

如果设备实施设备控制，则它们:

*   [C-1-1]必须报告 Android . software . controls . feature 标志为真
*   [C-1-2]必须通过 Android . service . controls . controls providerservice 和 Android . service . controls . control API，为用户提供能够从第三方应用程序注册的控件中添加、编辑、选择和操作用户收藏夹的功能。
*   [C-1-3]必须在启动器的三次交互内提供对该用户启示的访问
*   [C-1-4]必须在此用户启示中准确呈现通过 Android . service . controls . controls providerservice API 提供控件的每个第三方应用程序的名称和图标，以及 Android . service . controls . controls API 提供的任何指定图标、状态文本、设备类型、名称、结构、区域、自定义颜色和副标题

相反，如果设备实现不实现这样的控制，那么它们

*   [C-2-1]必须为 ControlsProviderService 和控制 API 报告 Null。

**通知中的对话**

 <picture>![](img/4cca62f628c5a1d2bc1ff607e87e3247.png)</picture> 

Conversations in Android 11\. Source: Google

与 iOS 相比，Android 的最大优势之一是前者处理通知的方式。随着“对话”的引入，这种可用性差距在 Android 11 中将会变得更大。在 Android 11 中，来自消息应用的通知被分组在一起，并显示在通知面板中的独立部分，位于大多数其他通知的上方。这使您可以快速查看和回复邮件，而不必滚动浏览所有其他待处理的通知。不幸的是，这种通知的巧妙变化可能并不适用于所有设备。谷歌让原始设备制造商选择他们是否想要“在非对话通知之前分组并显示对话通知。”原始设备制造商经常定制通知面板，所以谷歌在这里给原始设备制造商一个选择也就不足为奇了。尽管如此，令人遗憾的是，谷歌没有选择在 Android 11 中加强通知的一致性。

### 对 3.8.3.1 部分-通知提交的拟议更改(2020 年 8 月 4 日更新)

如果设备实现允许第三方应用通知用户值得注意的事件，它们:

...

Android R 引入了对对话通知的支持，这是一种使用 NotificationManager 的通知。MessageStyle 并提供已发布人员的快捷方式 ID。

设备实现包括:

*   [H-SR]强烈建议在非对话通知之前对对话通知进行分组和显示，但正在进行的前台服务通知和重要性:高通知除外。

如果对话通知被分组到单独的部分，设备实现

*   [H-1-8]必须在非对话通知之前显示对话通知，但正在进行的前台服务通知和重要性:高通知除外。

设备实现包括:

*   [H-SR]强烈建议从对话通知中提供对以下操作的访问:如果应用程序提供气泡所需的数据，则将此对话显示为气泡

AOSP 实现通过默认的系统 UI、设置和启动程序来满足这些要求。

**身份证-移动驾照**

最后，我最感兴趣的特性之一是 IdentityCredential API。[正如我们去年详细介绍的](https://www.xda-developers.com/google-android-digital-drivers-license/)，IdentityCredential API 旨在允许应用程序在设备上存储身份文档，如移动驾驶执照。世界上有几个国家(和美国的一些州)已经允许他们的公民将驾照存储在移动应用程序中。然而，谷歌正在努力通过将数据离线存储在安全的环境中来提高安全性。

 <picture>![](img/d43ba2ce0cf0045d9b35518d04325b52.png)</picture> 

A sample image of a digital driver's license accessed through the LA Wallet app. Source: Envoc

Android 11 的源代码包括 IdentityCredential API(开发者将调用该 API 在手机的安全环境中存储身份文档)和 IdentityCredential HAL(与手机的安全环境接口)，但 OEM 厂商不需要实现它们。当谷歌于 2020 年 1 月 10 日首次提出将 IdentityCredential 纳入 CDD 时，他们将其列为一项要求。然而，他们在 2020 年 3 月 18 日放宽了这一要求，现在只强烈建议 OEM 厂商支持这一功能。我们对 Google 放松这一要求并不感到惊讶——添加影响可信执行环境的更改将需要原始设备制造商的努力来实现。原始设备制造商可能只是需要更多的时间来为这一变化做准备。然而，对于用户来说，这意味着不能保证你的特定 Android 11 智能手机将支持在手机的安全环境中安全存储移动驾照。

我们应该注意到，没有技术限制阻止在 Android 11 设备中广泛采用 IdentityCredential 系统。实现身份认证系统的要求之一是设备具有可信执行环境(TEE)或专用安全处理器，其中“可信应用程序”与存储的身份文档进行交互。自 Android 7.0 Nougat 以来，谷歌要求所有现代 Android 设备支持“隔离执行环境”(根据[第 2.2.5 节-CDD 的安全模型](https://source.android.com/compatibility/android-cdd#2_2_5_security_model))。配备 ARM 处理器的设备通常采用 ARM 的 [TrustZone](https://developer.arm.com/ip-products/security-ip/trustzone) TEE，谷歌提供运行在 TrustZone 上的 [Trusty OS](https://source.android.com/security/trusty) 。TEE 的存在足以支持身份认证系统，尽管如果证书存储在嵌入式安全 CPU(如一些高通骁龙处理器的[安全处理单元)或分立的安全 CPU(如](https://www.xda-developers.com/qualcomm-snapdragon-865-spu-dual-sim-dual-standby-drivers-licenses-android-11/)[谷歌的 Titan M](https://www.xda-developers.com/google-pixel-3-titan-m-security/) 或[三星的新安全芯片](https://www.xda-developers.com/samsung-sell-galaxy-s20-hardware-security-chip/))中会更安全。值得注意的是，具有分立安全 CPU 的设备也能够支持 IdentityCredential 系统的“直接访问模式”功能，这将允许用户即使在设备剩余电量不足以启动主操作系统的情况下也能调出他们的身份文档。

### 提议的第 9.11.3 节(新)-身份证明(2020 年 3 月 18 日更新)

身份凭证系统允许应用程序开发人员存储和检索用户身份文档。

设备实现:

*   强烈建议[C-SR]实施身份凭证系统。

如果设备实现实现了身份凭证系统，则它们:

*   [C-0-1]必须为[IdentityCredentialStore # getInstance()](https://developer.android.com/reference/android/security/identity/IdentityCredentialStore#getInstance%28android.content.Context%29)方法返回非空值。
*   [C-0-2]必须使用代码实现“Android . security . identity . *”API，以便与在可信执行环境(TEE)或专用安全处理器上运行的可信应用程序进行通信。必须实现可信应用，使得身份凭证系统的[可信计算基础](https://en.wikipedia.org/wiki/Trusted_computing_base)不包括 Android 操作系统。

谷歌还在开发 IdentityCredential Jetpack 库，以使开发者更容易在 Android 上添加对安全存储身份文档的支持，但真正的挑战将是让政府授权应用程序使用该 API 来安全存储政府 id。据 [*Engadget*](https://www.engadget.com/south-koreans-can-now-store-their-driving-license-on-their-smartphones-094503272.html) 报道，韩国刚刚推出了在手机应用程序中存储驾照的支持，因此我们开始看到这项技术的接受度有所上升。就我个人而言，我很期待看到这一天的到来，因为这意味着我出门时可以少带一样东西。

* * *

我们获得的文件列出了 CDD 的变更日期。最新的更改是在 2020 年 6 月 10 日进行的，这意味着我们拥有的文档是最新的。谷歌可能会食言，在 Android 11 公开发布之前再次提出所有要求，但我们怀疑谷歌会突然让 CDD 变得更加严格。由于原始设备制造商的反馈，这些变化可能会放松，如果他们还没有计划这样做，他们将不得不回去实现这些功能。这需要时间、精力和金钱，这只会进一步推迟面向非谷歌设备的 Android 11 的发布。尽管如此，如果谷歌确实再次要求这些功能，我们将在 XDA 门户网站上发布更新。