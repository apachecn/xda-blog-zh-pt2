# 喜欢大声点吗？提高 Note 3 的最大音量

> 原文：<https://www.xda-developers.com/like-it-loud-boost-the-note-3s-maximum-volume/>

昨天，我们[为](http://www.xda-developers.com/android/increase-the-volume-on-the-sony-xperia-z1/ "Increase the Volume on the Sony Xperia Z1")[索尼 Xperia Z1](http://forum.xda-developers.com/xperia-z1) 做了一个快速恢复-可闪修改，提高了设备的最大音量。然而，事实证明，Xperia Z1 用户并不是唯一喜欢大声的人。

虽然[三星 Galaxy Note 3](http://forum.xda-developers.com/galaxy-note-3) 有一个绰绰有余的内置扬声器，但一些人仍然喜欢提高它的最大音量。即使对于那些认为内置扬声器足够大声的人来说，他们也可能不会对其连接的音频设备(如 dock 设备和 HDMI 扬声器)的最大音量感到满意。谢天谢地，XDA 资深成员 [jovy23](http://forum.xda-developers.com/member.php?u=4454815) 为 Note 3 创建了一个类似的 mod。

目前，该修改仅适用于骁龙驱动的 Note 3 设备(N9002 和 N9005)，而不是那些采用 Exynos 5 Octa 5420 处理器的设备(N9000)。对于受支持的设备，安装就像刷新一个可恢复的可刷新 zip 文件一样简单。出于好奇，zip 用三个版本之一替换了 */system/etc/snd_soc_msm* 路径中的 *snd_soc_msm_Taiko_CDP* 文件。

有三种不同的版本，用于三种不同的提高音量水平，以及一个恢复到库存压缩。我们只能假设这只能在 stock TouchWiz ROM 及其衍生产品上运行，但如果你正在运行一个笔记设备，你可能希望继续使用这个软件来支持 S Pen。

转到[修改线程](http://forum.xda-developers.com/showthread.php?t=2470890)开始。