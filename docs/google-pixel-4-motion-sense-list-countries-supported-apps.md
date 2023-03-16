# 谷歌 Pixel 4 的运动感应可以在 53 个地区和 23 个应用程序中工作

> 原文：<https://www.xda-developers.com/google-pixel-4-motion-sense-list-countries-supported-apps/>

去年的 Pixel 3 可能赢得了“历史上泄露最多的智能手机”的奖项，但 Pixel 4 已经非常接近击败它的前任。大量的 Pixel 4 泄露事件与它的软件有关，这要感谢众多在网上分享新应用的泄密者。新的 [Pixel 4 动态壁纸](https://www.xda-developers.com/download-google-pixel-4-live-wallpapers-port/)、 [Pixel Launcher](https://www.xda-developers.com/download-updated-google-pixel-launcher-4-swipe-down-notification-gesture/) 、 [Google Recorder 应用](https://www.xda-developers.com/google-recorder-app-pixel-4-download/)和 [Google Camera 应用](https://www.xda-developers.com/google-camera-7-0-google-pixel-4-leak-hands-on/)已经公开，但来自新 Pixel 的其他 apk 也已泄露。多亏了 [*Nextrift*](https://nextrift.com/) ，我们拿到了一个预发布的运动感应 APK，这是谷歌对 Soli 雷达手势的命名，它可以显示支持哪些国家和媒体应用。

对于那些最近没有跟上所有泄漏的人来说，这里需要一点背景知识。几年来，谷歌一直在研究它称为 Soli 的雷达技术。Soli 能够进行精确的手势检测，[谷歌正在用它来驱动 Pixel 4 上的运动感应手势](https://www.xda-developers.com/google-pixel-4-face-unlock-soli-gestures/),用于跳过歌曲、打盹闹钟或静音电话。Soli 对光不敏感，可以通过塑料材料工作，因为它的工作频率为 60GHz。由于这一无线电频率要求，谷歌需要[向国家监管机构认证 Pixel 4](https://www.xda-developers.com/pixel-4-fcc-wireless-charging-lte/) ，以允许在该范围内传输无线电频率。

如果谷歌没有完成 Pixel 4 在特定国家的认证，那么 Motion Sense 就不会在那里工作。我们已经看到[百思买登陆页面](https://www.xda-developers.com/pixel-4-soli-gestures-select-countries/)透露日本等国家将不会获得动作感应手势，但上周，[*9 to 5 谷歌*](https://9to5google.com/2019/09/26/pixel-4-motion-sense-38-countries/) 和我们一样获得了预发布的 APK，透露该功能将在 38 个地区工作。他们还[找到了](https://9to5google.com/2019/09/26/motion-sense-pixel-4-9-music-apps/)手势将支持的 9 个媒体应用的列表，这令人失望，因为我们假设手势会发送标准的意图来改变媒体轨道。

*9 到 5Google 发现了一个 APK 内支持 Motion Sense 的国家和媒体应用列表(包名为“com.google.oslo”)。支持的国家列表来自一个名为“isAvailableInCountry”的方法，该方法根据 38 个 MCC(移动国家代码)的列表检查手机的国家代码。)支持的媒体应用程序列表是在一个名为“SkipMediaTrack”的类中，在一个名为“isSupportedApp”的方法下找到的。*

然而，通过我们自己的挖掘，我们发现了 Pixel 4 的 Soli-radar 供电的运动感应手势支持的更完整的地区和媒体应用程序列表。事实上，我们认为目前至少支持 53 个地区和 23 个媒体应用程序，而不是之前报道的 38 个和 9 个。这是因为 *9to5* 找到的列表是在 APK 中硬编码的，它是从预发布的 Pixel 4 XL 中提取的。我们发现的列表在谷歌内部数据库中，用于控制其应用程序的配置值。更完整的国家列表来自一个名为“mcc_whitelist”的配置，而更完整的支持应用列表来自一个名为“media_app_whitelist”的配置，这两个列表都是针对“oslo”的，Oslo 是 Motion Sense 的代号。由于 APK 来自预发布的 Pixel 4 XL，而这个新列表来自谷歌内部数据库，我们认为我们的列表更准确，因为 APK 可能已经过时了。

## 动作感应应该工作的 53 个区域的列表

*   美属萨摩亚群岛
*   奥地利
*   澳大利亚
*   比利时
*   保加利亚
*   加拿大
*   克罗地亚
*   塞浦路斯
*   捷克共和国
*   丹麦
*   爱沙尼亚
*   芬兰
*   法国
*   法属圭亚那
*   法属印度洋领土(两个军事管制中心都列在清单上)
*   法属波利尼西亚
*   德国
*   希腊
*   瓜德罗普岛
*   关岛
*   匈牙利
*   爱尔兰
*   意大利
*   朝鲜；韩国
*   拉脱维亚
*   立陶宛
*   卢森堡
*   马耳他
*   马提尼克岛
*   荷兰
*   新喀里多尼亚
*   北马里亚纳群岛
*   挪威
*   波兰
*   葡萄牙
*   波多黎各
*   罗马尼亚
*   圣巴特梅
*   圣马丁岛
*   圣皮埃尔和密克隆
*   新加坡
*   斯洛伐克
*   斯洛文尼亚
*   西班牙
*   瑞典
*   瑞士
*   台湾
*   阿拉伯联合酋长国
*   联合王国
*   美利坚合众国
*   美属维尔京群岛
*   瓦利斯群岛和富图纳群岛

总共有 39 个国家，美国和法国的 13 个地区加起来构成了 52 个受支持地区的列表，加上一个，因为法属印度洋地区有两个 MCC。*9 to 5*发现的 MCC 列表仅提到美属维尔京群岛和美国 Somoa 为受支持地区，但我们的列表通过列出更多地区的 MCC 对其进行了扩展。我们的名单中最值得注意的是澳大利亚，百思买列为受支持，但没有出现在 *9to5 的*名单中。

有人怀疑谷歌 Pixel 4 是否会在所有这些地区销售。我们无法确认该设备将在哪些国家销售，并且该列表不应被视为意味着该设备将在特定国家销售。此列表仅告诉我们手势将在哪些区域被激活，因此如果您连接到未列入白名单的区域的网络，您将无法访问这些手势。

*   亚马逊音乐
*   昂哈密
*   苹果音乐
*   潮流音乐
*   温克音乐
*   伊海尔特拉迪奥
*   我们的音乐
*   加纳音乐
*   YouTube 音乐
*   Google Play 音乐
*   亨加马音乐
*   JioSaavn
*   珍妮音乐(Genie Music)
*   벅스(虫子音乐)
*   潘多拉
*   Napster 音乐
*   沙扎姆
*   SiriusXM
*   KKBOX
*   Spotify
*   Spotify 电台
*   Deezer 音乐播放器
*   美国酒类协会(American Wine Association)

我们发现有趣的是，JioSaavn、Wynk、Gaana 和 Hungama 都被列出来了，尽管印度没有出现在受支持地区的列表中，但有可能谷歌只是在为那些在印度以外使用这些应用的用户提供便利。也有可能他们正计划让运动感觉在这个国家发挥作用。

* * *

[由于](https://www.xda-developers.com/google-pixel-4-motion-sense-gestures-leak/) *[的泄露，这是今天的科技](https://www.xda-developers.com/google-pixel-4-motion-sense-gestures-leak/)，*我们确切地知道手势将如何工作。“跳过音轨”手势的工作原理是检测您何时向左或向右挥手,“静音”手势的工作原理是检测您何时在电话上挥手，而“伸手检查电话”手势的工作原理是检测您何时将手靠近电话。

*图片来源:[来自今日科技](https://www.youtube.com/watch?v=yp93W9kRvcw)的 m .李国豪。*

我们分析了 APK，可以确认没有任何隐藏的手势尚未被发现，这很不幸，因为我希望运动感应能够做得更多。尽管如此，我相信一旦手机发布，我们论坛上的某些人会想出如何定制或添加新的手势。

[**谷歌 Pixel 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**谷歌 Pixel 4 XL 论坛**](https://forum.xda-developers.com/pixel-4-xl)

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*