# Realme X50 5G bootloader 解锁工具和内核源代码现已推出

> 原文：<https://www.xda-developers.com/realme-x50-5g-bootloader-unlock-tool-and-kernel-source-code-are-now-available/>

随着[骁龙 765/G](https://www.xda-developers.com/qualcomm-snapdragon-765-processor-specifications-features/) SoC 的推出，高通帮助安卓手机制造商进军平价 5G 智能手机领域。几家中国原始设备制造商决定将这种芯片组集成到他们的手机中，我们已经在市场上推出了一些中端 5G 手机，如 [Redmi K30 5G](https://www.xda-developers.com/xiaomi-redmi-k30-5g-4g-120hz-display-snapdragon-765g-64mp-sony-imx686-china-launch/) 和[中兴 Axon 11](https://www.xda-developers.com/zte-axon-11-5g-smartphone-specs-pricing-availability/) 。Realme，[是 2019 年最大的成功故事之一](https://www.xda-developers.com/xiaomi-samsung-regain-market-share-india-q4-2019-realme-declined/)，也推出了基于同一芯片的第一款 5G 手机、 [Realme X50 5G](https://www.xda-developers.com/realme-x50-5g-snapdragon-765g-120hz-master-edition-ui/) 。为了促进该设备的第三方开发，Realme 现在允许 bootloader 解锁，并发布了 Realme X50 5G 的内核源代码。

[与其他 Realme 手机](https://www.xda-developers.com/realme-x-bootloader-unlock-kernel-source-code/)类似，Realme X50 5G 上的引导加载程序可以使用 Realme 在其论坛上发布的独特的设备特定解锁工具(又名*深度测试*)解锁。该过程完全擦除设备并禁用后续 OTA 更新。然而，可以通过引导程序接口将手机连接到 PC，并执行典型的`fastboot flashing lock`命令来重新锁定引导程序。如果你想查看详细的一步一步的引导装载解锁指南，可以在他们的论坛上查看下面的帖子。

**[Realme X50 5G Bootloader 解锁指令(中文)](https://www.realmebbs.com/post-details/1243126041673740288)**

Realme 还发布了这款设备的内核源代码，这将方便售后开发者定制恢复、内核和 rom。不过，该公司以发布不完整的源代码而闻名，因此修补者在处理这棵树时可能会面临一些困难。

**[Realme X50 5G 内核来源](https://github.com/realme-kernel-opensource/realmeX50-kernel-source)**

值得一提的是，Realme X50 5G 仅在中国发售。虽然大规模发布是在不久前推测的，但该公司向全球观众展示了一个更强大的 [Realme X50 Pro 5G](https://www.xda-developers.com/realme-x50-pro-snapdragon-865-65w-fast-charging-90hz-display/) ( [我们的印象](https://www.xda-developers.com/realme-x50-pro-5g-hands-on-first-impressions/))。尽管如此，非专业版本正在 Android 10 驱动的 Realme UI 的基础上获得稳定的软件更新，内核源代码和 bootloader unlocker 应用程序的发布应该有助于 kickstart 在设备上的开发。