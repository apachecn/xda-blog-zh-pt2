# 谷歌 Play 商店政策和要避免的常见错误

> 原文：<https://www.xda-developers.com/google-play-store-policies-and-common-mistakes-to-avoid/>

众所周知，谷歌会直接接受应用程序，而不经过审查程序。然而，这并不意味着没有你应该确保遵守的政策。忽略这些政策实际上是获得一些警告(以及你的应用被关闭)的最好方式，如果你不解决这些问题，你的整个帐户最终会被暂停。

如果您有兴趣将您的应用发布到 Google Play，您需要先查看相关政策。如果你过去没有检查规则就发布了一个应用程序，现在是你的机会了。整个过程不会超过 30 分钟(即使你不是律师！)，所以不用怕。

以下是您想要查看的资源的完整列表:

本文不会介绍所有这些政策，并假设您对它们有一定程度的了解。相反，它将尝试讨论政策中提到的一些要点，但你可能没有想到(要么是因为政策有点模糊，要么是因为你见过其他流行的应用程序这样做，所以你听起来不错)。

# 知识产权

**Using trademarked names/impersonation**

申请 RandomThing？Google Play 政策提到你不应该假冒其他产品或公司，但许多开发者不清楚你在标题中使用公司名称的方式是否可以被视为假冒。例如，你可以将你的应用程序命名为“RandomThing 浏览器”——你并不是在模仿 RandomThing，对吗？可惜没那么简单。幸运的是，这也不太复杂:对于商标名称，通常最好在应用程序标题的末尾使用它们，并以“for”作为前缀。这从标题就可以清楚的看出你的程序不是官方的。因此，不要把你的新应用程序命名为“RandomThing 浏览器”，而应该叫它“RandomThing 浏览器”。在类似的情况下，你也应该在你的应用程序的描述中这样做——不要让你的应用程序听起来像是官方的或由 RandomThing 认可的。你还应该在描述中包括必要的属性，例如:

*RandomThing 是 RandomCompany Inc .的商标*

公司有时会提供如何使用其品牌名称的指导，所以一定要检查他们的网站。如果有疑问，最好联系他们，询问更多信息。例如，谷歌提供了一套

[guidelines](https://developer.android.com/distribute/tools/promote/brand.html)

用于使用 Android 相关品牌(名称和图标/徽标)。请注意，对商标名称的一些修改也是不允许的(指南提供了“G00gle”和“Google++”作为例子，实际应用程序在过去曾因使用商标名称的一部分而收到警告)，因为这被认为是混乱的。

**Icons**

与上面类似，你不应该使用另一个产品或公司的图标(即使你修改了它)，除非它被明确允许。例如，你是

[allowed to use and modify](https://developer.android.com/distribute/tools/promote/brand.html)

特定条款下的 Android 机器人(它是根据知识共享署名 3.0 许可证授权的)。如果你不确定，创建你自己的图标或使用开放内容(例如，在一些知识共享许可下许可的作品)。

[FlatIcon](http://www.flaticon.com/)

也是一个很好的资源，使搜索、使用和提供 CC 图标的信用变得很容易。

**截图和资产**经过数周的努力，您终于完成了您的音乐播放器应用程序，并希望与全世界分享。为了展示其华丽的材料设计主题和专辑缩略图看起来有多漂亮，你决定拍几张你最喜欢的播放列表的截图…但是等等！专辑封面通常是有版权的，你不应该这样做。相反，当您计划在 Google Play 商店上使用截图时，可以创建原始图像或使用开放内容。这同样适用于你在应用程序中使用的资源(举几个例子:从你没有制作的游戏中提取的资源，从电影中提取的声音，等等)。

# 关键词垃圾邮件

你新制造的计算器简直令人难以置信——它什么都能做！很自然，你想让你的用户知道无限的可能性，所以你决定快速地列出它们:

*功能:乘法、加法、减法、除法、实数/虚数、幂、图形、方程求解、函数等等！*

…甚至:

*关键词:乘、加、减、除、实、虚、N、R、幂、图、方程求解、变量、函数。*

这被认为是垃圾邮件。相反，写几个句子来解释你的应用程序做什么，而不要填入关键词:

这个计算器应用程序支持你期望从计算器中得到的所有常规操作。它还支持函数和图形，可以很容易地解决方程和更多！

不相关的关键字也被视为垃圾邮件。这听起来可能很明显，但是像“比其他计算器更好”或“类似于 WolframAlpha”这样的提及也被认为是不相关的关键词，所以避免将你的应用程序与其他服务进行比较。

# 通过外部方式接受付款/捐赠

As a general rule, you're only allowed to use Google Wallet (via In-App Purchases or separate paid keys/"donation" apps). Other payment methods are only allowed for products that can be used outside of the app (e.g. buying books, but not emoji that can only be used by your app). If you want to provide alternate methods to buy your app or donate, do so on your website instead (possibly offering a separate version that checks for the license, independently from Google Play).

# 这些政策仍然适用于您的应用程序的 alpha 版本

If it's available and distributed through the Google Play store, your application must respect the policies. Don't postpone checking the complete guidelines just because your app is still in the alpha/beta stage -- it being only available to a group of testers doesn't make it an exception.

# 广告

当谈到广告时，Google Play 商店中的应用程序采用了许多做法。话虽如此，其他应用不遵守所有政策并不意味着你不遵守。这适用于上述所有要点，但也许更适用于这一节。你可能已经习惯了通过通知系统为你提供广告的应用程序，或者为了广告的目的而添加主页快捷方式或书签。你可能讨厌这些应用程序，但它正在被使用。如果你在考虑类似的事情:

[don't](https://support.google.com/googleplay/android-developer/answer/2986666)

。广告也必须与你的内容清楚地分开(所以对于在你的应用程序底部可见的广告，要留出空白并清楚地标记出来)。用户不能将它们与实际内容混淆，或者冒误点击它们的风险(如果它们太接近真实内容)。另一件值得注意的事情是:在你的应用程序之外显示广告

[prohibited](https://support.google.com/googleplay/android-developer/answer/2986667)

(例如，退出应用程序后显示的广告)。

# 最后的话

我们已经检查了一些对许多开发者来说可能不明显的情况，即使在检查了政策之后。这篇文章的灵感来自于看到许多开发者因为上述一个或多个原因而将他们的应用程序从 Play store 中删除或暂停他们的帐户。希望对新老开发者都有帮助。请再次注意，这绝不是完整条款和政策的替代品，即使其中大部分是常识。强烈建议您查看全文(本文顶部提供了相关资源的链接)。如果你的应用已经被移除，或者你的开发者账户由于任何原因被暂停，请务必访问

[support article](https://support.google.com/googleplay/android-developer/answer/4454563)

。最后但同样重要的一点是:不要被大量的政策所阻碍。其中很多非常容易理解，如果您有疑问，可以随时询问社区(请访问

[XDA App Stores](http://forum.xda-developers.com/marketing-analytics/app-stores)

关于 Google Play 的问题以及使用它的体验和印象的论坛)。