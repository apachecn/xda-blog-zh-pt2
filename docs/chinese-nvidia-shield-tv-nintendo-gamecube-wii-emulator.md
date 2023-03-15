# 装有任天堂游戏的中国 Nvidia Shield TV 实际上可能运行的是 GameCube/Wii 模拟器

> 原文：<https://www.xda-developers.com/chinese-nvidia-shield-tv-nintendo-gamecube-wii-emulator/>

任天堂几十年来一直固步自封。不过，近年来，它更愿意尝试。例如，它为第三方平台[发布了一款马里奥游戏](https://play.google.com/store/apps/details?id=com.nintendo.zara&hl=en)，并与中国的 NVIDIA 合作，将[精选 GameCube 和 Wii 游戏引入 NVIDIA Shield TV](https://www.xda-developers.com/nvidia-shield-nintendo-gamecube-nintendo-wii/) 。

NVIDIA Shield TV 长期以来一直被宣传为视频游戏玩家的 Android 电视设备。当然，它可能会播放各种媒体，但它的游戏控制器和以游戏为中心的服务，如 GeForce，现在意味着它的目标是游戏人群。这就是为什么当任天堂宣布它将推出诸如*新超级马里奥兄弟*、*超级马里奥银河、塞尔达传说:暮光之城公主*、*打卡游戏等游戏时，人们并不感到震惊！！*和 *Metroid Prime* 到中国的神盾局电视。但从技术角度来看，尚不清楚该公司是如何实现这一目标的。

现在有证据表明 NVIDIA 在中国盾电视上安装了 GameCube 和 Wii 模拟器。这一发现的细节来自 [ResetEra](http://resetera.com) ，社区成员[dragon ban](https://www.resetera.com/members/dragonbane.9332/)发现了《塞尔达传说:暮光之城公主之盾电视版中的一些表演怪癖。

根据报告，该端口没有任何图形问题，在游戏的大部分时间里，帧率都锁定在每秒 30 帧(FPS)。此外，加载时间与流行的 GameCube 模拟器 Dolphin 相当。但奇怪的是，在 Shield TV 上的 GameCube 版本的游戏上，不可能复制两个“臭名昭著”且记录良好的崩溃。

APK 的后续转储显示了一个带有模拟器警告字符串的本机可执行文件，包括一个 GameCube 函数“OSPanic”，当游戏遇到严重错误时会调用该函数:

“[代码]使可执行文件[...]实际上是一个 GC 模拟器，”dragonbane 写道。“一个 GC 模拟器，在与交换机相同的硬件上非常流畅地运行 Cube 上要求最苛刻的游戏之一。直觉告诉我，这个模拟器不仅仅是为了在中国的小众游戏机上模拟 2 款任天堂游戏而设计的。

假设 APK 是真的，还不清楚任天堂对 GameCube/Wii 模拟器有什么计划。无论如何，这是一个不可思议的发现。

* * *

[**来源:ResetEra**](https://www.resetera.com/threads/nintendo-and-nvidia-have-a-working-gc-wii-emulator-for-tegra-x1.19839/)