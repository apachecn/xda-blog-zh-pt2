# 谷歌文档暗示 API 等级 29 将是 Android Q

> 原文：<https://www.xda-developers.com/google-skip-android-9-1-pie-android-q/>

每年，谷歌都会推出新的 Android 版本。今年的新口味是 Android Pie，也称为 Android 9。虽然 Android 9 Pie 需要几个月的时间才能在 Android 版本分布统计数据中留下印记，但我们预计设备接收 Android 9 更新的速度将比去年接收 Android 8.0 Oreo 更新的速度更快(这要感谢 Project Treble)。现在 Android 9 Pie 已经在 AOSP 的[上市，是时候推测下一个主要的 Android 版本会是什么了。最近更新的一份谷歌文件表明](https://www.xda-developers.com/android-pie-source-code-aosp/) [Android Q](https://www.xda-developers.com/tag/android-q/) 将是下一个主要的 Android 版本，而不是 Android 9.1 Pie。

8 月 30 日，一个[提交](https://android-review.googlesource.com/c/platform/bionic/+/742226)被合并更新安卓的[仿生状态](https://android.googlesource.com/platform/bionic/+/HEAD/docs/status.md)。 [Bionic](https://android.googlesource.com/platform/bionic/) 是 Android 的 C 库、数学库、动态链接器。commit 列出了 C 库中即将来到 Android Q 的新函数，有趣的是，描述中指出 Android Q 将是 API 级别 29。

[API 级别](https://developer.android.com/guide/topics/manifest/uses-sdk-element#ApiLevels)标识 Android 框架的版本。比如安卓 8.0 奥利奥是 API 26 级，安卓 8.1 奥利奥是 API 27 级，安卓 9 派是 API 28 级。如果 Android Q 将是 API 级别 29，那么这表明 Android Pie 维护版本(MR)不会是 Android 的下一个主要版本。这仍然是可能的，而且很有可能，我们会看到 Android 馅饼 MRs，因为谷歌以前已经发布了 MRs，而没有冲击 API 水平。

去年当我发现 Android P l 的工作已经开始时，我推测谷歌会跳过 Android 8.1 Oreo。显然事实并非如此，因为我没有考虑到谷歌可能已经在他们的内部主分支完成了 Android Oreo MR1 的工作。然而，这一次，我没有必要去猜测 Android 版本 API Level 29 会是什么:谷歌已经基本上确认了它，通过合并提交不是[一次](https://android-review.googlesource.com/c/platform/bionic/+/742226)，而是[两次](https://android-review.googlesource.com/c/platform/bionic/+/748108)，将 Android Q 链接到 API Level 29。

如果 Android Q 真的是 API 级别 29，那么这意味着开发人员将使用的 API 应该在近一年内保持一致，直到 Android Q 开发人员预览开始。这对开发者来说是个好消息，因为[更新的谷歌 Play 商店要求](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)将要求应用程序在明年 8 月左右达到 API 等级 28。跟上所有最新的平台变化可能是一个挑战，但如果你想让你的应用在 Play Store 上蓬勃发展，谷歌开始强制这样做。拥有使用最新平台功能并遵守最新平台电池和内存优化限制的最新应用对消费者和 Android 生态系统都有好处。

一旦我们过了谷歌 Pixel 3 的发布日期，我们将有望得到关于是否会有 Android 9.1 的确认。Android 8.1 Oreo [在谷歌 Pixel 2 和 Pixel 2 XL 发布后两个月推出，但该 Android 版本开始在谷歌应用程序发布前被拆除。也许今年也会如此，尽管只有几个月后才能知道。](https://www.xda-developers.com/android-8-1-oreo-final-release-imminent/)