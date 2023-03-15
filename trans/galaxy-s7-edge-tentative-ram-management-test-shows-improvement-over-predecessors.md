# Galaxy S7 Edge RAM 管理测试显示改进

> 原文：<https://www.xda-developers.com/galaxy-s7-edge-tentative-ram-management-test-shows-improvement-over-predecessors/>

让我们先承认这一点:三星制造出了好手机。作为一个松散笼统的说法，有很多道理在里面。在 Android 历史的任何一个特定时间点，三星一直在制造与主流市场领导者竞争的设备，在很多情况下，他们自己就是市场领导者。

三星旗舰机，顾名思义，是硬件和软件的最佳组合，人们可以在发布时从该公司购买。如果你考虑正常的消费者使用和需求，硬件就进入了过度使用的领域。但是高级用户想要的越来越多，期望设备的硬件利用率达到绝对极限。因此，当一家旗舰企业在不该表现的部门表现不佳时，人们会感到惊讶，并提出疑问。

这就是三星 Galaxy S6 旗舰 duo 的情况。如果你在手机发布时浏览过三星 Galaxy S6 或 T2 S6 Edge 的 xda 子论坛，你会发现很多用户抱怨这些设备的内存管理不足。这些手机拥有 3GB 的内存，LPDDR4 也是如此。 [Android Authority 对 LPDDR4 比 LPDDR3 好多少进行了分析](http://www.androidauthority.com/lpddr4-everything-need-know-599759/)，因此 Galaxy S6 和 S6 Edge 在内存处理方面的预期是顶级的。下面是三星将 LPDDR4 与 LPDDR3 和 LPDDR2 进行比较的视频:

但是这都是理论上的谈话。当谈到实际性能时，三星 Galaxy S6 和 S6 Edge 遇到了一系列内存管理问题。起初，Android 5.0 Lollipop 臭名昭著的内存泄漏被归咎于长时间使用后不可避免地出现的速度变慢。甚至三星[也承认这是一个问题](http://www.forbes.com/sites/gordonkelly/2015/05/01/samsung-galaxy-s6-memory-problem/#37e0e93e5594)，向用户保证会为手机推出补丁。

随着 Android 5.1 Lollipop 最终在 Galaxy S6 和 S6 Edge 上推出，这些内存泄漏在很大程度上得到了修复，但其他问题也浮出了水面。这些手机被批评在内存处理上过于激进，用户在论坛上表达了他们的担忧。他们抱怨说，应用程序刷新非常普遍，许多应用程序在用户切换回上一个位置时会把他们踢出去。问题是[在某些情况下](http://forum.xda-developers.com/galaxy-s6/help/killing-apps-aggressively-t3084155/post60157244#post60157244)(例如 Chrome 和其他 webview 应用程序)如此严重，以至于即使你只是切换到一个应用程序并返回，应用程序也会刷新。对于一部号称性能领先的手机来说，逃避最基本的多任务处理是致命的失败。

当然，这是 XDA。因此[针对该问题的非官方修复被发现](http://www.xda-developers.com/fix-for-galaxy-s6-memory-issues/)。同一套修复程序甚至被移植到其他三星设备上，如 [Galaxy Note 4](http://www.xda-developers.com/psa-you-can-optimize-your-note-4s-recents-menu-ram/) 。但关键是，这样的修复首先不应该存在，对于一个多任务处理的基本问题来说更是如此，对于一部将被媒体和公众详细审查其所有声明的手机来说更是如此。

Galaxy Note 5 也存在同样的问题。以下是我们自己的马里奥在[对 Note 5 的广泛评论](http://www.xda-developers.com/failed-potential-the-note5-xda-review/#performance)中对其 RAM 管理的评论:

> Note5 拥有积极的内存管理，就像之前的 S6 和 S6 Edge 一样，也像许多 TouchWiz Lollipop 设备一样。这是一个遗憾，因为这款手机的性能不像 4GB 内存的手机(当与 ZenFone 2 或 OnePlus 2 并列比较时很明显)，但它的性能也像我同样受损的 Note 4 及其 3GB 内存一样差，甚至比我与之对抗的 2GB 内存设备更差。它真的很糟糕，但更讽刺的是，Note5 包括一个任务杀手应用程序和一个 RAM 清理功能，这两个功能都可以在 Smart Manager 下找到。然而这两者都几乎毫无用处。
> 
> RAM 管理很可能会通过类似的 build.prop 编辑来修复，该编辑是 XDA 成员为 S6 和[移植到 Note 4](http://www.xda-developers.com/psa-you-can-optimize-your-note-4s-recents-menu-ram/) 而设计的。但是开箱后，情况并不乐观，这违背了升级 RAM 的整个概念。

正如所料，同一套修复程序[也修复了 Note 5](http://www.xda-developers.com/psa-the-ram-management-fix-for-the-s6-works-on-the-note5/) 的问题。一点好消息是，泄露的 Note 5 的 Android 6.0 棉花糖 TouchWiz 版本[也没有内存管理问题](http://www.xda-developers.com/this-is-touchwiz-on-marshmallow-note-5-android-6-0-leak-hands-on/)。Note 5 的 Android 6.0 棉花糖版本目前正在分阶段推出，在任何重大问题解决之前，公众很快就可以在他们的旗舰设备上更流畅地进行多任务处理。

随着 Galaxy S7 和 S7 Edge 的[发布，这个问题显然会再次被提出。这些设备仍然存在内存管理问题吗？用户能指望在后台保持 5 个以上的应用程序打开吗？或者系统(确切地说是 TouchWiz)会继续在后台执行其激进的任务杀戮吗？](http://www.xda-developers.com/samsung-unveils-the-galaxy-s7-and-galaxy-s7-edge-what-you-need-to-know/)

对此的回答是，是的，已经有所改进。因其深度设备评测视频而受欢迎的 YouTuber [Erica Griffin](https://www.youtube.com/channel/UCB2527zGV3A0Km_quJiUaeQ) 在 2016 年 MWC 展会上上传了一个测试单元的暂定内存管理测试:

在视频中，Erica 能够加载并在 8 个应用程序之间切换，没有任何停顿，她指出(我们也同意)这是对以前 Galaxy 旗舰设备的明显改进，以前的 Galaxy 旗舰设备在运行 5 个左右的应用程序后会开始挣扎。当[炉石魔兽英雄](https://play.google.com/store/apps/details?id=com.blizzard.wtcg.hearthstone&hl=en)打开时，设备确实开始关闭应用程序(在这种情况下是 Chrome ),但由于炉石的内存密集型特性，我们不会真的责怪设备这样做。

炉石可能是一个在*应用*中演示多任务处理的糟糕选择(尽管考虑到展厅的限制，这是可以理解的)，但即使在游戏推出之前，三星 Galaxy S7 Edge 也表明它确实比其前辈更好地工作。至少，8 个打开的应用程序绝对是比 4 或 5 个更好的工作场景。但是，当仅限于应用程序时，即使是我们审查的低预算设备，如 [Elephone P8000](https://www.youtube.com/watch?v=gwrbVyWrkuU) 或 [OnePlus X](https://www.youtube.com/watch?v=Qsn8RQRq-aw) 在内存中保存 10-12 个应用程序并仍然能够在 3GB lpddr 3 RAM 上进行多任务处理也没有问题。

正如 Erica 指出的，她的测试本质上是试探性的。有问题的设备是一个带有测试固件的演示装置，很可能与公众将要接触到的固件大相径庭。但即使是临时性的，测试视频也给了我们一个很好的基础来判断 Galaxy S7 和 S7 相对于其前辈的优势，因为这些前辈直到最近才在股票软件上表现出来。

当我们有机会深入了解最终的零售设备时，将会发现 Galaxy S7 和 S7 Edge 的绝对极限。在那之前，我们可以说，是的，S7 和 S7 Edge 是有史以来最好的 Galaxy 设备。

敬请关注更多 MWC 2016 报道！