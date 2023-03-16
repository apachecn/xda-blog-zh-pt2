# 谷歌谈到了 Pixel 3 可能的 120Hz 刷新率，高亮度模式，Pixel 4 触觉，等等

> 原文：<https://www.xda-developers.com/google-talks-possible-120hz-refresh-rate-pixel-3-high-brightness-mode-pixel-4-haptics-more/>

安卓开发者后台播客最新一集近日发布。这一次，Android 框架团队的 Michael Wright、Android 开发人员关系团队的 Chet Haase 和 Android 工具包团队的 Romain Guy 参加了会议。在这一集中，开发人员关注了几个有趣的话题，包括谷歌 Pixel 3 上 120Hz 显示屏的可能性，高亮度模式，Pixel 4 触觉，等等。以下是第 129 集解决的所有关键问题的概要:

### 高刷新率显示的谷歌 Pixel 3？

随着 Pixel 4 的推出，谷歌跳上了高刷新率显示器的潮流，并在这两款设备上安装了 90Hz 的显示器。但你知道谷歌打算在 Pixel 3 上安装 120Hz 刷新率的显示屏吗？据 Android 开发者关系团队的 Haase 称，由于各种原因，较小的 Pixel 3 不应采用有机发光二极管显示屏，这也是谷歌考虑在该设备上使用夏普 120Hz 显示屏的原因。哈斯说，“所以这就像‘好吧，如果我们没有有机发光二极管，我们该怎么办？’所以其中一个考虑是‘也许我们可以做一个 120 赫兹的液晶显示器。’“遗憾的是，哈斯没有透露为什么公司最终选择了 P-OLED 面板而不是 120 赫兹的液晶显示器。

### Google 做了什么让高刷新率适用于整个生态系统？

在这一集里，开发人员还揭示了谷歌如何设法让高刷新率适用于整个 Android 生态系统。该公司在 Android 10 中引入了动态刷新率切换功能，可以在 90 和 60Hz 之间自动切换，以节省电能。该公司承认在早期版本中存在问题(可能指的是[亮度惨败](https://www.xda-developers.com/november-update-makes-90hz-smooth-display-behave-differently-pixel-4-pixel-4-xl/))，但表示他们现在已经处于一个更好的位置。

### 触摸采样

该团队对 Pixel 4 的一个大问题是，它使用了 120Hz 的触摸采样。该公司同意使用 120Hz，因为在 120Hz 和 180 Hz 之间切换触摸采样具有挑战性，并且功耗很大。该团队怀疑，随着公司想出如何降低电力成本并处理更多的输入，这种情况将在未来发生变化。90Hz 刷新率和 120Hz 触摸采样不是一个理想的组合，因为 120Hz 触摸采样意味着每隔一帧就有一次输入。

为了解决这个问题，谷歌使用了 Android 4.1 中 Project Butter 引入的重采样来插值/预测触摸事件。谷歌还在研究一种叫做 late-latch 的新技术，在这种技术中，他们会在渲染之前的最后一刻对事件进行重新采样。这项新技术有望改善滚动列表的体验。

### 聪明

在播客中，开发人员还透露，谷歌考虑根据 Android 10 中的应用程序调整亮度。原因是，由于大多数人都会调高照片和视频的亮度，因此 Android 自动调高亮度是有道理的。事实证明，这是一个非常糟糕的主意，因为人们讨厌这种失控。因此，它没有得到实施。

然而，拥有更高的亮度对于查看 HDR 内容很重要，所以谷歌只对 HDR 内容使用[高亮度模式](https://www.xda-developers.com/google-pixel-4-high-brightness-mode-fix/) (HBM)。在 Pixel 系列上，HBM 根据面板的不同将亮度提高到约 600-700 尼特。Wright 补充说，在所有情况下，你需要大约 700 尼特才能在阳光下可读，但 Pixel 在阳光下不使用 HBM。HBM 没有在 HDR 视频之外使用的原因主要是因为老化问题，而不是功率。

### 像素 4 触觉

最后，播客将焦点转移到 Pixel 4 系列的触觉上。如果你有一台 Pixel 4，你可能会注意到设备会随着铃声和闹钟的声音平稳振动。在 Pixel 系列的以前版本中，谷歌必须为每个铃声和闹钟声音创建一个触觉配置来实现这种效果，但这在 Pixel 4 中发生了变化。

在 Pixel 4 中，谷歌引入了音频耦合触觉反馈。现在，音频容器中有一个通道实际上是一个触觉信号，因为触觉信号看起来像一个真正的低频音频信号。但是，这仅适用于预装的铃声和闹钟。这些设备没有第三方铃声和警报的即时耦合。由于音频耦合触觉反馈并非在所有设备上都可用，因此还没有文档可供第三方开发者在他们自己的音频上这样做。

***你可以通过点击[这个链接](https://podcasts.google.com/?feed=aHR0cDovL2ZlZWRzLmZlZWRidXJuZXIuY29tL0FuZHJvaWREZXZlbG9wZXJzQmFja3N0YWdl&episode=dGFnOmJsb2dnZXIuY29tLDE5OTk6YmxvZy0xMDUyMTA4NTQ3OTk4MDgyNDY1LnBvc3QtMzE4OTA1OTg0NzgwMjI2MzM2Ng)在谷歌播客上听完整集。***

* * *

*感谢《XDA》撰稿人迪伦·拉格帮助整理这份摘要！*