# 新的 API 允许应用程序在匿名模式下打开键盘

> 原文：<https://www.xda-developers.com/api-apps-keyboard-incognito-mode/>

# 新的 API 允许应用程序在匿名模式下打开键盘

从 Android Oreo 开始，我们已经看到一个有趣的功能正在向 Gboard 发展:隐姓埋名模式。有一个 API 允许你在你的应用上启动它！

从 Android Oreo 开始，我们已经看到一个有趣的功能进入了 Gboard:隐姓埋名模式。与谷歌 Chrome 或大多数网络浏览器(如 Firefox 或 Samsung Browser)类似，键盘匿名模式允许您使用键盘，而无需实际保存任何击键或使用的单词。这是一个非常有用的特性，也是我们直到现在才知道需要的东西。而且谷歌也推出了 API 来匹配。

在 API 级别 26 中引入的 IME _ 标志 _ 否 _ 个性化 _ 学习 API 允许开发人员在特定活动或上下文中以编程方式启用键盘的匿名模式，以避免在用户在应用程序中执行特定任务时在键盘上记录打字历史和用户字典数据。从隐私的角度来看，这真的很棒，因为这意味着敏感数据或信息不会泄露到你的个人字典或打字记录中。**这个 API 也被引入到支持库中，所以它不是奥利奥独有的功能，而是支持 API 级别 13 及以上**，这意味着即使是 Android 3.2 蜂巢设备也将能够利用键盘上的隐身功能。

目前，只有谷歌 Chrome 以他们的匿名模式使用这个 API，这允许你浏览网页而不用键盘记录一切。感谢 Redditor[/u/SecondFloorMonstro](https://www.reddit.com/user/SecondFloorMonstro)，我们也知道它存在于 Mozilla Firefox 中，至少在夜间版本中是这样。此外，据我们所知，Gboard 是目前唯一一个具有匿名模式功能的输入法。甚至像 SwiftKey 这样的热门也还不允许这个功能。所以，目前，我们还停留在 Gboard +浏览器组合上。在很多情况下，隐名键盘会很有用，所以我们预计这个 API 会在一些流行的应用上更广泛地推广。如果你想看看这个 API 和它的所有可能性和功能，你可以去 Android 开发者网站，那里有完整的文档供开发者使用。

* * *

[**来源:安卓开发者**](https://developer.android.com/reference/android/view/inputmethod/EditorInfo.html#IME_FLAG_NO_PERSONALIZED_LEARNING)