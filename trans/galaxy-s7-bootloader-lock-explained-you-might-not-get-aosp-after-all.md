# Galaxy S7 引导装载程序解释说:你可能根本得不到 AOSP

> 原文：<https://www.xda-developers.com/galaxy-s7-bootloader-lock-explained-you-might-not-get-aosp-after-all/>

三星 Galaxy S7 和 S7 Edge 是你现在可以买到的最强大的设备。但我们的普通读者和论坛用户会知道，三星设备在开发方面并不是最好的。

三星和开发的许多问题都可以追溯到 [Exynos 及其缺乏文档](http://www.xda-developers.com/samsung-exynos-and-aosp-explained-a-story-of-betrayal/)。因此，当我们听到三星 Galaxy S7 将采用高通 Snapdragon 820 而不是三星自己的 Exynos 8890 的变种时，开发者社区自然会祈祷一切顺利。这可能是近年来第一款支持 AOSP 开发的三星旗舰吗？有没有可能将 TouchWiz 从三星旗舰产品中完全移除，享受没有任何臃肿的 AOSP 体验？如果不等待几个月三星将其移植到设备上，人们能指望获得最新的 Android 版本吗？

唉，那将是一厢情愿的想法。这条路一开始就有路障。首先，只有在美国销售的设备才会配备高通骁龙 820。在国际上销售的设备将配备 Exynos 8890，这意味着世界上很大一部分地区将失去 AOSP 的社区作品，就像三星以前的旗舰产品一样。然而，这是意料之中的，因此，这个消息并不令人惊讶。

然后，航母来了。美国运营商有很强的锁定设备的历史，威瑞森和美国电话电报公司是最糟糕的启动加载器锁定。因此，这些运营商的用户很可能会在很大程度上受到开箱即用的困扰。对 Android 系统的更新必须首先由三星在 TouchWiz 中实现，然后必须通过运营商才能到达设备，这在更新部署过程中又增加了一步。

所以，综上所述，Sprint 和 T-Mobile 的三星 Galaxy S7 和 S7 Edge 用户将是最幸运的，对吗？毕竟，尽管这些运营商在设备上进行 SIM 卡锁定实践，但在涉及三星 bootloaders 时，他们传统上并不像其他运营商那样紧张。这些设备仍然比不上*完全*解锁的设备，但有总比没有好，对吗？对吗？

不，不太喜欢。三星又做到了。

它始于我们的 T-Mobile 三星 Galaxy S7 Edge 论坛，在那里创建了一个预期的 [root 讨论线程](http://forum.xda-developers.com/tmobile-s7-edge/how-to/root-discussion-future-sticky-root-t3327399)，旨在尽快在设备上获得 root，然后以一种易于遵循的方式分发给其他论坛用户。XDA 认可的开发商[吴玉芳](http://forum.xda-developers.com/member.php?u=522448)做了一个[的快速观察](http://forum.xda-developers.com/showpost.php?p=65725759&postcount=28)暗示一切可能终究不是对的:

> 似乎引导加载程序被锁定，高通安全引导和安全下载都已启用。

呃，看起来还不算太糟。OEM 解锁仍然存在于开发者设置中，所以可能需要在继续之前进行切换。吴玉芳回答说他确实这样做了，但是[仍然希望通过其他方法](http://forum.xda-developers.com/showpost.php?p=65732096&postcount=38)获得根。

XDA 认出了开发者[泰克德](http://forum.xda-developers.com/member.php?u=4107827)和[一起插话他的观察](http://forum.xda-developers.com/showpost.php?p=65733856&postcount=43):

> 今天刚拿到我的设备...快速查看后，我没有看到任何锁定的内容。如果您指的是:
> 
> 高通 SECUREBOOT:启用
> 
> 安全下载:启用
> 
> 这很正常...没什么好担心的...

其他人也参与了讨论，但是很明显奥丁不能闪现任何东西，除了未动过的股票图片。

> 目前还没有 TWRP。我甚至不能用一个完全不变但重新打包的 initramfs 来编写内核。股票图像闪光罚款。

在这个阶段，三星发布了 Galaxy S7 和 S7 Edge 的 Exynos 变体的[内核源代码。除了符合 GPL 的最低要求之外，不要对任何东西感到困惑，这个内核源代码将只帮助开发 Exynos 变体的定制内核。到目前为止，AOSP 仍然是一个梦。](http://www.xda-developers.com/xda-external-link/samsung-uploads-kernel-source-code-for-the-exynos-s7-edge/)

在内核代码的刺激下，XDA 的高级成员 [jcadduono](http://forum.xda-developers.com/member.php?u=5672995) 能够将 [Galaxy S7](http://forum.xda-developers.com/galaxy-s7/development/recovery-official-twrp-herolte-t3333770) 和 [S7 Edge](http://forum.xda-developers.com/s7-edge/development/recovery-official-twrp-hero2lte-3-0-0-0-t3334084) 的国际(Exynos)所有者视为 TWRP 的构建，为用户群打开了可能性的世界。但是高通变种呢？好吧，这就是坏消息开始传来的地方。

Jcadduono [打电话给](http://forum.xda-developers.com/showpost.php?p=65804371&postcount=94)三星的工程移动部门，在那里他被告知 T-Mobile S7 有一个**安全闪存锁定引导加载程序**，这与威瑞森以前的三星设备相似。他还提到, [dm-verity](https://source.android.com/security/verifiedboot/) 在内核中启用，这意味着你将无法在当前状态下刷新修改的系统分区，这就是某些锁定的 Galaxy S6 型号获得其根源的方式。

为了进一步开发和研究， [jcadduono](http://forum.xda-developers.com/member.php?u=5672995) 在帖子中询问人们，看他们是否能闪现他为该设备构建的 TWRP。根据设备显示的错误，可以得出结论。然后，[所有的恐惧都被证实了](http://forum.xda-developers.com/showpost.php?p=65805289&postcount=112)。

这不是普通的写失败。简单地说，安全检查失败表示引导加载程序被锁定。就我个人的知识和[对](https://source.android.com/security/verifiedboot/)的理解而言，这阻止了任何操作的执行，除非文件的签名与存储在设备引导分区上的 OEM 公钥相匹配。这实质上限制了所有直接来自原始设备制造商的活动，在这种情况下是三星。你不能闪现任何东西，即使是没有其他修改的重新打包的图片也不行。

引用 XDA 知名开发商[吴玉芳](http://forum.xda-developers.com/member.php?u=522448)的话:

> 高通·塞库伯用近乎防弹的信任链束缚住了我们。

[Jcadduono](http://forum.xda-developers.com/member.php?u=5672995) [在回复中证实了同样的](http://forum.xda-developers.com/showpost.php?p=65805621&postcount=122):

问:*让 selinux 变得宽松会有帮助吗？据我回忆，这就是我们在 s6 上必须做的。*

答:*不行，恢复镜像都不能闪。问题不在于启动它，而在于实际刷新它。*

下载模式引导加载程序将 Odin 发送的映像加载到内存中，然后对映像运行校验和及签名验证。如果不匹配，它就从内存中释放出来，根本不写入设备。

除了让 T-Mobile 给我们的 TWRP 图像签名，我们什么也做不了。

* * *

为什么 T-Mobile 会锁定很可能是三星 2016 年最畅销设备之一的引导程序？[这里的](http://forum.xda-developers.com/showpost.php?p=65806062&postcount=138)是对他们为什么会选择这样做的一些猜测，尽管他们过去对其他几款设备很宽容:

我的猜测是，三星刚刚决定在所有骁龙版本上启用安全 flash 验证，因为这是所有其他运营商想要的。

据 T-Mobile 的 facebook 代表称，T-Mobile 现在取消了对 rooting 的保修，所以也许 T-Mobile 没有向三星索要解锁设备，而是决定加入其他公司。

发布消息来源并没有什么不同。你不能把任何东西闪到手机里，除非是 OEM 签名的。

凭借这一点，三星有效地锁定了 Galaxy S7 和 S7 Edge 的 Snapdragon 820 变种的所有开发。尽管大部分讨论存在于 T-Mobile S7 Edge 论坛中，但该场景和后果适用于所有运营商，也适用于 S7 (SD-820)。很长一段时间以来，三星本应是一款对开发者友好的设备，却变得比 Exynos 变种更加封闭。对于那些专门寻找三星开发设备的用户来说，这确实令人沮丧，因为根据过去的经验，他们更有可能选择 Snapdragon 820 版本，而不是 Exynos 版本。

### 已经完全失去了吗？这种设备会永远得不到发展吗？

现在的情况还不是百分之百的灾难。通过漏洞和攻击获取 root 用户的可能性仍然很小。这些都是获得根的粗糙方法，但它是可以做到的，尽管还没有找到。但漏洞和利用的问题是，它们会在未来的更新中得到修补。最终用户必须决定他是希望获得最新的更新，但在发现新的漏洞之前没有 root 用户，还是继续使用过时的更新并满足于 root 用户。你更新到最新的，你又回到了起点。

[Jcadduono](http://forum.xda-developers.com/member.php?u=5672995) 有[这个](http://forum.xda-developers.com/showpost.php?p=65806656&postcount=148)来说说设备的发展状况:

> 引导镜像有 dm-verity，这意味着如果你对系统分区进行任何装载/写入操作，你将得到一个引导循环。活根将是唯一的方法。
> 
> 好消息是，您应该能够在数据分区中创建一个循环设备映像，并使用可执行权限挂载它，以创建您自己的可写小型系统覆盖图**，如果一个活动的 root 漏洞出现**。我想类似于超级无系统。

这是对未来的乐观看法，主要是因为它严重依赖于存在以及发现一个活的根漏洞。可能不存在此类漏洞，或者可能存在，但没有人能够找到它。如果在所有美国运营商的基于 Snapdragon 820 的 Galaxy S7 和 S7 Edge 的开发场景中加入 T3，那将是一个非常大的T1。

我们真的感到惊讶吗？个人有点期待。随着 Samsung Pay 成为如此大的一笔交易，三星不会轻易在他们的移动支付解决方案上妥协。虽然从广泛的角度来看，开发人员社区的意图是干净的，但不可否认的是，root 和其他东西被用于邪恶的活动。找到并解锁引导程序的行为为设备打开了一个充满可能性的世界，这个世界既有积极的一面，也有消极的一面。当您考虑到大量民众预计会将他们的银行信息迁移到这些设备上，并在所有本地支付终端上使用它们时，事情就会变得严重。这其中的变数很大，三星当然不会拿自己设备的声誉以及 Samsung Pay 的声誉去冒险，与苹果和 Apple Pay 等更“安全”的替代产品竞争。

但是，这种封锁是可以接受的吗？不会。至少，一份免责声明应该呈现在公众面前。它甚至不需要负面营销。三星本可以在发布会上很好地提到这些安全功能，称这些设备为 Samsung Pay 增加了额外的安全层，使其难以被黑客攻击和利用。我们会领会这个暗示的，真的。

三星也可以推出一个解锁设备的特殊程序，就像索尼工作等其他 OEM 一样。这是仍然可行的可能性之一，可以两全其美。非开发者公众获得了一部安全的手机，充分发挥了三星目前的能力，而开发者社区以失去 Samsung Pay 和其他安全相关功能为代价解锁了他们的 bootloaders。

这无疑是一个令人失望的转变。在黑暗的达奇维兹世界，AOSP 最大的希望已经被像埃克斯诺斯这样的人削弱了。虽然三星的 Snapdragon 820 设备仍然存在根、自定义内核、恢复和 ROM 的可能性，但在这场毁灭性的打击后，它们吸引主要开发工作的可能性仍然很小。

你对这一事件的转变有什么看法？请在下面的评论中告诉我们！