# Android 通知麻烦:需要更智能的通知？他们来了

> 原文：<https://www.xda-developers.com/the-android-notification-nuisance-we-need-smarter-notifications-and-they-are-coming/>

通知是用户使用设备体验不可或缺的一部分。这是我们每天在手机上看到几十次甚至几百次的区域之一。它是通知用户他所关心的事情的主要区域——至少，这是计划。

但应用开发者往往高估了自己应用的重要性。这种趋势对知名公司的影响比对独立开发商的影响更大，并且在游戏中非常普遍。不是说应用对用户不重要，因为确实重要。但是由于这种情况经常发生，开发人员往往会忽略这样一个事实，即他们的应用程序并不是用户手机上唯一的应用程序。他们假设用户需要被通知哪怕是最小的动作，大多数应用程序的默认设置都体现了这一理念。

 <picture>![Mild Case of Notification Overload](img/cded6a00e75f57f3cc0933c29cb76308.png)</picture> 

Mild Case of Notification Overload

所做的假设是，用户将取消选中那些他不关心的通知，但没有考虑到大多数普通用户在设置过程后从未涉足应用程序的设置。

那么，当你有几个把自己放在最重要位置的应用时，会发生什么呢？为什么，你最终会遇到需要滚动通知页面的情况。为了找到对你来说重要的那一个通知，你必须浏览其他十个与你当前情况无关的通知。

谷歌在过去推出了各种方法来清除你的通知阴影。对于 [Android 4.4 Kitkat 和更低版本](http://developer.android.com/design/patterns/notifications_k.html)，以及 [Android 5.0+](http://developer.android.com/design/patterns/notifications.html) ，都有通知最佳实践的指南。我们鼓励应用程序开发人员在涉及与他人互动的时间敏感事件中使用通知，同时建议他们不要使用没有真正目的且本质上多余的通知，这些通知只是为了推广品牌或推出应用程序。

> 主要为**时间敏感事件**使用通知，尤其是当这些同步事件**涉及其他人**时。例如，聊天是一种实时同步的交流方式:另一个用户主动等待你的回复。
> 
> 避免通知用户不是特别针对他们的信息，或者不是真正对时间敏感的信息。例如，流经社交网络的异步和非定向更新通常不保证实时中断。对于关心他们的用户，**允许他们选择加入**。
> 
> 不要创建**没有真实通知内容**的通知，而仅仅是宣传你的应用。通知应该提供有用的、及时的、新的信息，而不应该仅仅用来启动一个应用程序。
> 
> 不要为了让你的品牌出现在用户面前而创建多余的通知。这样的通知会让你的听众感到沮丧并疏远他们。

随着手机硬件规格的普遍提高，以在存储中容纳更多的应用程序，以及用户参与的社交媒体平台的增加，手机上较低优先级通知的数量不断增加。在“你的部队已经准备好战斗了”和“你的燃料已经加满了！”的曲调中，加入来自各种通信平台的对话消息和其他各种通知这种混合物。由此产生的混乱是试图引起您注意的东西的大杂烩，其中实际上合格的通知丢失了。

尽管如此，一切还没有结束。如果你正在寻找摆脱这种困境的方法，那就有希望了。

一个这样的希望以[新解决方案](https://play.google.com/store/apps/details?id=com.oasisfeng.nevo)的形式来到我们面前。我们[提到过处于测试阶段的 Nevolution】，而由 Greenify 开发者](http://www.xda-developers.com/xda-external-link/greenify-dev-wants-to-evolve-androids-notifications-with-nevolution/) [oasisfeng](http://forum.xda-developers.com/member.php?u=4376588) 开发的这款应用现在已经退出了测试阶段，值得再次提及。

[Nevolution](http://forum.xda-developers.com/android/apps-games/nevolution-platform-to-evolve-android-t3305999) 的目标是为调整通知提供一个简单的基础。它允许您控制通知的几个方面，如抬头和多行文本。真正让这款应用脱颖而出的是内置在应用中的插件框架，它允许通知以独立于应用开发者的方式发展。这为社区驱动的插件打开了大门，用户可以决定如何最好地接收特定应用程序的通知，并与其他用户分享。目前这方面的功能有限，但这种方法肯定有空间，因为它激励开发人员积极关注他们应用程序的改进和非繁琐的通知模型，以免他们希望用户控制所有这些。无论哪种方式，最终结果都是用户的最终利益。

你可以在[论坛主题](http://forum.xda-developers.com/android/apps-games/nevolution-platform-to-evolve-android-t3305999)找到更多关于 Nevolution over 的信息。

Nevolution 在通知的表示方面起作用，在用户端也是如此。但是，如果有一种方法能够聪明地控制用户在第一时间收到哪些通知呢？

这就是[投影仪](https://www.projector.com/)的用武之地。

根据 Ars Technica 的说法，Projector 是一家旨在帮助开发者的初创公司，为他们提供工具，使他们的通知更加智能。这个想法是只有在合适的时候才打扰用户。通过选择这种理念，您可以立即为通过的通知增加实际的功能价值。通常被归类为垃圾邮件或低优先级的通知，如正在传播的 Twitter 帖子，或热门帐户的 Instagram 上传，将在到达用户之前首先被投影仪处理。投影仪服务将位于现有的应用服务器和通知服务器之间，为这些场景中应用的规则和机器学习提供中间空间。因此，当启动这种场景时，通过利用批量通知或其他技术来最大限度地减少垃圾通知。Projector 还将利用地理围栏技术来估计用户是否处于预期较少通知的情况下:例如驾驶时和开会时，并适当地优先考虑在这些情况下实际上很重要的通知，例如路线上的交通更新。

Projector 还旨在通过提供关于特定用户对哪些通知采取了行动以及对哪些通知不予理会的反馈来帮助开发人员。这将有助于创建用户配置文件，然后允许开发人员为特定的用户组定制请求。毕竟，通知的中心产品是一个用户，有他自己的个人喜好，这种东西只有用一个总括规则才能有效。

Android 的通知一塌糊涂，也不完全是 OS 的错。有意识的应用开发者确实采用了用户友好的通知系统。但是利用这个系统的人却污染了整个池塘。也许，谷歌应该建立更严格的通知准则，就像它对 Doze 所做的那样。因为随着 Android Wear 预计只会在未来流行，你关心的通知将成为当务之急。

**你对 Nevolution 和投影仪有什么看法？你认为 Android 的通知系统需要彻底的反思吗？请在下面的评论中告诉我们你的想法！**