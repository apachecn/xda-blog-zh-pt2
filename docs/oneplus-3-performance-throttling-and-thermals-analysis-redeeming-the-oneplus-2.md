# OnePlus 3 随时间推移的性能、节流和散热分析

> 原文：<https://www.xda-developers.com/oneplus-3-performance-throttling-and-thermals-analysis-redeeming-the-oneplus-2/>

几天前，我们快速浏览了一下 [OnePlus 3](http://forum.xda-developers.com/oneplus-3) 的 RAM 管理背后的问题[，这是一个围绕手机性能的热门话题。这款手机的骁龙 820 处理器的性能似乎不是什么大话题，*也不是热门话题*。](http://www.xda-developers.com/how-to-fix-the-oneplus-3s-memory-management-almost-double-the-apps-in-memory/)

结论可能已经被破坏了，但在我们即将到来的评测的初步测试中，我发现 OnePlus 3 是一个出色的表现者。在进入细节之前，值得指出的是，OnePlus 3 有很大的期望要实现。它的前身 [OnePlus 2](http://forum.xda-developers.com/oneplus-2) 带着一款骁龙 810 上市，这款骁龙 810 的主频不足，最终实现得很糟糕——因此[我们发现它是最差的骁龙 810 设备之一](http://www.xda-developers.com/oneplus-2-xda-review/#Performance)，因为它的节流和热量输出非常严重。尽管进行了大量的软件更新，OnePlus 2 仍然是 Snapdragon 810 性能最差的产品之一，即使不是最差的，即使问题的很大一部分是一加对处理器的管理。OnePlus 3 与许多采用相同芯片组的旗舰产品相抗衡，但这一次情况发生了变化。

这[不是我们发表的第一篇关于 Snapdragon 820 设备节流的](http://www.xda-developers.com/s7-edge-throttling-thermals-benchmark-stress-tests-of-sd820-810-808-exynos-7420/)深入研究，但这一次我们稍微缩小了关注范围。以下是对 OnePlus 3 和 OnePlus 2 之间的温度和性能随时间变化的分析，*主要是*，以展示一加通过其新的硬件配置实现了多大的改进。我们还将展示其他有用的设备作为参考，注意任何适用的细微差别。

* * *

从以 CPU 为中心的测试开始，我们在 OnePlus 2 中针对 Snapdragon 810 的 A57+A53 配置测试了 Snapdragon 820 的 Kryo 内核。作为参考，我们也在 Nexus 6P 上进行了相同的测试。所有设备在相同的体外温度(29°C | 84.2°F)和相同的表面上开始连续的基准测试。OnePlus 2 的 GeekBench 多核从 4810 下降到 2327，单核得分从 1142 下降到 669，从而大幅降低了速度。测试编号下面列出了温度，您会看到它上升到了 37.2 摄氏度| 98.96 华氏度。

另一方面，OnePlus 3 的多核分数 5619 仅降至 5522，单核分数从 2370 降至 2357。从百分比来看，OnePlus 3 的多核分数下降了不到 2%，而 OnePlus 2 的分数在相同数量的测试中下降了 50%以上。

作为参考，搭载相同骁龙 820 的 HTC 10 在多核评分上下降了近 6%。OnePlus 3 的最高温度是在第十次测试中达到的，最高温度为 33.8 摄氏度| 92.84 华氏度，而 OnePlus 2 在第五次测试中超过了这个数字，最高温度为 37.2 摄氏度| 98.96 华氏度，是这组结果中最热的。OnePlus 3 还优于我们之前分析过的 Galaxy S7 Edge，并标志着自己是 Snapdragon 820 最高效的实现之一。

 <picture>![g5](img/7eabd1d136f79cfac76293420066a62c.png)</picture> 

Resolution plays a huge role in on-screen tests.

转到图形性能和游戏，情况非常相似，同样令人满意。我们在各种以 GPU 为中心的基准测试中测试了 OnePlus 3 和 OnePlus 2，包括 3DMark(弹弓，屏幕)和 GFXBench(曼哈顿 3.1 和 T-Rex)。我们再次连续运行这些测试，看看它们在如此大的负载下表现如何。然而，绝对值得注意的是，OnePlus 3 由于其 1080p 分辨率而比其他 Snapdragon 820 设备具有内在优势，这使其在屏幕测试和某些游戏上具有优势(然而，并非所有游戏都以原生分辨率运行)。在我们的全面审查中，我们将通过调整竞争对手 820 设备的分辨率来考虑这一点——在本文中，我们将使用另一台 820 设备作为 3DMark 的基准，因为这一特定测试以 2560 × 1440 渲染，然后根据每台设备的显示分辨率进行缩放。

将 3DMark 基准测试分数与 Galaxy S7 Edge 的分数进行比较，发现后者的分数下降更明显。在这个基准测试中，OnePlus 3 的表现优于我们测试的所有其他 Android 智能手机，包括 HTC 10 和 LG G5 等其他 Snapdragon 820 设备，在第五次测试中得分下降了 8%。OnePlus 2 仍然有一些性能损失(约 21%)，其得分也很低。当在 GFXBench 和 gaming 上比较这两款设备时，最大的差异就出现了，尽管这两款设备都依赖于分辨率，这意味着我们必须专注于将 OnePlus 3 与其前身(均为 1080p)进行比较。

GFXBench 的 Manhattan 经过 30 次迭代后，OnePlus 3 的帧性能下降了不到 5%，而 OnePlus 2 和 Snapdragon 810 的帧性能下降了约 27%。同样值得注意的是，我们几周前评测的 HTC 10 在这些测试中出现了显著的性能下降——在某些情况下接近 30%——但该设备也有一个 1440p 的屏幕，需要更大的马力(OnePlus 3 在这次测试中的每秒帧数几乎是 S7 的两倍，HTC 10 的每秒帧数比 S7 少 1 帧，这表明分辨率在这里发挥了多么重要的作用)。

在 GFXBench 的 T-Rex 测试中，OnePlus 3 的表现甚至更好:它的帧数没有明显下降，在 30 次耐力测试中，我们的最终分数几乎每次都比第一次高几帧。与此同时，在相同次数的迭代后，OnePlus 2 失去了三分之一的初始分数。我们发现令人惊讶的是，GFXBench 进行了唯一一次 OnePlus 3 比 OnePlus 2(以及其他设备)更热的测试，但它没有看到同样的性能下降。如果有什么不同的话，这表明 OnePlus 3 可以在受到攻击时保持冷静。

 <picture>![IMG_20160618_224316-01](img/4fbf6b50e9fd0811be4e08e0bce23690.png)</picture> 

The OnePlus 3 can get hot after 30 GPU tests in a row, but even then it performs very well.

最后，我们到达游戏测试。虽然我们批评了 OnePlus 2 在游戏性能期间的[严重节流，但 OnePlus 3 表现出了原始的耐用性。事实上，从我在这款设备上玩游戏的时间来看，我可以自信地说这是我测试过的最好的游戏 Android 手机之一。让我们来看看:](http://www.xda-developers.com/oneplus-2-xda-review/#GPU)

即使是最苛刻的 3D 游戏也能在开发商设定的 FPS 上限下保持相当一致的帧率。唯一的例外是死亡触发 2，其中某些闪电效果在相机聚焦它们的那一刻将帧速率减半-即使如此，它最终也超过了可接受的平均帧速率 42。OnePlus 3 在游戏部门远远超出了我的预期，在这方面与 OnePlus 2 的差异是本次分析中最重要的一个。这是少数几个能够在 GTA: San Andreas 中保持稳定帧率的设备之一，最大设置超过了 10 分钟(它的前任只节流了两分钟)，这不是一个小壮举。

 <picture>![Taken with SM-G935T, Android 6.0.1](img/67a270a076da2d8300bd10681b5e127b.png)</picture> 

OnePlus 3 heat distribution

* * *

该分析仅是我们全面评估的性能报告的一小部分，它仅关注一段时间内的性能，而不是相对于其他设备的性能、理论最大值和(最重要的)实际性能。也就是说，随着时间的推移，关注性能是有用的，因为你可能会长时间使用这款设备，至少每天一次。我很高兴地报告，虽然所有这些高要求的场景已经显示出稳定的性能和相对凉爽的温度，但真实世界的 UX 甚至更好，具有舒适的温度和灵活的性能。

一加凭借 OnePlus 3 实现了巨大的飞跃，它成功地从一代人的笑柄变成了硅角斗士。很高兴看到该公司解决了专门困扰其以前设备的问题——尽管这些结果与他们以前的旗舰产品相比令人印象深刻，但缺乏 1440p 面板使得许多结果无法与其他旗舰产品相比。我们将通过降低我们其他 820 设备的分辨率并进行许多这样的测试来解决这一问题，但考虑到 OnePlus 3 用户必须坚持使用 1080p，而且许多人选择这款设备*恰恰是*因为他们不需要超过 1080p，这是一个很好的性价比。

总的来说，我们对 OnePlus 3 的节流不足和整体性能以及日常任务中的最低热量感到非常满意。Dash 充电器甚至更好，我们在未来几天和我们的全面审查中分享了一些关于这个主题的好结果。对于你们当中的游戏玩家来说，OnePlus 3 是一款出色的手机。对于那些想要一个非常经得起未来考验的设备的人来说，这也是正确的手机(特别是现在我们发现了如何释放它的内存)。关于这款设备还有很多值得讨论的地方，还有很多惊喜等待着我们。有关 OnePlus 3 的更多深度报道，请继续关注 XDA！

[**查看 XDA OnePlus 3 论坛> >**](http://forum.xda-developers.com/oneplus-3)