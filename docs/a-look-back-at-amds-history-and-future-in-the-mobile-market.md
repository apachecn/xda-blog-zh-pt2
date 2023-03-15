# 回顾 AMD 在移动市场的历史和未来

> 原文：<https://www.xda-developers.com/a-look-back-at-amds-history-and-future-in-the-mobile-market/>

十年前，AMD 收购了加拿大 GPU 制造商 ATI Technologies，试图扩大他们的产品组合，并致力于集成系统，就像我们现在看到的他们的 Fusion APUs(不要与其他刚刚宣布的 [Fusion 芯片](http://www.xda-developers.com/a-widening-gap-the-a10-fusion-puts-a-chokehold-on-qualcomms-prospects/) )以及今天的移动 SOC 混淆。收购后不久，他们出售了一些非核心业务部门，以便专注于台式机和笔记本电脑的 CPU 和 GPU。

在 2008 年和 2009 年，AMD 出售了他们的制造部门([【global foundries】](https://en.wikipedia.org/wiki/GlobalFoundries))、他们的机顶盒 SoC 部门([xil Leon](https://en.wikipedia.org/wiki/Xilleon))，以及他们的移动 GPU 部门(当时称为 Imageon，现在称为 [高通 Adreno](https://en.wikipedia.org/wiki/Adreno) )。虽然他们以相对较低的价格向高通出售 Imageon，仅[【6500 万美元](http://www.eweek.com/c/a/Mobile-and-Wireless/AMD-Sells-Handset-Division-to-Qualcomm-for-65-Million) 因为它在当时由功能手机和 PDA 主导的移动市场中表现不佳，但他们确实看到了未来重新进入市场的潜力，并决定保留 Imageon 品牌名称(他们没有为 Xilleon 这样做)。AMD 收购 ATI 和出售 Imageon 之间的短暂时间导致了一些有趣的组合，如[HTC Advantage](http://forum.xda-developers.com/htc-advantage)，2007 年初的一款 5 英寸触摸屏手机，配有 [ARM 英特尔 CPU](https://en.wikipedia.org/wiki/XScale) 和 AMD 显卡。

AMD 保留了 Imageon 品牌名称，因为即使在那个时候，手机、笔记本电脑和台式机的融合已经开始变得明显，尽管很少有人预测它会发生得多快。随着处理器变得越来越快，我们将不再需要笔记本电脑的更多处理能力来完成大多数人使用电脑完成的任务，因此我们将重点放在能效和电池寿命上。

随着 AMD 的 Zen 处理器即将推出，AMD 重新进入平板电脑市场的时机可能已经成熟

随着笔记本电脑 CPU 和 GPU 功耗的下降，我们开始看到越来越小的差距，一些笔记本电脑甚至运行在本质上是平板电脑的芯片上。小型 4.5w TDP SOC，不需要冷却风扇，集成了 GPU 和 CPU，就像你在手机中看到的一样。

随着 AMD 的 [禅](https://en.wikipedia.org/wiki/Zen_(microarchitecture)) 处理器即将上市，AMD 重新进入平板电脑市场的时机可能已经成熟。不幸的是，他们缺乏 LTE 无线电将阻止他们直接进入手机市场(这也是 Nvidia 和英特尔陷入困境的原因)，但这并不阻止他们将他们的技术授权给其他制造商，这些制造商正在寻找 ARM Mali GPU 之外的东西。



AMD 对许可他们的 GPU 技术并不陌生，早在 2007 年就已经将 [许可给意法半导体](http://www.theregister.co.uk/2007/02/13/amd_licenses_phone_gpu_tech/) ，据报道去年正在与 [谈判将它许可给联发科](http://www.fudzilla.com/news/graphics/37209-mediatek-to-license-amd-graphics) 。看到[传言](http://www.xda-developers.com/xda-external-link/samsung-allegedly-attempting-to-license-nvidia-and-amd-gpu-technology/)三星正试图授权 Nvidia 或 AMD 的 GPU 设计真的不应该感到惊讶。Nvidia 似乎有点不太可能，特别是看到他们如何在平板电脑市场上直接与三星竞争，并投入大量资金到他们的 [动态二进制翻译](http://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-2-oems-cheating-benchmarks-custom-cores-honest-manufacturers/) 丹佛 CPU 核心，这些核心只用于他们的 Tegra 芯片，但 AMD 可能是一个有趣的合适人选。

AMD 正在寻找额外的收入来源，以帮助他们在 GPU 市场上与 Nvidia 进行双管齐下的斗争(其中 [图形核心 Next](https://en.wikipedia.org/wiki/Graphics_Core_Next) 显示出强劲的[Vulkan](http://www.xda-developers.com/vulkan-api-means-more-control-but-not-outright-replacement-of-opengl/))和英特尔在 CPU 市场(其中他们的[ZenCPU 似乎在与【的失败斗争多年后恢复了竞争力)将 GPU 技术授权给手机和平板电脑芯片带来的额外收入可以帮助他们为跟上英伟达和英特尔所需的大量研发支出提供资金，但更重要的是，这将有助于为未来进入移动领域的尝试铺平道路。它将解决 Android 对 AMD GPUs 支持的许多小问题。](http://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-2-oems-cheating-benchmarks-custom-cores-honest-manufacturers/)

这是关键。支持。 **软件支持** 。如果 AMD 想要进入平板电脑 SoC 和无风扇笔记本电脑市场，他们需要为运行在这些平台上的操作系统提供软件支持。AMD 一直在大力改进他们的 Linux 支持， [开源了过去两年来他们 GPU 堆栈的很大一部分(](https://lists.freedesktop.org/archives/dri-devel/2015-April/081501.html)[和 GPUOpen](http://www.xda-developers.com/robert-hallock-gpuopen-is-amds-long-term-open-source-strategy/) 等外围工具)，其中很大一部分转移到了 Android 上(开源代码对促进售后开发支持特别有帮助)。让他们的 GPU 进入几个第三方 SoC 将使他们有时间真正消除错误，并在推出自己的平板 SoC 之前改善对 Android(和 Linux)的支持。

AMD 能利用他们的异构系统架构成功进入平板电脑市场吗？AMD 应该尝试让他们的 GPU 进入像 Imagination Technologies(PowerVR)、ARM 和 Vivante 这样的第三方 SOC 吗？请在下面的评论中告诉我们！