# Android 上的谷歌 Chrome 将停止背景标签以提高性能

> 原文：<https://www.xda-developers.com/google-chrome-android-stop-background-tabs/>

# Android 上的谷歌 Chrome 将在 5 分钟后停止背景标签以提高性能

谷歌工程师一直在努力提高性能，Android 版 Chrome 很快就会在不活动 5 分钟后停止背景标签。

曾经由微软的 Internet Explorer 主导的谷歌 Chrome 在主导整个网络浏览器市场方面做得很好。各种报告预测 Chrome 的使用率在 50%到 62%之间，这实际上是一件好事也是一件坏事。谷歌已经因为他们的行为受到了俄罗斯和欧洲的调查，他们的做法在不久的将来可能不得不改变。然而，尽管 Chrome 浏览器很受欢迎，用户还是有很多抱怨。谷歌工程师最近一直在努力改进这些，Android 版 Chrome 将在 5 分钟不活动后停止背景标签。

 <picture>![](img/5dbc7d008c362e680920d085c7ee0e0f.png)</picture> 

The flag for the feature which will be removed since it will be enabled by default for everyone.

我们首先在 Chromium Gerrit 中发现了一个[提交，这表明该团队正在努力提高谷歌 Chrome 在 Android 上的性能。这是一个原本应该默认启用的特性，但是从来没有实现过。然后，我们发现另一个](https://chromium-review.googlesource.com/c/chromium/src/+/1139042)[提交再次提到了 StopLoadingInBackground](https://chromium-review.googlesource.com/c/chromium/src/+/1139042) 标志，但是这一次注释说该特性将默认开启。这里已经概述了这个新功能的[摘要，](https://groups.google.com/a/chromium.org/forum/#!topic/blink-dev/83sXW-6caZ0)但它的要点是，Android 的谷歌 Chrome 试图通过在渲染器在后台超过 5 分钟时停止加载任务和获取 Chrome 标签的资源来提高你的设备的性能和节省电池寿命。

谷歌的人在过去的 5 个月里一直在进行一项实验，并相信他们已经解决了他们能够发现的所有问题。他们的测试指标显示，后台的 CPU 工作减少了(这再次节省了设备的电池寿命)，并且当加载两个或更多标签时，前台性能也有所提高。谷歌意识到，人们用 Chrome 以画中画模式听音乐和看视频，因此自然地，这些媒体播放被排除在干预之外。

对于那些对这个实验的更多技术细节感兴趣的人来说， [Google 已经在这里](https://docs.google.com/document/d/1DEGgG9HfA2ixJpXQDsKbYCJJyHILWz3CQmuNEJr9Xho/edit#heading=h.7nki9mck5t64)公布了他们的设计文档。