# PPSSPP 现在支持 Vulkan 图形 API，以实现更流畅的 PSP 仿真

> 原文：<https://www.xda-developers.com/ppsspp-vulkan-graphics-update/>

# PPSSPP 现在支持 Vulkan 图形 API，以实现更流畅的 PSP 仿真

PSP 模拟器 PPSSPP 获得了对 Vulkan 图形 API 的支持。理论上，这将转化为所有平台的性能提升。

索尼 PlayStation 便携式 Android 设备模拟器 PPSSPP 是目前最强大的模拟器之一。它不仅可以让你在任何基于 Android 的智能手机或平板电脑上玩你最喜欢的 PSP 游戏，而且它支持 Vulkan Graphics API，这意味着它可以在旧的片上系统上运行良好。

如果你没有听说过 Khronos Group 的 [Vulkan](http://xda-developers.com/t/vulkan) Graphics API，那就把它当成 OpenGL 或 OpenGL ES 之类的图形 API 的低开销替代品吧。它得到了英伟达和英特尔等公司的支持，旨在给开发者在编写跨平台游戏时提供更多选择。(理论上，Android 上的 Vulkan 图形开发应该在 Vulkan 支持的 PC 硬件上运行。)它相对较新，但已经在游戏中实现了，如 Codemasters 的[网格](http://xda-developers.com/t/grid)和 EA 的[极品飞车](http://xda-developers.com/t/need-for-speed)。

Vulkan 需要一种“亲自动手”的图形开发方法；在事物的发展过程中通常会有更多的工作要做。但结果是更低的 CPU 开销，这通常会提高整体性能。这对于像 PPSSPP 这样的平台来说是非常有益的，在 PPS spp 中，每一个释放的处理周期都可以导致难以模仿的游戏加速。

完整的变更日志在下面。

> *   全面的 Vulkan 支持，现在也支持 Android。在支持的设备上非常快。(#10033, #10049)
> *   更智能的图形状态管理，降低所有后端的 CPU 消耗(#9899)
> *   Android:支持阿拉伯语和其他我们以前无法支持的脚本
> *   修复 Android 小工具、屏幕缩放(#10145)
> *   修正了视频转储
> *   修正了荣誉勋章中的几何问题
> *   实施即时抽奖，修复 Thrillville (#7459)
> *   软件渲染的改进，速度和准确性
> *   PSP 贝塞尔曲线和样条曲线的硬件镶嵌(被一些游戏使用)
> *   部分 sceUsbGps 和 sceUsbCam 支持(Android)
> *   Android“持续性能模式”可避免热量限制(#9901)
> *   Linux 控制器映射修复(#9997)
> *   各种错误修复和兼容性改进

自上周更新以来，随后的一个补丁- PPSSPP 1.5.2 -修复了一些由 Vulkan 引起的不稳定和崩溃。如果您过去尝试过 PPSSPP，但对其性能感到失望，那么值得再试一次。你可能会印象深刻。