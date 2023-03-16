# 非官方的 TWRP 现可用于一加 8 和一加 8 专业版

> 原文：<https://www.xda-developers.com/unofficial-twrp-oneplus-8-oneplus-8-pro/>

# 非官方的 TWRP 现可用于一加 8 和一加 8 专业版

一个统一的非官方建立的 TWRP 现在可用于一加 8 和一加 8 专业，礼貌 XDA 资深成员毛罗诺弗里奥。

一加最近[发布了一加 8(代号“instantnoodle”)和一加 8 Pro(代号“instant noodle”)的内核源代码](https://www.xda-developers.com/oneplus-8-pro-kernel-source-code-now-available/)，以促进第三方开发。该社区还设法获得了设备专用的[unbrick](https://www.xda-developers.com/oneplus-8-unbrick-tool-msmdownloadtool-edl-available/)软件包，这对于在修补过程中出现问题的情况下恢复手机非常方便。如果你是那种改装手机的人，那么你应该很高兴地知道，一加 8 和一加 8 Pro 现在都有了统一的非官方 TWRP 版本。

**[一加 8 XDA 论坛](https://forum.xda-developers.com/oneplus-8) ||| [一加 8 亲 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro)**

**[在亚马逊上预订一加 8 系](https://www.amazon.in/b/?node=21439725031&tag=xdaportalin-21)**

由 XDA 资深成员 mauronofrio 为这些手机编译的 TWRP 的当前版本将允许你没有任何麻烦地刷新 Magisk 和定制内核，但是许多东西仍然是坏的。虽然您可以挂载像“系统”、“供应商”和“产品”这样的分区，但是您不能修改它们的内容。整个情况与 Android 10 的“超级”分区的引入直接相关，该分区包含多个可动态调整大小的分区。谷歌为 AOSP 在 Android 10 中的恢复实现带来了一些变化，最终[迫使 TWRP 团队](https://www.xda-developers.com/twrp-lead-explains-android-10-support-custom-recovery/)重组定制恢复，并重写了一些内部组件，以支持使用 Android 10 发布的设备，如一加 8 duo。该过程尚未完成，因此可能需要一段时间才能得到一个完全适用于一加 8/8 专业版的 TWRP。

除了 TWRP 特有的错误，数据解密还不能在这个版本上运行。还建议用户在执行备份时使用“系统映像”和“供应商映像”条目，而不是“系统”和“供应商”。根据开发者的说法，最好是避免在一加 8 或一加 8 Pro 设备上永久刷新恢复映像，而是选择使用快速启动界面进行临时启动:`fastboot boot twrpname.img`。

**TWRP 下载讨论线程:[一加 8](https://forum.xda-developers.com/oneplus-8/development/recovery-unofficial-twrp-oneplus-8-t4101315)| |[一加 8 Pro](https://forum.xda-developers.com/oneplus-8-pro/development/recovery-unofficial-twrp-oneplus-8-pro-t4101313)**