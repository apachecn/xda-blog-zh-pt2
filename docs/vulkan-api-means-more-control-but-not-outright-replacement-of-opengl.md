# Vulkan API 意味着对 OpenGL 的更多控制和替代[更新]

> 原文：<https://www.xda-developers.com/vulkan-api-means-more-control-but-not-outright-replacement-of-opengl/>

在[错过了在 2015 年底](https://www.khronos.org/news/permalink/vulkan-working-group-update)发布初始 Vulkan API 规范的目标之后， [Khronos group](https://www.khronos.org) 现在已经完成了 API 的 1.0 发布。到目前为止，我们的大多数读者也知道 [Android 是支持的平台之一](http://android-developers.blogspot.com/2015/08/low-overhead-rendering-with-vulkan.html)。但是这对开发者和用户意味着什么呢？

令人欣慰的是，Vulkan 网站上的新闻稿和材料给了我们大量的信息，让我们开始回答一些可能存在的基本问题。

首先，Vulkan 不是 OpenGL 或 OpenGL ES 的替代品。这是图形开发的另一种方法，更多的控制权在开发人员手中。关于 Vulkan 的另一件值得注意的事情是，它被设计成在整个生命周期中保持统一的规范——这在 OpenGL 中是做不到的。当然，实现在硬件和驱动程序级别会有差异，但是 API 的目标是尽可能保持它在所有平台上的通用性。

 <picture>![Courtesy Khronos Group](img/6de37cec010ddbb0a5f2c76a28c121aa.png)</picture> 

Courtesy Khronos Group

上面的图形有助于显示这两种控制之间的关键权衡。在 OpenGL 中，开发人员将图形处理的更多控制权让给了 OpenGL 驱动程序和 API。Vulkan 提供了一种替代方案，它让您在较低的级别上对硬件进行更多的控制，这也意味着消除了可能会发现的开销。如果这听起来很熟悉，那是因为你已经听说过 AMD 的 Mantle API 和现在的 Microsoft DirectX 12 中的类似努力，也称为“更接近金属”Vulkan 提供了在移动领域获得更多控制权的机会。当我们谈论移动场景中的开销时，我们也在谈论可以在比桌面或更大规模使用更有限的设置中运行并消耗电池或性能的东西。

显然，SDK 刚刚推出，没有任何真实世界的例子来进行比较；但这并不意味着我们看不到移动场景的精彩。仅仅回顾一下今天的新闻稿就可以发现几条值得强调的引言。我用粗体字强调了读者可能特别感兴趣的内容。

 <picture>![Image courtesy Khronos Group](img/4d972b559c8da4d44d6a65fa87982fe2.png)</picture> 

Image courtesy Khronos Group

高通的产品管理总监 Micah Knapp:

我们很高兴能够为 Khronos 新 Vulkan API 的定义做出贡献。高通科技公司将是首批发布符合 Vulkan 驱动程序的公司之一，**首先是我们的高通骁龙 820 嵌入式高通 Adreno 530 GPU，随后是我们的 Adreno 4xx 系列 GPU**。Vulkan 通过在 adre no GPU 中添加**多线程命令缓冲生成和高级图形功能的显式控制，实现了下一代图形性能。我们希望在骁龙开发者工具中支持 Vulkan，包括骁龙 Profiler 和 Adreno SDK，以帮助应用开发者在为智能手机、平板电脑、VR HMDs 和各种使用骁龙处理器的其他类型的设备创建图形和计算应用时利用这一出色的新 API。**

**美国东部时间 2017 年 2 月 2 日上午 9:45 更新:**4xx 系列包括骁龙 805/808/810 系列，这是当今市场上的大量设备。

NVIDIA 内容与技术高级副总裁 Tony Tamasi:

Vulkan API 使开发人员能够充分利用 NVIDIA GPUs，我们为自己在开发过程中发挥的作用感到自豪。我们正在为 Windows、Linux、**和 Android 平台提供 Vulkan 驱动程序，就在规范发布**的同一天，我们将继续在 Khronos 内开展工作，以确保 Vulkan 不断发展，满足行业需求。

**更新 2/17 上午 9:45 CT:**说到做到，支持 Vulkan 的开发者 OS 镜像可以在[这里](https://developer.nvidia.com/shield-developer-os-images)获得。该网站称，支持 Vulkan 的公共在线旅行社有...正在进行最终验证，但应该很快就可以使用了。”

三星电子移动通信业务副总裁金泰勇:

*三星对 Vulkan 今天的发布感到兴奋，这将有助于跨平台扩展游戏生态系统。我们在 Khronos 内部一直致力于支持一个开放标准，以实现高性能和尖端技术。 **Vulkan 将为移动游戏提供更加激动人心的沉浸式用户体验。***

自然地，Khronos 集团的许多成员都对这个新版本发表了声明，所以请前往[查看新闻稿](https://www.khronos.org/news/press/khronos-releases-vulkan-1-0-specification)了解所有的好东西。虽然这可能需要一点时间才能到达您选择的设备，但为开发人员提供其他图形选项看起来确实是一个明智的选择。同样重要的是要注意，即使 Khronos 小组也认为许多开发人员使用 OpenGL ES 会更好。这是有意义的，因为从初学者的角度来看，这是一个更稳定的标准，更容易实现。但我知道我会期待看到这对消费者有什么影响。谁知道呢？如果 Vulkan 为移动设备的基本使用提供了更低的开销，我们最终可能会看到基于 Vulkan 的 ui。

火山 Github Repos:

那么，随着这款面向开发者的新工具问世，你认为它会改变游戏规则吗？或者更多的是打哈欠？请在下面的评论中告诉我们！