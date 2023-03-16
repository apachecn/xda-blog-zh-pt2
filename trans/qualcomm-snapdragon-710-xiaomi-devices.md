# 独家:高通骁龙 710 是一个重新命名的 670，至少有两个小米设备

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-710-xiaomi-devices/>

高通的[最高端的骁龙系列](https://www.xda-developers.com/qualcomm-snapdragon-845-hands-on-benchmarks-first-impressions/)吸引了媒体的大部分注意力，因为它是高通拥有最多数量和最新功能的地方。但是，运行高端高通骁龙 845 的手机不会占新智能手机销售的大部分，事实上，那些拥有该公司预算和中端片上系统的智能手机将会大卖。随着新一代片上系统的出现，制造工艺和其他方面的改进最终会转化为其他 SoC 设计。有传言称，[高通骁龙 670](https://www.xda-developers.com/snapdragon-670-launch-2018/) 将在今年推出，作为[更便宜的骁龙 845](https://www.xda-developers.com/qualcomm-snapdragon-670-kernel-source/) 的降级版本，但现在看来，高通正在将骁龙 670 (sdm670)重新命名为高通骁龙 710 (sdm710)，我们也可以确认它将在至少两款即将推出的小米设备上推出。

* * *

## 高通骁龙 710，具有 2 个大 CPU 内核+ 6 个小 CPU 内核的 SoC

几天前，我[报道了](https://twitter.com/MishaalRahman/status/982706807108972544)两款代号为“sirius”和“comet”的小米设备将采用未宣布的骁龙 670。这些信息是基于由 [@FunkyHuawei](https://twitter.com/FunkyHuawei) 获得的固件文件，他是 [FunkyHuawei.club](https://funkyhuawei.club/) 服务的幕后人，该服务允许用户[更新](https://funkyhuawei.club/models)、 [unbrick](https://www.reddit.com/r/FunkyHuawei/comments/7d5wsi/introducing_funkyhuawei_unbrick_flash_tool/) 或[更名](https://www.reddit.com/r/FunkyHuawei/comments/7a5sab/introducing_funkyhuawei_rebrand_tool_rebrand_any/)华为，并对手机收费。自从那份初始报告以来，我已经得到了更新的固件文件，其中所有提到骁龙 670 的地方都被替换成了骁龙 710。起初，我认为小米只是决定使用更新的高通骁龙芯片，但一个可靠的消息来源告诉我，未宣布的骁龙 670 不再存在，而是被重新命名为即将到来的 710。

这种变化的进一步证据可以在高通 CodeAurora 论坛上的提交中找到，如下所示。

来自 *WinFuture* 的 Roland Quandt 最初报道了骁龙 710 的存在，尽管他当时无法分享任何进一步的细节。不幸的是，这是因为所有的细节都已经被他记录下来了。通过挖掘 sdm670 的内核源代码，他发现了 CPU 和 GPU 的大部分规格。现在被称为 710 的 670 将拥有一个双核高端 CPU 集群(定制的 ARM Cortex-A75)和一个六核低端 CPU 集群(定制的 ARM Cortex-A55)。我们还可以通过我们在小米设备固件中的发现来证实这种不寻常的核心配置，如下所示。

至于 GPU，会是 Adreno 615，频率在 430MHz-700Mhz 之间。更多详情可点击查看[。](https://www.xda-developers.com/qualcomm-snapdragon-670-kernel-source/)

* * *

## 小米“彗星”和“天狼星”

我们现在能够分享即将发布的小米设备的一些初步规格和功能，这些设备的代号为“彗星”和“天狼星”。我们用要点格式列出了我们的发现，以便于理解。遗憾的是，目前我们无法分享任何关于确切的相机硬件或设备营销名称的信息。此外，请记住，这些设备中的一个或两个可能永远不会上市——小米和其他原始设备制造商一直在内部测试从未售出的设备。

### 彗星

*   sdm710
*   具有始终显示功能的有机发光二极管
*   安卓 8.1 奥利奥
*   小米 mi 设备
*   双 SIM 卡
*   红外线增强器
*   3100 毫安时电池
*   无 NFC
*   没有 microSD 卡插槽

### 天狼星。亦称 DOG STAR

*   sdm710
*   带显示槽口的有机发光二极管，始终显示功能
*   安卓 8.1 奥利奥
*   小米 mi 设备
*   双 SIM 卡
*   红外线增强器
*   3120 毫安时电池
*   无 NFC
*   没有 microSD 卡插槽
*   相机中的肖像模式

如果我们对这些设备或骁龙 710 有更多的了解，我们一定会让你们知道。