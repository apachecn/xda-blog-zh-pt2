# [更新:修复]谷歌改变了 Play Store 变更日志的预览方式，导致了一些尴尬的措辞

> 原文：<https://www.xda-developers.com/google-play-store-changelog-awkward-phrasing/>

**更新 1(美国东部时间下午 5:08):**谷歌已经确认这个问题现在已经在 Play Store 上得到修复。

谷歌 Play 商店在过去的几个月里收到了一些更新。谷歌增加了[一键按钮](https://www.xda-developers.com/google-play-store-one-tap-unsubscribe-betas-clear-wishlists/)来离开测试版和更多内容， [Google Play Pass 订阅](https://www.xda-developers.com/google-play-pass-monthly-subscription-store-apps-games/)，以及全新的[素材主题重新设计](https://www.xda-developers.com/google-play-store-material-theme-redesign/)。那个新设计(最终)给了我们一个[黑暗主题](https://www.xda-developers.com/google-play-store-dark-theme-android-10/)，可以与 Android 10 系统设置一起工作，但它也给 changelog 预览带来了一个奇怪的变化。

应用列表上的“新功能”部分是开发者可以分享更新中包含的任何新功能或修复的地方。一些开发人员比其他人更好地使用这一点，但这是一个不同的话题。谷歌在重新设计素材主题时做出了一个奇怪的决定，那就是通过删除摘录中间的文本来缩短变更日志。changelog 的开头和结尾用省略号分隔在一起。这里有两个例子:

如你所见，这是一个缩短摘录的混乱解决方案。根据屏幕大小、字体缩放和屏幕方向，文本在不同的位置组合。从结尾截断这段摘录会更有意义。谷歌方法的一个副作用是一些幽默和 NSFW 的文本组合出现在 Play Store 中。这里有两个例子:

**PayPal**

此版本的新功能:改进和缺陷...所以你总是得到最新和最好的。

**HotStar**

我们定期更新我们的应用程序，为您提供...别担心，保持你的更新状态。

一个开发人员自己动手创建了一个脚本，可以根据您的 changelog 生成多种可能的简短文本结果。然后，脚本会自动检查不良词汇，并告诉您是否找到了什么。诚然，这是一个相当奇怪的问题，但这是人们在 Play Store 上注意到的事情。如果你想避免你的变更日志被分割成不恰当的措辞，请查看下面 GitHub 上的项目。

**来源:[GitHub](https://github.com/bernaferrari/SafeChangeLog)**

* * *

## 更新:已修复

在谷歌问题追踪器上，一名谷歌员工[证实](https://issuetracker.google.com/issues/142859268#comment3)该问题现已解决。游戏商店的变更日志不再会被笨拙地从中间分割。