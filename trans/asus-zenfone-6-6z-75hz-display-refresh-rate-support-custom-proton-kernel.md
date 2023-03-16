# 华硕 ZenFone 6 通过自定义内核获得 75Hz 显示刷新率支持

> 原文：<https://www.xda-developers.com/asus-zenfone-6-6z-75hz-display-refresh-rate-support-custom-proton-kernel/>

华硕 Zen fone 6(T1)或在印度被称为 T2 的华硕 6z(T3)是今年令人惊讶的发布之一，对于那些不喜欢更经常被推荐的主流选项的人来说，它是 T4 非常好的智能手机替代品。华硕为这款手机带来了几项关键更新，如带来了【2019 年 8 月的安全补丁、更多智能按键选项、[谷歌 Duo 拨号器集成](https://www.xda-developers.com/asus-zenfone-6-update-google-duo-dialer-integration-aptx-notification/)，甚至[相机旋转稳定性改进](https://www.xda-developers.com/asus-zenfone-6-update-improves-camera-quality/)。华硕一直非常支持这款设备，在其发布前后发布了[引导加载器解锁工具和内核源代码](https://www.xda-developers.com/asus-zenfone-6-bootloader-unlock-tool-kernel-source-code/)。由于这一及时的发布，开发人员已经能够致力于定制内核和其他修改，如 [GCam](https://www.xda-developers.com/arnova-google-camera-port-asus-zenfone-6-oneplus-7-7-pro/) 和 [LineageOS 16](https://www.xda-developers.com/asus-zenfone-6-razer-phone-samsung-galaxy-a3-a5-s5-neo-lineageos-16/) 。现在，XDA 资深会员 [kdrag0n](https://forum.xda-developers.com/member.php?u=7291478) 的[质子内核](https://forum.xda-developers.com/zenfone-6-2019/development/kernel-zenfone-6-proton-kernel-v1-0-t3963948)为华硕 ZenFone 6 带来了将显示器刷新频率设置为 75Hz 的能力，高于普通的 60Hz 刷新率。

**[【ASUS zenfone 6/ASUS 6z xd a 论坛】](https://forum.xda-developers.com/zenfone-6-2019)**

质子内核是华硕 ZenFone 6 或华硕 6z 的定制内核，旨在用于该设备的股票华硕 Android Pie ROM。因为这是一个定制的内核，你需要一个解锁的引导程序和一个定制的恢复程序，比如 TWRP，来把它安装到你的设备上。内核有一个长长的功能列表，但一些亮点包括 75Hz 的屏幕刷新率，sultanxda 的[简单的低内存黑仔](https://github.com/kerneltoast/simple_lmk)，magisk 保存，最新的高通 CAF 源与最新的主线 LTS 更新合并，以及 exFAT 支持。

**[质子内核为华硕 ZenFone 6 - XDA 线程](https://forum.xda-developers.com/zenfone-6-2019/development/kernel-zenfone-6-proton-kernel-v1-0-t3963948)**

对于 75Hz 的刷新率，用户需要关闭屏幕，然后在每次引导后打开屏幕，以便它可靠地工作。更高的刷新率确实有相关的风险，所以如果您只是想尝试一下内核，而对更高的刷新率不感兴趣，您可以简单地将“60hz”或“60fps”附加到内核 zip 名称，flasher 输出将相应地进行调整以确认更改。

* * *

**你在华硕 ZenFone 6 上试用过质子内核吗？就流动性和电池寿命而言，你对 75Hz 的体验如何？请在下面的评论中告诉我们！**