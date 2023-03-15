# 硬件抽奖活动仍在继续:三星 Galaxy S8/S8+在 UFS 2.0 和 UFS 2.1 之间有所不同

> 原文：<https://www.xda-developers.com/the-hardware-lottery-continues-with-the-samsung-galaxy-s8s8-varying-between-ufs-2-1-and-ufs-2-0/>

几周前，[有报道称，华为对华为 P10 和 P10 Plus](https://www.xda-developers.com/huawei-admits-p10-and-p10-plus-can-feature-memory-chips-with-different-specifications/) 做出了一些有争议的决定。简而言之，华为 P10 和 P10 Plus 可以采用 LPDDR3 或 LPDDR4 的 RAM 和 eMMC 5.1、UFS 2.0 或 UFS 2.1 的存储组合。这实质上使得购买设备成为硬件彩票，因为你为设备支付的价格与其他人相同，但你购买的设备可能客观上比其他人的 P10/P10+更差。

硬件抽奖现象现在显然已经出现在今年迄今为止最受关注的旗舰产品中——三星 Galaxy S8 和 Galaxy S8+。

显然，三星 Galaxy S8 和 Galaxy S8+可能会采用 UFS 2.0 或 UFS 2.1 的存储。三星早期的宣传材料吹嘘其存储是 UFS 2.1，但眼尖的 XDA 高级成员 [lch920619x](https://forum.xda-developers.com/member.php?u=2389874) [发现在三星的官方网页上提到 UFS 2.1 的存储被悄悄地删除了](https://forum.xda-developers.com/galaxy-s8/how-to/ufs-2-0-2-1-identify-flash-chip-s8-t3601656)。

用户报告称，他们设备上的顺序读取速度存在显著差异。UFS 2.1 设备的顺序读取速度徘徊在 700-800 MBps 之间，而 UFS 2.0 存储设备的顺序读取速度在 500-600 MBps 之间。

到目前为止，还没有一种清晰而简单的方法来确定你在购买这款设备之前会选择哪一款。

然而，XDA 的资深成员 [lch920619x](https://forum.xda-developers.com/member.php?u=2389874) 确实提到了[一旦你把设备拿在手里就能最终确定](https://forum.xda-developers.com/galaxy-s8/how-to/ufs-2-0-2-1-identify-flash-chip-s8-t3601656)相同的方法。使用终端模拟器应用程序，用户可以输入以下命令:

```
cat /proc/scsi/scsi
```

这将返回您的闪存芯片的确切型号。你可以谷歌一下型号，了解更多关于存储的信息。 [lch920619x](https://forum.xda-developers.com/member.php?u=2389874) 在他的 SM-g 950 FD[基于 Exynos 的三星 Galaxy S8 Duos]上找到了型号为“KLUCG4J1ED - B0C1”的芯片，原来是三星制造的 UFS 2.1 内存芯片。

东芝制造的存储芯片出现了抽奖的情况。如果返回的型号是“THGAF4G9N4LBAIRB”，那么你足够幸运地获得了一台 UFS 2.1 的设备。但是，如果返回的型号是“THGBF7G9L4LBATRC”，则您的设备符合 UFS 2.0 存储规范。

您也可以使用[和](https://play.google.com/store/apps/details?id=com.andromeda.androbench2&hl=en)来检查设备上的顺序读取，但是检查型号是准确找出设备内部内容的最准确方法。

有趣的是，就 UFS 规格而言，华为 Mate 9 也存在同样的情况。Twitter 用户[@ Yao _ 云帆分享了一个方便的参考表](https://twitter.com/yao_yunfan/status/855799247186219009)，列出并区分了 Mate 9 上的型号，Mate 9 也被宣传为 UFS 2.1 设备。表中列出的型号与三星 Galaxy S8 和 S8+用户报告的型号一致，表明迫使华为在 P10、P10 Plus 和 Mate 9 上采取行动的 UFS 2.1 危机也影响了三星最新的 Galaxy 旗舰产品。

![](img/28b5fdf33373cad37da45db68edf445a.png)

猜测和轶事证据表明，三星旗舰上的硬件抽奖只与某些骁龙 Galaxy S8 设备有关，但这可能是不正确的。Galaxy S8+的两种处理器都采用了 UFS 2.1，这是旗舰产品中更大更贵的一款。Galaxy S8 的 Exynos 变种似乎也在使用 UFS 2.1。由于三星尚未就此问题发表官方声明，看来*初步证据*骁龙 S8 用户可能是客观上劣质设备的用户。

### 为你的设备安装 UFS 2.0 而不是 UFS 2.1 有多糟糕？

从理论上讲，UFS 2.0 和 UFS 2.1 之间的差异是客观存在的，并且大到足以让手机 OEM 厂商吹捧一个优于另一个。

实际上，大多数普通用户，甚至智能手机爱好者**都无法区分**UFS 2.0 和 UFS 2.1 的性能，除非他们将两者并列比较。在现实生活和日常使用中，UFS 2.0 不太可能成为你旗舰体验的瓶颈。如果三星选择了 eMMC 5.1，内存规格将对您的体验产生更加深远和显著的影响。因此，作为一线希望，三星目前只是在 UFS 2.0 和 UFS 2.1 之间徘徊。

不过，归根结底，如果你以旗舰价格购买了今年主观上“最好的智能手机”，那么你就应该得到最好的。特别是当 UFS 2.1 被吹捧为一个功能，并提到它随后悄悄地删除，这表明了 OEM 在处理他们的客户的不透明。那只是我们的看法。

* * *

对于我们现在在三星 Galaxy S8 旗舰产品上看到的硬件抽奖趋势，你有什么想法？请在下面的评论中告诉我们你的想法！