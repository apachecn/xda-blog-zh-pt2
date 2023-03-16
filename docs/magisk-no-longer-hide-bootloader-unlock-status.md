# Magisk 可能不再能够隐藏应用程序的引导加载程序解锁

> 原文：<https://www.xda-developers.com/magisk-no-longer-hide-bootloader-unlock-status/>

XDA 公认的开发者 topjohnwu 的“Magisk”项目在 Android 社区中基本上已经成为了“root”的同义词。它如此受欢迎的一个主要原因是因为它可以隐藏用户已经修改了他们的设备的事实。然而，谷歌可能正在打击 Magisk 向应用程序隐藏引导加载程序解锁状态的能力。

为了根你的手机，你通常需要解锁引导加载程序，这允许你刷新修改后的引导镜像。这是必需的，因为 Magisk 修改引导映像来欺骗引导加载程序状态和/或验证的引导状态检查。Google 的 SafetyNet 认证 API 是 Google Play 服务的一部分，用于告诉应用程序它是否在被篡改的设备上运行；如果 SafetyNet API 检测到引导加载程序已经解锁，那么它将返回“基本完整性”检查的失败状态。然后，未通过该检查的设备可以被使用 SafetyNet API 来确定设备完整性的应用锁定；这类应用通常包括银行应用、支付应用(如 Google Pay)和许多在线游戏(如 Pokémon Go)。然而，由于 SafetyNet API 迄今为止仅使用软件检查来确定设备是否被篡改，Magisk 可以简单地欺骗引导加载程序和/或验证的引导状态，因为它安装在较低的级别，并且具有比 Google Play 服务和其他用户空间应用程序更高的权限。正如 topjohnwu 解释的那样，MagiskHide“为检测过程创造了一个隔离的‘安全环境’，它通过谷歌的 API 创造了一个不反映设备真实状态的*合法*安全网结果。”

不过最近，用户已经注意到他们的引导程序解锁的设备没有通过 SafetyNet 的基本完整性检查，即使他们使用 Magisk 来修补引导映像。根据 topjohnwu 的说法，这是因为谷歌可能已经实现了硬件级的密钥证明，以验证启动映像没有被篡改。具体来说，这意味着 Google Play 服务“[发送]未修改的密钥库证书到 SafetyNet 服务器，验证其合法性，并检查证书扩展数据以了解您的设备是否[已]验证启动启用(引导加载程序状态)。”这意味着可能无法再隐藏 bootloader 已经解锁的事实，这将导致 Google Pay 和 Pokémon Go 等应用无法正常运行。

正如 topjohnwu 指出的，安全网检查引导加载程序解锁状态的方式的这种变化来自于对 Google Play 服务中包含的安全网 API 的服务器端更新。然而，并不是每个用户都无法通过这些更新的安全网检查，因此新的硬件级密钥证明可能还没有广泛实施。

我们一次又一次地看到 topjohnwu 克服技术障碍。谷歌经常在 SafetyNet 中推出新的检查，然后 topjohnwu 在 Magisk 中发现并绕过这些检查。Android 的每一个新版本都会带来分区结构或者引导镜像的改变，需要 topjohnwu 去研究这些改变，然后实现新的打补丁方法。然而，即使是 topjohnwu 这次也可能很难找到一个旁路。

这是因为这一次的解决方法将涉及入侵设备的可信执行环境(TEE)固件以检索私钥。然而，这很难做到，因为它需要找到固件中的漏洞，而固件的设计是非常安全的。事实上，如果发现这样的漏洞，许多公司会支付数十万美元。例如，谷歌为 Pixel 可信执行环境中的远程代码执行漏洞支付 25 万美元，为 [Titan M](https://www.xda-developers.com/google-pixel-3-titan-m-security/) 安全芯片中的漏洞支付[高达 100 万美元](https://www.xda-developers.com/google-pays-1-5-million-titan-m-security-vulnerabilities-pixel/)。即使私钥以某种方式被泄露，它也不太可能有多大用处，因为[谷歌可以远程撤销密钥](https://twitter.com/shawnwillden/status/1237836365238337536)，所以它不能用于验证设备的完整性。

一旦 SafetyNet 广泛实施硬件级密钥证明，大多数运行 Android 8.0 Oreo 或更高版本的解锁引导加载程序的设备将无法通过 SafetyNet 的基本完整性检查。这是因为所有使用 Android 8.0 Oreo 或更高版本的设备都需要在 TEE 中实现硬件密钥库。如今，某些设备甚至具有专用的硬件安全模块(HSM ),通过将 TEE 从主处理器移开，使得开发更加困难；Pixel 4 中的 Titan M 和 Galaxy S20 中的三星新安全芯片就是这方面的例子。

Topjohnwu [还解释说](https://twitter.com/topjohnwu/status/1237830555523149824)其他潜在的变通办法要么是不可能的，要么极具挑战性。使用 Xposed 框架来修改 Google Play 服务中的安全网证明 API 可能不会起作用，因为“适当的安全网检查将在远程服务器上验证结果，而不是在可由代码注入框架操纵的设备上验证结果。”此外，Google Play 服务是高度模糊的，这使得创建这样一个 Xposed 模块首先变得非常困难。伪造安全网的测试结果也是不可行的，因为安全网的响应“来自谷歌服务器，并用谷歌的私钥签名。”

几年来，谷歌已经有能力使用硬件支持的密钥认证来加强安全网检查。事实上，他们三年来没有这样做，这使得用户可以享受 root 和 Magisk 模块，而不会牺牲使用银行应用程序的能力。然而，似乎 Magisk 有效隐藏 bootloader 解锁状态的能力很快就要结束了。这是一个我们期待多年的变化，但我们很难过地看到它最终付诸实施。我们希望谷歌更新安全网证明 API，以返回状态检查是否使用了基于硬件的证明，因为这将允许应用程序开发人员决定他们是否要阻止所有解锁引导加载程序的用户。

* * *

*感谢丹尼尔·迈凯(@ [丹尼尔·迈凯](https://twitter.com/DanielMicay))对此事的投入！*