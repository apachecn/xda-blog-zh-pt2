# [更新:延迟]谷歌可能会添加 API，以便第三方应用程序可以实现 RCS 消息

> 原文：<https://www.xda-developers.com/google-rcs-api-3rd-party-apps/>

**更新 1(2019 年 2 月 22 日@美国东部时间下午 1 点 43 分)**:该功能已被延迟，将不再在 Android Q 中提供。

至少可以说，谷歌的消息传递方式令人困惑，但该公司似乎终于有了一个明确的方向:RCS。这一切都始于五月份关于他们“聊天”计划的新闻。Android Messages 目前[享受许多 RCS 的好处](https://www.xda-developers.com/google-pixel-3-3-xl-verizon-rcs/)，但谷歌可能很快会添加 API，允许第三方应用程序也实现 RCS 消息。

Android Messages 是少数几个支持“丰富通信服务”的消息应用之一如果你更喜欢 Play Store 中无数其他优秀消息应用中的一个，那就太糟糕了。我们可能会在 Android Q 中看到一些将改变这种情况的 API。[一个新的提交](https://android-review.googlesource.com/c/platform/frameworks/base/+/849669)(通过[*9 to 5 谷歌*](https://9to5google.com/2019/01/07/android-q-rcs-third-party-developers/) )指向第三方开发者的 RCS 相关 API。这些 API 将允许应用程序管理 RCS 消息。这些 API 处于非常早期的“框架”阶段，它们都被标记为“TODO”

```
Skeleton implementation of RCS APIs

这一更改增加了 RCS 存储 API 的类。在那里

还没有实现业务逻辑吗

代码实际上什么都不做。

这是必需的，因为这些 API 需要相互连接，即

使用 RcsPart，应用程序开发人员将需要 RcsMessage，并且对于

他们需要 RcsThread 等等。
```

在下一个主要的 Android 版本发布之前，我们可能会看到一些好东西，但看起来 Android Q 将包括更多的 RCS 支持。一名开发人员在评论一项代码更改时说，他将在“q”实现一个丰富的通信服务 API。这对 Android 粉丝来说是一个非常好的消息，因为选择是该平台的一个主要部分。尽管 Android 消息可能很棒，但 Android 爱好者希望能够使用其他应用程序。更多的第三方应用工具总是受欢迎的。

* * *

## 更新 1:延迟

正如[*9 to 5 谷歌*](https://9to5google.com/2019/02/22/android-q-rcs-api-delay/) 再次发现的，新的 API 对开发者来说是[隐藏的](https://android-review.googlesource.com/c/platform/frameworks/base/+/909259)。提交描述如下:“这个特性是从 Android Q 中弹出的。这个改变隐藏了 API。”因此，你最喜欢的第三方短信应用将无法利用 Android Q 中的 RCS 功能。