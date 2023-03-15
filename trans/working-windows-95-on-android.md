# Android 的 Windows 95 工作端口

> 原文：<https://www.xda-developers.com/working-windows-95-on-android/>

我们已经看到了许多不同类型的 Windows Mobile 设备的移植，但是如何将不同的操作系统移植到 Android 呢？XDA 成员和传奇人物 mamaich 为我们带来了两款 Android 设备模拟器，这两款模拟器将允许 Android 用户启动 Windows 95。QEMU 和 BOSCH 都在知道如何使用它们的人中广受欢迎，因为它们已经在其他项目中用于在其他设备上运行不同的 Windows 版本。

虽然项目进展顺利，但仍有待改进。不幸的是，mamaich 提到他不会继续开发这些港口。然而，他分享了所有的资源和知识，这些资源和知识是任何有适当技能的人从他中断的地方重新开始所需要的。在众多要求中，需要一个具有大量 RAM 的设备和至少一个 VGA 屏幕。

> BOCHS 太慢，无法使用，但非常稳定。
> 
> QEMU 确实很快——但是漏洞百出。SB16 模拟正在工作，但没有 MIDI 音乐。FPU 模拟不正确/不完整，因此可能会导致某些程序无法运行或行为异常。网络不工作。键盘/鼠标模拟远非完美。
> 
> 如果你在 QEMU 中禁用 32 位磁盘驱动程序，Windows 9x 可以在 QEMU 中工作。这是 Android 的一个 bug(pread/p write 功能不起作用)。Windows 9x 速度真的很快。
> 
> 这个 QEMU 构建基于 0.9.1，更新的版本在 ARM TCG 中有 bug，不能引导 Windows 或类似的操作系统。
> 
> 我不会继续从事这两个项目。如果有人感兴趣-我会提供所有的来源和一些关于建设的信息。需要具备 C++、ARM 和 x86 asm 的知识。

你可以在[端口线程](http://forum.xda-developers.com/showthread.php?p=6661598)中找到更多信息。