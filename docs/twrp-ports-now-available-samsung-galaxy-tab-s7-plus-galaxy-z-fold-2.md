# 三星 Galaxy Tab S7 Plus 和 Galaxy Z Fold 2 现在可以使用 TWRP 端口

> 原文：<https://www.xda-developers.com/twrp-ports-now-available-samsung-galaxy-tab-s7-plus-galaxy-z-fold-2/>

# 三星 Galaxy Tab S7 Plus 和 Galaxy Z Fold 2 现在可以使用 TWRP 端口

由 XDA‌资深会员 ianmacd 提供，TWRP 的非官方版本现在可用于三星 Galaxy Tab S7 Plus 和 Galaxy Z Fold 2。

对于那些已经设法挑选了三星 [Galaxy Tab S7 Plus](https://www.xda-developers.com/samsung-galaxy-tab-s7/) 或 [Galaxy Z Fold 2](https://www.xda-developers.com/samsung-galaxy-z-fold-2/) 的人来说，你会很高兴地知道，非官方的 TWRP 版本现在已经为你的设备推出了。根据最新的 [TWRP 3.4.0](https://www.xda-developers.com/twrp-3-4-0-enables-ozip-decryption-realme-oppo-devices-support-legacy-devices-upgraded-android-10/) 代码库编译，该版本由 XDA‌高级成员 [ianmacd](https://forum.xda-developers.com/member.php?u=7187684) 提供。当前的恢复映像集已经过测试，可以在 Galaxy Tab S7 Plus 5G 的 **SM-T976B** 变体和 Galaxy Z Fold 2 的 **SM-F916B** 变体上成功引导。

**[三星 Galaxy Tab S7 / Tab S7+论坛](https://forum.xda-developers.com/galaxy-tab-s7) || [三星 Galaxy Z Fold 2 论坛](https://forum.xda-developers.com/samsung-galaxy-z-fold-2)**

正如所料，你需要一个带有可解锁引导程序的模型来刷新 TWRP。美国运营商的变种通常不适合改装，因为他们不能解锁。即使你有一个解锁的模型，并有兴趣尝试 TWRP，请记住，安装第三方二进制文件(如 TWRP) **将永久跳闸诺克斯**。你没有办法扭转这种局面，这意味着**你将永远无法访问 Samsung Pay** 和**的安全功能，如依赖 Knox 安全的安全文件夹**。如果你准备好处理这样的后果，通过点击下面的链接获取所需的文件，前往你各自设备的 TWRP 线程。值得一提的是，除了恢复映像之外，您还必须刷新一个虚拟 vbmeta.img，才能在您的设备上正确引导 TWRP。

**TWRP 下载讨论线程:[三星 Galaxy Tab S7+](https://forum.xda-developers.com/galaxy-tab-s7/development/twrp-samsung-galaxy-tab-s7-5g-t976b-t4163853) || [三星 Galaxy Z Fold 2](https://forum.xda-developers.com/samsung-galaxy-z-fold-2/development/twrp-samung-galaxy-z-fold2-5g-f916b-t4163833)**

据开发商称，定制恢复不支持三星专有的基于文件的加密(FBE)。如果您[禁用自动加密例程](https://forum.xda-developers.com/galaxy-s10/samsung-galaxy-s10--s10--s10-5g-cross-device-development-exynos/g97xf-multi-disabler-encryption-t3919714)并随后格式化数据分区，您应该能够使用 TWRP 执行数据备份/恢复。此外，MTP 在这些端口是坏的，但你可以在 TWRP 安装设置中禁用 MTP，并使用 ADB 将文件从电脑推送到设备(或反之亦然)。

**[三星 Galaxy Z Fold 2 回顾:可能是年度手机](https://www.xda-developers.com/samsung-galaxy-z-fold-2-review/)**