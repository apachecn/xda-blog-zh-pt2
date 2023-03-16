# Khronos 宣布推出 Vulkan Graphics API v1.2 版，进行了重大改进

> 原文：<https://www.xda-developers.com/khronos-vulkan-graphics-api-1-2/>

# Khronos 宣布推出 Vulkan 图形 API 1.2 版

Vulkan 1.2 是 Vulkan 图形 API 的最新版本，现已发布，进行了关键的改进和优化。看看吧！

自 Khronos Group 在 2016 年 2 月宣布 Vulkan Graphics API 的第一个版本以来，已经过去了大约四年。简单来说，这是一个新的图形 API——意味着作为 OpenGL 的继任者——能够有效地利用多核处理器，考虑到最近主流的八核处理器已经变得如此之大。多年来，它已经开始在许多游戏中使用，我们日常使用的大多数主要操作系统，如 Android 和 Windows 10，都支持该 API。1.1 版本[发布于 2018 年 3 月](https://www.xda-developers.com/khronos-group-vulkan-1-1-specs/)，进行了关键改进，现在，Khronos 正式宣布了 1.2 版本。

版本 1.2 中最大的改进是将许多以前发布的扩展——准确地说是 23 个——整合到核心 Vulkan API 中。这将使开发更容易，并减少某些平台上不可用的某些扩展的不确定性。另一个改进是时间轴信号量，被吹捧为处理多线程操作的更有效的方式。它将以前的 VkFence 和 VkSemaphore 解决方案统一为一个统一的 64 位解决方案，涵盖了跨设备队列和主机的同步，同时消除了以前解决方案的痛苦限制。其他改进包括内置的正式内存模型，用于定义跨不同线程的内存操作/同步的语义，描述符索引支持，对用 HLSL 编写的着色器的更深入支持，等等。

Vulkan 1.2 将不需要任何新的硬件，这意味着所有当前的 GPU 都将能够支持 1.2。此外，AMD、NVIDIA 和 Intel 等几家 GPU 供应商已经通过了 Khronos 的一致性测试，实现了适当的 Vulkan 1.2。更新的驱动程序已经可以下载，或者很快就可以下载，到本月底，Vulkan 1.2 应该会在许多编译器、调试器和开发工具中得到支持。如果你是一名开发者，并且你有兴趣阅读更多关于 Vulkan 1.2 的内容以及查看官方文档，你可以查看 Vulkan 资源页面[这里](https://www.khronos.org/vulkan/)。