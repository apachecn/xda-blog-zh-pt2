# GeekBench 4:看看新的、更准确的移动 CPU 排名

> 原文：<https://www.xda-developers.com/geekbench-4-how-the-processor-ranking-changed-under-the-new-more-accurate-benchmark/>

Geekbench 4 [已经发布](http://www.geekbench.com/blog/2016/08/geekbench-4/)，我们已经看到了一点分数的重新平衡。一些芯片的分数上升了，而其他芯片的分数则大幅下降。通过 Geekbench 4，灵长类动物实验室试图创建迄今为止最准确的 Geekbench 版本，他们似乎已经完成了一项了不起的工作。

在整个科技界，从记者到评论者到软件维护者，对 Geekbench 4 的反应绝对热烈。所以，事不宜迟，我们已经准备了一些东西，看看自 Geekbench 3 以来发生了什么变化；狼群是如何被重新洗牌的。

现在，请记住，Geekbench 3 和 Geekbench 4 之间的分数并不直接可比(Geekbench 3 是针对得分为 2500 的英特尔酷睿 i5-2520M 进行标准化的，而 Geekbench 4 是针对得分为 4000 的英特尔酷睿 i7-6600U 进行标准化的)，因此我们无法直接比较芯片分数是如何增加还是减少的，**但是，查看芯片相对于彼此的位置可以了解它们的表现。**

首先是单核性能。除了高通骁龙 820 之外，几乎所有芯片都相对于三星 Exynos 8890 的平均得分**有所提高。尽管 S820 在 Geekbench 3 中大幅领先，但采用丹佛内核的 Nvidia Tegra K1(来自 [HTC Nexus 9](http://forum.xda-developers.com/nexus-9) )在改变后的单核性能上甚至超过了 S820。**

麒麟 950 中的 A72 内核(来自[华为 Mate 8](http://forum.xda-developers.com/mate-8) 和 [Honor](http://forum.xda-developers.com/honor-hub/) [8](http://forum.xda-developers.com/honor-8) )和麒麟 955(来自[华为 P9](http://forum.xda-developers.com/p9) )尤其显著，使其从 E8890、S820 和 K1 之后，几乎与 E8890 持平。

这将表明**三星的 M1 核心和高通的 Kryo 核心与其竞争对手相比之前都被高估了，而不仅仅是高通的 Kryo 核心。也就是说，高通的 Kryo 核心的降幅确实比三星的 M1 核心大得多。**

最大的收获之一是，这表明 ARM 似乎真的知道他们在单核性能方面做什么，这让人质疑整个*“真正的男人使用定制内核”*的想法是否真的有任何价值，或者它是否纯粹是为了营销。请记住，虽然高通最初在 S810 中仓促实施的 A57 在 20 纳米时遇到了问题，但三星在 14 纳米工艺上实施的 A57 内核表现更好，并且在 Geekbench 4 上的地位有所提高。

在多核测试中，散热限制变得很明显。虽然在单核测试中，除了 S820 之外，每个芯片都相对于 E8890 有所改善，但在多核测试中，麒麟 920、S600、S810 和更老的 Exynos 芯片(除了在 [Galaxy S6](http://forum.xda-developers.com/galaxy-s6) 、 [Note 5](http://forum.xda-developers.com/note5) 和[魅族 Pro 5](http://forum.xda-developers.com/meizu-pro-5) 中发现的 E7420)相对于 E8890 也有所下降。

| 处理器 | 核心 | Geekbench 3 单曲 | Geekbench 3 Multi | Geekbench 4 单机版 | Geekbench 4 Multi |
| Exynos 5433 | A57 | 1145 | 4033 | 948 | 3053 |
| Exynos 7420 | A57 | 1267 | 4290 | 1272 | 3915 |
| Exynos 8890 | M1 | 2161 | 6480 | 1761 | 5199 |
| 麒麟 920 | A15 | 850 | 3042 | 740 | 1730 |
| 麒麟 950 | A72 | 1691 | 6294 | 1703 | 5346 |
| 骁龙六百 | 金环蛇 | 630 | 2274 | 704 | 1671 |
| 骁龙 801 | 金环蛇 | 920 | 2599 | 960 | 2344 |
| 骁龙 805 | 金环蛇 | 1021 | 2881 | 1004 | 2508 |
| 骁龙 810 | A57 | 1013 | 3451 | 1155 | 2450 |
| 骁龙 820 | 克里欧 | 2357 | 5339 | 1573 | 3520 |
| 整数 K1 | 丹佛 | 1880 | 3195 | 1643 | 2616 |

有趣的是，只有一款手机在多核测试中的得分比单核测试中的得分低。在[的某些版本](http://browser.geekbench.com/v4/cpu/search?utf8=%E2%9C%93&q=oneplus+E1003)上的 [OnePlus X](http://forum.xda-developers.com/oneplus-x) 似乎有一个调度程序问题，导致它在多核部分的得分仅为 880 左右，而在单核部分的得分约为 960。在没有这个问题的版本上，OnePlus X 在单核测试中的得分约为 960，在多核测试中的得分约为 2400(这与基于 S801 的手机的预期表现一致)。麒麟 950 尤其是最有趣的跳跃，甚至超过了 Exynos 8890。这可能是由于 Exynos 8890 上的 A53 小核心的时钟速度比麒麟 950 上的相同核心略低。

灵长类动物实验室因 Geekbench 4 的准确性提高而受到称赞，我不得不同意这一点。这些结果与 SPEC 之前显示的非常一致，除了获得结果所需的时间和精力的一小部分。让更多人更容易报告准确的数据带来了更多关于不断变化的 SoC 市场的问题。虽然高通在 GPU 和蜂窝无线电性能方面仍然非常强大，但他们似乎正在失去我们在 Scorpion 和 Krait 内核时代看到的 CPU 优势。本周晚些时候，我们将进一步探讨这些问题。

另外，请关注我们对灵长类动物实验室首席执行官约翰·普尔的[深度采访](http://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-1-64-bit-mobile-throttling-scores-design-a-benchmark-and-more/)，采访马上就要开始了。

*编辑 2016 年 9 月 4 日:增强图形的易读性。*