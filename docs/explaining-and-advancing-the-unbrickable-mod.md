# 解释和推进不可点击模式

> 原文：<https://www.xda-developers.com/explaining-and-advancing-the-unbrickable-mod/>

UnBrickable Mod 团队仍在努力，将我们的设备带到一个屈服的水平，甚至会打动最古怪的施虐者。XDA 知名开发者 AdamOutler [贴出了一份逆向工程硬件指南](http://forum.xda-developers.com/showthread.php?t=1338073)，以及一个[新的不死复生者](http://code.google.com/p/hummingbird-hibl/downloads/list)。此外，不可点击的模式是[现在可用于 7 英寸的 Galaxy Tab](http://forum.xda-developers.com/showthread.php?t=1312391) P1000。如果这对你来说还不够，AdamOutler 还为 Galaxy Tab 发布了[Heimdall One-Click Back to Stock。](http://forum.xda-developers.com/showthread.php?t=1341666)

新的 UnBrickable 复活器允许你实时监控你的设备的状态，或者如果它被阻止，它会告诉你是否有可能复活它。根据开发商的说法，有四种已知的砖块类型，UnBrickable Ressurector 会告诉你你手上有哪种。只需将您的设备插入 Linux 计算机，然后运行程序。

> 硬砖-设备没有响应，不会枚举 USB，基于硬件的解决方案是恢复这种类型的砖的唯一方法
> 
> 软砖-设备在屏幕上显示一些东西或可能什么都没有，固件下载是可能的，因为这是一种“下载模式”。
> 
> unbrackable-该设备已经过修改，可以接受不可更改的调试模式闪存。
> 
> 幸运砖-设备以不可点击的调试模式结束，最终的不可点击的复活器可以在不修改硬件的情况下使用来复活设备。

【AdamOutler 发布的指南首先使用破坏性最小的方法，引导我们找到哪些 xOM 电阻引脚需要移除或保留。他用同样的方法把不可复制的 Mod 带到新的设备上。

> 从[阿达穆特勒](http://forum.xda-developers.com/member.php?u=3682533)
> 
> 我在这里使用的方法可以在几乎任何设备上用于几乎任何目的，而不仅仅是定位引导模式。使用我在这里介绍的技术，您可以定位任何芯片上的任何物理内存寄存器。