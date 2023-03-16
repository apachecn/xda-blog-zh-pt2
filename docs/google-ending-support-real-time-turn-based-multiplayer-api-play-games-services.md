# Play Games Services 将终止即时和回合制多人游戏 API

> 原文：<https://www.xda-developers.com/google-ending-support-real-time-turn-based-multiplayer-api-play-games-services/>

# 谷歌将终止对 Play Games 服务中实时和回合制多人 API 的支持

Google Play 游戏服务将结束对实时和回合制多人 API 的支持，迫使开发者升级到 Firebase 或 Google Cloud。

移动游戏开发可能相当有利可图，但对于许多独立开发者来说，这只是他们为了好玩而做的事情。对于那些开发者来说，如果他们所依赖的服务不再免费，就不值得去维护一个游戏。这就是为什么一些开发者对谷歌[终止对用于制作即时和回合制多人游戏的](https://support.google.com/googleplay/android-developer/answer/9469745?hl=en) [Play Games 服务 API](https://www.xda-developers.com/google-describes-migration-new-play-games-services-apis/)的支持感到不安。

在几天前发给开发者的一封电子邮件中，谷歌宣布他们将在 Play Games 服务中终止对上述 API 的支持。从昨天起，[实时](https://developers.google.com/games/services/android/realtimeMultiplayer)和[回合制](https://developers.google.com/games/services/android/turnbasedMultiplayer)多人支持 API 被标记为不推荐，并且不可用于新游戏。目前在游戏中使用这些 API 的开发者必须在 2020 年 3 月 31 日之前，将他们的游戏迁移到替代产品，如 [Firebase 实时数据库](https://firebase.google.com/docs/database)或[谷歌云公开赛](https://cloud.google.com/blog/products/open-source/open-match-flexible-and-extensible-matchmaking-for-games)。

如果你计划支持跨平台多人游戏，切换到 Firebase 是有意义的，但实现它意味着你必须考虑如何制定你的隐私政策，因为数据会提交到 Firebase 控制台。然而，最重要的是，除了最基本的“星火计划”层，它[不是免费的](https://firebase.google.com/pricing)，这可能不足以支持大多数多人游戏。如果你确实想迁移到谷歌提供的替代方案，你可以使用这个表格向谷歌[寻求帮助。](https://support.google.com/googleplay/android-developer/contact/game_services)

除了放弃你一直在做的游戏，另一个选择是在托管服务上实现你自己的应用，尽管这对于一个激情项目来说可能太麻烦了。Google Play 游戏服务是免费的，对于简单的实时和回合制多人游戏来说足够好，但 Google 现在希望你支付一些现金，如果你想让游戏中的多人服务继续工作的话。我们的情报贩子的游戏可能会因为这个改变而被杀死，我相信至少你们中的一些人正在考虑类似的举动。

* * *

Kieron Quinn，谢谢你的建议！