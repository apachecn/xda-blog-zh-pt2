# 分区扫描仪帮助您的 EMMC 砖砌设备

> 原文：<https://www.xda-developers.com/partition-scanner-helps-your-emmc-bricked-devices/>

对于那些一直生活在岩石下的人来说，几个月前发布了几款不同三星设备的有问题的 ic 泄露版本。例如，三星 Galaxy Note N7000 的用户很快发现他们的设备受到了 MMC_CAP_ERASE bug 的影响。这件事发生后不久，XDA 资深成员 [hg42](http://forum.xda-developers.com/member.php?u=3597010) 想出一个办法让[复活被击落的装置](http://forum.xda-developers.com/showthread.php?t=1667886)。

现在，多亏了他的一些独创性，hg42 还开发了一个叫做分区扫描器的配套应用程序来帮助这个过程。应用程序功能:

> **emmc _ scan _ all _ partitions _ once . zip**
> 
> **emmc _ scan _ all _ partitions _ infinitely . zip**
> 
> 这允许以 1mb 的步长快速扫描所有 emmc 分区的所有块。
> 
> 主要目的是访问每个 emmc 块，以便在重新分区后找到分区中的任何分块。
> 
> “无限”变体无限地运行检查，这可能有助于发现仅偶尔发生的 emmc 砖块效应(如果这种效应确实存在)。你想运行多久就运行多久。重新启动以完成。
> 
> 如果这样冻结，显示的最后一个分区内部可能有砖块。
> 
> **emmc _ find _ brick _ start . zip**
> 
> **emmc_find_brick_end.zip**
> 
> 这些扫描整个 emmc 设备。
> 
> emmc_find_brick_start 从设备的开头向上开始扫描。
> 
> emmc_find_brick_end 搜索设备的末端，然后向下扫描。
> 
> 如果运行到最后或下降到零(显示一条消息“completed - > OK”)，则没有发现砖块。
> 
> 如果冻结，最后显示的块带有“...”线的末端是那个方向的第一个砖块。
> 
> 带有“-> ok”的前一行是砖块之前/之后的第一个可用砖块。

该应用获得了极好的评价，所以如果你是那些目前面临 EMMC 问题的人之一，或者你以前有过这个问题并放弃了你的设备，请前往[同伴线程](http://forum.xda-developers.com/showthread.php?t=1823918)并尝试一下。