# XDA，精灵宝可梦 GO &骗子:随着骗子蜂拥至我们的论坛，位置欺骗线程的流量增加

> 原文：<https://www.xda-developers.com/xda-pokemon-go-cheats-traffic-increase-in-location-spoofing-threads-as-cheaters-flock-to-our-forums/>

当 Ingress 在 2012 年作为封闭测试版推出时，书呆子和极客蜂拥至 Google+，寻找获得一种新的移动体验邀请的方法。到底是哪一款游戏需要你穿越整个城市才能玩并统治世界呢？

增强现实、基于地理位置的交互和社交团队合作都是 Ingress 中混合在一起的酷概念，它抓住了许多技术爱好者的想象力，给了他们一个最终走出户外与人互动的理由。 ***还是做到了...？***

如果你在过去玩过 Ingress，你会知道在每一场比赛中都存在的问题:作弊。由于入口是一个独特的概念，其基于位置的交互是其主要的差异化点，这也是游戏中最可利用的领域之一。毕竟，你的“位置”只有在你手机的 GPS 传感器反馈回来时才是准确的。如果你是一个技术爱好者(如果你在 Ingress Beta 中使用 Google+，你很有可能是)，你就会知道操纵和修改所有这些感官数据是多么容易。

这正是 Ingress 发生的事情。从其仅限邀请的测试版到今天，Ingress 继续受到位置欺骗者的困扰。这些“玩家”(和/或机器人)修改他们的位置，在他们不在的地方玩游戏。谷歌成立之初负责 Ingress 的团队当时自称为 Niantic Labs，现在以 Niantic Inc .的名义独立运营，该团队对 banhammer 非常严厉，其反作弊算法也不透明。如果你被其他玩家发现进行位置欺骗，并随后被报告了足够的证据(这个过程需要时间，但它通常是有效的)，或者你触发了团队多年来在 Ingress 中建立的几个反作弊机制(无论是作弊还是其他)，你会收到一个不会加载地图的帐户。永远不会。

> 那么，神奇宝贝在这幅图中处于什么位置呢？

你肯定听说过所有关于围棋的流行，我们不会用它有多大和有多大影响力的细节来烦你。但是，在 XDA 开发者大会上，我们注意到了一个有趣的趋势，那就是我们在论坛上的一些帖子。这一趋势表明，委婉地说，并不是每个人都在“探索自己的领域”。一些精选主题的受欢迎程度有非常明显的增加，这与 Pokémon GO 的发布和受欢迎程度相吻合。在 Pokémon GO 之前，其中一些线程以自己的方式流行，但幕后数字的新一轮增长表明，通过位置欺骗的方式作弊在 Pokémon GO 中相当猖獗(或者至少是诱人的)。

以下是超级流行的[超级线程](http://forum.xda-developers.com/showthread.php?t=1538053)在游戏发布时的趋势:

 <picture>![SuperSU](img/91a41472c81ce8436f1b926568a52ed0.png)</picture> 

SuperSU Thread Popularity

在 Android 设备上伪造你的位置的第一步包括在你的手机上找根。SuperSU 是一个超级用户访问管理工具，仍然是一个流行的和经常推荐的选择，以控制哪些应用程序可以在您的设备上拥有 root 访问权限。事实证明，在 Pokémon GO 退出邀请阶段前后，对 SuperSU 线程的访问增加了。随后，这一突如其来的飙升变得平缓，但仍然高于《精灵宝可梦 GO》发布前的水平。只是说说，你知道...

位置欺骗的下一步是利用 Android 上的位置编辑应用。我们的论坛上有一些在 Pokémon GO 之前就已经存在的用于位置欺骗的应用程序，这种趋势当然很明显。

[假安卓位置](http://www.xda-developers.com/fake-android-location/)帮助页面:

 <picture>![Fake Android Location](img/338d765cf2366103d8f7324d80170186.png)</picture> 

Fake Android Location Page Popularity

[漂浮物假定位 App](http://forum.xda-developers.com/android/apps-games/app-floater-fake-location-floating-fake-t3397641) :

 <picture>![Floater Fake Location](img/cd411fa48d58a68e57c437cd354e32d4.png)</picture> 

Floater Fake Location Thread Trend

这个特定的线程是最近创建的，但随着应用程序成为牢记游戏运动机制的首选推荐，数字一直在稳步攀升。

一些欺骗方法需要使用 Xposed 框架和几个模块，以试图更好地欺骗和防止欺骗。显然，几个依赖位置的应用程序有额外的限制需要跳过，而 Xposed 框架使几个限制更容易绕过。

同样，《神奇宝贝 GO》的效果在几个区域都清晰可见。[曝光论坛](http://forum.xda-developers.com/xposed)的访客趋势:

 <picture>![Xposed](img/550fa6d7eaedf6e490bb5c456f9e5772.png)</picture> 

Xposed Forum Popularity

[暴露的安装程序主线程](http://forum.xda-developers.com/showthread.php?t=3034811):

 <picture>![Xposed Installer Main Thread](img/d01b11bd4abcb84dc4944a3880b8c0aa.png)</picture> 

Xposed Installer Main Thread Popularity Trend

[Lataclysm 伪定位模块](http://forum.xda-developers.com/xposed/modules/mod-lataclysmfake-location-t3230816):

 <picture>![Lataclysm Fake Location Module](img/4c28db5431be4c3a10e04de875ee6895.png)</picture> 

Lataclysm Fake Location Module Thread Trend

[MockMockLocations 暴露模块线程](http://forum.xda-developers.com/xposed/modules/mod-mockmocklocations-prevents-apps-t2910660):

 <picture>![MockMockLocations](img/ae270242baeeea65433c0b9a787d2f44.png)</picture> 

MockMockLocations Thread Popularity Trend

这些数字给了我们一个非常清晰(但在某种程度上，阴暗)的画面。自从 Pokémon GO 公开以来，Xposed 论坛的流量平均增加了 52%。MockMockLocation Xposed 模块线程的流量是 Pokemon Go 之前的 20 倍，新创建的 Floater Floating Location 线程的流量也是我们通常看到的 21 倍。

我不是说很多人在 Pokémon GO 上作弊。但是在启动后的几天内，有大量的人成功达到了 20+级，却没有太多关于入口地标或者如何使用他们的腿的知识，这让我很怀疑。这一点，以及人们用来进行位置欺骗的工具的受欢迎程度突然超常增长，表明 Niantic 对《精灵宝可梦 GO》的 banhammer 有点手软。这是因为这款游戏非常受欢迎，还是因为农村地区缺少神奇宝贝，还是因为他们有更优先的任务，如全球推广和服务器问题要解决，目前还不得而知。

现在，一些人*正在*报告他们在 Pokémon GO 中收到了临时禁令，禁令的描述表明 Pokémon 会逃跑，Pokéstops 不会给物品，他们的禁令会在 15 分钟到 6 小时的时间内重置。然而，资深玩家会记得这是 GPS 跳跃的后果，当手机 GPS 较差时，这种情况甚至经常发生在合法玩家身上。Ingress，很可能还有 Pokémon GO，都是基于你的旅行速度来计算你从 A 点到 b 点的旅行速度。如果两者之间的时间很短，并且显示出上帝般的速度，游戏会将你置于软禁令状态，直到正常人以合理的速度旅行通过这段距离。Ingress 目前还将用户置于速度锁定状态，如果他们的速度超过大约 30 英里每小时(/50 公里每小时)，所以这可能是《精灵宝可梦 GO》中相同的算法。然而，与 Ingress 不同，我还没有在 Reddit 等平台上看到任何关于 Pokémon GO 的明确禁令。

这并不意味着《精灵宝可梦 GO》或者我们 XDA 的开发者鼓励作弊。事实上，我将强烈强调游戏的整个要点是社会同化，地理欺骗从多人“现实生活”游戏的整个体验中带走。从我 2012 年 12 月加入 Ingress 时的个人经历来说，游戏的社交角度和地理发现方面是让 Ingress 和 Pokémon GO 成为如此令人愉快的体验的原因。对我来说，进入是一个走出家门，克服我个人内向性格的借口。它帮助我与人交往，解决我的社交尴尬，给我经验和信心去冷火鸡地接近人们。团队动力是 Ingress 的重要组成部分，虽然 Pokémon GO 目前缺乏任何重要的团队元素，但他们肯定会增长，因为这款游戏已经比 Ingress 更受欢迎，[第三方解决方案已经开始涌现。你需要给游戏一个提高的机会**你**:不要把游戏和“赢”或者打败他们当成最终目标。把它看作是一个通往更好的社会生活和提高对周围环境的认识的旅程，同时成为最好的，就像从来没有人一样，一次一个新的神奇宝贝。](https://www.reddit.com/r/pokemongo/comments/4sq5y3/real_nice_pokemon_go_localized_chat_that_lets_you/?st=iqo3xivd&sh=50dd94fe)

我想用**不要欺骗**这句话来结束这篇文章。不仅因为有一天 Niantic 可能会禁止你，还因为你玩错了。

**你同意《精灵宝可梦 GO》中的位置欺骗概念吗？请在下面的评论中告诉我们你的想法！**

*编者按:我们不提倡也不纵容为了抓神奇宝贝而使用作弊工具。在 XDA，我们是真正的培训师，并为我们的多多系列感到自豪。至少我们合法地抓住了他们。*