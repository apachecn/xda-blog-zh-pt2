# NVIDIA 正在制作一个桌面模式，可能是一个新的 2 合 1 盾平板电脑

> 原文：<https://www.xda-developers.com/nvidia-desktop-experience-shield-tablet-2019/>

NVIDIA 最出名的是其台式机和笔记本电脑 GPU，但该公司的移动设备 SOC 已经取得了相当大的成功。大获成功的任天堂 Switch 由 NVIDIA Tegra X1 SoC 驱动，这使得该交换机成为最受欢迎的 Tegra 芯片组移动产品。但任天堂 Switch 并不是唯一一款采用 Tegra 硬件的移动设备，因为它早于 NVIDIA SHIELD Portable、Tegra Note 7 和 SHIELD Tablet。虽然 NVIDIA 停止了所有 3 款产品，[取消了](https://fccid.io/VOB-P2290W/Letter/Dismissal-Request-Letter-3094244)在 2016 年发布新的 SHIELD 平板电脑的计划，但该公司最终可能会准备推出新的硬件。根据我们在最新的 SHIELD Experience 软件中检查的代码，一个新的桌面模式软件功能正在为代号为“mystique”的新产品开发中。此外，NVIDIA 在网上公布的源代码揭示了“mystique”的一些可能的硬件规格，表明它可能是像微软 Surface Book 一样的二合一电脑。

*从左到右:SHIELD Portable、Tegra Note 7、SHIELD Tablet K1。*

* * *

## NVIDIA 桌面体验

虽然 NVIDIA 有为平板电脑构建 Android 的经验，但自 2018 年 3 月以来，他们没有为 SHIELD Tablet K1 发布新的软件版本。SHIELD Experience 5.4 是当时的最新版本，但一年多后，该软件已经达到了[版本 7.2.3](https://www.xda-developers.com/nvidia-shield-experience-7-2-3-xbox-elite/) 。由于 NVIDIA 不再为平板电脑构建软件版本，我们可以从最新的 SHIELD Experience 版本(为 Android TV 构建)中获得的关于平板电脑新功能的信息量是有限的。假设英伟达(NVIDIA)的一款正在开发的非 Android 电视产品将只与 SHIELD TV 的现有 SHIELD Experience builds 共享某些系统应用和框架文件，因为 Android TV 涉及一套专门的系统应用，这些应用在平板电脑或智能手机的标准 Android 版本中找不到(例如 leanback launcher)。

尽管如此，来自 SHIELD TV 最新软件版本的代码指向了一个代号为“NvDtExp”的新软件功能，可能是 NVIDIA Desktop Experience 的简称。几乎可以肯定，该软件功能不是为现有的 SHIELD TV 产品设计的。NVIDIA 也不太可能用这一功能升级其现有的平板电脑，因为距离他们上次发布 SHIELD Tablet K1 的更新已经超过一年了。最后，代码多次引用了代号为“mystique”的产品，这表明这个新特性是为这个新产品设计的。

代码首先被一个定制 ROM 开发者发现，他与 XDA 开发者分享了他的发现。我们确认了这段代码的存在，它似乎可以处理 NVIDIA 桌面体验的 UI 模式之间的切换，在 SHIELD Experience 的生产版本中可以追溯到 2018 年 12 月，并延续到上个月的最新 SHIELD Experience 7.2.3 版本。尽管 [SHIELD Experience 7.2](https://www.xda-developers.com/nvidia-shield-android-tv-smbv3-amazon-music/) 是第一个包含桌面模式切换器代码的版本，但我们怀疑 NVIDIA 在首次公开发布之前已经开发了这个功能数月。

从代码中，我们可以确认关于 SHIELD 桌面体验功能的几个细节。首先，有 3 种支持的 UI 模式:动态、平板和桌面。没有来自平板电脑专用的 SHIELD Experience 7.2+版本的更新启动器和系统用户界面，我们无法确认 3 种模式之间的确切用户界面差异。然而，如果我们猜测，那么平板模式可能是一个标准的 Android 平板界面，桌面模式可能是一个具有底部任务栏和自由形式多窗口支持的新界面，而动态模式可能是平板和桌面模式的某种混合。提到了桌面 UI 模式的开始菜单可见性和鼠标悬停控制。我们在当前固件中看到的 SHIELD 桌面体验的其他方面包括在启动时设置 UI 模式的能力，如果连接了键盘，则启动桌面模式，以及截取某些按钮组合以显示状态栏，显示电源菜单对话框，关闭活动窗口或切换全屏模式。

*安卓 q 中未完成的桌面模式*

NVIDIA 也在测试一种通过 shell 命令和广播意图控制 SHIELD 桌面体验的方法，尽管这些命令在现有的 SHIELD TV 设备上不起任何作用，因为代码会检查设备是否“神秘”。事实上，有多个配置值是桌面模式特有的，它们引用了“神秘感”可悲的是，尽管我们对自己对 SHIELD 桌面体验功能的理解很有信心，但我们对“神秘感”的了解却不那么确定鉴于 SHIELD Desktop Experience 的代码最近才浮出水面，毫无疑问这是一个正在开发中的新软件功能。此外，由于代码存在于生产固件中，并引用了一个新的未发布的产品，我们可以合理地假设“mystique”是一个运行 Android 的消费设备。然而，我们对“神秘感”的硬件细节可能已经过时了。

* * *

## “神秘感”

“神秘感”这个代号符合英伟达使用漫威角色名字的模式。例如，SHIELD Portable 最初的代号是“thor”，尽管后来被改为“roth”“WX”，或武器 X，和“某人”，或鸣禽，也曾在过去使用过。在电视上，我们已经看到了诸如“布莱克”、“贾维斯”、“佩珀”、“雷霆一击”、“达西”和“福斯特”等代号。因此，在公共源代码中发现“神秘性”是第一次提醒我们它可能是一个正在开发的产品，但真正将这些点联系起来的是我们对 SHIELD Desktop Experience 功能的发现。

去年的源代码显示，“mystique”有一个来自松下的 13.5 英寸 3000x2000 (3:2)液晶显示器。对于平板电脑来说，13.5 英寸的面板相当大，这就是为什么我们认为“mystique”是一台二合一电脑。这个想法符合我们所知道的 SHIELD 桌面体验和它的 3 种 UI 模式。值得注意的是，微软 Surface Book 也有一个 13.5 英寸的 3000x2000 (3:2)显示屏，但我不认为“mystique”，如果它存在，一定会成为 Surface Book 的竞争对手，因为我们对它的完整规格信息知之甚少。(有趣的是，Tegra 4 微软 Surface 2 和 Tegra 4 开发者平板电脑可以启动 Android，因此 NVIDIA 与 Surface 系列有一段历史。)

*微软 Surface Book。来源:微软。*

在某一点上，NVIDIA 正在开发 Tegra X2 (t186)的“神秘感”，但最近的提交显示 Tegra Xavier (t194)的设备树中有“神秘感”。)Tegra Xavier 是一款大型高性能芯片，旨在用于汽车和人工智能计算，如 2018 年底发布的 [Jetson AGX Xavier](https://devblogs.nvidia.com/nvidia-jetson-agx-xavier-32-teraops-ai-robotics/) 模块所示。与最大功率 30W 相比，Jetson 可以在更低的 10W 功率下运行，因此如果它确实由 Xavier SoC 供电，那么“mystique”也将在更低的功率下运行。相比之下，SHIELD Tablet K1 由 2014 年的 Tegra K1 驱动，而被取消的 2016 年 SHIELD Tablet 代号为“鹰眼”，预计将与 Tegra X1 一起推出，就像任天堂 Switch 和 SHIELD Android TV 一样。拥有 Tegra Xavier 将使“mystique”成为 NVIDIA 最强大的消费产品，但同样，我们必须强调我们对其硬件规格知识的不确定性，因为我们发现的代码可能不会反映产品的当前状态。

*Tegra Xavier 概述。来源:Michael Ditty，热芯片 30: NVIDIA Xavier SoC。(通过[维基百科](https://en.wikichip.org/wiki/nvidia/tegra/xavier)检索)。)*

* * *

## 新盾片的不确定性

鉴于 NVIDIA 在 2016 年取消了他们的 SHIELD Tablet K1 继任者[并引用](https://fccid.io/VOB-P2290W/Letter/Dismissal-Request-Letter-3094244)未指明的“商业原因”，NVIDIA 带着新的移动产品重新进入市场似乎有些奇怪。任天堂 Switch 的发布可能在英伟达 2016 年平板电脑的取消中发挥了重要作用，尽管我们不知道。我们联系了英伟达，看看该公司是否愿意对我们关于英伟达桌面体验功能和“神秘感”的调查结果进行评论。英伟达的一位发言人拒绝置评，但他们让我参考了我之前收到的一份声明，以及英伟达首席执行官黄仁勋在 CES 2019 上公开发表的评论。作为参考，这是我之前写的关于[新盾遥控器和盾控制器](https://www.xda-developers.com/nvidia-new-shield-controller-shield-remote/)的存在的声明:

> #### 在代码库中出现不同的概念代码名称是相当标准的做法。即使这个概念不太可能投入生产，这些参考资料仍然存在。我们不能评论哪些代号代表活跃的产品概念，哪些是不活跃的，因为它可能是不固定的。但是，我可以确认，下面的代号没有一个是指已经公开推出的产品。

至于的言论，这位发言人将我与 TechCrunch 的一篇文章联系起来，这篇文章引用了黄“在一次小型记者招待会上”的言论当然，我们在研究 NVIDIA 屏蔽线的最新消息时独立地看到了这篇文章，并已经考虑了它与我们的发现的相关性。在仔细阅读了这位首席执行官的评论，并与英伟达的一位消息人士以及文章作者讨论后，我们得出的结论是，黄健华实际上并不是说，由于任天堂等第三方的成功，该公司没有开发新移动产品的计划。相反，这位首席执行官表示，如果新设备只是对市场上现有设备的微小改进，英伟达将不会制造新设备。相反，他对新的 SHIELD 产品的态度是，NVIDIA 应该只做一个在某些方面令人兴奋或创新的新产品。

> #### “我们真的致力于(屏蔽电视)，但在移动设备上，我们认为没有必要...我们只会制造东西，而不会获得市场份额。英伟达不是一家“抢占别人市场份额的公司”。我觉得那是真的生气了。这是一种令人愤怒的经营方式。创造新的市场，扩大视野，创造世界上没有的东西，这是建立一个企业的好方法。——NVIDIA 首席执行官黄仁勋在 CES 2019 上对记者说，据 [*TechCrunch*](https://techcrunch.com/2019/01/09/dont-expect-a-new-nvidia-shield-tablet-anytime-soon/) 的 Frederic Lardinois 报道。

“神秘感”有资格成为令人兴奋或令人敬畏的产品吗？鉴于缺乏新的 Android 平板电脑，它肯定会在市场上脱颖而出。毕竟，对于更大的 iPad Pro 来说，并没有真正的基于安卓系统的竞争对手。鉴于 Android 缺乏针对平板电脑优化的应用，作为平板电脑操作系统的 Android 远不如 iOS 有吸引力，因此我质疑 Android 与如此强大的硬件配对是否有意义。此外，新的桌面模式可能没有得到充分利用，因为许多 Android 应用程序不支持自由形式的多窗口模式，尽管这可能会在未来改变，一旦开发人员[开始为 Android Q](https://www.xda-developers.com/android-q-desktop-mode/) 构建。

我对“神秘感”的目的有很多疑问假设这款设备有 13.5 英寸的显示屏，它应该比现有的 SHIELD 平板电脑有更大的电池，但 Tegra Xavier 对消费者来说似乎仍然有点大材小用。我无法想象如果这款产品最终运行 Android，它会有巨大的市场，尽管它可能最终成为针对开发者的利基产品。

NVIDIA 对其产品计划守口如瓶，因此我们对其未来产品的唯一一瞥来自于我们在代码中能找到的任何东西。这意味着我们获得的信息可能不准确，因为它取决于我们对代码的正确解释，或者它可能已经过时，因为我们无法访问最新的源代码。虽然我们相信 NVIDIA 正在开发桌面模式功能，但我们对围绕“神秘感”的一切不太有信心，考虑到该术语的字典定义，这是非常合适的。

* * *

*注意:特色图片仅用于说明目的。它并不反映实际传闻的产品。*