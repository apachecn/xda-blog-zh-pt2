# [更新:谷歌的回应]猎豹移动被指控在几个应用程序中进行广告欺诈

> 原文：<https://www.xda-developers.com/cheetah-mobile-ad-fraud-android-apps/>

Play Store 中有超过 260 万个应用程序，谷歌一直在与困扰其生态系统的欺诈和恶意应用程序作战。与此同时，谷歌试图推广高质量的应用程序供用户享受，尽管有时他们选择的应用程序质量可疑。猎豹移动可能是我们用户中最臭名昭著的开发公司之一，因为他们收集用户数据和提供大量粗略广告的做法。他们对 QuickPic 的收购导致许多 XDA 会员争相寻找曾经被高度推荐的 gallery 应用的替代品。但是，尽管猎豹移动的产品质量很差，我们从来没有任何理由怀疑他们有任何真正的恶意——直到现在。来自 [Kochava](https://www.kochava.com) 的最新研究向 *BuzzFeed News* 提供了证据，证明猎豹移动的几个安卓应用和 Kika 的一个应用涉嫌广告欺诈。

## 一些背景

尽管猎豹移动以在 Android 上开发应用程序而闻名，但它实际上是一家专注于销售数据的公司*。他们一点也不隐瞒这个事实，尽管很多用户都没有意识到这一点。然而，用户很难确切说出*猎豹移动如何使用他们收集的数据。Clean Master 是 CM 开发的一款下载量超过 10 亿次的应用，旨在清理 Android 设备上的缓存。然而，Kochava 指责猎豹移动在 Clean Master 等应用程序中使用额外权限，作为广告欺诈计划的一部分。*

根据 AppBrain 的数据，Kika Keyboard 是 Play Store 上一款受欢迎的第三方键盘应用，下载量超过 2 亿次。Kika Keyboard 不属于猎豹移动，但该应用程序也被发现从事类似的行为。

*猎豹移动运营一项名为“[猎豹数据](http://data.cmcm.com/)的服务，该服务“基于猎豹移动产品矩阵积累的海量数据构建全面的产品指数。”感谢[蒂尔·科特曼](https://medium.com/melon-pancakes/cheetah-mobile-a-web-of-trash-2f2ee875f6e5)为我们指出这一点！

## 广告欺诈

为了收回开发成本，一些开发人员通过在他们的应用程序中放置广告来创收。开发者有时可以因为推荐用户安装广告中显示的其他应用程序而获得奖金。奖金通常从 0.5 美元到 3.00 美元不等。该系统是这样工作的:你展示一个展示另一个应用程序的广告，用户下载赞助的应用程序并运行它，然后赞助该广告的应用程序将奖励推荐应用程序的开发者。Kochava 通过 BuzzFeed News 的报道声称，当他们的应用程序可能不会在推荐用户下载应用程序方面发挥直接作用时，猎豹移动要求获得推荐奖金。如果属实，这将从谷歌和通过广告将其应用货币化的开发者那里净赚 CM 的钱。下面是典型的广告推荐流程(左图)与假想的劫持广告推荐流程(右图)的对比。图片由 *BuzzFeed 新闻*提供。

这可以通过欺骗 Google Play Install Referrer API 来实现，CM Master 和大多数 CM 应用程序都可以访问这个 API。Kochava 的研究还发现，作为这一计划的一部分，猎豹移动在其应用程序中主要使用内部开发的库和 API，猎豹移动称这些都是他们无法控制的第三方 API。

## 受影响的应用

以下是涉嫌参与欺诈性广告计划的应用程序列表。如果您的任何 Android 设备上安装了它们，我们建议您立即卸载它们。

1.  清洁母版
2.  安全主管
3.  CM 发射器 3D
4.  Kika 键盘(归 Kika Tech 所有)
5.  电池医生
6.  猎豹键盘
7.  CM 储物柜
8.  CM 文件管理器

令人担忧的是，世界上一些最大的设备制造商过去已经使用过这些应用程序。例如，三星通过在三星体验中实现 Clean Master 和[指导用户](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=%5BUpdate%3A+Google%27s+Response%5D+Cheetah+Mobile+is+accused+of+committing+Ad+Fraud+in+several+apps&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fcheetah-mobile-ad-fraud-android-apps%2F&u1=UUxdaUeUpU22978&url=https%3A%2F%2Fwww.samsung.com%2Fuk%2Fsupport%2Fmobile-devices%2Fhow-do-i-manage-my-apps%2F&ourl=https%3A%2F%2Fwww.samsung.com%2Fuk%2Fsupport%2Fmobile-devices%2Fhow-do-i-get-the-clean-master-speed-booster-app-on-my-samsung-galaxy-device%2F)安装应用程序来推广 Clean Master。微软已经与猎豹移动合作，在 CM Launcher 3D 中实现了该公司的数字助理 Cortana。

## 猎豹移动的结论和声明

正如你所怀疑的，猎豹移动的主要兴趣是出售你的数据。但这一最新发展表明，他们可能愿意在使用授予他们的应用程序的权限方面做得更多。如果这个广告欺诈计划是真的，它不仅滥用了用户的信任，窃取了谷歌的收入，也窃取了开发者的收入，而这些开发者原本应该获得推荐奖金。我们希望谷歌继续调查这些应用程序，如果他们证实了 Kochava 的发现，就从 Play Store 中删除它们。至于用户，我们建议您卸载上一节中列出的应用程序，同时记住该列表可能不全面。为了确保您的设备安全，请确保始终检查应用程序请求的权限，并对应用程序背后的团队进行一些研究。

如果你想阅读猎豹移动和 Kika 提供的完整声明，请点击此处的链接[查看最初的 *Buzzfeed 新闻*报道](https://www.buzzfeednews.com/article/craigsilverman/android-apps-cheetah-mobile-kika-kochava-ad-fraud)。猎豹移动也通过[的新闻稿](https://www.prnewswire.com/news-releases/cheetah-mobile-responds-to-recent-article-regarding-app-installation-attribution-300755861.html)跟进此事，声明公司“正在与所有 SDK 提供商沟通，调查这些指控。”新闻稿继续表示，CM“致力于防止其应用程序中集成的任何 SDK 参与不当活动，如果发现任何 SDK 提供商参与欺诈活动，将暂停与他们的业务合作。”在第二份后续新闻稿中，该公司声明他们“对这些第三方广告平台没有控制权”，“既没有意图也没有能力指导这些广告平台参与所谓的‘点击注入’。”最后，CM 宣布，他们已经“计划对 Kochava 等政党采取法律行动”，他们认为这些政党“产生并传播了那些不真实和误导性的声明”。"

## 更新:谷歌移除两款应用

据 BuzzFeed 新闻 报道，谷歌已经通过从 Play 商店移除 CM 文件管理器和 Kika 键盘对该报道做出回应。“我们非常重视这些指控，我们的 Google Play 开发者政策禁止我们平台上的欺骗性和恶意行为。如果一个应用违反了我们的政策，我们会采取行动，”谷歌发言人告诉 *BuzzFeed 新闻*。猎豹移动和 Kika 可以对这一决定提出上诉，但据 BuzzFeed News 报道，这两款应用已经从谷歌的 AdMob 移动广告网络中移除。猎豹移动发布了一份[新闻稿](https://finance.yahoo.com/news/file-manager-app-contributed-0-142000662.html)回应 CM 文件管理器的移除，称 CM 文件管理器是一款“就对公司的收入贡献而言并不重要的应用。”报告首次发布后，电池医生和 CM 启动器都被猎豹移动自愿下架，但尚未返回 Play 商店。更多信息请阅读[原文 *BuzzFeed 新闻*报道](https://www.buzzfeednews.com/article/craigsilverman/google-removes-cheetah-kika-apps)。

* * *

*本文于 2018 年 11 月 27 日下午 7:58(美国中部时间)更新，以反映猎豹移动对被指用于广告欺诈计划的 API 的立场。*

*本文于 2018 年 11 月 28 日上午 9 点 44 分进一步更新，以回应猎豹移动法律团队的询问。*

本文于 2018 年 12 月 4 日下午 2 点 14 分更新，添加了谷歌对指控的回应。