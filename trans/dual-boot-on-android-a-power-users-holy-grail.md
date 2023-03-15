# Android 双启动优点和解决方案

> 原文：<https://www.xda-developers.com/dual-boot-on-android-a-power-users-holy-grail/>

你们中的许多人可能会双重启动自己的个人电脑，无论是在运行 Windows 的同时运行 Linux，还是因为你有一台 Mac 而讨厌 OS X。在计算机平台上，由于各种原因，特别是软件兼容性/集成，这个过程可能是一个救命稻草。使用 Linux 分区的计算机程序员或使用 bootcamp 进行视频游戏的 Mac 游戏玩家并不少见。在电脑上，随着时间的推移，这一过程变得相对简单，微软和苹果通常支持这一概念。在 Android 上，情况就不同了。

[![android](img/f8794b0b5e7327ce333f930564720f94.png) ](http://www.xda-developers.com/wp-content/uploads/2015/04/android.png) Android 的座右铭是“选择”，它的旗帜是它为实现这样的座右铭而提供的自由。但是大多数 Android 用户在 a 选择(也就是他们运行的 ROM)内有无限的选择*。一个简单的例子是，一个用户在 Lollipop 上运行三星 ROM，但还不能使用 Xposed。当然，有一些 AOSP rom 可以运行 Xposed，但是用户可能不想仅仅为了这些额外的好处而切换。孤立的岛是分散的 rom，这意味着，虽然用户在岛上有无限的自由，但决策空间受到岛上内容的限制。它旁边的一个岛可能有许多用户想要的东西。*

这本质上是 Windows 和 Mac 的问题所在，但不是以如此激烈的方式，因为它们本质上是专有的，不像 Android 那样开放。由于平台在开放性方面的相似性，Linux 用户获得了特别同构的体验。但是双引导在 Android 上仍然是非常可能的，即使不是那么主流。幸运的是，XDA 的开发者和其他人也想出了不同的方法让你的设备同时运行两个 Android ROMs，甚至不同的操作系统。

双启动在电脑上有意义，但在手机上有意义吗？也许对普通用户来说不是这样。甚至有经验的用户[可能会称之为一个没有问题的答案](http://arstechnica.com/gadgets/2014/03/dual-boot-phones-the-answer-to-a-question-that-nobody-is-asking/)，它也确实有一些烦恼。但是对于 XDA 的我们来说，额外的自由和选择意味着，如果使用得当，双重引导可以成为超级用户的圣杯。我们来探究一下原因。

## **一些解决方案**

**[![20150420185549115](img/fc420af2648e45e121ffa1675908d534.png) ](http://www.xda-developers.com/wp-content/uploads/2015/04/20150420185549115.png) MultiROM** 位于你的引导程序之后，在 Android 上获得类似 GRUB 的体验，并允许你加载到不同的 ROM，甚至其他操作系统，如 Ubuntu Touch。MultiROM 由 XDA 知名开发者 [Tasssadar](http://forum.xda-developers.com/member.php?u=3418703) 提供，它可能是 Android 上最著名的双引导解决方案之一。我们在 XDA 电视专题节目中介绍了安装过程，但请记住，官方支持仅限于少数设备，如 Nexus 4、Nexus 5 以及 2012 年和 2013 年的 Nexus 7 平板电脑。还有一些非官方的端口和版本正在开发中，所以在这里查看兼容性。

XDA 资深知名开发者 [Hashcode](http://forum.xda-developers.com/member.php?u=4243514) 创造了一个名为 **Safestrap** 的选项，许多拥有锁定引导加载器(感谢运营商)的 XDA 用户已经爱上了这个选项。遗憾的是，这款软件目前还没有得到 Hashcode 的官方支持，这意味着官方开发已经停止。也就是说，那些仍然可以利用 Safestrap 的幸运儿可以访问额外的 ROM 插槽和许多其他好东西。

XDA 资深成员[陈小龙](http://forum.xda-developers.com/member.php?u=4277844)创造了**双引导补丁**，你可以用它来修补 rom(以及像 GApps 这样的闪存)并使它们可用于多重引导。你可以在这里获取最新的快照补丁[，但是请记住，你的设备可能需要一些额外的步骤。例如，对于 Galaxy Note 4 设备，](https://snapshots.noobdev.io/)[我使用的指南](http://forum.xda-developers.com/note-4/general/dual-boot-n910f-snap-dragon-variant-t3065211)需要 XDA 资深会员 [rlorange](http://forum.xda-developers.com/member.php?u=3145598) 重新修补。最后，它还与交换 rom APK 一起使用，在 rom 之间跳跃。

开发者 Michael Zimmermann 也为 Android 开发了 GRUB，这是一个高通设备的引导加载程序替代品，它的行为就像 GRUB 一样。你可以查看 [+GRUB4Android](https://plus.google.com/+Grub4androidOrg/posts) 社区的新闻和信息，以及资源链接。还有很多其他的多重引导选择，所以不要认为这些是你所有的选择。特别是 XDA 的开发者已经设法通过各种方法将功能应用到许多特定的设备上，这是我们[从](http://www.xda-developers.com/dual-boot-achieved-on-the-samsung-galaxy-s-4/)[追溯到](http://www.xda-developers.com/create-a-gingerbreadice-cream-sandwich-dual-boot-sd-card-for-the-nook-color/) **以来就喜欢的特色。找到双引导解决方案的最好方法是在你的设备的特定 XDA 论坛中搜索一个。如果你确实找到了一个你可以使用的解决方案，这就是我们编辑团队认为你应该去做的原因:**

## **美德**

首先，它最好的部分是有一个工作用的 ROM 和一个娱乐用的 ROM，或者说，有一个日常驱动和一个备用 ROM。我个人在我的 Note 4 上运行 TouchWiz，因为它的生产力功能在跑步或做研究、家庭作业或工作时非常有用。因为当我不再忙于任务时，我可以启动我的 CM12.1 ROM(或任何我碰巧运行的 AOSP ROM)来获得一个更光滑、更好的 UX，让我更好地解压。还有一个事实是，有些只读存储器具有独特的功能，或者有某些优点和缺点:

像 TouchWiz 这样的 OEM ROMs 可以提供更好的图像处理，从而提高相机质量，而当过渡到 AOSP ROM 时，这一点就完全丧失了。一些 rom 也有更好的音质或在关键区域的性能，或功能，如耐力模式或吹捧的“超节能”功能。必要时，这些功能会派上用场，而且有了双引导，你就不必为了另一个 ROM 而牺牲它们。如果你需要另一个“岛”的特性，重启会在不到一分钟的时间内把你带过去。

对于 also 爱好者来说，双启动也提供了安全试用新 rom([和 Firefox OS](http://nexus5.wonderhowto.com/how-to/install-firefox-os-other-experimental-roms-your-nexus-5-without-any-risk-0150964/) 之类的东西)或测试某些 mod(通常)的机会，而不会危及你日常驱动程序的完整性。在门户网站团队中，我们分享了这样的故事:希望在深夜对我们的手机进行一些调整，但如果出现问题，我们将不得不花费额外的宝贵睡眠时间在第二天早上修复它。如果你有额外的 ROM 插槽，你可以调整东西或尝试 mods，而不用担心在一天的剩余时间里会有不利的后果。请记住，出于明显的原因，这并不包括*所有的*mod，因为一些仍然可以设法弄乱你的其他 ROM(和更多)。但是**有了合适的标准**，你就可以毫无顾虑地改变。

然而，这也有不利的一面。根据您的解决方案，该过程可能相当“杂乱无章”,有时风险很大，这意味着您必须非常小心每一步，至少要做好备份。许多用户抱怨初始设置，因为设置设备总是相当烦人。幸运的是，Lollipop ROMs 简化了这个过程，有了谷歌的数据备份、应用程序下载计划和 Titanium 备份，这个过程并不太烦人(我们现在可能都习惯了)。**根据您的方法**，重复数据可能会成为一个问题，尤其是当您的内存不足时。然而，一些解决方案在 rom 之间共享数据，不像 PC 上分区系统的封闭性。这些都是你应该知道的事情，但是我们认为积极的一面远远大于消极的一面。

## **结论**

如果说 Android 是关于开放性的，那么双引导给这个想法增加了一个维度。双引导不仅对手机上的 Android 有利，对 Android Wear 也有利，我们讨论过这是对 [Wear 开放性难题](http://www.xda-developers.com/wear-openness-possible-model-alternatives/)的解决方案，希望有一天能成为现实。最终，如果你是一个超级用户，双引导可能会帮助你的爱好，同时，使你的 UX 更有价值。我个人喜欢在一分钟或更短时间内切换 rom 的选项，它允许我享受最新的软件开发以及对我的用例最有用的软件。如果你愿意尝试，搜索你的设备的 XDA 论坛，看看你的选择！

****你的安卓手机双开机吗？如何看待双开机？下面讨论。****