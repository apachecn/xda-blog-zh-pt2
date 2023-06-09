# [更新 2:最多 7 天或更长时间]谷歌 Play 商店批准新应用现在需要更多时间

> 原文：<https://www.xda-developers.com/google-play-store-approval-new-apps-time/>

**更新 2(美国东部时间 2019 年 8 月 30 日下午 4:20):**谷歌表示，他们可能需要 7 天或更长时间来审查某些开发者提交给 Play Store 的应用。

****更新(美国东部时间 2019 年 8 月 22 日凌晨 2:30):**根据 Techcrunch 的一份报告，谷歌否认 Play Store 批准新应用程序将需要所有开发者更多的时间，坚称这只是针对新开发者。请阅读文章底部的更新。下面保留了 2019 年 8 月 18 日发表的文章的其余部分。**

 **毫无疑问，谷歌 Play 商店是 Android 上最重要的应用分发平台。由于其“官方”性质，以及 Play Store 预装在绝大多数 Android 设备上的事实，Play Store 充当了连接用户和应用程序及其开发者的中心点。谷歌在这个位置上对双方都负有很大的责任——保护用户免受恶意应用程序的攻击，同时也让开发者以一种轻松的方式利用商店的影响力，相对而言，T2 是 T3。争论可能会略有增加，因为谷歌已经开始通知开发者，由于审查过程的变化，谷歌 Play 商店批准新应用程序将需要更多时间。

以基于文本的互动游戏而闻名的游戏选择有限责任公司[发布了一篇博客文章，向其他开发者通报了新应用审查流程的最新变化。在发布新应用程序的过程中，谷歌 Play 商店现在会显示一个新的横幅:](https://play.google.com/store/apps/developer?id=Choice+of+Games+LLC)

“了解更多”超链接会转到[该支持页面](https://support.google.com/googleplay/android-developer/answer/6334282)，该页面试图澄清“*对于某些开发者账户*，谷歌将会花更多时间“*彻底*审查应用程序，以更好地保护用户。开发者可以在应用仪表板上看到一个通知，告诉他们这需要多长时间。该页面进一步建议开发者在提交应用程序和期望它在谷歌 Play 商店上线之间应该包括至少三天的缓冲期。

Choice of Games LLC 对这一横幅和变更提出了一些问题。在我们看来，最大的问题是，在您提交应用程序以投入使用后，警告才出现，这对于通知开发人员他们的计划可能会受到审核流程的影响来说有点太晚了。也没有简单的方法来安排一个新的应用程序何时上线(尽管有一个解决方法，我们稍后会谈到)。支持页面还指出，对于某些开发者帐户，更长的审核时间将是“*”，这一说法对于为这一特殊待遇选择的标准非常模糊。也没有办法加快审查过程，所以你在 Play Store 的现有声誉可能对你的新应用立即发布没有任何帮助。现有应用程序的更新将更快地通过审查过程，但新应用程序开始时没有跟踪记录，所以这将需要一些时间。*

令人惊喜的是，Choice of Games LLC 的博文引起了来自[Android 开发者关系总监 Jacob Lehrbaum](https://twitter.com/jlehrbaum?lang=en) 先生的[回应](https://www.reddit.com/r/androiddev/comments/cqug6u/google_warns_developers_that_all_new_android_apps/ex40krh/)。Lehrbaum 先生提到，对知名开发商的审查通常很快，因此需要调查 Choice of Games LLC 的情况，看看审查是否可以更快。他还提到，虽然对开发者来说非常快速的应用审查是理想的，但谷歌也需要在保证用户安全的能力之间进行平衡。Lehrbaum 先生还分享了开发人员如何在谷歌 Play 商店上安排新应用程序的发布，这是一个应该对开发人员有很大帮助的变通办法:

1.  在封闭的 Alpha 轨道中创建释放。
2.  保存并检查版本后，单击“开始向 alpha 版本推出”。
3.  等待 Alpha 版本获得批准。这一步不能计时，但在封闭的 alpha 中，该应用程序也不能公开使用。
4.  alpha 上线后，点击并切换商店展示>商店列表>定时发布
5.  返回应用程序版本，并通过单击保存、审查和开始推广到生产来创建生产版本。
6.  等待产品发布获得批准。
7.  发布获得批准后，单击“上线”。

通过首先将应用发布到封闭的测试轨道，然后使用定时发布进行应用更新，开发人员可以有效地对新应用的发布进行定时。这不是一个非常直接的方法，但它行得通。希望开发者现在能够考虑新应用的新审查期，并确保他们提前向谷歌 Play 商店提交他们的应用。

**来源:[游戏选择](https://www.choiceofgames.com/2019/08/google-warns-developers-that-all-new-apps-require-three-days-for-approval/)；故事 Via:[/r/Android dev](https://www.reddit.com/r/androiddev/comments/cqug6u/google_warns_developers_that_all_new_android_apps/ex40krh/)**

* * *

### 更新 1:谷歌否认了关于谷歌 Play 商店新应用审批程序花费所有开发者更多时间的报道

奇怪的是，谷歌否认了关于新应用程序审批过程耗时更长的报道，称这些报道“不准确”。谷歌澄清说，新的延长时间表仅适用于 Play Store 上的未建立的开发者，同样的时间表并没有扩展到所有开发者。据 *Techcrunch* 报道，混乱源于谷歌 Play 商店开发者支持和游戏开发商 Choice of Games LLC 之间的沟通不畅。开发者支持主管试图提醒开发者关于【2019 年 4 月生效的新政策，但没有意识到开发者对 Play Store 并不陌生，他们已经在商店上发布应用近十年了。

谷歌的否认没有认识到这样一个事实，即整个问题源于一个已建立账户的应用程序在应用程序审查中被阻止；而不是因为服务人员与开发人员沟通不畅。除了承诺进行调查之外，谷歌还没有(据我们所知)就为什么这件事会发生在一个知名开发商身上，以及这是故意的还是仅仅是一个错误进行沟通。在这个前提下，假定该过程已经扩展到所有开发人员是合乎逻辑的。然而，谷歌的官方立场是，更长的时间线仅适用于新开发者的新应用。

**来源:[Techcrunch](https://techcrunch.com/2019/08/21/google-denies-reports-of-unannounced-changes-to-android-app-review-process/)**

* * *

## 更新 2:长达 7 天或更长时间

谷歌更新了支持页面上关于发布一款应用需要多长时间的措辞。该页面现在表示，审查时间可能需要“7 天或更长时间”，“某些应用程序”在“特殊情况下”可能需要 7 天或更长时间的审查时间目前还不清楚什么是“特定应用”或“例外情况”我们期待今后对此有所澄清。

**来源:[谷歌支持](https://support.google.com/googleplay/android-developer/answer/6334282)****