# Moto G8，Moto G Stylus，其他骁龙 665 Moto 手机接收统一的 OmniROM

> 原文：<https://www.xda-developers.com/moto-g8-moto-g-stylus-motorola-snapdragon-665-unified-omnirom/>

# Moto G8、Moto G Stylus 和其他几款骁龙 665 摩托罗拉手机都采用统一的 OmniROM 版本

OmniROM 的统一版本现在可用于 Moto G8、Moto G Stylus 和其他配有高通骁龙 665 的摩托罗拉手机。

此时，[高通骁龙 665](https://www.xda-developers.com/qualcomm-snapdragon-665-snapdragon-730g/) 芯片组已经问世一年多了，但摩托罗拉等原始设备制造商在设计其最新的中端产品时仍然喜欢使用这种八核 SoC。迄今为止，联想拥有的品牌已经发布了几款基于骁龙 665 的智能手机，包括 [Moto G8](https://www.xda-developers.com/motorola-moto-g8-official-snapdragon-665/) 、 [Moto G Stylus 和 Moto G Power](https://www.xda-developers.com/moto-g-stylus-moto-g-power-officially-announced/) 。这些设备的发布策略非常有趣:在美国销售的 [Moto G Fast](https://www.xda-developers.com/moto-g-fast-moto-e-2020-affordable-announced-us/) 不过是引擎盖下的 Moto G8，而欧洲的 [Moto G Pro](https://www.xda-developers.com/motorola-moto-g-fast-moto-g-pro/) 与 Moto G Stylus 具有相同的 DNA。

尽管这些设备的内部相似，摩托罗拉继续为这些设备发布了[单独的](https://www.xda-developers.com/motorola-moto-g-power-kernel-source-code-available/)[内核](https://www.xda-developers.com/kernel-sources-samsung-galaxy-tab-s7-moto-g-stylus-motorola-one-zoom-motorola-one-fusion-moto-e-2020-available/)源代码包。现在，OmniROM 的贡献者 [Vache Ounet](https://github.com/Vachounet) ，在我们的论坛上被称为 XDA 认可的开发者 [vache](https://forum.xda-developers.com/member.php?u=1829889) ，正试图通过他的 OmniROM 统一构建带来混乱中的和谐。它基于 Android 10，可以在前述大多数智能手机之间交叉兼容。

**XDA 论坛:[Moto G Power/G8 Power](https://forum.xda-developers.com/moto-g-power)| | |[Moto G8/G Fast](https://forum.xda-developers.com/moto-g8)| | |[Moto G Stylus/G Pro](https://forum.xda-developers.com/moto-g-stylus)**

他的所有努力都始于为 Moto G8 Power 开发一个非官方的 OmniROM。后来，vache 在为这些骁龙 665 Moto 手机[创建统一设备树](https://github.com/sofiar-dev/android_device_motorola_sofiar)方面做了出色的工作，目前的版本就是基于该树。除了威瑞森手机数据的一个小问题，开发者认为统一定制的 rom 是稳定的。SELinux 设置为 enforcing，预计所有设备变体都将通过 SafetyNet 认证。

统一 OmniROM 版本目前支持的手机列表如下:

OmniROM 预装了 Google apps。你不需要像 TWRP 那样定制恢复来安装它，因为 ROM 被设计成可以通过快速启动界面刷新。看看上面链接的论坛帖子，按照第一篇帖子中的说明在你的设备上安装并运行 ROM。