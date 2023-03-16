# 基准作弊反击:一加和其他人如何被当场抓住，他们做了什么

> 原文：<https://www.xda-developers.com/benchmark-cheating-strikes-back-how-oneplus-and-others-got-caught-red-handed-and-what-theyve-done-about-it/>

几年前，当许多主要制造商被发现在基准测试中作弊时，引起了轩然大波。各种规模的原始设备制造商(包括[三星](https://www.xda-developers.com/analysis-of-the-galaxy-note-3-android-5-0-leak/)、 [HTC](https://www.xda-developers.com/m9-is-throttling-a-non-issue-cant-we-trust-benchmarks/) 、[索尼](http://www.primatelabs.com/blog/2014/03/combatting-benchmark-boosting/)和 LG)都参与了这场试图愚弄用户而不被抓住的军备竞赛，但谢天谢地，在与[行业专家](https://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-2-oems-cheating-benchmarks-custom-cores-honest-manufacturers/)和记者进行了一些坦率的讨论后，他们最终停止了基准测试作弊。

回到 2013 年，正是 [发现了](http://www.anandtech.com/show/7187/looking-at-cpugpu-benchmark-optimizations-galaxy-s-4) 三星在某些应用中人为提升其 GPU 时钟速度，引发了一系列 [调查](http://www.anandtech.com/show/7384/state-of-cheating-in-android-benchmarks) 成为整个制造商范围内的基准作弊。当时，调查发现，除了谷歌/摩托罗拉，几乎所有制造商都在进行基准测试作弊。他们都在投入时间和金钱，试图在基准测试中为他们的手机增加一点额外的性能，以对日常使用没有任何积极影响的方式，试图欺骗用户，让他们认为他们的手机比实际速度快。这些开发工作涵盖了整个领域，从设置时钟速度下限，到强制时钟速度达到其最大设置，甚至到创建仅在基准测试时可用的特殊高功率状态和特殊时钟速度，这些工作通常只会使基准测试提高几个百分点。

当它被发现时，引起了极大的愤慨，因为这些基准测试作弊的企图与基准测试本身背道而驰。大多数基准测试并不是为了告诉你手机在实验室条件下的理论最大性能，这些性能在日常使用中是不可重复的，而是为了给你一个参考点，以便在现实世界中对手机进行比较。在受到技术出版物、行业领袖和普通公众的一些公开指责(和一些私下谈话)后，大多数制造商明白了基准测试作弊是不可接受的，并因此停止了活动。少数没有停止的大多数在那之后不久就停止了，因为对运行的基准测试数量进行了实质性的改变，试图阻止基准测试作弊(通过减少作弊带来的好处)。许多基准测试都做得更长，这样最大化时钟速度的热节流就会立即显现出来。

当我们 [采访](https://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-2-oems-cheating-benchmarks-custom-cores-honest-manufacturers/)geek bench 的创始人约翰·普尔(John Poole)时，基准测试作弊以及灵长类实验室这样的公司可以做些什么来防止它的话题就上来了。特别是灵长类动物实验室使 Geekbench 4 比 Geekbench 3 长得多，部分是为了减少基准测试作弊的影响。为了保证开发 [降低收益，进行基准测试作弊的成本](https://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-2-oems-cheating-benchmarks-custom-cores-honest-manufacturers/) 。

*“问题是，一旦我们有了这些大的运行时间，如果你开始通过提高时钟速度或禁用调节器之类的方式来玩游戏，你就会开始给手机带来真正的危险。...如果你想玩的话...你不会从中得到太多。你可能仍会得到几个百分点，但这真的值得吗？”——约翰·普尔《T3》*

* * *

## 发生了什么

不幸的是，我们必须报告一些原始设备制造商再次开始作弊，这意味着我们应该再次警惕。令人欣慰的是，制造商对这类问题的反应越来越快，只要引起正确的关注，这个问题可以很快得到解决。鉴于上次尝试的反弹有多严重，看到制造商实施基准测试作弊有点令人震惊(一些基准测试完全将作弊设备从他们的性能列表中排除)。与基准测试作弊通常带来的微不足道的性能提升形成鲜明对比(上次大多数尝试带来的分数提升不到 5%)，我们真的希望这一切都成为过去。

这一尝试的时机尤其不合时宜，因为几个月前，基准作弊离开了纯粹的爱好者关注的世界，并进入了公共领域，当时大众汽车和菲亚特克莱斯勒都被发现在排放基准上作弊。两家公司都实施了软件来检测他们的柴油车何时接受排放测试，并让它们切换到低排放模式，这种模式会导致燃油经济性下降，试图在燃油效率方面与汽油车竞争，同时仍保持在排放测试的监管限制范围内。到目前为止，丑闻已经导致数十亿美元的罚款，数百亿美元的召回成本和指控——当然不是原始设备制造商因夸大其基准分数而受到的惩罚，这些分数纯粹是用于用户比较，而不是用于衡量任何监管要求。

在调查高通如何在当时新的高通骁龙 821 上实现更快的应用程序打开速度时，我们注意到在 [OnePlus 3T](http://forum.xda-developers.com/oneplus-3t) 上有一些奇怪的东西，我们无法在[小米 Note 2](http://forum.xda-developers.com/mi-note-2) 或[谷歌 Pixel XL](http://forum.xda-developers.com/pixel-xl) 以及其他骁龙 821 设备上重现。我们的主编马里奥·塞拉费罗(Mario Serrafero)使用高通·特雷普恩(Chris Trepn)和骁龙性能可视化工具来监控高通在打开应用程序时如何“提升”CPU 时钟速度，并注意到 OnePlus 3T 上的某些应用程序在打开后没有回落到正常的空闲速度。根据一般经验，我们尽可能避免在性能监控工具打开的情况下测试基准，因为它们会带来额外的性能开销(特别是在没有官方桌面工具的非骁龙设备中)，但是在这次事件中，它们帮助我们注意到了一些奇怪的行为，否则我们可能会忽略这些行为。

当进入某些基准测试应用程序时，OnePlus 3T 的内核对于小内核来说会保持在 0.98 GHz 以上，对于大内核来说会保持在 1.29 GHz 以上，即使 CPU 负载降至 0%。这很奇怪，因为正常情况下，OnePlus 3T 上的两组内核在空载时都会降至 0.31 GHz。第一次看到这一点时，我们担心一加的 CPU 比例设置有点奇怪，但是在进一步测试后，我们得出结论，一加必须针对特定的应用程序。我们的假设是，一加以这些基准测试为目标，并进入另一种 CPU 扩展模式来提升它们的基准测试分数。我们主要担心的一个问题是，一加可能会在这种模式下设置更宽松的散热限制，以避免他们在 OnePlus One、OnePlus X 和 OnePlus 2 上遇到的问题，这些手机在 Geekbench 的多核部分处理额外的内核时表现不佳，因此偶尔会大幅减速(OnePlus X 有时在多核部分的得分低于单核部分)。你可以在我们的 [OnePlus 2 评测](https://www.xda-developers.com/oneplus-2-xda-review/)中找到严重的节流，我们发现该设备可能会降低高达 50%的 Geekbench 3 多核分数。后来，当我们开始比较设备之间的节流和散热时， [OnePlus 2](http://forum.xda-developers.com/oneplus-2) 成为原始设备制造商应该避免的教科书范例。

我们联系了[灵长类实验室](https://www.primatelabs.com/)(geek bench 的创建者)的团队，他们在揭露第一波基准测试作弊中发挥了重要作用，并与他们合作进行进一步的测试。我们带了一台 OnePlus 3T 到灵长类动物实验室在多伦多的办公室进行一些初步分析。最初的测试包括一个 ROM 转储，它发现 OnePlus 3T 直接通过名称寻找相当多的应用程序。最值得注意的是，OnePlus 3T 正在寻找 Geekbench、AnTuTu、Androbench、Quadrant、Vellamo 和 GFXBench。由于此时我们已经有相当明确的证据表明一加在进行基准测试作弊，灵长类动物实验室为我们构建了一个 [*【鲍勃的迷你高尔夫推杆】*](https://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-2-oems-cheating-benchmarks-custom-cores-honest-manufacturers/) 版本的 Geekbench 4。由于 Geekbench 3 和 4 之间的[重大变化](https://www.xda-developers.com/geekbench-4-how-the-processor-ranking-changed-under-the-new-more-accurate-benchmark/)，因此*“迷你高尔夫”*版本必须专门为这次测试从头开始重新构建。这个版本的 Geekbench 4 旨在避免任何基准检测，以便允许 Geekbench 在作弊的手机上作为正常的应用程序运行(超越了愚弄大多数基准作弊尝试的包重命名)。

* * *

## 令人惊讶的例子

一打开应用程序，差别就很明显了。OnePlus 3T 的空闲频率为 0.31 GHz，这是大多数应用程序的做法，而不是像常规 Geekbench 应用程序那样，大内核为 1.29 GHz，小内核为 0.98 GHz。一加让它的 CPU 调控器变得更加激进，在 Geekbench 中产生了一个实际的人工时钟速度下限，这在隐藏的 Geekbench 版本中是没有的。它不是基于 CPU 工作负载，而是基于应用程序的包名，隐藏版本可以欺骗这个包名。虽然单次运行的差异很小，但热节流松弛在我们的持续性能测试中表现出色，如下所示。

从我们的测试来看，这似乎已经成为氢 OS 的一个“特性”有一段时间了，直到 Nougat 发布前的社区构建时才被添加到氧 OS 中(在[两个 rom 合并](https://www.xda-developers.com/oneplus-updates-new-oxygenos/)之后)。这有点令人失望，特别是考虑到一加在合并 rom 后这个月出现的软件问题，从[引导程序漏洞](https://www.xda-developers.com/oneplus-33t-bootloader-vulnerability-allows-changing-of-selinux-to-permissive-mode-in-fastboot/)到 [GPL 合规问题](https://www.xda-developers.com/xda-developers-urges-oneplus-to-comply-with-gplv2-and-release-kernel-sources/)。我们希望随着两支球队合并后尘埃落定，一加将恢复状态，并继续将自己定位为一个对开发商友好的选择。

手里拿着 Geekbench 的*“迷你高尔夫”*版本，我们也开始测试其他手机的基准作弊。令人欣慰的是，我们的测试显示，五年前卷入丑闻的公司没有作弊。在我们的测试设备上，HTC、小米、华为、Honor、谷歌、索尼和其他公司似乎在常规 Geekbench 版本和*“迷你高尔夫”*版本之间拥有一致的分数。

不幸的是，我们确实发现了基准测试作弊的可能证据，但我们还无法从其他几家公司那里得到证实，我们将进一步调查这些证据。最糟糕的例子是搭载 Exynos 8890 的魅族 Pro 6 Plus，它将基准作弊推向了另一个极端。

* * *

## 一个可怕的例子

魅族一直以来都非常保守地设定他们的 CPU 规模。值得注意的是，他们经常设置他们的手机，以便大内核很少上线，即使在他们的“性能模式”下，使他们放入旗舰手机的旗舰处理器(如优秀的 [Exynos 8890](https://www.xda-developers.com/exynos-8890-vs-snapdragon-820-note-7-performance-analysis-peaks-throttling-thermals/) )像中端处理器一样工作。这在去年达到了顶点，当时 [Anandtech](http://www.anandtech.com/show/10545/the-meizu-pro-6-review/) 指责魅族在基于联发科 Helio X25 的魅族 Pro 6 上的 Anand tech JavaScript 基准测试中表现不佳，并指出大内核在测试的大部分时间里保持离线状态(而测试本应几乎只在大内核上运行)。Anandtech 上周注意到，魅族 Pro 6 的软件更新终于允许魅族充分利用这些内核。Anandtech 的智能手机高级编辑 Matt Humrick，[评论道](http://www.anandtech.com/show/10545/the-meizu-pro-6-review/5)*“在更新到 Flyme OS 5.2.5.0G 之后，PRO 6 的性能大幅提升。北海巨妖、WebXPRT 2015 和 JetStream 的分数提高了约 2 倍至 2.5 倍。魅族显然调整了负载阈值，允许线程更频繁地迁移到 A72 内核，以获得更好的性能。”*

不幸的是，他们似乎没有改善新设备的 CPU 扩展以获得更好的基准测试分数，而是将手机设置为在某些应用程序运行时切换到使用大内核。

在打开一个基准测试应用程序时，我们的魅族 Pro 6 Plus 建议您切换到“性能模式”(仅此一项就足以确认他们正在寻找特定的包名)，并且它似乎产生了实质性的差异。在标准的“平衡模式”下，手机在 Geekbench 的单核和多核部分的得分一直在 604 和 2220 左右，但在“性能模式”下，它的得分为 1473 和 3906，这在很大程度上要归功于大内核在“平衡模式”下的大部分测试中保持关闭，并在“性能模式”下打开。魅族似乎将小内核锁定在 1.48 GHz 的最大速度，并在“性能模式”下运行 Geekbench 时为两个 1.46 GHz 的大内核设置了硬地板(其他两个大内核可以自由扩展，并且相当激进)，这在运行*“迷你高尔夫”*版本时我们没有看到。

虽然能够在高功率模式和低功率模式之间进行选择可能是一个不错的功能，但在这种情况下，它似乎只不过是一个客厅把戏。魅族 Pro 6 Plus 在常规 Geekbench 应用程序的“性能模式”中获得了不错的分数，但当使用 Geekbench 的*“迷你高尔夫”*版本时，它的性能就下降到了与设置为“平衡模式”时相同的水平。魅族 Pro 6 Plus 的更高性能状态只是为了进行基准测试，而不是为了日常使用。

值得注意的一点是，当我们用 Geekbench 的秘密版本在“性能模式”下测试魅族 Pro 6 Plus 时，如果我们用高通特雷普记录时钟速度，大核心就会上线。我们还没有确定魅族是否认识到 Trepn 正在运行并打开大内核，部分原因是因为它，或者它只是因为它产生的额外 CPU 负载而打开大内核。虽然这听起来可能与直觉相反，即后台的额外负载(例如当我们在测试期间保持性能图表时)会*增加基准测试的结果*，但魅族的保守扩展可能意味着额外的开销足以将其推到边缘，并调用大内核采取行动，从而提高所有任务的性能。

* * *

## 当接受原始设备制造商处理反馈时...

测试之后，我们就发现的问题联系了一加。作为回应，**一加迅速承诺停止针对基准测试应用的基准测试作弊，但仍打算保留对游戏的作弊行为(游戏也会进行基准测试)。在 OxygenOS 的未来版本中，这种机制将不会被基准测试**触发。一加已经接受了我们的建议，也增加了一个开关，这样用户就知道在引擎盖下发生了什么，至少基准测试中不公平和误导性的优势应该得到纠正。不过，由于中国春节假期和他们的功能积压，我们可能需要一段时间才能看到这一性能功能面向用户的定制选项。虽然纠正行为本身是一种改进，但在常规应用程序(如游戏)中仍然有点令人失望，因为它是针对特定应用程序的拐杖，而不是改善实际的性能扩展。通过人为提高处理器的积极性，从而提高特定应用的时钟速度，而不是提高他们的手机识别何时实际需要更高时钟速度的能力，一加为他们的手机创造了不一致的性能，这只会随着手机变得更旧和更多一加没有瞄准的游戏发布而变得更加明显。然而，目前的实现确实让游戏表现更好。一加还为本文提供了一份声明，您可以在下面阅读:

为了在资源密集型应用程序和游戏中为用户提供更好的用户体验，特别是图形密集型应用程序和游戏，我们在社区和 Nougat 版本中实施了某些机制，以触发处理器更积极地运行。“基准测试应用的触发过程将不会出现在基于 OnePlus 3 和 OnePlus 3T 的即将到来的 OxygenOS 版本中。”

我们很高兴听到一加将从他们的手机中删除基准作弊。展望未来，我们将继续尝试向原始设备制造商施加压力，尽可能对消费者更加友好，并将密切关注未来的基准测试作弊行为。

不幸的是，对这种类型的欺骗唯一真正的答案是持续的警惕。作为智能手机爱好者群体，我们需要警惕像这样欺骗用户的企图。我们感兴趣的不是基准测试分数本身，而是基准测试对手机性能的评价。虽然当我们审查时，基准作弊尚未在 [OnePlus 3](https://www.xda-developers.com/oneplus-3-xda-review/) 上活跃，但一个简单的软件更新足以添加这一误导性的“功能”，并清楚地表明，在设备首次推出时检查基准作弊是不够的。像这样的问题可能会在设备发布后的几天、几周、几个月甚至几年内增加，从而人为地夸大基准测试几个月后收集的全球平均值，影响最终的数据库结果。应该注意的是，即使制造商不得不投入时间和金钱来开发这些调整，**我们通常只会看到基准测试分数增加几个百分点**(不包括魅族这样的几个边缘案例，在那里作弊掩盖了更大的问题)。几个百分点，这比性能最好和最差的设备之间的差距要小得多。然而，我们认为，随着设备运行越来越相似的硬件，这些额外的百分点可能是用户最终查看排名图表的决定性因素。更好的驱动程序优化和更智能的 CPU 扩展可以对设备性能产生绝对巨大的影响，在 Geekbench 上，性能最高的基于高通骁龙 820 的设备和性能最差的设备(来自一家主要 OEM)之间的得分差异超过 20%。20%来自驱动程序优化，而不是花几个百分点的时间和金钱来欺骗你的用户。而且这还只是说可以影响基准分数的开发努力。投资改进设备软件的许多最大好处并不总是在基准测试中体现出来，因为一加在他们的设备中提供了出色的真实性能。在这种情况下，公司的开发工作应该集中在哪里，这确实应该是明确的。我们正在接触更多在基准测试中作弊的公司，我们希望它们能像一加一样接受。

* * *

我们要再次感谢灵长类动物实验室的团队，感谢他们与我们一起揭示了这个问题。如果没有 Geekbench 的“迷你高尔夫”版，要正确测试基准作弊将会困难得多。