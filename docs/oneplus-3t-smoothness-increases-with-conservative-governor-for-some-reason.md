# OnePlus 3/3T 平滑度随着“保守”调速器而增加...说真的(OxygenOS)

> 原文：<https://www.xda-developers.com/oneplus-3t-smoothness-increases-with-conservative-governor-for-some-reason/>

几天前， [u/AmirZ](https://www.reddit.com/user/AmirZ) 震惊了[一加子编辑](http://www.reddit.com/r/oneplus)，他发现将 [OnePlus 3T](http://forum.xda-developers.com/oneplus-3t) 的“大核心”集群设置为一个“保守”的调控器会显著*增加*流动性。是啊，说真的。

对于那些没有抓住这里的矛盾的人来说，内核的调控器负责管理处理器的缩放行为，而“保守的”调控器将手机偏向其最低设置频率。这意味着处理器将在更大和更持久的负载下提升频率，这反过来以牺牲流畅度和响应性为代价延长了电池寿命。OnePlus 3 和 3T 默认使用“交互式”调节器，正如任何 Android 手机所预期的那样，它在 OEM 或用户设置的频谱上扩展和跳跃更快。如果您曾经打开内核管理器应用程序来调整您的设置，您无疑会遇到这两种调控器的变体，但是“保守的”通常不是用户的首选，因为它引入了性能障碍，并且因为“交互的”通常对我们大多数人来说都做得很好。除非事实并非如此。

一加 subreddit 完全没有预料到这样的变化实际上会提高滚动性能，尽管用户很快分享了他们的体验和一两张屏幕截图，但许多人仍然不相信。老实说，我非常怀疑这一调整是否合法，尽管我也足够信任总体结论，放弃了我在 OnePlus 3T 上设置的 LineageOS ROM，闪现了最新的 Oxygen 7.1.1 测试版，并进行尝试。令我惊讶的是，它的效果远远好于我的预期，而且它不仅仅是某种集体安慰剂。

**记住**:这些文章的发现仅限于滚动性能和帧速率，*而不是*速度。这里还有很多我们没有涉及的细微差别，这肯定与这些调控器根据采样时间进行缩放的方式有关。例如，交互中的峰值可能是由处理器在两次轮询之间降低频率引起的。简而言之，记住这不是一个普遍积极的修改，请**不要给内核开发者发垃圾邮件来要求这个改变。**

我已经向一加发出了请求，并请我的一些更聪明的朋友研究这个问题，但到目前为止，我还没有得到任何一方的回复。我不想不负责任地猜测为什么“交互式”管理器在这里做得如此糟糕，所以我将向您展示我的一些发现。如果你想在你的**根** OxygenOS ROM 上试试这个，你需要 **1)下载一个内核管理应用**，然后 **2)将“大核心”集群的管理器设置为“保守”**——“按需”也可以，但我发现没有什么区别值得失去前者的节能。一些用户报告说，相反，他们通过切换“小”集群的调控器也获得了这些结果。

* * *

我首先切换了 GPU Profiling 选项卡，并通过切换调控器发现了即时、一致且完全可重现的改进，这很快排除了混淆变量。然后，我决定转储 framedata 并绘制输出，同时在默认设置下执行显示显著丢帧的特定任务。这些包括在设置菜单中滚动(两秒钟内向上、向下、再向上)，在 Gmail 中滚动(在两个菜单上持续三秒钟)，在包含表情符号、图像和视频预览的不活跃 Hangouts 聊天中滚动(在两个菜单上持续三秒钟)。最后，我看了看我最讨厌的东西:切换到氧气发射器最左边屏幕时的帧率问题。你可以找到下面的情节。

如你所见，差异*显著*。“conservative”上的 OnePlus 3T 总体上设法保持了低得多的帧渲染时间，峰值和抖动帧也少得多。我已经设置了绿线来表示 16ms 线，就像常规的屏幕 GPU 分析栏一样，正如你所看到的，“交互式”设置即使在简单的滚动过程中也很难保持在该线下。您还可以看到，在“交互式”调控器未能保持在每帧 16 毫秒以下的片段中，保守样本要么没有越界，要么恢复得更快。在 Hangouts 滚动样本中，可预测的尖峰来自于 YouTube 视频预览和图像的滚动，总体而言，“保守”的州长做得更好。最后，差异如此之大，以至于回想起来，我应该设置一个固定的比例，因为“保守”样本上的绿线要高得多，因为它看到的尖峰要少得多，也短得多。

***建议阅读:*** *[解剖一加 3T 的表现](https://www.xda-developers.com/dissecting-speed-how-oneplus-leveraged-excellent-real-world-performance/)*

总的来说，这是你绝对应该检查的东西。您的里程数可能会有所不同，但这似乎不会给我的使用带来任何负面影响(从逻辑上讲，除了性能之外，不应该有任何其他问题，在这个特殊而奇怪的实例中，情况似乎并非如此)。[ **警告:**前方轶事证据]我昨天一整天都在运行这个修改，我的 OnePlus 3T 完全在 LTE 上从早上 7 点持续到晚上 11 点，有 4 个小时的屏幕时间，一些 GPS 使用和至少两个小时的 YouTube 红色背景播放(屏幕关闭)。我真的不能说它是否比 T2 好得多，但是它让我度过了忙碌的一天。

**试试看！**

* * *

[**Credit:u/AmirZ**](https://www.reddit.com/r/oneplus/comments/5wvrfw/root_smoothness_on_oxygenos_conservative_big_cores/?utm_content=title&utm_medium=hot&utm_source=reddit&utm_name=oneplus)[**查看 XDA OnePlus 3T 论坛！> > >**](forum.xda-developers.com/oneplus-3t)