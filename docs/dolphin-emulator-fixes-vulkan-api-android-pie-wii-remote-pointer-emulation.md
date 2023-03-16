# Dolphin Emulator update 增加了 Android Pie 上 Vulkan API 的修复，Wii 远程指针仿真等等

> 原文：<https://www.xda-developers.com/dolphin-emulator-fixes-vulkan-api-android-pie-wii-remote-pointer-emulation/>

Android 上的 Dolphin Emulator 是制作最精良的模拟器之一。你可以直接从手机上玩 Wii 游戏和 GameCube 游戏，只要它足够强大。如今，像 Razer Phone 2 和一加 6T T1 这样的设备足以做到这一点。我个人很喜欢《辛普森一家:打了就跑》( Simpsons: Hit and Run)和《超级粉碎兄弟》(Super Smash Bros Brawl)。虽然性能并不完美，但仍有很大的改进空间。2018 年 12 月和 2019 年 1 月的最新 Dolphin progress 报告记录了模拟器 Android 版本的许多性能增强更改，其中一些非常棒。

### Vulkan:修复 Android 9 Pie 更新中新 Adreno 驱动程序的渲染问题

首先，也是最重要的更新之一，是对运行 Android Pie 的高通骁龙设备的 Vulkan API 的修复。随着高通向 OEM 厂商提供的 Android 9 Pie BSP 附带的更新 Adreno 图形驱动程序，Dolphin Emulator 由于 Adreno 驱动程序损坏而无法正确使用 Vulkan API，这是一个问题，因为最有可能尽最大能力运行游戏的设备也最有可能更新到该版本。使用 Vulkan API 通过 Dolphin 运行游戏通常会比只使用 OpenGL 带来更好的性能，但有时会出问题。不过，使用它更好，所以不能使用意味着设备所有者没有充分利用他们的智能手机。现在，由于 Dolphin Emulator 的开发人员所做的一个变通办法，这个问题已经解决了，用户应该会看到更好的性能。

### 包围盒固定在 GLES

边界框是一种用于像《纸上马里奥:千年之门》和《超级纸上马里奥》这样的游戏中的特定效果的功能。模拟功能依赖于 OpenGL ES 功能，但 Adreno 和 Mali GPUs 使用的 GL ES 功能比 OpenGL ES 少得多。由于模拟器编码中的一个错误，模拟器调用了 GL ES 中不可用的函数，像《纸上马里奥:千年之门》这样的游戏在非 NVIDIA SHIELD 设备上会崩溃。

### Wii 远程指针仿真

除此之外，Wii 的远程指针模拟已经加入。像超级马里奥银河这样的游戏在某种程度上依赖于 Wii 遥控器指向屏幕的能力，如果没有海豚吧，这是不可能的。现在工作已经完成，所以你可以简单地点击屏幕上你想指向的地方。对于射击者来说它会很笨重，但是对于那些你可能不需要同时移动和指向的游戏来说它非常好用。《动物穿越:城市居民》是另一个可以与 Wii 远程指针仿真完美结合的游戏。

https://thumbs.gfycat.com/InsistentZestyIchidna-mobile.mp4

### 杂项变更

虽然功能改进很棒，但底层优化也很出色。GameCube 官方适配器现在可以工作了，Wii 官方遥控器也可以工作了。大量的计算和渲染修复也已经完成，所以你可以从更精确的模拟中获益。查看下面完整的博客文章，了解 Android 上改进 Dolphin 模拟器的细节。

* * *

[**来源:海豚模拟器**](https://dolphin-emu.org/blog/2019/02/01/dolphin-progress-report-dec-2018-and-jan-2019/)