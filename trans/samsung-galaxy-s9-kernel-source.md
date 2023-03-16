# 三星 Galaxy S9 和 Galaxy S9+内核源代码现已推出

> 原文：<https://www.xda-developers.com/samsung-galaxy-s9-kernel-source/>

# 三星 Galaxy S9 和 Galaxy S9+内核源代码现已推出

三星 Galaxy S9 和 Galaxy S9+内核源代码现在可用于 Exynos 和骁龙型号。这为 TWRP 和 Exynos 模型的定制 rom 的创建铺平了道路，尽管骁龙仍然需要一个可解锁的引导加载程序。

在几乎所有关于这两款设备的信息都被泄露后，三星 Galaxy S9 和 Galaxy S9+于上个月在 T2 正式发布。这两款设备看起来并没有比它们的前辈升级多少，相反，它们[为 Galaxy S8 系列的较弱方面添加了波兰](https://www.xda-developers.com/samsung-galaxy-s9-s9-plus-hands-on/)。像往常一样，许多人来到 XDA 论坛，以便通过改装他们的设备将他们的智能手机体验掌握在自己手中。既然内核源代码对 [Galaxy S9 和 Galaxy S9+](https://www.xda-developers.com/tag/samsung-galaxy-s9/) 都可用，用户和开发者就可以开始这个过程了——至少对 Exynos 模型是这样。

有了内核源代码，开发人员可以开始将流行的 [TWRP](https://www.xda-developers.com/tag/twrp/) 定制恢复移植到设备上。这将使备份分区更加容易，因为用户将不再需要依赖 ODIN 闪存映像。此外，这将缓解闪烁[项目高音](http://xda-developers.com/tag/project-treble)通用系统映像(GSI ),因为三星在其设备上不提供快速启动协议。这意味着我们很快就能测试 AOSP ROM 是否能工作，比如 XDA 资深成员 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的 [Phh-Treble ROM](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/experimental-phh-treble-t3709659) 。如果有任何问题，内核源代码可用性将有助于调试它们。

然而，内核源代码只有在设备的引导装载程序不可锁定的情况下才有用，遗憾的是，骁龙型号并不是这样的。骁龙 Galaxy S9 设备的所有者将不得不希望他们的设备存在像三星 Galaxy Note8 的 [SamFAIL](https://www.xda-developers.com/samsung-galaxy-note-8-root-samfail/) 这样的根漏洞，因为否则他们将无法修改系统分区。谢天谢地，有了 Project Treble compatibility，如果确实发现了这样的漏洞，那么理论上骁龙设备也将能够品尝到 AOSP 的美味，因为 Treble GSI 只需要修改系统分区。

[**下载三星 Galaxy S9 和 Galaxy S9+内核源代码**](http://opensource.samsung.com/reception/receptionSub.do?method=sub&sub=F&searchValue=G96)