# 据报道，谷歌 Play 商店无法在搜索中显示新发布的应用

> 原文：<https://www.xda-developers.com/google-play-store-reportedly-failing-show-newly-published-apps-search/>

**更新(美国东部时间 12/18/19 @下午 4:15):**谷歌修复了 Play Store 的一个错误，该错误阻止了新发布的应用程序显示在搜索结果中。

在过去的几个月里，谷歌为 Play Store 引入了几个新功能。Play Store 最近收到了 Android 10 上的[新黑暗主题](https://www.xda-developers.com/google-play-store-dark-theme-android-10/)、退订测试版的[一键按钮、清晰愿望清单](https://www.xda-developers.com/google-play-store-one-tap-unsubscribe-betas-clear-wishlists/)等。我们甚至已经看到了[即将推出隐姓埋名模式](https://www.xda-developers.com/google-play-store-warn-install-unknown-apps-sideload-permission/)的暗示。但是，尽管谷歌可能正在努力开发这些新功能，但谷歌 Play 商店上还有一个重大缺陷尚未解决。问题中的漏洞会影响 Play Store 的搜索功能，并且不会显示最近添加的应用程序，即使你使用了正确的关键字。

根据 Android Authority 最近的一份报告，该漏洞阻止你在谷歌 Play 商店上找到某些应用和游戏。这些应用肯定是实时的，即使你输入完整的名字，它们也不会出现在搜索结果中。例如，搜索游戏“送鸭子”只会显示相关结果，而不会显示游戏本身。即使你用全称‘送鸭水游戏’搜索，游戏也不会显示出来。然而，如果你搜索“Deliver_The_Duck ”,这个游戏就会出现。

几个知名开发者在 Google Play 帮助论坛和 Google Issue Tracker 上报告了这个错误。截至目前，还不清楚这种情况下的问题是什么，但看起来谷歌可能出于某种原因隐藏了这些搜索结果。然而，你可以通过稍微改变搜索关键词来找到应用的事实让我们相信，这个问题可能是搜索算法最近一些变化的结果。虽然谷歌尚未就此事发布官方声明，但问题追踪器上的评论显示，该问题已经上报给开发团队。当谷歌就此事发布声明时，我们会更新这篇文章。

**来源: [Google Issue Tracker](https://issuetracker.google.com/issues/145040410) ， [Google Play Help](https://support.google.com/googleplay/thread/15162444?msgid=15162444) ，**

**Via: [安卓权威](https://www.androidauthority.com/hidden-android-apps-1063722/)，[Reddit](https://www.reddit.com/r/androiddev/comments/e6yfps/what_is_happening_with_google_play_search/)**

* * *

## 更新:已修复

本月早些时候，Play Store 中的一个错误导致新发布的应用无法在搜索结果中显示。根据问题跟踪线程和支持论坛上的评论，看起来 Google 已经解决了这个问题。大多数开发人员报告说这个问题已经解决了。这是个好消息，因为搜索结果对有多少人能找到一个应用程序起着很大的作用。

**来源:[问题跟踪者](https://issuetracker.google.com/issues/145770685)，[问题跟踪者](https://issuetracker.google.com/issues/145040410)，[支持论坛](https://support.google.com/googleplay/thread/15162444?msgid=15162444)**