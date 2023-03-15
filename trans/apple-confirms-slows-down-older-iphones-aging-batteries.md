# 苹果公司证实，由于电池老化，它降低了老款 iPhones 的速度

> 原文：<https://www.xda-developers.com/apple-confirms-slows-down-older-iphones-aging-batteries/>

我们通常不会在 XDA 开发者上讨论与苹果产品相关的话题，但最近与 iPhone 相关的新闻吸引了安卓用户的大量关注。苹果公司已经证实，它故意减慢老款 iPhones 的速度，以延长功能寿命，防止老化的锂离子电池关闭设备。

如果你感到困惑，你并不孤单。对于一些背景信息，许多用户抱怨他们的 iPhone 在拥有几年后开始感觉缓慢。据称受影响的设备是 iPhone 6、iPhone 6s 和 iPhone SE。尽管苹果当时没有发布任何声明，但当 iPhone 7 收到 iOS 11.2 更新时，这个问题再次成为人们关注的焦点。用户开始发出同样的抱怨:他们的设备变慢了。

事实证明，他们的设备由于 iOS 中的故意行为而变慢。两位开发商的调查证实了这一点。首先，灵长类动物实验室的研究人员约翰·普尔(John Poole)在发现他的 iPhone 6s 更换电池导致性能几乎翻倍后，调查了这个问题。我们之前在 XDA 就 2016 年发布的 [Geekbench 4](https://www.xda-developers.com/geekbench-4-how-the-processor-ranking-changed-under-the-new-more-accurate-benchmark/) 基准测试采访了 Poole 先生。

普尔通过多项测试证实了他的 iPhone 6s 性能的提升。虽然 iOS 告诉他手机只剩下 20%的电量，但性能提升远不止这些。所以他绘制了 iPhone 6s 在多个 iOS 版本上的 Geekbench 4 分数的内核密度。iOS 10.2 原来是设备性能出现节流迹象的版本。到了 iOS 11.2，这种效果变得更加明显。

在用 iPhone 7 重复测试时，普尔发现同样的事情也发生在了新的设备上。在 iPhone 7 上，iOS 10.2.1 不是受影响的版本；反而在 iOS 11.2 看到了影响。他还表示，他认为这个问题很普遍。

*图片来源:[灵长类实验室](https://www.geekbench.com/blog/2017/12/iphone-performance-and-battery-age/)*

其次，iOS 开发者吉尔赫梅·rambo‏(guil herme Schmidt)跟进了普尔的工作，发现 iOS 代码中存在“Powerd ”:一种他称之为“负责根据 iPhone 电池健康状况控制 CPU/GPU 速度和功耗”的电源模式除了有一个故障保险来确保用户的 iPhones 和 iPads 不会着火，Powerd 据说“随着你的电池电量下降，越来越慢”，同时独立于 iOS 的低功耗模式工作。

作为回应，苹果公司证实，软件过程正在按预期工作(即，在检测到电池健康状况不佳时降低 CPU 和 GPU 的速度)，并声明:

> #### 我们的目标是为客户提供最佳体验，包括整体性能和延长设备寿命。在寒冷条件下，锂离子电池供应峰值电流需求的能力下降，电池电量较低，或者随着时间的推移而老化，这可能导致设备意外关机以保护其电子组件。
> 
> #### 去年，我们为 iPhone 6、iPhone 6s 和 iPhone SE 发布了一项功能，仅在需要时平滑瞬时峰值，以防止设备在这些条件下意外关机。我们现在已经将该功能扩展到装有 iOS 11.2 的 iPhone 7，并计划在未来添加对其他产品的支持。

苹果的做法确实有一定的道理，因为锂离子电池确实具有随时间退化的特性。因此，储存的电量和峰值电流确实下降。显然，存在差异，一些电池比其他电池持续时间更长，但在无法获得数据的情况下，很难说 iPhone 电池是否特别容易以异常快的速度老化。

事实是，苹果公司选择了两害相权取其轻，决定降低用户设备的速度，以保持其功能。另一种选择是什么都不做，这可能会导致设备过早关闭。某些设备的所有者，如 Nexus 5X T1 和 T2 Nexus 6P T3，已经因为这个问题而无法操作，所以这肯定是合理的。然而，苹果缺乏透明度，导致一些人认为这一举动是故意设计来吸引用户升级到更新的设备。

真正的进步是什么？答案是:不会快速自然降解的电池。我们将关注这一领域的发展。

* * *

[**资料来源 1:灵长类实验室**](https://www.geekbench.com/blog/2017/12/iphone-performance-and-battery-age/)

[**来源 2: The Verge**](https://www.theverge.com/2017/12/20/16800058/apple-iphone-slow-fix-battery-life-capacity)