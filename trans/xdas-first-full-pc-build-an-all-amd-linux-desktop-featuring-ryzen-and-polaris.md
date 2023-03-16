# XDA 第一个完整的 PC 构建:一个全 AMD Linux 桌面

> 原文：<https://www.xda-developers.com/xdas-first-full-pc-build-an-all-amd-linux-desktop-featuring-ryzen-and-polaris/>

随着 GPU 价格在过去几个月里呈指数级增长，很难再给 PC 定价了。这座特别建筑花了我们将近一年的时间来组装；将所有部件组装在一起是一项挑战。(我们的视频制作人 TK 在 1 月份的消费电子展之后提供了最后一块拼图。)

我们的目标是展示一个像样的预算可以让你在一个全 AMD 的建设，以及什么样的性能，你可以期待它。多亏了 AMD 锐龙和北极星，我们才能够做到这一点。

## 五金器具

像往常一样，我们列出了构建中包含的所有硬件。我们也注意到制造商提供的部件不是由 XDA 或 XDA 员工购买的。

我们想对帮助实现这一目标的公司表示感谢:AMD、技嘉、Rosewill、Team Group 和 XFX。构建花了这么长时间的部分原因是寻找所有必要的部分，我们感谢支持。

**CPU:** AMD 锐龙 1700 x*(AMD 提供)*

**冷却器:**冷却器 Master MasterLiquid Lite 240

**主板:**技嘉 GA-AB350-Gaming 3 *(技嘉通过 AMD 提供)*

**PSU:** 罗斯威尔夸克系列 850 *(由罗斯威尔提供)——这原本是一个 750 瓦的 PSU*

**案例:**罗斯威尔库里南*(罗斯威尔提供)*

**内存:**团队夜鹰 RGB DDR4-3200 16GB *(团队组提供)*

**SSD:**Team T-Force Cardea m . 2 480 GB*(团队组提供)*

**GPU:** [XFX GTS XXX 版 RX 580 8GB](http://xfxforce.com/en-us/products/amd-radeon-rx-500-series/rx-580-gts-8gb-dd-rx-580p8dfd6) *(由 XFX 提供)*

为了了解自项目开始以来发生了多大的变化，我在过去一年的最低点对每个组件进行了定价。(你可以在 PCPartPicker 上找到[调查价格的链接。)如果你有耐心在合适的时间分别购买每台电脑，这款电脑的售价应该在 1200 美元左右，我们认为这是高端电脑的最佳价位。更大的 m.2 驱动器可以换成更小的以节省资金，或者 GPU 换成 580 的 4GB 版本或更便宜的东西。](https://pcpartpicker.com/user/garwynn/saved/P3VQVn)

今天，*如果*你能找到制造这台电脑的所有零件，[它将花费超过 1700 美元](https://pcpartpicker.com/user/garwynn/saved/#view=fysFdC)。主要归咎于 GPU 价格上涨，这是加密货币开采爆炸式增长的结果。你仍然可以在 MSRP 上找到交易，但是越来越少了。在这个价格范围内，只要有点耐心，你就可以轻松找到 Vega 或 NVIDIA GeForce GTX 1080 Ti GPU，并且不会超出预算。

如果你想了解更多关于我们在这个版本中使用的组件的信息，我们建议从我们的[团队 T-Force Cardea 和 Night Hawk RGB 评论这里开始](https://www.xda-developers.com/team-t-force-night-hawk-ddr4-cardea/)。我们无法给 GA-AB350-Gaming 3 一个合适的外观，因为问题[在最初的锐龙审查](https://www.xda-developers.com/xda-takes-on-ryzen-in-depth-look-of-amds-new-processors-on-the-linux-side/)中突然出现，但我们这次将通过它的步伐，以及我们收到的这个版本的新组件。

## 软件

为了避免问题并保持我们最近评论的一致性，我们坚持选择 Ubuntu 17.10 作为我们的操作系统。我们只做了让系统启动的基本工作——RX 580 工作了，尽管没有 HDMI 音频，没有 4.13 内核上的 amdgpu-pro。

我们还安装了 DaVinci Resolve 14 来测试 Linux 的视频编辑能力。最后，我们安装了 Steam 和几款游戏来测试游戏性能。从那里开始，TK [按照我们的测试程序](https://docs.google.com/document/d/1I3G046Nb5NIcirQnkmQccVYBKd2r8dXZq3LvOjdcK_s/edit?usp=sharing)开始工作。

## 照片/装置

这里有一些装置的照片。如果你想看更多，请看看文末来自 TK 的视频。

## 基准测试- Phoronix 测试套件

要查看 Phoronix 的完整结果，请参考[OpenBenchmarking.org 链接](https://www.google.com/url?q=http://openbenchmarking.org/result/1801244-GARW-TKRYZEN83&sa=D&ust=1519127989495000&usg=AFQjCNGrCvN9RkOGQu6oygUPCIQAiVYtXw)。我们已经包括了来自我们[最近的 HEDT 处理器审查](https://www.xda-developers.com/test-ryzen-intel-amd-core-x-threadripper/)的结果，因为测试是在 30 天内进行的，应该可以提供最好的比较。我们在标准速度下测试了 1700X 和 HEDT 芯片。

**FFTW**

FFTW 是快速傅立叶变换的单线程基准。结果与我们在 AVADirect 上看到的不太匹配，但这种差异可能是由于我们的 Ubuntu 17.10 安装中的不同软件包版本造成的。

#### **GZip 压缩**

GZip 是一种常见的压缩方案，它是对日常性能的一个很好的测试。与 AVADirect 的结果有所不同，但在这里会更好。

#### **开膛手约翰**

我们的密码基准测试[开膛手约翰](http://www.openwall.com/john/)显示的结果与我们的预期非常一致。

#### **C 射线 1.1 版**

该小组的 [C 射线](https://openbenchmarking.org/test/pts/c-ray-1.1.0)结果也非常接近 AVADirect 1700X 的结果。

## 基准:构建性能

#### **构建测试:ImageMagick**

这个构建测试的性能让我很惊讶，我有点不明白为什么增加了近 15%。我最初认为这是一个异常值，但考虑到后续测试的结果，我不太确定。

#### **构建测试:GCC**

我们的 GCC 构建测试结果稍慢一些，但是从 900 秒到 30 秒有 3%的差异，这很容易被认为在误差范围内。这里的附加测试可能有助于获得更好的平均值。

我们两个的构建时间都比我真实预期的要长，但是我们已经看到构建时间不时会有这样的变化。当我们继续测试这个版本时，我很想知道这是如何变化的。

有关游戏和工作效率基准，请查看评测视频。简而言之，这个版本可以轻松处理达芬奇密码中的 4K 视频和 Steam 上的流行游戏。我自己对类似硬件的基准测试将包含在我即将发布的对 Powercolor 红魔鬼 Vega 56 的评测中。

## 印象

总的来说，系统的表现和我们预测的一样好。可以肯定的是，还有微调的空间，我们计划将这个版本发送给我们的一个固定贡献者，看看他能做些什么。这位贡献者最近为工作目的构建了一个类似的版本，但使用了非常不同的显卡，我很想知道他对我们的系统与那个系统相比表现如何的看法。

Rosewill Cullinan，结合来自千兆字节主板和团队 RAM 的 led，看起来令人惊叹。这是一个非常红色的建筑(考虑到这是 AMD 的品牌颜色，非常合适)。它从系统中移除了额外的驱动器，这意味着更少的布线和更整洁的整体构建。团队卡迪亚适合这里的法案，因为它的散热器，虽然我不得不承认，我有点难过，不得不把它送给 TK。不过，最终结果还是值得的。

通过使用更新的内核版本或安装 amdgpu-pro，应该可以挖掘 RX 580 的真正潜力。它可以很容易地作为一个双启动系统工作，就像我用 Sapphire RX 480 设置锐龙 7 1700 一样，并以 1080p 的分辨率处理几乎任何游戏，并以合理的高帧率处理大多数最大设置。进一步调整内存和 CPU 电压应该会让系统的性能比我们在基准测试中看到的更好。

## 构建视频

这是我们的劳动成果。我们感谢 TK 构建和测试 PC(以及拍摄和编辑此视频)，并再次感谢帮助实现这一构建的公司！

看完这个造型后，你有什么想法？我们很高兴能让这一切发生，并与我们的读者分享(睁大你的眼睛，你很可能会看到这个版本再次出现)。请通过论坛、脸书、推特或评论让我们知道。