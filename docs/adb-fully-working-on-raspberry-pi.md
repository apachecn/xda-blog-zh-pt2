# 亚行全力研究树莓 Pi

> 原文：<https://www.xda-developers.com/adb-fully-working-on-raspberry-pi/>

有几款小型 PC 套件可供人们将计算能力掌握在手中。其中许多实际上是低功率设备，通常装载 Android 或某种 Linux 发行版，其存在的唯一目的是——嗯，我们仍然不确定那一个，但它肯定填补了笔记本电脑和平板电脑之间的尺寸差距。也就是说，这些超微型小型电脑套件中没有一个能与臭名昭著且几乎不可能得到的[树莓派](http://forum.xda-developers.com/forumdisplay.php?f=1845)相提并论。事实上，就在昨天[我们在 XDA](http://www.xda-developers.com/android/forums-added-for-the-raspberry-pi-lg-optimus-g-htc-one-vx-and-htc-desire-x) 给了这个设备自己的家。

在过去的几个月里，Raspberry Pi 获得了如此多的关注，以至于它聚集了来自 XDA 各地的开发者来探索它所拥有的秘密。这是多用途的，以至于我们最喜欢的开发人员和杰出的硬件黑客之一，XDA 精英公认的开发人员 [AdamOutler](http://forum.xda-developers.com/member.php?u=3682533) ，决定尝试移植 Android 设备中最有用的功能之一——并且成功了！

ADB (Android Debug Bridge)似乎有点不可能，但也不是完全不真实。正因为如此，Adam 花了几天时间来编译和移植 ADB，但是就像任何这类工作一样，错误从各个不同的方向而来。这就是这个社区的魅力所在，因为其他背景与 Adam 不同的开发人员开始在帖子中提出建议，并在其他领域提供帮助。进展仍在继续，直到 XDA 论坛成员 [trevd](http://forum.xda-developers.com/member.php?u=4179234) 发布了一个帖子，声称他能够让港口运行起来。他着手建立了一个 github 树，让每个人都可以快速浏览已经完成的工作，并尝试让它在其他 ARMv6 设备上运行。

不用说，如果你有 RPi，请试一试，如果效果不错，给开发者留下一些反馈。

> *更新:trevd 已经设法制作了一个合适的 adb 1.0.29 frm 源。对于那些希望简单使用二进制文件的人，你可以在这里下载*

更多信息可以在[原线程](http://forum.xda-developers.com/showthread.php?t=1924492)中找到。

想在门户网站上发表什么吗？联系任何新闻记者。