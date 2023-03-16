# 开发者将 ARM 上的 Windows 10 移植到三星 Galaxy S8 上

> 原文：<https://www.xda-developers.com/developers-port-windows-10-on-arm-to-the-samsung-galaxy-s8-and-other-snapdragon-835-powered-phones/>

# 开发人员将 ARM 上的 Windows 10 移植到三星 Galaxy S8 和其他 Snapdragon 835 手机上

一个自制的 UEFI 固件使 Snapdragon 835 驱动的三星 Galaxy S8 能够启动 ARM 版本的 Windows 10。继续阅读，了解更多信息！

像一加和索尼这样对开发者友好的 OEM 厂商以发布内核源代码和[设备树](https://www.xda-developers.com/xperia-10-xperia-10-plus-open-devices-program/)而闻名；后者作为一种机制，一旦主引导程序启动，就向 ARM 平台上基于 Linux 的 Android 内核描述硬件。然而，像 Microsoft Windows 这样的操作系统利用高级配置和电源接口(ACPI)来完成相同的任务，而低级硬件初始化现在由统一可扩展固件接口(UEFI)来处理。有趣的是，通过大量的*黑客攻击*，可以将 UEFI 和 ACPI 支持移植到现有的 ARM 设备上，因此你可以在像[树莓派](https://www.xda-developers.com/raspberry-pi-4-upgraded-cpu-4gb-of-ram-dual-4k-displays/)这样的设备上技术上启动 Windows 10。

Windows 10 确实[原生支持](https://www.xda-developers.com/microsoft-qualcomm-and-intel-the-windows-10-arm-dustup/)ARM 架构，这在这个移植游戏中确实是个加分项。被称为 [Evsio0n](https://github.com/Evsio0n) 的开发者现在公布了一个概念验证方法，可以在高通骁龙 835 驱动的三星 Galaxy S8 上启动 ARM 上的 Windows 10。这不是我们第一次看到 [Windows 10 在 Android 手机](https://www.xda-developers.com/windows-10-arm-oneplus-6t/)上运行，但 Evsio0n 也分享了基于 [TianoCore](https://www.tianocore.org/) 项目为 Galaxy S8 构建准系统 UEFI 固件的源代码。

在报告时，[固件](https://github.com/Evsio0n/edk2sdm)能够引导 Windows 预安装环境(又名 [WinPE](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-intro) )，但是缺乏完整的 ACPI 实现阻止了完全成熟的 Windows 10 的引导。内存管理单元(MMU)在一定程度上是工作的，足以让主线 Linux 5.x 内核的 Debian Linux 启动。

Evsio0n 对王炳兴，又名 [imbushuo](https://github.com/imbushuo) 和 [fxsheep](https://github.com/fxsheep) 在这一领域的贡献给予了肯定。另一位名叫[汤姆·克里斯多佛·丹尼尔·佩雷斯](https://github.com/tomchrisdperez)的鼓吹者[在小米 Mi 6 上做了](https://twitter.com/tomchrisdperez/status/1249265248860684289)(但后来删除了)类似的开发(可能基于 [fxsheep 现有的用于设备](https://github.com/fxsheep/edk2-sagit)的 UEFI 端口)，这表明该项目最终可能支持其他基于 Snapdragon 835 的手机。虽然当前的端口远远不是日常驱动程序，特别是与 Lumia WOA 项目相比，Windows 10 可能有助于显著延长这些传统旗舰的寿命。

**[下载三星 Galaxy S8](https://github.com/Evsio0n/edk2sdm/releases)T3 的 UEFI 固件**

**[三星 Galaxy S8 论坛](https://forum.xda-developers.com/galaxy-s8)**