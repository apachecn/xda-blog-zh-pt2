# 华硕 ROG 电话 3 引导加载程序解锁工具，固件和内核源代码

> 原文：<https://www.xda-developers.com/asus-rog-phone-3-bootloader-unlock-tool-firmware-kernel-sources-release/>

华硕的“玩家国度”(ROG)子品牌面向游戏爱好者，新发布的 ROG 手机 3 提供了手机游戏玩家梦寐以求的一切。除了拥有顶级的规格，如高通的旗舰[骁龙 865 加](https://www.xda-developers.com/qualcomm-snapdragon-865-plus-launch/) SoC，高达 16GB 的 LPDDR5 RAM，512GB 的 UFS 3.1 存储，华硕 ROG 手机 3 还附带[三个月的免费 Stadia Pro 订阅](https://www.xda-developers.com/asus-rog-phone-3-three-months-free-stadia-pro/)。这家台湾 OEM 厂商甚至允许修补者使用 ROG UI 的“X 模式”来摆弄底层内核参数，以便最大限度地利用 CPU 和 GPU。如果你想要一些严肃的售后发展，如建立 TWRP 或移植一个基于 AOSP 的 ROM，那么你会很高兴知道华硕已经发布了这款设备的内核源代码和官方 bootloader 解锁应用程序。

**[华硕 ROG 手机 3 XDA 论坛](https://forum.xda-developers.com/asus-rog-phone-3)**

**[华硕 ROG Phone 3 XDA 点评:游戏智能手机之王回来了](https://www.xda-developers.com/asus-rog-phone-3-review/)**

有趣的是，解锁程序显示了第三代 ROG 手机的代号“奥比万”。尽管是“强制敏感的”(*双关语意为*)，解锁这部手机上的引导加载程序会使保修无效，并且还会禁用后续的 OTA 更新。此外，解锁过程会自动执行工厂重置，因此强烈建议您在继续之前备份数据。

一旦你有了一个解锁的引导程序，并且可以访问官方的内核源代码，你就可以开始构建 rom 和内核了。华硕已经在一个档案中公布了这款设备的中文和全球版本的统一内核源代码，链接如下。不幸的是，在这样的打包方式下，你找不到合适的提交历史。

华硕还发布了 ROG Phone 3 的官方固件包，这将有助于恢复手机上的操作系统。请注意，在中国单元上交叉刷新全局固件(反之亦然)可能会影响获得 OTA 更新的能力，因此请始终为您的型号获取合适的软件包。

**[华硕 ROG 手机 3: Bootloader 解锁工具&内核来源](https://www.asus.com/Phone/ROG-Phone-3/HelpDesk_Download/)**