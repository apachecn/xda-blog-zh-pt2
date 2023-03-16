# 高通的骁龙 Wear 3300 是 Wear OS 智能手表的芯片

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-wear-3300-smartwatch-chip-wear-os/>

谷歌的智能手表 Android 操作系统 Wear OS 远不如智能手机、平板电脑或电视的 Android 操作系统成功，对此有很多指责。我们可以指责谷歌没有足够的信心推出自己的智能手表硬件，或者指责 T2 在其大型开发者大会上几乎没有给 Wear OS 时间，或者我们可以指责高通未能设计出有竞争力的智能手表 SoC。三星、华为和苹果的智能手表采用定制的操作系统和 SOC，电池续航时间往往比搭载 Wear OS 和高通骁龙 Wear 2100 或 3100 的智能手表长得多。高通目前的可穿戴平台是基于 28 纳米制造工艺制造的；相比之下，三星在 Galaxy Watch 系列中发现的 Exynos 9110 是用 10 纳米制造工艺制造的。然而，高通可能会通过其下一代可穿戴 SoC 来弥合这一差距，它可能会以骁龙 Wear 3300 的形式出现。

我们第一次听说高通的下一代可穿戴芯片组[是在 7 月](https://www.xda-developers.com/qualcomms-next-chip-may-finally-make-wear-os-smartwatches-worth-getting/)的时候，当时 *WinFuture* 报道了两款处于原型阶段的芯片组的存在。人们认为，其中一个芯片组可以作为骁龙磨损 2700 和其他骁龙 429 磨损上市，但芯片组仍然处于非常早期的发展，没有迹象表明他们将何时推出。感谢 XDA 知名开发商 [arter97](https://forum.xda-developers.com/member.php?u=4898097) 的提示，我们知道高通确实正在准备一款基于[2018 年中期骁龙 429 移动平台](https://www.xda-developers.com/qualcomm-snapdragon-632-439-429-mobile-platforms/)的芯片组，它很可能被称为骁龙 Wear 3300。

在 Code Aurora 论坛上，高通上传了其各种芯片组的 Linux 内核源代码，上传了一个为“SDW3300 设备”添加设备树的[提交](https://source.codeaurora.org/quic/la/kernel/msm-4.9/commit/arch/arm64/boot/dts/qcom/sdw3300-bg-1gb-wtp.dts?h=LA.UM.8.3.r1-06300-sdm845.0&id=ddcf98f1bfc270f5829306ab629ceb3e775de0ed)上传的设备树源(DTS)文件名为“sdw3300-bg-1gb-wtp.dts”，代码表明新平台基于骁龙 429，代号为“斯派罗”

高通骁龙 429 于 2018 年年中推出，是一款 12 纳米芯片，配有 4 个主频高达 1.95GHz 的 ARM Cortex-A53 CPU 内核。高通可能会将这 4 个 CPU 内核与低功耗协处理器、PMIC、集成 DSP 和其他组件配对，形成新的骁龙穿戴平台。[骁龙 Wear 3100](https://www.xda-developers.com/qualcomm-snapdragon-wear-3100-wear-os-smartwatch/) 的最大问题是其主要应用处理器仍然是采用 28 纳米工艺制造的 4 个 ARM Cortex-A7 CPU 内核，因此新的可穿戴 SoC 应该更加节能，从而提供更长的电池寿命。[搭配 1GB 内存](https://www.xda-developers.com/ticwatch-pro-4g-lte-review-only-as-good-as-its-weakest-link/)，未来的 Wear OS 智能手表也将比以往表现更好。

当然，在这一点上，这仍然只是一个谣言。高通尚未正式确认其下一款可穿戴 SoC 的任何细节。我们联系了高通进行评论，如果有回音，我们会更新这篇文章。