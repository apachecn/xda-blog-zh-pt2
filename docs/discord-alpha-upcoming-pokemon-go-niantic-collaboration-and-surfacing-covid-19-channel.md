# 不和谐阿尔法暗示即将到来的精灵宝可梦 GO 合作，并浮出水面新冠肺炎频道

> 原文：<https://www.xda-developers.com/discord-alpha-upcoming-pokemon-go-niantic-collaboration-and-surfacing-covid-19-channel/>

Discord 于 2015 年开始其旅程，当时是一家主要专注于游戏玩家的聊天服务，提供 VoIP 服务，以补充 MOBAs 中的实时策略。多年来，这项服务巩固了它作为聊天平台的地位，也成为 IRC 的一个很好的替代品。Discord 作为一个 app 和服务，允许用户为一个专门的伞形主题创建不同的服务器，然后在服务器内创建不同的通道，用于进一步的主题分叉。然后，用户可以在这些通道中相互交谈，并且您可以跟踪通道中预期的对话主题。Discord 最近越来越受欢迎，增加了一些功能，如[向朋友显示游戏活动](https://www.xda-developers.com/discord-android-game-detection/)、 [AMOLED 黑暗主题](https://www.xda-developers.com/discord-9-8-2-hidden-amoled-dark-theme-android/)、[临时静音、斜线命令](https://www.xda-developers.com/discord-android-993beta-temporary-mute-slash-commands-mark-unread/)、[二维码登录](https://www.xda-developers.com/discord-easy-pc-logins-qr-code-prepares-friend-sync/)等等。最新的 Discord alpha 透露，该应用正在与 Pokémon GO 合作，并通过 [Discover 功能](https://www.xda-developers.com/discord-tests-discover-feature-servers/)向更多用户提供有用的新冠肺炎频道。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

## 神奇宝贝 GO - Discord 合作

Discord v16 alpha 7 正在与 Pokémon GO 进行可能的合作，正如这些字符串所示:

```
 <string name="invite_pokemon_go_announcements_label_long">Get latest announcements for Pokemon GO raids in Los Angeles!</string>
<string name="invite_pokemon_go_announcements_label_short">Get latest announcements</string>
<string name="invite_pokemon_go_friendship_label_long">Make new friends who are also passionate about Pokemon GO in your area!</string>
<string name="invite_pokemon_go_friendship_label_short">Make new friends</string>
<string name="invite_pokemon_go_strategy_label_long">Share tips and strategy so you can train the strongest Pokemon!</string>
<string name="invite_pokemon_go_strategy_label_short">Share tips and strategy</string> 
```

鉴于新冠肺炎发布的健康建议，Pokémon GO 正在致力于[带来探索虚拟地图和从家中参与突袭战的能力](https://www.xda-developers.com/niantic-considers-adding-options-explore-raid-home-indoors-pokemon-go/)。这个提议的改变给 Niantic 提出了一个有趣的问题。到目前为止，Pokémon GO 避免在游戏中实现任何 P2P 通信方式(在我们看来，如果 Ingress COMM 体验是任何基准的话，这是一件好事)。因此，玩家不得不依靠在突袭战中与其他玩家偶遇，然后根据自己的判断互相分享联系人/即时消息的详细信息。

随着 Raid 战斗体验从室外转移到室内，这种与其他本地玩家交流和工作的机会将会丧失。4 星和 5 星的 Raid 战斗需要团队合作来完成，因为它们不能由一个单独的玩家成功完成。如果在 Discord 的最新 alpha 中发现的字符串有任何迹象，Discord 正在与 Niantic 合作，为玩家提供游戏之外的 IM 媒介，以便彼此交流。字符串表明，该功能将首先在洛杉矶进行测试，Niantic 在那里有一个办公室。Discord 服务器本质上将是本地的，主要集中在 Raid 战斗协调上。

和 Discord 合作 Pokémon GO 的想法其实很好。Discord 有大量的 VoIP 功能，这在人手不足的突袭战中很有帮助。用户也不需要在 Discord 上分享他们的个人身份，因为该服务使用用户名和数字标识符，不像 WhatsApp 等目前流行的替代品。Pokémon GO 将如何处理 Discord 及其服务器还有待观察——游戏内部是否会有任何集成，Niantic 是否会创建基于位置的区域服务器，或者用户是否可以创建区域服务器，然后提交给 Niantic。Niantic 尚未证实这一合作的任何方面，但他们确实在他们的[公告帖子](https://www.xda-developers.com/niantic-considers-adding-options-explore-raid-home-indoors-pokemon-go/)中暗示了一些事情，声明如下:“*我们正在增强我们在游戏中的虚拟社交功能，使玩家在现实生活中无法见面时能够保持联系*。最终实现还有待观察。

* * *

## 新冠肺炎-服务器发现

最新的 alpha 也包含这些新字符串:

```
 <string name="guild_discovery_covid_body">Visit the community-run Coronavirus Discord to talk about COVID-19, and head to [CDC.gov](%1$s) for more information.</string>
<string name="guild_discovery_covid_button">Visit COVID-19 Discord</string>
<string name="guild_discovery_covid_title">Stay safe and informed</string> 
```

这些字符串表明，Discord 将利用 [Discover 功能](https://www.xda-developers.com/discord-tests-discover-feature-servers/)引导用户访问社区运营的新冠肺炎服务器，在那里他们可以找到关于该主题的更多信息。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*