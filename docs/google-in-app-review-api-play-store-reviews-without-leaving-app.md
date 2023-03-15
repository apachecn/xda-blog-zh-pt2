# 谷歌推出应用内评论 API 简化 Play Store 评论

> 原文：<https://www.xda-developers.com/google-in-app-review-api-play-store-reviews-without-leaving-app/>

# 谷歌新的应用内评论 API 允许开发者在不离开应用的情况下请求 Play Store 评论

谷歌推出了新的应用内评论 API，允许开发者请求播放商店评论，而无需将用户重定向到播放商店列表。

在去年年底 APK 对 Play Store 应用(v15.9.21)的拆除中，我们了解到谷歌正在研究一种方法，让用户通过应用内对话框查看 Play Store 应用。这项新功能将帮助用户对应用进行评级，而无需前往应用的 Play Store 列表。谷歌现在已经推出了[应用内审查 API](https://developer.android.com/guide/playcore/in-app-review) ，这将允许开发者在他们的应用中添加应用内审查对话框。

根据该公司最近的一篇博客文章，新的 API 将允许开发者在他们的应用程序中添加一个应用内评论对话框，并选择他们希望何时提示用户写评论。该 API 是 [Play 核心库](https://developer.android.com/guide/playcore)的一部分，支持公开和私有评论。正如你在所附图片中看到的，该 API 将允许开发者显示一个对话框，让用户轻松地为任何应用程序留下星级，而无需离开应用程序。

一旦用户选择了一个评级，对话框将在提交评级之前给他们留下书面评论的选项。为了确保用户的应用内审查过程是无缝的，谷歌为开发者强调了 API 集成的四个步骤:

1.  定义要求评估的条件和最佳位置
2.  向 API 请求审查流程
3.  在适当的时候启动审查
4.  评审完成后继续流程

谷歌补充说，该 API 被设计为独立的，不需要额外的提示，以确保用户的反馈是公正的。此外，该公司对应用内评论设置了上限，因此如果用户选择不留下评论，他们不会受到过多的提示。

* * *

**来源:[安卓开发者博客](https://android-developers.googleblog.com/2020/08/in-app-review-api.html?m=1)**