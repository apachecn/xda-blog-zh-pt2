# 8 月诺基亚手机安全更新阻止引导加载程序解锁方法

> 原文：<https://www.xda-developers.com/august-security-update-on-nokia-phones-blocks-the-only-bootloader-unlock-method/>

Bootloader 解锁是 Android 改造必不可少的一部分。在你考虑在你的设备上安装一个定制的 ROM 之前，你首先需要解锁你的设备的引导程序，这样你就可以引导未签名的引导镜像。但是，在解锁引导加载程序之前，您需要手动完成一系列步骤，以确保您了解解锁引导加载程序的风险。其中一些步骤涉及禁用安全功能和/或请求启动加载器解锁代码，这些代码可能会立即被授予，或者在小米设备的情况下，可能需要几天才能收到。无论你需要经历多少磨难才能控制你自己花钱购买的设备，一些智能手机制造商仍然选择阻止你解锁设备的引导程序。HMD Global 就是这样一家设备制造商，该公司最近为其诺基亚品牌的智能手机推出了 8 月份的安全补丁,阻止了唯一已知的引导加载程序解锁方法。

当 HMD Global 首次宣布诺基亚品牌的复兴时，我们非常兴奋。我们更兴奋地听到 HMD Global 将推出诺基亚品牌的智能手机，搭载近乎库存版本的安卓系统。然后，他们宣布 2018 年所有面向国际市场的智能手机都将加入 Android One 计划。最近，他们甚至承诺[将所有诺基亚品牌的智能手机更新为](https://www.xda-developers.com/hmd-global-nokia-android-p-update/)安卓系统！HMD Global 显然很关心让他们的客户满意，但有一件事阻碍了我们完全支持他们的品牌，那就是他们拒绝为所有人提供 bootloader 解锁。进入非官方的 bootloader 解锁工具。

## 诺基亚品牌的手机与解锁的引导加载器的地下场景

我们论坛上的大多数用户都知道诺基亚品牌的智能手机无法解锁，但一些社区成员实际上找到了一种方法来做到这一点。你可能在我们的 Nokia 7 Plus 和 Nokia 6.1 论坛上看到过一些建议你解锁引导程序的帖子，比如这些 [帖子](https://forum.xda-developers.com/nokia-6-2018/how-to/guid-to-flash-treble-gsi-nokia-6-2018-t3808660)。甚至还有诺基亚 8 在 TWRP 的官方发布，即最近在 T4 发布的 T5。让这些线程成为可能的是 XDA 资深成员 [hikari_calyx](https://forum.xda-developers.com/member.php?u=7601808) 及其团队成员发现的引导加载程序解锁方法。他们想出了一种方法来为诺基亚品牌的智能手机生成引导加载程序解锁代码，尽管他们决定以付费服务的形式提供他们的工具。不幸的是，随着 8 月份安全补丁的发布，他们的工具生成的引导加载程序解锁代码将不再解锁引导加载程序。

非常明确地说，**我们不反对 HMD Global 修补这种解锁引导程序**的特殊方法。正如莱恩·chương 和萨缪尔·里多斯科在[媒体博客](https://medium.com/@Hello_37847/hmd-officially-blocked-bootloader-unlocking-now-is-the-time-to-take-action-ef5905f5bf98)上解释的那样，这种方法不可否认地包含了漏洞。HMD Global 可以也应该修补他们设备软件中的任何漏洞或安全漏洞。然而，我们感到失望的是，**公司仍然没有提供一个官方方法来解锁引导程序**，这样用户就不必转向一个封闭源代码的第三方付费服务。

## HMD 全球延迟的承诺

关于未锁定的引导加载程序的安全问题已经讨论了很多年了。某些制造商和运营商选择完全锁定他们的设备，理由是安全原因。华为最近做出了[有争议的决定，停止提供 bootloader 解锁代码](https://www.xda-developers.com/huawei-stop-providing-bootloader-unlock-codes/)，这一决定在我们的一些读者眼中影响了他们对智能手机的看法。如果没有可解锁的引导程序，大多数华为设备的所有者([排除了](https://www.xda-developers.com/huawei-p20-emui-9-android-pie/)华为 P20 系列和[即将推出的](https://www.xda-developers.com/huawei-mate-20-notch-render-specifications/)华为 Mate 20 系列)将不得不等待数月才能看到 Android Pie 发布到他们的设备上。有了解锁的引导程序，他们现在就可以安装[非正式版本](https://www.xda-developers.com/android-pie-honor-view-10-huawei-mate-10-pro/)。

当然，我们会承认 HMD Global 已经迅速提供了每月的安全更新(尽管[也有一些问题](https://www.xda-developers.com/nokia-6-1-may-security-update-major-wi-fi-issues/))，并在他们的设备范围内相当快地推出了 Android Oreo 更新。正如我们之前所说，他们已经承诺向他们的整个设备系列推出 Android Pie。但是，一旦 HMD Global 放弃对他们的旧预算和中端设备的官方支持，将会发生什么呢？这些设备占了他们产品组合的大部分。如果没有定制的 rom 来非正式地更新它们，用户最终将不得不放弃他们功能完美的智能手机，如果他们想针对一些(但不是全部)新发现的漏洞保持最新的话。或者，他们可能只是想体验最新的 Android 版本，而不必花钱进行他们不想要或不需要的升级。

此外，诺基亚用户再也不能自己重新安装手机固件了，因为目前在线提供的闪存工具变得毫无用处——如果出现问题，你需要将手机带到服务中心。保修应该涵盖这些问题的大部分，所以如果你没有物理损坏你的手机，你应该没事。但如果你的保修失效或过期，你可以自己修理或在当地修理店修理，这是额外的费用。

去年，HMD Global 的首席技术官 Mikko Jaakkola 在 Twitter 上表示，允许 bootloader 解锁“确实在他们的积压中”，然而，近一年后，用户仍然没有办法正式这样做。我们甚至没有触及该公司未能遵守 GPL 的问题，没有为他们的许多智能手机上安装的 Linux 内核二进制文件发布内核源代码。

我们联系了 HMD 就此事发表评论，如果有回复，我们会及时更新。与此同时，如果你有兴趣表达你的观点，你可以[签署这份请愿书](https://www.change.org/p/hmd-global-give-us-the-ability-to-unlock-the-bootloader-of-our-nokia-handset)或者在[官方诺基亚支持论坛](https://community.phones.nokia.com/support/discussions/topics/7000024502)上发表评论。