# 小米发布的 Redmi Note 8 Pro(联发科 Helio G90T)内核来源

> 原文：<https://www.xda-developers.com/xiaomi-redmi-note-8-pro-mediatek-helio-g90t-kernel-sources-released/>

在一系列[泄露和预告](https://www.xda-developers.com/redmi-note-8-series-70-inch-redmi-4k-smart-tv-august-29/)之后，小米在中国的一次活动中发布了红米 Note 8 Pro 以及红米 Note 8、红米 Book 笔记本电脑和红米电视[。红米 Note 8 Pro 是小米最成功的产品系列之一的最新旗舰产品，继](https://www.xda-developers.com/xiaomi-redmi-note-8-pro-redmibook-tv-china-launch/)[小米红米 Note 7 Pro](https://www.xda-developers.com/xiaomi-redmi-note-7-pro-goes-on-open-sale-in-india-as-xiaomi-retains-top-spot-in-market/) 等设备之后。与中国 OEM 厂商最近的做法一致，小米发布了红米 Note 8 Pro 的 Android Pie 版本的内核源代码。

凭借 Redmi Note 8 Pro，小米进行了一次赌博，从多年来在其几款最受欢迎的设备中使用的久经考验的高通骁龙 SOC 切换到不久前发布的新款[联发科 Helio G90T](https://www.xda-developers.com/mediatek-helio-g90-series-hyperengine-game-technology-launched/) 。联发科 Helio G90T 是对联发科 Helio P90 SoC 的专注于游戏的升级。基于 12 纳米工艺，SoC 包括 2 个 Cortext-A76 @2.05Ghz 和 6 个 Cortex-A55 @ 2 GHz；连同 ARM Mali-G76 MC4 GPU -和联发科声称，该 SoC 有能力与类似的[高通骁龙 730G](https://www.xda-developers.com/qualcomm-snapdragon-665-snapdragon-730g/) 竞争。

从社区的角度来看，高通骁龙 SOC 一直比联发科 SOC 更受青睐。过去使用联发科 SOC 的智能手机原始设备制造商因没有按时发布适当的内核源代码而臭名昭著，在很多情况下甚至根本没有发布。在小米红米 Note 2、红米 Note 2 Pro 和红米 Note 3(联发科变种)等设备的问题上，小米自己也有过错。此外，高通的 [CodeAurora Forums](https://www.codeaurora.org/) (CAF)也是开发者的重要资源，因为高通在这里上传其内核源代码以及部分芯片组特定代码，这极大地帮助了独立开发者构建这些 SOC。

随着 Redmi Note 8 Pro(内置联发科 Helio G90T SoC)Android Pie 版本的内核源代码的发布，小米补救了过去困扰联发科 SoC 的一部分问题。随着这些内核源代码的发布，我们可以预计 Redmi Note 8 Pro 的定制内核和恢复工作将会启动。

**[内核来源为小米红米 Note 8 Pro(联发科 Helio G90T)](https://github.com/MiCode/Xiaomi_Kernel_OpenSource/tree/begonia-p-oss)**

**[为联发科增加内核模块](https://github.com/MiCode/MTK_kernel_modules/tree/begonia-p-oss)**

不过有一个问题。在这个阶段发布的内核源代码仍然不完整，因为它显然缺少触摸屏的固件。小米还没有正式宣布这些内核源码已经发布，所以有可能还在上传完整源码的过程中。当完整的资料上传并被我们所知时，我们将更新这篇文章。但就目前而言，即使这一小步也代表着联发科 SOC 方向的良好变化。奇怪的是，总部位于高通骁龙的 Redmi Note 8 的内核源代码还没有上传，尽管我们预计很快也会上传。