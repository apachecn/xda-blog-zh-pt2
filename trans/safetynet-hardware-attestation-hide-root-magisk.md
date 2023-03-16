# 安全网的硬件认证将使隐藏 Magisk 中的根变得非常困难

> 原文：<https://www.xda-developers.com/safetynet-hardware-attestation-hide-root-magisk/>

早在三月份，一些安装了 Magisk 的用户[注意到](https://www.xda-developers.com/magisk-no-longer-hide-bootloader-unlock-status/)他们的设备没有通过安全网认证。这一消息令 XDA 的社区感到不安，因为这意味着许多重要的银行/金融应用程序和流行游戏，如 Pokémon Go 和 Fate/Grand Order，拒绝在根设备上运行。一段时间以来，SafetyNet 中收紧的限制似乎被收回了，只是在过去几周内又向少数用户推出了。然而，谷歌在 5 月初悄悄证实，他们正在测试硬件支持的 SafetyNet 响应证明，这使得 Magisk 无法隐藏 3 月份的引导加载程序解锁状态。如果这一变化广泛展开，这将意味着用户将不得不在访问根/自定义 ROMs 内核/等之间做出选择。或者他们喜欢的银行应用和游戏。Android 对高级用户的最大吸引力之一可能很快就会消失。

为了概括这一系列事件，我们应该首先谈谈安全网本身。SafetyNet 是 Google Play 服务中的一组 API。SafetyNet 证明 API 就是这些 API 中的一种，它可以被第三方应用程序调用，以检查设备的软件环境是否被以任何方式篡改。API 检查各种东西，比如超级用户二进制文件的标志、引导加载程序解锁状态等等。当你用 Magisk 给一个设备根时，它“为[安全网]检测过程[创建]了一个隔离的'安全环境'，它通过谷歌的 API 创建了一个不反映设备真实状态的*合法*安全网结果，”XDA 资深公认开发人员 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 说。这允许用户根他们的电话，同时确保 API 对于任何引导装载器解锁检查总是返回“假”。这种绕过 SafetyNet 的引导加载程序解锁检测的方法在过去几年里一直适用于 Magisk，但这只是因为谷歌推迟了使用硬件证明验证引导映像的完整性。今年 3 月，谷歌似乎终于开始在 SafetyNet 中采用硬件认证来验证启动映像，但我们从未从谷歌获得官方声明来确认这一变化，只有少数用户受到影响。然而，正如 XDA 资深成员 [Displax](https://forum.xda-developers.com/member.php?u=6345368) 所指出的，谷歌在 2020 年 5 月 5 日确认，来自一些设备的安全网认证 API 响应现在包括硬件支持的检查。

在“安全网 API 客户端”的 Google 小组上，Google 详细介绍了认证 API 的一个新特性:evaluationType。来自某些设备的 JSON Web 签名(JWS)响应将具有一个名为“evaluationType”的字段，该字段“将为开发人员提供对每个单独的安全网证明 API 响应有贡献的信号/测量类型的洞察”该字段中支持的令牌之一是“HARDWARE_BACKED ”,其指示 API“使用了远程设备的可用硬件支持的安全特征(例如，[硬件支持的密钥证明](https://developer.android.com/training/articles/security-key-attestation))来影响[其]评估。”谷歌表示，他们“目前正在评估和调整设备的资格标准，我们将依赖硬件支持的安全功能。”这意味着，在一些设备上，Google Play 服务现在使用硬件支持的证明来检测设备的软件是否被篡改。谷歌没有在谷歌集团的公告之外正式记录这一变化，所以一些使用 SafetyNet 的开发人员可能不知道这一变化(因此还没有检查 JWS 响应中的“HARDWARE_BACKED”字段。)然而，对于那些正在检查这一领域的应用程序，现在没有办法对他们隐藏 root 访问权限，只要你的设备是谷歌正在进行的测试的一部分。

根据 topjohnwu 的说法，硬件支持的证明意味着 Google Play 服务现在“向 SafetyNet 服务器[发送]未经修改的密钥库证书，[验证]其合法性，并[检查]证书扩展数据，以了解您的设备是否[已]验证启动启用(引导加载程序状态)。”由于密钥库证书所源自的私钥是由电话的隔离安全环境支持的，因此检索它们将涉及破坏电话的可信执行环境(TEE)或专用硬件安全模块(HSM)的安全性。如果有人以某种方式泄露了私钥，一旦谷歌发现，[密钥将很快被撤销](https://twitter.com/shawnwillden/status/1237836365238337536)。谷歌为任何影响 Pixel 手机 TEE 的关键安全漏洞提供了数十万美元的奖励，这只是表明这不太可能成为绕过引导加载程序解锁检测的潜在途径。

Magisk 可以继续欺骗引导加载程序解锁状态的另一个潜在方法是修改 SafetyNet 的客户端代码，使其始终使用基本评估。然而，正如 topjohnwu 指出的那样，这需要通过类似 Xposed 框架的挂钩框架将定制代码注入到 Google Play 服务中。这不仅很难做到，因为 Google Play 服务非常混乱，而且也不可能隐藏，因为“一些内存空间分析将非常容易地揭示代码操纵。”此外，这也只有在谷歌的服务器继续接受基本评估，并且在支持硬件的设备上不强制执行硬件支持的评估的情况下才有效。(根据 topjohnwu 的说法，安全网的响应“[来自]谷歌服务器，并用谷歌的私钥签名”，因此实际的响应不可能是欺骗的。)

自 Android 7 Nougat 以来，谷歌要求所有设备都有一个隔离的安全环境，这意味着 SafetyNet 如何验证引导加载程序解锁的这一变化将影响大多数设备。由于没有隔离安全环境的旧设备显然无法执行硬件支持的证明，Magisk 仍将能够隐藏这些设备上的 root 访问。但如果这一变化大范围展开，其他人将不得不在 root 访问和银行应用之间做出艰难的选择。

不幸的是，可能有很多应用程序在不需要的时候使用安全网检查。topjohnwu 引用的一个例子是麦当劳的官方应用程序，它似乎拒绝在 bootloader 解锁的设备上运行。在 Twitter 上，topjohnwu 指出过度使用 API 的应用程序为高级用户创造了一个充满敌意的环境。XDA 认可的开发人员 Quinny899 讲述了他的团队如何考虑使用 SafetyNet 来检查设备安全状态的轶事。他们最终决定不这么做，因为他的团队的应用程序会加密所有敏感数据。他认为，安全网不应该用来代替适当的安全和数据处理实践，尤其是考虑到超级用户利用的[可能性。](https://www.xda-developers.com/mediatek-su-rootkit-exploit/)

有关新的安全网变化如何影响 Magisk 的更多信息，请查看 topjohnwu 在 Twitter 上的[精彩 FAQ。如果你只是想检查你的设备是否是谷歌新安全网测试的一部分，那么你可以遵循 XDA 高级会员 Displax 的](https://twitter.com/topjohnwu/status/1237830555523149824)[这个指南](https://forum.xda-developers.com/showpost.php?p=82935207&postcount=40370)或者下载最新的 Magisk Manager 版本。

* * *

*本文更新于美国东部时间 2020 年 6 月 30 日上午 10:46，更正谷歌只对 Pixel 手机中发现的 TEE 漏洞进行悬赏。此外，添加了有关最新 Magisk Manager 版本的详细信息，该版本现在显示内置 SafetyNet checker 中的 evaluationType 字段。*