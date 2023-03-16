# 优化任何根植麒麟 970 华为/Honor 手机的电池寿命

> 原文：<https://www.xda-developers.com/optimize-battery-life-rooted-huawei-honor-kirin-970/>

# 通过调整内核来优化任何植根于麒麟 970 华为/Honor 手机的电池寿命

XDA 的资深成员 otonieru 已经创建了一个指南，用于调整任何带有麒麟 970 的华为/Honor 手机的内核。结果是延长了电池寿命。

华为和 Honor 的部分高端智能手机搭载了[麒麟 970 SoC](https://www.xda-developers.com/how-the-kirin-970-uses-ai-to-take-better-photos/) 。这种芯片已经显示出强大的功能，但一些人认为它在电池优化方面有所欠缺。很难在原始功率和电池寿命之间找到平衡。大多数定制内核开发人员更倾向于某一方。如果你有一个运行麒麟 970 系统芯片的华为设备，那么这个来自我们论坛成员的内核调整指南可能会让你感兴趣。

多亏了 XDA 资深会员 otonieru 的帮助，这本指南才得以完成。他拥有华为 Mate 10，但他认为 4000 毫安时的电池应该比现在的电池寿命更长。软件优化确实在整体电池寿命中发挥了作用，但控制 GPU 和 CPU 提升到什么频率的是内核。根据 XDA 社区其他成员的报告，这一点以及本指南中包含的其他调整已经延长了电池寿命。

他首先引用了 XDA 资深成员 soniCron 的不同指南，soniCron 致力于如何在几乎任何设备/内核等上优化交互式调控器。通读该指南后，otonieru 发现 1210Mhz 频率与 1402Mhz 阶跃使用相同的电压，因此我们不妨完全忽略较低的阶跃。

同样的事情也发生在其他一些频率上，因此本指南将展示如何解决所有这些问题。然后，使用 soniCron 的一些公式来计算每个可用频率的最佳 CPU 负载配置。一旦计算完所有这些数据，您就可以使用免费的内核调整应用程序(如 Kernel Adiutor)并将这些值插入 CPU 调控器可调参数(或另一个应用程序中的等效程序)。对于那些不熟悉调整内核的人来说，这可能太复杂了，但 otonieru 在为华为和 Honor Kirin 970 SoC 设备收集所有这些信息方面做了很好的工作。

* * *

[**在我们的华为 Mate 10 论坛**](https://forum.xda-developers.com/mate-10/how-to/guide-advanced-interactive-governor-t3718123) 查看完整指南