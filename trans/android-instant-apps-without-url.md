# 开发者现在不用网站就可以发布即时应用

> 原文：<https://www.xda-developers.com/android-instant-apps-without-url/>

# 开发者现在不用网站就可以发布即时应用

你是一个开发者，对即时应用感兴趣吗？好吧，我们很高兴让你知道，从今天开始，你不需要一个网站来创建一个。

早在 2016 年 5 月谷歌 I/O 期间，谷歌就宣布了即时应用[。对于那些不知道的人，即时应用程序不需要安装在你的设备上。你只需点击“立即尝试”按钮，它就会立即打开。这对于媒体或其他类型的小应用程序来说非常好。甚至游戏开发者也可以使用这一功能，让用户在实际安装游戏之前试用游戏。这个概念很酷，很多开发人员已经采用了它。](https://www.xda-developers.com/google-io-2016-roundup-part-2/)

但是，使用该功能需要有自己的网站。该网站还必须通过[意图过滤器](https://developer.android.com/guide/components/intents-filters)和[数字资产链接验证](https://developer.android.com/training/app-links/instant-app-links)连接到游戏。意图过滤器用于让网站知道何时请求启动活动，以及应用程序何时准备好进行流式传输。数字资产链接验证允许网站将内容推送至设备。简而言之，所有这些都是开发人员的额外成本和额外工作。

今天，谷歌宣布他们不再需要这些，因为开发者不再需要他们即时应用的 URL。从现在开始，你可以只使用新的[深度链接 API](https://developer.android.com/distribute/marketing-tools/linking-to-google-play#kotlin) ，它对 [Kotlin](https://www.xda-developers.com/google-android-p-developers-reddit-ama/) 和 Java 语言都可用。所有这些都使得开发和发布即时应用软件*变得更加容易。新的无网址功能适用于应用程序和游戏。*

下面的链接提供了制作即时应用程序的说明。我相信很多开发者会因为这个改变而高兴。也许你们中的一些人一直想使用即时应用程序，但负担不起价格或所需的麻烦。也许你从来没有听说过他们(并不奇怪)，现在喜欢这个概念。你使用即时应用程序吗？你将来会使用它们吗？请在评论中告诉我们。

* * *

[**来源:安卓开发者博客**](https://android-developers.googleblog.com/2018/08/streamlining-developer-experience-for.html)