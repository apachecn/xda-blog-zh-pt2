# Pokémon GO 的最新更新阻止根设备进入游戏

> 原文：<https://www.xda-developers.com/latest-update-to-pokemon-go-blocks-rooted-devices-from-entering-the-game/>

如果我周围的街道、你和其他任何地方都有任何迹象的话，Pokémon GO 时尚的最强点已经超过了我们。虽然每个人和他们的狗都很兴奋尝试在现实生活中成为神奇宝贝训练师的感觉，但实际的游戏及其机制让很多人感到沮丧。

再加上追踪器的移除，这个游戏实质上变成了用神奇宝贝扔纸，最终，人们厌倦了，放弃了享受。

最新的更新试图找回一些迷失的人群，但在典型的 Niantic 时尚中，它前进了一步，后退了两步。此次发布带来了一个新功能，即“神奇宝贝伙伴”，这是一个虚拟的 mon，它会出现在你的个人资料页面上，如果你在 mon 被激活为“伙伴”的情况下走了一定的距离，就会为其物种提供糖果奖励。

截图由 reddit 用户 [Mich4x](https://www.reddit.com/user/Mich4x) 提供。

> 那么，关键在哪里？对于根用户来说，关键在于[公告贴](http://pokemongolive.com/en/post/ver-update-091016/):

*培训师，*

*Pokémon GO 正在更新至 Android 设备的 0.37.0 版本和 iOS 设备的 1.7.0 版本。以下是我们开发团队的一些发布说明和评论:*

*   实施伙伴神奇宝贝:训练者现在可以选择一个神奇宝贝作为他们的伙伴。训练者可以通过走一定的距离来为他们的伙伴神奇宝贝赢得糖果。
*   更容易在屏幕上选择较小的神奇宝贝。
*   修正了鸡蛋有时会孵化而不显示动画的问题。
*   *提高了设备切换网络时的性能可靠性，不再导致应用程序挂起或停止更新。*
*   *神奇宝贝走加支撑*
*   微小的文字修正。

*我们继续致力于从 Pokémon GO 中消除机器人和刮刀。**pokémon GO**不支持根设备或越狱设备。记得只从谷歌 Play 商店官方或 iTunes 应用商店下载 Pokémon GO。*

这个更新，版本 0.37.0，本质上阻止了根用户。如果您有根设备，这是您尝试登录时会遇到的屏幕:

随着更新，Niantic 正式采取了反对所有 rooted 用户或越狱用户(如果你是 iOS 用户)的立场。我们想推测，这一举动是针对大量出现的 GPS 欺骗者，通过凭空出现来捕捉健身房。许多基本的 GPS 欺骗应用程序需要 root 才能工作，所以锁定 root 用户是有意义的，对吗？

> #### 不，不完全是。

神奇宝贝 GO 秘籍最基本的形式涉及简单的 root，这些往往是命中或错过。奏效的欺骗手段通常完美无缺，利用了 Android 上的 Xposed 框架。如果您安装了 Xposed 框架，并且您有意欺骗，那么您可以很容易地找到对应用程序隐藏 root 的方法。银行应用已经有这样的模块了，所以把 Pokémon GO 列入黑名单真的很简单。见鬼，如果你能[用 root 和 Xposed](http://www.xda-developers.com/use-android-pay-with-xposed-without-rebooting-with-magisk/) 运行 Android Pay，没什么能说 Pokémon GO 比这更难的了。类似地，越狱的 iOS 设备也有调整，从应用程序中屏蔽越狱，其中一些已经存在，也适用于 Pokémon GO。

Niantic 在更新中所做的是扼杀那些有 root 用户但没有作弊的用户的热情。Root 除了在游戏中作弊之外还被用于很多其他的事情，假设所有的 root 用户都是骗子是愚蠢的。有足够动机作弊的作弊者将毫无困难地跳过一个圈，让游戏像更新前一样工作。但对于那些已经对游戏失去兴趣的休闲玩家来说，Niantic 确实让玩游戏又多了一个障碍。而且很多这样的临时工都不会介意。

Pokémon GO 的最新 apk 可以在这里找到[。根用户将需要](http://www.apkmirror.com/apk/niantic-inc/pokemon-go/pokemon-go-0-37-0-release/pokemon-go-0-37-0-android-apk-download/)[x 暴露框架](http://forum.xda-developers.com/showthread.php?t=3034811)和可能的[rootpackop](http://forum.xda-developers.com/xposed/modules/mod-rootcloak-completely-hide-root-t2574647)模块来让游戏再次运行。

**忍者编辑:**经过更多的阅读，看起来 Niantic 实际上是在使用安全网检查来检查 root。XDA 资深会员[马尔兹](http://forum.xda-developers.com/member.php?u=4024698) [在游戏代码中发现了名为](https://www.reddit.com/r/pokemongodev/comments/524gcc/037_not_supported_on_rooted_devices/d7haglp)的安全网络服务。Niantic 确实让用户跳过了整个九码，因为这与 Android Pay 采用的方法相同。这意味着，如果你确实需要在根设备上运行 Pokémon GO，你需要经历整个 [Magisk 和无系统根](http://www.xda-developers.com/use-android-pay-with-xposed-without-rebooting-with-magisk/)的过程。或者完全不玩了，因为那是 Niantic 希望你做的。

**你对 Pokémon GO 锁定 root 用户有什么想法？请在下面的评论中告诉我们！**