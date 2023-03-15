# Twitter 修改了其 API，为第三方应用提供了备受欢迎的功能

> 原文：<https://www.xda-developers.com/twitter-api-v2-3rd-party-apps/>

**更新 1(08/13/2020 @ 03:20PM ET):**Twitter 最初推迟了其新 API 的公开发布，因为在一场大丑闻之后这么快就推出它是不明智的，但该公司现在已经在近一个月之后推出了该 API。滚动到底部了解更多信息。下面保留了 2020 年 7 月 16 日发表的文章。

退一步说，Twitter 度过了有趣的一周。在众多高调账户[被劫持以推广加密货币骗局](https://techcrunch.com/2020/07/15/twitter-accounts-hacked-crypto-scam/)导致 Twitter 暂时停止许多已验证账户的新推文的一天后，这家社交媒体公司宣布对其 API 进行一些重大改变。他们称之为 Twitter API v2，这是自 2012 年以来首次重建的新基础。一些重要的变化将会影响我们熟悉和喜爱的第三方应用。

你可能知道，Twitter 的 API 给第三方应用开发者造成了很多摩擦。过去，由于达到了有争议的 100，000 令牌限制，许多受欢迎的 Twitter 客户端已经从 Play Store 中撤出。早在 2018 年，Twitter 做出了改变，即[从第三方开发者那里移除了关键功能](https://www.xda-developers.com/twitter-third-party-apps-api-changes/)。这些变化[在那年晚些时候](https://www.xda-developers.com/twitter-new-api-third-party-clients/)生效，尽管流行应用的开发者发起了一场运动。随着 API v2 的发布，这些关键特性中的一些最终将再次对开发者开放。

下面是 Twitter 对 API v2 新增功能的简要说明:

*   更易于使用的更简洁的 API，具有新的开发人员特性，如指定返回哪些字段的能力，或者在同一响应中从对话中检索更多推文的能力
*   API 中缺少的一些最受欢迎的功能，包括对话线程、推文中的投票结果、将推文固定在个人资料上、垃圾邮件过滤以及更强大的流过滤和搜索查询语言

最后一点是第三方 Twitter 应用的粉丝最应该感到兴奋的。认为第三方客户端不被允许显示投票、线程对话或显示固定推文是非常疯狂的。这些是任何人都希望在 Twitter 客户端看到的社交媒体平台的基本功能，它只会损害不使用官方应用程序的用户的 Twitter 体验。我们很高兴看到 Twitter 已经开放了这些功能。

以前，Twitter API 分为三层:标准(免费)、高级(自助付费)和企业。API v2 将用为适应不同开发人员群体而设计的产品轨道来取代所有三个层次。Twitter 表示，新歌有望让每个人都有所收获。以下是该公司对三个产品系列的描述:

*   标准版:首先提供，这将是大多数开发者的默认产品轨道，包括那些刚刚入门的，为了乐趣，为了一个好的理由，为了学习或教学而构建一些东西的人。我们计划将来在这条轨道上增加高架通道。
*   **学术** **研究** : [学术研究人员](https://developer.twitter.com/en/use-cases/academic-researchers)使用 Twitter API 了解公共对话中发生的事情。未来，合格的学术研究人员将有办法获得相关终端的提升或定制访问权限。我们还提供了[工具和指南](https://developer.twitter.com/en/use-cases/academic-researchers/helpful-tools)，让使用 Twitter API 进行学术研究变得更加容易。
*   **业务**:开发者在 Twitter API 上建立业务，包括我们的 [Twitter 官方合作伙伴](https://partners.twitter.com/en)和[企业数据客户](https://data.twitter.com/en/customers/enterprise-data)。我们喜欢他们的产品帮助其他人和企业更好地理解和参与 Twitter 上的对话。将来，该路线将包括对相关端点的提升或自定义访问。

Twitter 意识到旧的定价和费率限制限制了开发者，尤其是那些只是为了好玩而开发东西的人。随着这些变化，我们可以看到有趣的小 Twitter 工具和机器人在标准轨道上的复兴。说到这里，标准课程将于今天推出，而商业和学术/研究课程将“很快”推出每个轨道还包含基本、提升或自定义访问级别。这些曲目的定价目前尚未公布。

所有开发人员都可以通过免费的基本访问级别提前访问新端点的初始设置。有兴趣尝试这些功能的开发者可以注册一个开发者账户，然后在这里申请。公共路线图可在[这个 Trello 板](https://trello.com/b/myf7rKwV/twitter-developer-platform-roadmap)上获得，供开发者跟踪 API v2 的进展。

**来源:[推特](https://blog.twitter.com/developer/en_us/topics/tools/2020/introducing_new_twitter_api.html) | Via: [TechCrunch](https://techcrunch.com/2020/07/16/twitter-introduces-a-new-fully-rebuilt-developer-api-launching-next-week/?guccounter=1)**

* * *

## 更新 1:现已发布

Twitter 上个月公开了其针对第三方的新 API，但他们推迟了发布，因为该公司最近刚刚成为一次大型社会工程攻击的受害者。然而昨天，Twitter 更新了它的官方博客，指出新的 API 已经推出。感兴趣的开发者可以访问新的 [Twitter 开发者门户](https://developer.twitter.com/en/portal/opt-in)开始。