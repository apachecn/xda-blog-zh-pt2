# 谷歌正在为 Pixel 手机和 Chromebooks 开发自己的芯片

> 原文：<https://www.xda-developers.com/google-is-working-on-its-own-chip-for-pixel-phones-and-chromebooks/>

定制 SOC 在当今的高价值移动设备市场中非常罕见，但在旗舰智能手机中仍然可以找到。高通的 SOC 主导着智能手机行业，而联发科的 SOC 则是一种成本更低的替代产品。在高端，三星和华为的海思继续做定制 SOC，而且仅限于自己的手机。苹果、三星和华为这三大智能手机制造商目前都使用定制 SOC(尽管三星在一些市场销售其带有骁龙 SOC 的旗舰手机)。谷歌长期以来一直想在智能手机市场上与大联盟竞争，但由于各种原因，其 Pixel 手机风险投资即使在三年半后也未能起飞。今年，一些证据显示，谷歌 Pixel 5 [可能由中端高通骁龙 765 SoC](https://twitter.com/mishaalrahman/status/1237802880331022336)驱动，而不是传统选择的高端骁龙 865 SoC。但是明年，事情可能会变得更加有趣。

在过去的两个月里，两家韩国出版物[*【et news】*](https://www.etnews.com/20200213000095)和[*【Clien.net】*](https://www.clien.net/service/board/cm_stock/14811926)都报道称，谷歌可能正在开发自己的 SoC，用于未来版本的谷歌像素。这一点现在已经被 *Axios* 所证实。 *Axios* 独立报道称，谷歌已经在开发自己的处理器方面取得了“重大进展”,最快明年将用于未来的谷歌 Pixel 手机。最终，定制芯片也将支持 Chromebooks。

Axios 指出，此举可以帮助谷歌更好地与苹果竞争，苹果自 2010 年以来一直设计自己的芯片，自 2012 年以来一直设计自己的定制 CPU 内核。这将对高通造成损害，该公司为绝大多数旗舰 Android 手机提供骁龙 SOC，包括迄今发布的所有 Pixel 手机。

到目前为止，关于这种芯片的细节很少。它的代号为“白教堂”，是与三星合作设计的。有趣的是，该报告提到三星的尖端 5 纳米工艺将用于制造芯片。5 纳米工艺(使用 EUV)有望用于下一代移动 SOC。这对三星代工厂来说将是一个提振，因为在过去的四年里，它已经失去了苹果和高通这两个主要客户。Axios 报告提到三星也生产苹果的 iPhone 芯片，这是不正确的，但这是错误的，因为自 2015 年供应一半的苹果 A9 芯片以来，三星实际上没有生产过 iPhone SoC。自 2016 年起，苹果 A 系列芯片由 TSMC 制造。如今，三星在其 7 纳米 LPP (EUV)工艺上生产中端高通[骁龙 765](https://www.xda-developers.com/qualcomm-snapdragon-765-processor-specifications-features/) ，以及自己的 Exynos 芯片。例如，旗舰产品 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) 就采用三星自己的 7 纳米 LPP 工艺制造。

Axios 表示，最近几周，谷歌收到了该芯片的第一个工作版本。不过，这些谷歌设计的芯片预计要到明年才能用于 Pixel 手机。该芯片的后续版本可能会支持 Chromebooks，但报告称这可能会更远。该芯片将拥有一个 8 核 ARM 处理器(根据之前的报道，它可能有两个 Cortex-A78 +两个 Cortex-A76 +四个 Cortex-A55 核心)，还将包括针对谷歌的机器学习技术优化的硬件。它的一部分芯片也将致力于提高谷歌助手的性能和“永远在线”的能力。在 GPU 方面，预计它将采用 ARM 的现成 IP(Mali GPU)。调制解调器是一个问题，因为不知道它是否将由三星提供。

这不是谷歌第一次尝试制造定制芯片。2017 年，它与英特尔合作开发了 Pixel 2 的 Pixel 视觉核心，并为 Pixel 3 保留了这一核心。另一方面，Pixel 4 以[神经核心](https://www.xda-developers.com/google-pixel-4-specs-features-pricing-availability/)的形式升级了张量处理单元(TPU)。谷歌还从苹果和英特尔等公司聘请了许多芯片专家。

所有这些都还没有得到证实，因为谷歌还没有确认它的任何计划。然而，独立报告应该是可靠的。开发定制 SoC 是一件大事。但是，重要的是要记住，开发定制的 SoC 不同于从头开始设计定制的 CPU 内核。例如，华为使用定制的[麒麟 SOC](https://www.xda-developers.com/huawei-hisilicon-kirin-990-5g-integrated-modem/)，但这些芯片采用来自 ARM 的[现成 CPU 核心，并使用 ARM 的 Mali GPUs。三星在 2016 年以 Exynos M1 开始了自己的定制核心项目，但它未能与 ARM 竞争，更不用说苹果了。该项目现已结束，Exynos 990 中的 Exynos M5 是三星在可预见的未来最后一个完全定制的核心。正如我们在](https://www.xda-developers.com/arm-now-says-itll-continue-supplying-chip-technology-to-huawei/) [Galaxy S20+评测](https://www.xda-developers.com/samsung-galaxy-s20-plus-review/)中发现的那样，Exynos M5 无法匹配 ARM 的普通 Cortex-A77 内核。同样，高通最后一个完全定制的内核是 Snapdragon 820/821 中的 Kryo 内核。

因此，即将推出的谷歌定制 SoC 预计不会采用定制内核。它可能会使用 ARM 的下一代 CPU 内核，如 Cortex-A78。从这个意义上说，它看起来不会与三星明年的旗舰 Exynos SoC 有太大区别，因为报告提到定制的谷歌 SoC 将与三星合作设计。

* * *

**来源:[Axios](https://www.axios.com/scoop-google-readies-its-own-chip-for-future-pixels-chromebooks-e5f8479e-4a38-485c-a264-9ef9cf68908c.html)**