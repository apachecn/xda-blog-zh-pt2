# 我给我的三星 Galaxy Note 20 Ultra 加了根——以下是我这么做的原因

> 原文：<https://www.xda-developers.com/samsung-galaxy-note-20-ultra-root-us-unlocked-snapdragon-865/>

这是 XDA 开发人员，与普遍的看法相反，我们实际上谈论了许多关于开发的东西。这篇文章与更多的新闻或教程相关的内容略有不同。在此，我谈谈我对 root 及其 2020 年效用的看法，并向你展示我的 root[三星 Galaxy Note 20 Ultra](https://www.xda-developers.com/samsung-galaxy-note-20/) 。如果你想的话，底部可能还会有一个链接指向如何给你自己的 US Galaxy 加根的说明，但是你必须保证阅读整篇文章。答应吗？平奇-发誓？好的，很好。

## 历史

回到 2018 年，我买了 [Galaxy Note 9](https://www.xda-developers.com/samsung-galaxy-note-9-september-2020-security-update-rolling-out/) 。但不是任何一部 Galaxy Note 9。我通过易贝进口了 Exynos 变种。我为什么要做这种事？有两个主要原因。美国的颜色有点无聊。我真的想要铜色。美国版本也不能解锁引导程序，我喜欢 root 访问。额外的好处:在那个时候，它比美国的版本要便宜得多。

我有 T-Mobile，所以拥有一部国际三星手机并不可怕。波段支持不完整(没有 LTE Band 71)，但 WiFi 通话和 VoLTE 工作正常。我有根，所以对我来说这是一个值得的交换。主要问题是动力不足和效率低下的 Exynos 处理器，以及缺乏保修。

快进到 2020 年，事情有些不同。T-Mobile 的 LTE Band 71 在我所在的地区比 2018 年突出了很多，这意味着兼容手机将获得更好的覆盖。由于 5G 的混乱，国际 Galaxy 手机的频段支持也更加分散。而且现在进口国际星系不像 2018 年那么容易了，可用的设备通常比美国的变种更贵，这就打破了平衡。

终于有了一台 Note 9 可以以旧换新。三星曾经(现在仍然)为 Note 9 提供 550 美元的折价。这很有价值。如果我把我的 Note 9 寄给一个随机的易贝卖家，他不会给我 550 美元的三星手机，在 Swappa 上卖给一个谨慎的买家也不会卖这么多。

我是 Galaxy Note 阵容的忠实粉丝。我喜欢在需要时使用合适的有源手写笔，即使我不经常需要它。所以，当然，我想得到 Galaxy Note 20。基本版本可能只有 1000 美元，但对于 T2 做出的所有妥协来说，这根本不值得。所以我买了 Note 20 Ultra。利用那 550 美元的折价，大约 7%的学生折扣，以及 5%的推荐奖金，我的购买价格降到了 700 美元。由于我预购了我的设备，我还免费得到了价值 150 美元的配件。我在手机上省下了 600 美元，在一些有用的小玩意上省下了“额外”150 美元。

**[三星 Galaxy Note 20 Ultra 回顾:给那些走在曲线前面的人](https://www.xda-developers.com/samsung-galaxy-note-20-ultra-review-exynos/)**

现在，你可能对此有不同的看法，但对我来说，拥有 root 真的不值得今年所有的权衡。所以现在我有了美国解锁的 Galaxy Note 20 Ultra(当然是神秘青铜色)。

但是我有根！为什么我有根？我怎么有根？你必须继续阅读才能找到答案。

## 为什么我喜欢根

首先，也许我应该解释一下为什么我喜欢 root 访问。

第一个原因是方便。我是一名应用程序开发人员，我为 Android 开发一些非常低级的应用程序。其中很多都需要特殊许可，只有通过亚洲开发银行才能授予....或者用 root！在应用程序中点击“授权”按钮比插入我的电脑，打开命令提示符，手动输入 ADB 命令要快得多。如果您需要在一个月内这样做几次，这可能不值得争论，但是任何超出这个范围的频率增加都会使 root 成为一个有价值的步骤。

 <picture>![Grant Write Secure Settings permission on rooted Samsung Galaxy Note 20 Ultra](img/9f61c61104ea2e33bf107eeae693c253.png)</picture> 

Tapping the "GRANT" button here is a whole lot easier than using ADB, especially if I'm frequently clearing app data for testing reasons.

其次:主题化。我知道在三星设备上，可以使用 Synergy 之类的工具在没有 root 用户的情况下安装自定义主题。但还是很麻烦。安装主题有很多限制和步骤。如果你对频繁更新的第三方应用进行主题化，情况只会变得更糟。

用 root 进行主题化就像按一个按钮然后重启一样简单。我使用自己的应用程序 OneUI Tuner 来解决 OneUI 的一大堆麻烦，比如在快速设置标题中添加更多磁贴，或者启用时钟秒。我还使用 Swift Installer 让我的通知阴影变得透明，让我的应用程序看起来更统一。没有 root，这一切都是可能的，但这要麻烦得多。

第三，我喜欢修补。Root 让我可以访问整个文件系统。我可以使用 MiXplorer 查看各种分区和文件夹，也许会发现一些有趣的东西。我还可以使用 Root Activity Launcher 之类的应用来打开已安装应用中隐藏或受限的活动。

 <picture>![HiddenMenu on rooted Samsung Galaxy Note 20 Ultra](img/802c65fadc5812eea1ce8358fbb3a0a8.png)</picture> 

Samsung has a Hidden Menu app. While it's possible to launch some parts of it using dialer codes, most of it is inaccessible unless you're rooted.

第四个原因是 DSU。Android 10 有一个很好的功能，在引导程序解锁的设备上，你可以临时加载和引导一个 GSI。这是一种测试 Android 11 的简单方法，无需清除数据或重新安装固件。在 Android 11 上，这可能不再需要，但我不在 Android 11 上。不幸的是，这在 Note 20 Ultra 上无法开箱即用。它安装了，但无法引导。我确信对内核做一些修改是可能的，但那不是我的专业领域。

还有一个原因是广告拦截。当然，有很多非根广告拦截器，如 DNS66 或 NextDNS，但根据我的经验，没有一个像 AdAway 这样的根解决方案那样有效。非根应用程序不断让广告通过 Chrome 和其他应用程序，而 AdAway 覆盖系统主机文件的方法工作得很好。这种方法还具有不使用任何额外电池寿命的优点。

 <picture>![AdAway on rooted Samsung Galaxy Note 20 Ultra](img/bf306f1efef735277eb93522aadb45bf.png)</picture> 

Enabling AdAway is a one-click process, and it doesn't need to have a VPN running in the background to work.

终于是**我的**手机了！我希望能够按照自己的方式使用它。三年后，我可能会闪存一个基于 AOSP 的 ROM，或者一个后来的设备的一个 UI 端口。或者我可能不会。那应该是我说了算，而不是三星。

## 为什么其他人喜欢根

现在，可能我扎根和解锁的理由对你来说没有对我来说那么有说服力。这完全公平。但这些并不是这样做的唯一原因，我也不是唯一经历过这一过程的人。以下是其他人给他们的美国 Galaxy 设备提供的一些理由。

*   更好的音频调节，例如 Viper4Android。- @mentalmuso
*   适当的应用程序去模糊，这是不够的。- @mentalmuso，@perennialexhaustion
*   隐私功能，如冻结或删除不可信的应用程序，并阻止侵入服务。- @perennialexhaustion
*   使用定制内核以获得更好的性能或电池寿命。- @klabit87
*   安装原生 Linux 工具，如`iptables`，使终端使用更加强大。- @perennialexhaustion

这里是我想到的一些原因，它们对我来说不是特别有吸引力，但是在根空间中非常流行。

*   **无线亚行**。是的，我知道这是 Android 11 上的原生功能，你可以通过有线 ADB 来启用它，但我在 Android 10 上，使用有线 ADB 来启用无线 ADB 有点违背了目的。
*   **定制 rom**，无论是基于股票还是 AOSP。许多人对他们的股票光盘中包含的功能不满意，或者他们只是喜欢更普通的 Android 体验。
*   **App 逆向工程**。有一个叫做 Frida 的工具可以帮助你一步一步地逆向开发 Android 应用程序。但是它需要根。
*   **内核调优**。并不是对内核的每一个改变都必须通过定制来完成。使用像 Kernel Adiutor 这样的应用程序，你可以微调电池寿命和性能之间的平衡，以符合你的个人品味。
*   **启用预发布或隐藏功能**。例如，谷歌因 A/B 测试其应用程序的新功能而臭名昭著。Root 允许您为自己强制启用这些功能。
*   **曝光**。是的，Xposed 仍然存在。但现在它被称为 EdXposed，并由于 Magisk 而无系统地工作。

如果你是根场景的新手(或者你从来没有真正关注过它)，Xposed 框架是 Android 的一个强大的定制和修改。它允许模块开发人员覆盖、添加和删除 Android 中的各种行为。这反过来可以让你做一些事情，比如制作深入的主题，给你的菜单添加按钮，移动状态栏图标，基本上是你想做的任何事情。Xposed 已经存在很久了，现在它的最新形式 EdXposed 仍然吸引了很多关注。

例如，有一个针对一个 UI 的 EdXposed 模块，它就像一个服用了类固醇的 One UI 调谐器。不再局限于资源覆盖支持什么， [Firefds Kit](https://forum.xda-developers.com/xposed/modules/xposed-firefds-kit-0-0-1-0-alpha-1-t4044757) 允许你做一些事情，比如重启后启用生物识别解锁，或者禁用应用签名验证。

尽管如此，很有可能您仍然不相信 root 是必需的。这也是完全合理的。如果 root 不适合你，它就不适合你。但我可以告诉你，至少还有 25 个人用这种方法解锁了至少一台美国 Galaxy 设备。我们有几十个人！几十个！

## 三星 Galaxy Note 20 Ultra 上的 Root 证明

在任何人抱怨之前(尽管这已经是 1300 字了)，我实际上是有根的，我可以用证据来支持这种说法。看看下面的截图和视频。

如你所见，我已经安装并运行了 Magisk v20.4，还有一个用于国际骁龙版本的 TWRP 版本和一个定制内核。内核和 TWRP 是由 mentalmuso 制造的，他也将很快有一个 bootloader 解锁美国 Galaxy Note 20 Ultra。

我还更换了我最近的提供商，使用 Lawnchair，而不是三星的默认或 Good Lock 的任务转换器。当然，我正在使用 Swift Installer 和 OneUI Tuner 对我的设备进行主题化和定制。虽然 Swift Installer 和 OneUI Tuner 都可以在没有 root 用户的情况下工作，但通过使用 Synergy，它们在安装了 Magisk 的情况下会更容易使用。

## 还是根深蒂固的三星智能手机

这不是什么神奇的根漏洞什么的。我的 Galaxy Note 20 Ultra 正确地解锁了引导程序，这意味着 KNOX 已经被触发。我不会用三星 Pass 和三星 Pay。前者检测到我有根，就像在国际变体上一样。奇怪的是，Samsung Pay 并没有抱怨 root。相反，它似乎有某种服务器连接问题。无论哪种方式，都行不通。当然，不经过修改，安全文件夹是无法工作的，但是我不使用它，所以我不在乎。最后，OTA 禁用。尝试检查更新会导致连接错误。但是对于像 SamFirm、Frida 或 Samloader 这样的工具，这对我来说不是问题。

**[三星 Galaxy Note 20 XDA 论坛](https://forum.xda-developers.com/galaxy-note-20)**| |**|[三星 Galaxy Note 20 XDA Ultra 论坛](https://forum.xda-developers.com/galaxy-note-20-ultra)**

但是其他一切都很好。Magisk Hide 仍然允许 SafetyNet 通过，所以像 Google Pay 这样的东西没有问题。我可以(并且已经)毫无问题地安装 Magisk 模块，现在我已经获得了我想要的体验，拥有完全的美国兼容性*和适当的保修*。

### 三星 Galaxy Note 20 Ultra

三星 Galaxy Note 20 Ultra 拥有所有 Android 智能手机中最好的硬件，但三星的 One UI 软件并不是每个人都喜欢的。所以我才买下来扎根。

**Affiliate Links**

Samsung

[View at Samsung](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=I+rooted+my+US+Samsung+Galaxy+Note+20+Ultra%2C+and+here%27s+what+I%27m+doing+with+it&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fsamsung-galaxy-note-20-ultra-root-us-unlocked-snapdragon-865%2F&u1=UUxdaUeUpU29806&url=https%3A%2F%2Fwww.samsung.com%2Fus%2Fsmartphones%2Fgalaxy-note20-5g%2Fbuy%2Fgalaxy-note20-5g-128gb-unlocked-sm-n981uznaxaa%2F)