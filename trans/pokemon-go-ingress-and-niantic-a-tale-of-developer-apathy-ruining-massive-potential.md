# Pokémon GO，Ingress 和 Niantic:开发者的冷漠如何摧毁潜力

> 原文：<https://www.xda-developers.com/pokemon-go-ingress-and-niantic-a-tale-of-developer-apathy-ruining-massive-potential/>

2016 年 7 月初，世界目睹了一个让许多人目瞪口呆的现象。当世界上的人们通常低着头全神贯注于他们的智能手机时，人类的很大一部分正在向一个他们已经忘记存在的领域前进——户外世界。

随着越来越多的人试图冒险到户外捕捉神秘的生物，让他们想起重新做一个孩子的快乐，这种最初作为童年传说的一部分的东西很快改变了互联网居民的日常生活。

没错，我们说的就是 Pokémon GO。即使你在过去的一个月里住在一块岩石下，你也可能会碰到某个人，无论是成人还是儿童，在玩这款病毒游戏和寻找神奇宝贝时闲逛。我们不需要告诉你这个游戏是如何运行的——很有可能，你已经告诉了别人这个游戏是如何运行的。这款游戏在美国公开发售后，获得了巨大的需求和成功。需求如此之大，以至于发布地区以外的人继续在 Android **和** iOS 上下载游戏，导致服务器频繁中断以及登录和加载问题，以至于游戏在一段时间内充满了挫折感。

但是，即使有这些问题将人们从最基本的水平上推离游戏，他们仍然这样做。几天之内，整个社区都衍生出了 Pokémon GO。扑克竞走在当地组织起来(尽管服务器几乎不能工作)，企业开始利用现在在户外漫游并聚集在扑克站和健身房的 playerbase。T-Mobile 甚至出去为 Pokémon GO 应用程序提供免费数据，这一举动公然违反了网络中立性，否则会引起人们的愤怒。但是没有人会惊讶，因为在一天结束的时候，你必须抓住他们，而免费数据让这部分变得更容易。

## 三步错误

随着游戏开始扩展到越来越多的地区，游戏的开发商 Niantic Labs 致力于解决由压倒性需求造成的供应缺口。渐渐地，一小时又一小时，游戏服务器变得越来越稳定，能够容纳所有的在线玩家，一旦美国醒来就不会崩溃。在这个服务器强化过程中，Niantic 不得不与游戏的一个核心方面妥协，以确保人们至少可以登录(并保持登录)。这项功能通常被称为“3 爪印”或“3 足”神奇宝贝定位器，因为游戏中的用户界面会提示你附近有什么神奇宝贝，以及它们离你报告的位置大约有多远。

Niantic Labs 没有发布任何关于这项功能确切工作方式的官方细节或数字，但 playerbase 已经通过反复试验找到了机制。当你接近神奇宝贝的产卵位置时，显示在神奇宝贝下面的三个脚印的数量会减少——当脚印减少到零时，神奇宝贝就会出现在你的手机屏幕上。如果有足够的时间，玩家可以三角定位他们最喜欢的动物，并有机会捕捉它们。这个特殊的功能对于游戏的核心部分是至关重要的，即在“猎杀”神奇宝贝的同时探索你的周围环境。因此，当 Niantic 不得不**从服务器端**禁用功能，并基本上导致客户端游戏出错，并且总是显示每个神奇宝贝的恒定 3 步时，所有玩家都在呻吟和抱怨，但还是接受了这个决定。毕竟，这意味着他们至少可以登录游戏，亲身体验一下到底是怎么回事。

 <picture>![Pokemon GO's nearby feature back when it worked. Paw prints indicate approximate distance.](img/db5cb06e20e658980e1701c92c88e0bb.png)</picture> 

Pokemon GO's nearby feature back when it worked. Paw prints indicate approximate distance.

然后服务器稳定了。停电变得比我所在城市的迷你龙还少，人们开始享受快乐时光。游戏本身缺乏深度，但对神奇宝贝的热爱和游戏的社交方面仍然吸引着人们。大多数人都希望在不久的将来，这个游戏会修复被破坏的部分，所有人都会继续前进和发展。唉，绝大多数玩家都不知道(或不关心)这款游戏的开发者是 Niantic Labs，该公司唯一的其他游戏开发仍然是激烈的反开发者和边缘反玩家。

我为什么这么说？让我们倒退几年，看看 Ingress 发生了什么，然后我们将它与神奇宝贝的现状联系起来。对于任何一个 Ingress Beta 玩家来说，当前的 Pokémon 情况将会是一种巨大的似曾相识的感觉，我预测你会同意我们的观点。

## 入口和第三方开发

回到 2012 年末，当 Ingress 发布时，Ingress 的场景与 Pokémon GO 非常相似，尽管范围不同。Ingress 还处于起步阶段——应用程序经常崩溃，bug 比播放器还多，服务器故障也经常发生。一个人需要邀请才能加入游戏，邀请主要通过 Google+分发(Niantic 在成为 Alphabet 子公司之前是谷歌的一部分)。游戏的测试性质，以及 Google+本身的普通“早期采用者”受众意味着游戏是由技术娴熟的用户，或者换句话说，软件和硬件开发者玩的。

由于 Ingress 测试版非常容易出错、落后、资源密集，并且缺乏 Ingress 目前所具有的深度和易用性，一些开发人员自行修复了 Niantic 花了太长时间才修复的问题(假设他们想修复它——我们将再次讨论这一方面)。在大多数情况下，这些第三方开发者在没有任何金钱激励的情况下修复了游戏中的许多错误，并经常开源他们的修改，以便用户和 Niantic 本身可以看到发生了什么变化。

一个这样的开发者是 XDA 认可的开发者 [Brut.all](http://forum.xda-developers.com/member.php?u=1922851) ，这个人[在 2010 年创建了 apktool](http://forum.xda-developers.com/showthread.php?t=640592) 用于逆向工程 apk 文件(是的，就是那个人)。Brut.all 打造了一款 [**开源**修改](http://forum.xda-developers.com/showthread.php?t=2289699)的官方(和闭源) Ingress 应用，比 Niantic 更“优化”Ingress 可以优化自己的游戏。这项名为 [Broot Mod](http://forum.xda-developers.com/showthread.php?t=2289699) 的修改，通过缩小图形，使游戏可以在 ldpi 和 mdpi 分辨率下玩，可以选择禁用游戏坚持要有的各种花哨的图形动画，并有一个方便的库存管理图表。所有这些特征都是生活质量的改变，如果你进入，生活会变得更容易。由于是开源的，这些修改本可以被重新整合到游戏中，从而让每个人的生活变得更加轻松。

 <picture>![Screenshot of Broot Mods inventory management summary. Such a feature remains unimplemented in Ingress till this day, despite its usefulness and demand.](img/17146e0ea5a486b43c259f8ade51b601.png)</picture> 

Screenshot of Broot Mods inventory management summary. Such a feature remains unimplemented in Ingress till this day, despite its usefulness and demand.

但是 Niantic 做了唯一一件迎合技术社区早期用户的游戏不应该做的事情:他们[向一个独立的第三方开发者发出了停止通知](http://forum.xda-developers.com/showthread.php?p=42027875#post42027875)。尊重 Niantic 的意愿，Broot Mod 的开发被主要开发者中止，但其他独立开发者接过了接力棒，因为这是一个开源项目。Niantic 不满足于一次开发压制，最终**禁止所有阅读任何非官方 apk 的用户**。引用他们的服务条款，明确禁止任何和所有第三方软件和修改，玩家群必须学会与 Niantic 的低于标准和蜗牛速度的官方开发 Ingress 一起生活，以免他们希望自己的帐户被禁止。好吧，很公平。

入口有另一个非常受欢迎的修改。这不依赖于 apk，而是作为 Ingres 的另一个工具之上的一个层。入口有一张地图，上面显示了“入口”和游戏中的链接和领域机制。就像官方 apk 一样，[官方地图网站](http://www.ingress.com/intel)很慢，很慢；可怜的 UX，在早期(现在)是一段可怕的经历。为了解决这个问题，第三方开发者再次为基础网站创建了一个非官方的开源脚本，名为[Ingress Intel Total Conversion](http://iitc.jonatkins.com/)(简称 IITC)。不用说，尼安蒂克不爱 IITC。虽然，在 IITC 用户的大规模社交活动之后，Niantic 现在对这个脚本视而不见，但**仍然不承认建立在自己工作基础上的一个非常优越的工具**的存在。只是将用户群体积极想要的东西重新整合到官方资源中...

## Pokémon GO 和第三方开发

所以现在我们又回到了神奇宝贝 GO 和它坏掉的 3 步神奇宝贝追踪器。为了填补 Niantic 为玩家留下的在旅途中狩猎神奇宝贝的空白，玩家基地再次转向...*惊喜惊喜*，第三方修改。由于 Pokémon GO 没有 Ingress 拥有的“地图”(尽管 Pokémon GO 提升了 Ingress 门户数据库以填充其自己的神奇宝贝站和健身房)，第三方开发者创建了实时绘制 Pokémon 现场观看地图的工具。这些工具利用了 Pokémon GO 与服务器通信的相同方式，因为它模仿了在游戏的有限地理半径内扫描 Pokémon，然后使用一系列这些扫描来填充几乎实时的地图。最终结果是，玩家现在可以找到他们最近的神奇宝贝，尽管游戏中的追踪器坏了！耶！

 <picture>![Python based script for locating Pokemon. Many websites emerged that offered similar functionality in easy to use manners.](img/f221c9b76cad308ef794ce15fa90a02a.png)</picture> 

Python based script for locating Pokemon. Many websites emerged that offered similar functionality in easy to use manners.

### 除...之外...

Niantic 最近杀死了大多数追踪者。没错。就在 Niantic 首席执行官 John Hanke 说他不喜欢这些追踪网站的做法之后，这些追踪网站已经不再这么做了。

> 你对[神奇宝贝雷达](http://www.forbes.com/sites/ryanmac/2016/07/27/pokevision-pokeradar-pokemon-go-apps/#14eaacee4971)和那些挖掘代码并显示神奇宝贝在哪里繁殖的东西有什么感觉？
> 
> JH:对，我不太喜欢那样。不是粉丝。
> 
> 我们现在有优先考虑的事情，但是他们将来可能会发现这些事情可能行不通。人们只是在伤害自己，因为这让游戏失去了一些乐趣。人们试图从我们的系统中窃取数据，这违反了我们的服务条款。

这些追踪地图中最受欢迎的是神奇宝贝。它受欢迎的原因是易于使用，因为它不需要最终用户进行任何设置。看到几乎每个人都可以访问 Pokémon GO，这对于在追踪器崩溃时期移动的每个用户来说都是一个福音。但事实证明，PokéVision 被最近更新的 Pokémon GO 游戏关闭了。

### 好吧，网站关闭了。但是你说游戏的更新出来了，对吗？它修好了追踪器，对吧？

不。事实上，坏掉的三步跟踪器从作为 bug 的**变成了作为特性的****。 [Niantic 选择完全移除 3 步追踪器](http://www.androidpolice.com/2016/07/30/pokmon-go-update-fixes-the-footprints-tracker-by-removing-it-adds-avatar-adjustment-and-other-tweaks/)，因此玩家根本看不到 3 个爪印，只是在某处模糊地显示出神奇宝贝*。结合流行的扫描神奇宝贝的方法也不复存在的杀戮，玩家群非常沮丧和*咸*因为 Niantic 实际上从 Pokémon GO 中删除了神奇宝贝狩猎方面。***

 ***## 开发者冷漠:零沟通版

但是故事并没有就此结束。Reddit 的 Pokémon GO subreddit 上的许多投诉表明，如果公司真的承认这个问题并保证他们正在解决这个问题，玩家仍然可以为了 Pokémon 而经历这一切。

问题是，如果有一件事 Niantic 做得比支持第三方开发者更差，那就是与它的玩家群沟通。这是 Ingress 的一个问题，目前的症状也不看好 Pokémon GO。玩家们长期以来想要的入口特性花了几年时间才实现(物品多点掉落，有人吗？)，但大多数建议都没有这么幸运，因为它们还没有被公之于众，即使它们有潜力极大地改善游戏性。更糟糕的是，Niantic 甚至不承认 Ingress 应用程序或其游戏机制存在问题，也不承认他们正在听取玩家的反馈(更不用说整合它了)。对沟通的冷漠和漠不关心是如此之多，以至于 2-3 年前提交门户网站的玩家(回到门户网站提交被允许的时候)仍然在等待 Niantic 关于门户网站是被批准还是被拒绝的回复。看到入口的存在如何成为 Ingress 游戏(以及现在的 Pokémon GO)的一个重要驱动因素，人们会期望稍微好一点。

诚然，Ingress 没有 Pokémon GO 那么成功，所以他们当时的响应时间让人感觉......过得去。但看到他们如何在 Pokémon GO 上取得巨大成功，这款游戏使用了来自一个成熟的特许经营权的知识产权，以及该公司除了谷歌以外还有其他股东，人们预计 Niantic 会加强他们的游戏。他们正在加速他们的游戏，因为他们还在招聘社区经理。但在这种情况发生之前(这种情况已经持续了一段时间，所以我不会屏住呼吸)，Niantic 没有就这些问题进行任何沟通。服务器宕机，应用崩溃，丢失或冻结扑克球，缺乏战略深度或**该死的 3 步跟踪器**；Niantic 仍然是一个与玩家群体互动的可怕例子，玩家群体是他们病毒式成功的直接原因。事实上，当我们在一篇关于[的讨论文章中问我们的读者是什么让一个应用程序值得为](http://www.xda-developers.com/what-makes-an-app-worth-paying-for/)付费时，很大一部分人都同意**如果人们期望为它付费，一个有沟通能力的开发者是必要的**。Niantic 希望你购买游戏中的物品和一个看起来很有趣的可穿戴设备，甚至计划添加赞助地点——来吧！

 <picture>![Google Play Apologizes in Advance for Pokemon GO](img/2fa202e274b96cf54b394f87bd7f6cd2.png)</picture> 

Google Play Apologizes in Advance for Pokemon GO

玩家保持愤怒但保持安静只是时间问题。一旦大多数人受够了，他们就会开始用评论影响游戏的声誉。在《神奇宝贝 GO 》(非官方)子版块中有如此多的抱怨和愤怒的帖子，以至于版主不得不为所有的抱怨创建一个大帖子。现在存在一些线索和讨论，指导玩家让他们的意见更容易被听到，包括但不限于:[在商店](https://www.reddit.com/r/pokemongo/comments/4vhx98/effect_of_july_31st_release/)将应用程序评级为 1 星，要求为他们在游戏中购买的产品退款，取消他们的 Pokémon GO Plus 可穿戴产品订单，联系 Niantic 和其他所有合作伙伴，希望他们的声音被听到。见鬼，你知道这是一个问题，即使 [Google Play 已经有了一个道歉](https://www.reddit.com/r/pokemongo/comments/4vl1tl/google_play_now_has_an_apology_for_pokemon_go_in/)，重定向你到 Niantic。

人们痴迷于 Pokémon GO，然后 Niantic Labs *带走了*。现在观众很愤怒，但是尼安蒂克还是尼安蒂克。我从 Ingress 学到的一个教训是，即使事情变得糟糕，沟通也有助于保持某人的信任。

Niantic 在其一场比赛的历史中从未面临过这样的反应，其过往记录也没有显示出它有能力独自处理这场火灾。这也是第一次，它对第三方开发者和他们的工作的憎恨给他们带来了无法预料的后果。Niantic Labs 曾经承诺为 Ingress 提供一个 API，但现在它面临着愤怒的客户群，这直接影响了它的百万美元收入、声誉和神奇宝贝知识产权的声誉。

 <picture>![Pokemon GOs average rating. Guess when the new update released.](img/1d3f1b9eabb71730906463626bf8320d.png)</picture> 

Pokemon GOs average rating. Guess when the new update released.

如果开发商 Niantic Labs 继续对其用户漠不关心，Pokémon GO 将从一个社会现象变成失败的客户服务的历史教训。非常感谢对当前问题的修正，但是在这些修正到来之前，你至少应该承认问题的存在。

我们希望 Niantic Labs 解决他们的沟通问题，并改善他们对第三方开发者的态度。当他们这么做的时候，他们也看了看游戏中所有的骗子。

现在请原谅我正在为这个我永远也找不到的丢失的迷你龙而愤怒。

*专题图片鸣谢:Reddit 用户[pt rain 377](https://www.reddit.com/user/ptrain377)*

**你对 Pokémon GO、Ingress 和 Niantic Labs 有什么看法？请在下面的评论中发表意见！*****