# UFS 3.1 宣布提高闪存芯片的速度和能效

> 原文：<https://www.xda-developers.com/ufs-3-1-speed-power-efficiency-flash-storage-chips/>

通用闪存，即 UFS，是用于旗舰手机和中端手机的闪存标准。三星 Galaxy S6 是 2015 年第一款使用 UFS 存储的手机。在此后的几年里，它已经慢慢蔓延到低成本市场，以至于最新的低端中档手机现在也有了 UFS 存储。UFS 存储比 eMMC 闪存标准快得多，后者仍在廉价手机中使用。2019 年，负责微电子行业标准制定的 JEDEC 固态技术协会[公布了](https://www.xda-developers.com/western-digital-ufs-3-0-storage-smartphones/) UFS 3.0。虽然大多数 2019 年的旗舰机选择坚持使用旧的 UFS 2.1 NAND，但一些手机，如[一加 7](https://www.xda-developers.com/oneplus-7-review/) 系列、三星 Galaxy Fold、[三星 Galaxy Note 10](https://www.xda-developers.com/samsung-galaxy-note-10-review/) 系列和 [Realme X2 Pro](https://www.xda-developers.com/realme-x2-pro-xda-review/) 确实选择使用更新、更快的 UFS 3.0。现在，JEDEC 发布了 UFS 3.1，通过提高速度和功效改进了 UFS 3.0 标准。

UFS 3.1(jesd 220 e)的发布是与一个新的可选配套标准(JESD220-3: UFS 主机性能增强器(HPB)扩展)一起宣布的。JESD220E 和 JESD220-3 均可从 JEDEC 网站下载。

UFS 3.1 JESD220E 标准比 UFS 3.0 标准有三大改进。首先，它有一个写加速器，一个 SLC 非易失性缓存，可以提高写入速度。其次，新的 UFS 设备低功耗状态称为深度睡眠，目标是与其他功能共享 UFS 稳压器的低成本系统。最后，它有一个性能调节通知，允许 UFS 设备在存储性能调节到高温时通知主机。SLC 非易失性缓存的使用可能是这里最重要的特性，因为它将有助于提高实际性能。这项技术用于使用移动 NVMe 固态硬盘的设备，如苹果 iPhone 和 iPad。此外，固态硬盘已经支持所有这些功能，因此在 UFS 3.1 中包含这些功能将有助于缩小两者之间的差距。

JESD220-3 主机性能提升(HPB)扩展)提供了一个选项，用于在系统的 DRAM 中缓存 UFS 设备逻辑到物理的地址映射。JEDEC 声明:“对于具有大密度的 UFS 设备，使用系统 DRAM 提供更大和更快的缓存，从而提高设备的读取性能”。

JEDEC UFS 公司继续与 MIPI 联盟合作以形成其互连层。它参考了 MIPI M-PHY 4.1 版物理层规范和 MIPI UniPro 1.8 版传输层规范。

既然 UFS 3.1 已经宣布，它很可能会被一些 2020 年的旗舰所采用。一加 8 系列将是主要竞争者，三星 Galaxy Note 20 系列也是如此。这并不像 UFS 3.0 对 UFS 2.1 的更新那样大(因为理论上的最高带宽速度仍然保持在 23.2Gbps)，但低成本设备在存储性能和电池寿命方面的实际改进将受到欢迎。存储性能一直是移动设备的瓶颈，因此很高兴看到这方面的持续改进。

* * *

**来源:[杰德克](https://www.jedec.org/news/pressreleases/jedec-publishes-update-universal-flash-storage-ufs-standard)**