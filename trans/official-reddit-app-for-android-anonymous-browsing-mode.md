# Android 的官方 Reddit 应用现在有了匿名浏览模式

> 原文：<https://www.xda-developers.com/official-reddit-app-for-android-anonymous-browsing-mode/>

Reddit 通常被称为互联网的首页，它的自发性和受欢迎程度来自于围绕各种主题细分的社区。现有的系统允许个人发布内容，然后其他人可以根据内容是否适合主题片段和他们的观点对内容投赞成票或反对票。这些赞成票和反对票决定了该内容进一步获得多少关注。因此，个人是 Reddit 功能的中心。一些用户可能不理解 Reddit 可以个性化推荐的事实。为了迎合这一特定需求，Reddit 的官方应用[引入了匿名浏览模式](https://www.reddit.com/r/changelog/comments/hbm5eh/introducing_anonymous_browsing_on_android/)。

顾名思义，匿名浏览允许用户浏览 Reddit 移动应用程序上的内容，而无需将搜索和查看的社区等活动与用户的 Reddit 帐户相关联。官方声明规定，在匿名浏览中，Reddit 不会:

*   将您的浏览或搜索历史保存到您的 Reddit 帐户
*   使用您的 Reddit 活动个性化您的推荐
*   使用您的 Reddit 活动向您发送个性化通知

当然，当用户匿名浏览时，他们将无法发帖、投票、评论或采取其他需要帐户的行动。但是，在登录档案和匿名浏览之间切换很容易，没有痛苦，所以当需要交互时，人们总是可以切换回来。如果匿名浏览会话在 30 分钟内不活动，会话将结束，用户将切换回上次活动的配置文件。

公告帖子进一步详细说明了该功能与简单注销以及之前的匿名浏览模式(简单模拟注销行为)有何不同:

### 新行为

1.  当您开始匿名浏览会话时，该会话会被分配一组新的唯一 id，因此该会话与您的 Reddit 帐户之间没有任何联系。这就像你每次启动匿名浏览会话时都在用一组新的 id 创建一个新的帐户。
2.  因为唯一的 id，Reddit 的个性化引擎在你每次进入和退出模式时都会重置(对引擎来说，在匿名浏览会话期间，你看起来像一个新手，没有搜索历史)。
3.  在匿名浏览时，您也不会收到基于您在会话期间的 Reddit 活动的个性化推送通知(您在匿名浏览期间收到的任何个性化通知都将与您登录的 Reddit 帐户之前的活动相关)。
4.  当您退出匿名浏览会话时，您会返回到之前使用的帐户，Reddit 会清除并删除您正在使用的设备上该会话的浏览和搜索历史记录。在会话期间收集的任何数据仅连接到唯一的 id，而不是您的 Reddit 帐户。

Android 应用程序的官方 Reddit 正在推出匿名浏览功能。要使用此功能，请点击您的个人资料图片，然后点击用户名以打开帐户列表，并选择新选项。

虽然大多数 Redditors 更喜欢不同的第三方客户端访问网站，但官方应用自推出以来一直持续受欢迎。Android 应用程序的官方 Reddit 在过去获得了几项关键更新，如[剧透和 NSFW 标记，账户切换](https://www.xda-developers.com/reddit-for-android-3-41-spoiler-nsfw-tagging-account-settings-prepares-gif-animated-emote-comment/)，[查看子编辑维基的能力](https://www.xda-developers.com/reddits-official-android-app-view-subreddit-wikis-easier-format-links/)，[在发布高度温和的子编辑之前显示警告](https://www.xda-developers.com/reddit-tests-posting-warnings-moderated-subreddits/)，[黑暗模式](https://www.xda-developers.com/reddit-for-android-android-q-dark-mode/)，[和更多](https://www.xda-developers.com/tag/reddit/)。

* * *

**来源:[/r/changelog](https://www.reddit.com/r/changelog/comments/hbm5eh/introducing_anonymous_browsing_on_android/)**