# ARM 的下一代 Mali GPU 将通过 Play Store 支持可更新的驱动程序

> 原文：<https://www.xda-developers.com/arms-next-mali-gpu-updateable-drivers-google-play-store/>

高通在 2019 年 12 月宣布了[骁龙 865](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/) 和[骁龙 765/765G](https://www.xda-developers.com/qualcomm-snapdragon-765-processor-specifications-features/) 移动平台，这些芯片组支持的游戏功能列表中一个有趣的新增功能是支持可更新的 GPU 驱动程序。虽然 GPU 驱动程序通常与 OTA 更新捆绑在一起，但高通解决了通过应用商店推出更频繁更新的方法，[小米成为今年早些时候第一个推出 Mi 10 系列和 Redmi K30 Pro 更新的智能手机品牌。在这起诉讼之后，硅设计公司 ARM 也宣布了对其 Mali 类 GPU 的类似支持，这些 GPU 在联发科、华为的海思和三星的 Exynos 移动处理器上可以找到。](https://www.xda-developers.com/xiaomi-adreno-gpu-driver-update-snapdragon-865/)

就像个人电脑一样，智能手机上可更新的 GPU 驱动程序可以方便地修复错误，提高图形性能，或添加 OpenGL 或 Vulkan APIs 的新功能。由于制造商需要几个月的时间来完善 OTA 更新，当独立于系统更新时，GPU 驱动程序的更新可以通过应用商店更快更频繁地发送。

通常，OEM 可以通过使用 GPU 应用程序的占位符来准备他们的软件，等待芯片制造商(高通、联发科、华为或三星)在更新的 [BSP](https://en.wikipedia.org/wiki/Board_support_package) 中实现更新的 GPU 驱动程序，并在签署应用程序后通过 app store 将更新的 GPU 驱动程序推送到所有支持的设备。如上所述，小米已经受益于该功能，并通过自己的应用商店向[米 10(评测)](https://www.xda-developers.com/xiaomi-mi-10-review/)、[米 10 Pro(评测)](https://www.xda-developers.com/xiaomi-mi-10-pro-review/)和 Redmi K30 Pro 上的 Adreno 650 GPU 发送更新。

在[博客文章](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/mali-gpu-drivers-and-android-gpu-inspector)中，ARM 宣布它已经实现了对 Mali GPUs 可更新驱动程序的支持，但没有透露哪些 GPU 将受益于该功能。我们怀疑这适用于最近[与 ARM 的 Cortex-A78 CPU](https://www.xda-developers.com/arm-announces-cortex-a78-cpu-mali-g78-gpu-ethos-n78-npu/) 架构一起发布的 Mali-G78 GPU。Mali-G78 GPU 预计将出现在联发科、三星和华为即将推出的移动平台上——尽管海思可能无法收获这一发展的果实，可能不得不[求助于重用去年的麒麟处理器](https://www.xda-developers.com/huawei-honor-high-end-mediatek-chipsets-new-phones-new-u-s-trade-restrictions/)，因为半导体制造商[已经被禁止与华为](https://www.xda-developers.com/us-government-blocks-chip-makers-huawei-hisilicon-kirin-soc/)开展业务，这是美国政府实施的[贸易禁令的一部分。](https://www.xda-developers.com/google-revoke-huawei-android-ban-blacklist/)

多年来，包括目前旗舰芯片组上的 Mali-G77 在内的 Mali GPUs，如三星 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) 和联发科 [Dimensity 1000/1000L](https://www.xda-developers.com/mediatek-dimensity-1000-7nm-soc-integrated-5g/) 一直无法跟上高通 Adreno 系列中同行的性能。对可更新的 GPU 驱动程序的支持意味着这种情况有一定的改善空间，有利于高通以外的公司。

除了可更新的 GPU 驱动程序，ARM 还宣布即将推出的 Mali GPUs 将支持 [Android GPU Inspector](https://www.youtube.com/watch?v=7n9vTYs17_Q) ，这是一款开源的分析工具，将帮助游戏开发人员优化其游戏和应用程序的图形性能，旨在实现更高的帧率和更好的渲染质量，适用于来自多家供应商和跨多种设备的不同 GPU。三星 Galaxy S10、三星 Galaxy Note 10、三星 Galaxy S20 和谷歌 Pixel 4 是即将在 Android GPU Inspector 上支持的一些设备。