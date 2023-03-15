# 微软的“金钥匙”泄漏允许禁用安全引导

> 原文：<https://www.xda-developers.com/microsofts-debug-mode-flaw-and-golden-key-leak-allows-disabling-of-secure-boot/>

基于 Windows 的操作系统不再是移动领域的默认和首选。Android 的开源特性在原始设备制造商中找到了许多粉丝，因此，现在越来越少的手机使用 Windows。

但是如果你是那些仍然在日常生活中使用 Windows 设备的人之一，那么有一个好消息要告诉你。好还是坏，这将取决于你的立场和对这条新闻用例的解释。

据 [Ars Technica](http://arstechnica.com/security/2016/08/microsoft-secure-boot-firmware-snafu-leaks-golden-key/) 和 [TheRegister](http://www.theregister.co.uk/2016/08/10/microsoft_secure_boot_ms16_100/) 报道，来自[网站的消息可能会让你头疼](https://rol.im/securegoldenkeyboot/)(不是开玩笑)，一些开发人员( [@never_released](https://twitter.com/never_released) 和 [@TheWack0lian](https://twitter.com/TheWack0lian) )发现，微软为了调试目的而植入的一个后门打开了禁用 Windows 设备安全引导的可能性。

## 安全引导和它是什么？

当您第一次启动 Windows 设备时，启动过程会按以下顺序进行:UEFI(统一可扩展固件接口，它是 BIOS 的替代品)->启动管理器-->启动加载程序--> Windows。UEFI 是安全引导功能存在的地方。顾名思义，安全引导，旨在通过在接下来的步骤中要求数字签名来提高安全性。本质上，如果引导程序没有使用 UEFI 期望的密钥进行签名，引导设备的过程将不会完成。

安全引导是一个可选功能，但微软已经强制启用它，以便从 Windows 8 及更高版本获得 Windows 认证。这里的理由是，安全引导将使恶意软件作者难以将代码插入引导过程。然而，安全引导的一个副作用是，它使 Windows 机器上的双重引导变得有点复杂，因为第二个操作系统及其所有先决条件也需要进行数字签名，或者需要禁用安全引导。还有很多其他的问题，经验丰富的双重启动者会比我在一个段落中解释的更多。

现在，有一些设备上的安全引导不能被用户禁用，即使他们想禁用。在这个领域，我们的主题从所有 Windows 设备(包括台式机)大幅缩小到特定的 Windows 设备，如 Windows Phone 设备、Windows RT 设备、一些 Surface 设备甚至 HoloLens。这些最终用户设备在上锁定了**安全引导，这意味着**最终用户不能修改或禁用与安全引导**相关的方面，进而，他们不能以未经微软授权的方式接触操作系统。**

但是为了正在进行的官方开发，安全引导需要放松一点。在锁定了安全引导的设备上，存在安全引导策略，它可以帮助授权开发，而无需禁用安全引导。正如研究用户提到的，这个安全引导策略文件是由引导管理器在 windows 引导过程的早期加载的。策略文件还可以包含注册表规则，这些规则进而能够包含策略本身的配置等。同样，策略文件必须经过签名，并且存在其他规定，以确保只有 Microsoft 可以提供这些更改。

签名元素还依赖于在应用时使用的 DeviceID。我会让博文在这里解释，因为有几个部分我不太清楚:

*还有，有一种东西叫 DeviceID。这是一些 UEFI PRNG 输出的加盐 SHA-256 散列的前 64 位。在 Windows Phone 和 Windows RT 上应用策略时使用它(mobilestartup 在 Phone 上设置它，在 RT 上第一次启动时使用 SecureBootDebug.efi)。* *在手机上，策略必须位于 EFIESP 分区的特定位置，文件名包括十六进制格式的 DeviceID。(在 Redstone 中，这被更改为 UnlockID，由 bootmgr 设置，只是 UEFI PRNG 的原始输出)。*

*基本上，bootmgr 会在加载时检查策略，如果策略包含的 DeviceID 与运行 bootmgr 的设备的 DeviceID 不匹配，则策略将无法加载。任何允许启用 testsigning 的策略(MS 称这些零售设备解锁/ RDU 策略，安装它们就是解锁设备)都应该被锁定到 DeviceID(在 Redstone 和更高版本上为 UnlockID)。事实上，我有几个类似的策略(由 Windows Phone 产品证书签名)，唯一的区别是包含的 DeviceID 和签名。如果没有安装有效的策略，bootmgr 将使用位于其资源中的默认策略。该策略使用 BCD 规则阻止启用测试签名等。*

这是事情变得有趣的部分。在 Windows 10 v1607 的开发过程中，微软创建了一种新型的安全引导策略(为了简洁起见，以下简称为 SBP ),用于内部测试和调试。该策略本质上是“补充性的”,没有 DeviceID，它会将其设置合并到现有的引导策略中。引导管理器加载旧类型的 SBP，然后验证其签名和真实性，然后加载这些补充引导策略。这里的问题是没有进一步核实补充政策本身。此外，早于 Windows 10 v1511 的引导管理器不知道这些策略的补充性质的存在，因此，的反应就好像它们加载了完全有效且已签名的策略。同样，这种行为很可能是内部开发，所以开发人员不应该签署每一个操作系统版本和他们必须在设备上做的微小变化。

这个 SBP 被称为“金钥匙”,因为它基本上取消了签名检查的目的。这款 SBP 无意中被装在零售设备上，尽管处于停用状态。开发者发现了这个 SBP，并公布了他们的发现。现在，SBP 可以在互联网上到处浮动，这个特殊的 zip 被用来在 Windows RT 设备上安装 SBP。

## 这是什么意思？

如果您加载了补充 SBP，则可以启用 Windows 的测试签名，以允许您加载未签名的驱动程序。此外，由于这些策略在引导过程中的引导管理器阶段之前发挥作用，您可能会危及整个订单的安全性并运行未经授权的(读取自签名)代码。这为打算未经授权修改 Windows 部分内容的用户和恶意软件创建者打开了许多可能性。

这一发现的作者关注的是整个惨败的讽刺性。微软在某些设备上锁定了安全引导，以防止未经授权的更改，但随后建立了一个后门，让他们继续开发和调试。但是这个后门为所有运行 Windows 的设备禁用安全引导铺平了道路，使得整个考验毫无意义。

现在，不仅愿意的用户可以在只安装 Windows 的平板电脑和手机上安装 Linux 发行版(可能还有 Android ),不愿意的用户也可以安装恶意的 bootkits，如果他们破坏了对设备的物理访问的话。虽然前者是我们可以在空中跳起来的东西，但后者并没有真正灌输很多信心。这是双向的，它向我们展示了为什么安全是一把双刃剑。此外，SBP 本质上是通用的，允许其在任何设备上使用，而不管其架构如何。它对于那些安全引导可以被轻易关闭的台式机来说并不是特别有用，但是对于那些不能乱用安全引导的设备来说，它有着巨大的作用。

## 那么，解决办法是什么？

微软确实发布了一些补丁，但是开发者坚持说这个问题还没有完全解决。你可以查看这些补丁( [MS16-094](https://technet.microsoft.com/en-us/library/security/ms16-094.aspx) 和 [MS16-100](https://technet.microsoft.com/en-us/library/security/ms16-100.aspx) )，然后在[的博客文章](https://rol.im/securegoldenkeyboot/)上阅读为什么它们不能解决这个问题。如果他们是正确的，这个问题看不到修复或补丁，尽管这不会阻止微软试图在路上设置更多的路障。

## 接下来呢？

有一个可能性的世界，其中一些正在我们的 Windows 论坛上酝酿。你可以查看我们关于 [Windows Phone 8 开发和黑客攻击](http://forum.xda-developers.com/windows-phone-8)的论坛，以及我们关于 [Windows 8、Windows RT 和 Surface 开发和黑客攻击](http://forum.xda-developers.com/windows-8-rt)的论坛。你还可以找到一些设备的[指令线程](http://forum.xda-developers.com/windows-8-rt/rt-development/easiest-windows-rt-umci-unlockjailbreak-t3435701)，其他用户也在讨论同样的问题。

* * *

这个调试后门的存在和 SBP 的泄露不仅对锁定 Windows 设备的第三方开发很重要，它们还向我们展示了一个严峻的提醒，如果故意留下后门会发生什么。最近对安全的关注已经转向调查机构，他们迫切要求利用这种后门来帮助他们的合法调查目的。但是这些方法**迟早会**落入坏人之手。本来是用来打击犯罪和伸张正义的工具，有一天会变成犯罪本身的工具。

你对调试 SBP 的泄露有什么看法？你觉得像这样的“金钥匙”应该存在吗？请在下面的评论中告诉我们！