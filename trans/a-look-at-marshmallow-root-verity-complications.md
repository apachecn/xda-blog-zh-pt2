# 看看棉花糖根和 Verity 复杂功能

> 原文：<https://www.xda-developers.com/a-look-at-marshmallow-root-verity-complications/>

随着 Android 6.0 版本的尘埃落定，Nexus 的大量用户正在寻找 OTA 和 T2 工厂图片，并为 Android 操作系统的最新版本做准备。

虽然从外表上看，Android 6.0 似乎(至少在视觉上)与 Android 5.0 和 5.1(棒棒糖版本)非常相似，但在内部的*上有许多重大变化。其中一个可能会对定制 ROM 和根社区产生**影响**。首先，一点背景。如果你对此不感兴趣，直接跳到“为什么这很重要”。*

### 名为 Verity 的功能

这个问题(如果你喜欢 root 和修改设备的话，这是一个问题)源于我很久以前指出的一件事，当它第一次袭击 AOSP 的时候——将 [dm-verity 引入 Android](http://www.xda-developers.com/google-taking-aim-at-device-modders-in-android-4-4-kitkat/) 。Verity 是一种安全功能，最初出现在 ChromeOS 中，旨在提供放心可信的计算设备，防止恶意软件修改设备。回到 Android 4.4，谷歌宣布了 Android 的 verity，然后一切都保持安静。虽然有一些关于使用 verity 的[研究，但在很大程度上，事情一直很平静。直到现在，那是。](http://nelenkov.blogspot.co.uk/2014/05/using-kitkat-verified-boot.html)

随着 Android 6.0 的推出，谷歌已经开始在设备安全方面加大投入。其中一个基本要求是防止设备上的软件在用户不知情的情况下被修改——虽然 XDA 的许多人认为 root 是理所当然的，但想象一下用户的设备在他们不知情或未同意的情况下被 root，root 访问被用来窃取他们的数据。为此，谷歌已经开始在一些设备上实现系统分区的验证。他们最近也更新了他们的[支持页面](https://support.google.com/nexus/answer/6185381)来解决这个问题。

### 这对 Rooted 用户意味着什么？

有了 verity，**对系统分区的任何更改都将在引导或访问时被检测到**。然后，您将面临上面看到的一个错误。有些允许您继续，有些希望通过阻止设备启动来保护您。有三种状态可用。一个是当引导加载程序解锁时显示，表明您可能有危险，直到您重新锁定引导加载程序。这是因为修改后的内核映像可以绕过 verity，因为内核 ramdisk 包含用于验证系统状态的密钥。

> 对于锁定设备上渴望根用户来说，事情看起来相当无趣。

当 verity 被禁用或关闭时，或者由于对 ramdisk 的修改而无法检查时，会显示下一个状态。我不能确定，因为我没有 Nexus 5X 或 6P 来调查，但我怀疑(根据消息)如果你加载另一个 ROM，然后将它自己的内核放到设备上，就会出现“不同的操作系统”页面。

最后一种状态是红色警告，表示设备已损坏。我怀疑这意味着图像包含验证，但由于系统图像被修改，验证失败。同样，如果没有硬件在手，我们也不能确定，但是如果一个库存设备被恶意软件修改了，你就会看到这个错误。

### 为什么这很重要？

在 Android M (6.0)上，除了文件系统之外，root 当前还需要修改内核映像。这意味着，即使我们忽略 verity(例如在旧的 Nexus 设备上，如 [Nexus 7 2013](http://forum.xda-developers.com/nexus-7-2013) )，也需要一个新的内核映像，以绕过阻止 root 访问工作的 SELinux 保护。

如果你现在想在 Android Marshmallow 上使用 root，你需要使用一个修改过的引导镜像。

到目前为止，已经有[个修改过的内核](http://forum.xda-developers.com/showpost.php?p=63158038&postcount=210)将 SELinux 设置为许可模式，但这并不是一个理想的修复，因为这意味着你无法获得 SELinux 保护的安全优势。而且，在经历了[的舞台恐惧](http://www.xda-developers.com/stagefright-explained-the-exploit-that-changed-android/) [的传奇](http://www.xda-developers.com/a-demonstration-of-stagefright-like-mistakes/)之后，我想你可以看到 SELinux 和其他针对安全漏洞的保护措施的好处。

XDA 资深公认开发者， [Chainfire](http://forum.xda-developers.com/member.php?u=631273) ，万物根的主人发布了一个[SuperSU](http://forum.xda-developers.com/apps/supersu/wip-android-6-0-marshmellow-t3219344)的更新版本，它保留了强制模式下的 SELinux，但是它再次要求对引导镜像的 SELinux 配置进行修改。这意味着您需要安装 SuperSU，以及修改后的引导映像。

这一切都很好，直到美国运营商加入进来。众所周知，反消费者选择的堡垒，像 AT & T 和威瑞森这样的中坚分子喜欢锁定设备，阻止用户通过他们的引导装载锁安装定制固件。事实上，威瑞森甚至不擅长将固件更新传递给用户，索尼 Xperia Z3v [没有设置接收棉花糖](http://forum.xda-developers.com/z3/xperia-z3v-general/kick-teeth-t3219177)，而 Z3 系列的其余产品(实际上还有 Z2 系列)会。见鬼，他们甚至还没有在这款设备上推出棒棒糖，尽管它已经在普通 Z3 上[上市很长时间了](http://www.xda-developers.com/lollipop-finally-lands-on-the-xperia-z3/)(2014 年 11 月)。

代替非官方的引导加载程序解锁(这些在最近相当罕见，除了泄露的一些三星设备的工程引导加载程序)，如果没有一些神的干预，你似乎不太可能在 Android 6.0 上获得 root——DM-verity(阻止你的手机在对系统分区进行任何修改的情况下启动)和 ramdisk 中 SELinux 更改的要求(让 root 工作)的结合，看起来会让这些锁定设备的渴望 root 的用户变得相当无趣。

### 安卓平板电脑

最后，Android Pay。这听起来可能与本文的其余部分完全无关，但实际上却非常相关。Android Pay 依赖于谷歌专有服务框架内的新[safety net API](https://developers.google.com/android/reference/com/google/android/gms/safetynet/SafetyNet)，该框架旨在提供设备状态证明，说明设备是否是根设备，或者是否被修改或在未经批准的状态下运行。

虽然有一个[项目](https://github.com/pylerSM/NoDeviceCheck)正在研究对 SafetyNet 的欺骗响应，但它目前需要一个 Xposed 插件，鉴于它的工作方式，这看起来不太可能改变。Xposed 需要 root，并对系统分区进行修改。这使得在锁定引导程序的设备上很难实现这一点。即便如此，这类事情也只是进入了谷歌的猫捉老鼠游戏。使用 SafetyNet，根设备(或者实际上是被修改的设备)被视为“不符合 CTS”，这是被修改设备的委婉说法。

在这篇关于安全网[的博客文章](https://koz.io/inside-safetynet/)中，有更多关于安全网的内容，但我们似乎可以确定谷歌想要取缔的一些领域。首先，他们不喜欢 root、Xposed 和任何修改系统分区的东西。其次，谷歌似乎正在考虑检测启用了广告拦截的用户——`pubads.g.doubleclick.net`上的 SSL 握手检查无疑向我暗示，谷歌想知道你是否在你的设备上拦截广告。考虑到 root 通常是一个先决条件，但 VPN API 可能会在没有 root 的情况下被用来做这件事，看起来谷歌至少想知道谁(或多少人)在屏蔽广告。鉴于苹果推动在网络浏览器中支持广告屏蔽，广告屏蔽是一个热门话题(可以说是为了鼓励人们更多地使用应用程序，他们可以控制体验，并提供不可屏蔽的广告)，这些举措很有趣。

## 结论

如果你现在想在 Android Marshmallow (6.0)上使用 root，你需要使用一个修改过的引导镜像。虽然这种情况是否会无限期地保持下去还有待观察，但看起来有可能是这样——SELinux 的变化使得在不修改引导映像的情况下获得 root 访问权限变得更加困难。由于修改引导映像需要解锁的引导加载程序，这可能会终止设备上的 root(以及 Xposed 和其他 root 功能),这些设备附带了最终用户无法解锁的引导加载程序。Dm-verity 也在亮相，它似乎在新设备上以强制模式启用。这将使修改/system 变得很困难，即使你获得了根用户权限，也不会再有一个解锁的引导装载程序。

这是否会改变你对锁定引导程序设备的看法？Android 是否已经到了这样一个阶段:如果你的运营商给你一个好价钱、**，你仍然会购买一个锁定了引导程序的设备，或者你只对解锁的设备感兴趣？在锁定的引导加载程序上，你会错过哪些根应用程序或功能？**

欢迎在下面的评论中分享你的想法。