# KDZZ 从 KDZ 文件中为 LG 手机构建了可刷新的 zip 文件

> 原文：<https://www.xda-developers.com/kdzz-build-flashable-zips-kdz-files-lg/>

# KDZZ 从 KDZ 文件中为 LG 手机构建了可刷新的 zip 文件

KDZZ Zip 包创建工具让你从 KDZ 固件文件为 LG 设备创建可刷新的 Zip 包。继续阅读，了解更多信息！

如果你熟悉 LG 设备上的 flash，你就知道 KDZ 文件是什么了。kdz 是 LG 在其网站上发布官方固件版本的首选格式，这意味着每一个库存的 LG ROM 都将正式采用. KDZ 格式。这使得这些固件文件通过 TWRP 闪存有点痛苦。

[KDZZ](https://forum.xda-developers.com/tmobile-g6/development/tool-kdzz-create-flashable-zip-kdz-files-t3902423) by XDA 资深会员 [weakNPCdotCom](https://forum.xda-developers.com/member.php?u=9374982) 是一款从 KDZ 文件自动构建可 flash 化的 zip 文件的工具。该工具处于 alpha 和积极开发阶段，目前支持两种设备:T-Mobile 上的 LG G6(H872)和 T-Mobile 上的 LG v 30(H932)；尽管您可以通过上面提到的说明添加对不支持设备的支持。KDZZ 也是[开源](https://github.com/adanvdo/KDZZ)。

安装工具本身就像解压一个 zip 文件一样简单。该工具的使用需要 Windows LG Firmware Extract Tool 从 DZ 文件中提取系统 bin，因此您还需要手头的 KDZ 文件。该工具可以为 bootloader、modem、fullstock 或 LAF (LG Advanced Flash)创建 zip 包。相应地，KDZZ 自动重命名所有 bin 文件，排列它们，构建更新程序脚本，并将其压缩。跟随[论坛线索](https://forum.xda-developers.com/tmobile-g6/development/tool-kdzz-create-flashable-zip-kdz-files-t3902423)试试吧。

[**KDZZ - Zip 包创建工具**](https://forum.xda-developers.com/tmobile-g6/development/tool-kdzz-create-flashable-zip-kdz-files-t3902423)