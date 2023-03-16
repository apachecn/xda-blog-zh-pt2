# Bootloader 解锁高通 SOC 的传统中兴手机

> 原文：<https://www.xda-developers.com/unlock-bootloader-zte-phones/>

# 几十部带有高通处理器的旧中兴手机现在可以解锁引导程序了

你现在可以通过利用不安全的 EDL 模式来解锁几款高通骁龙供电的传统中兴手机的引导程序。继续阅读，了解更多信息！

典型的高通骁龙芯片组驱动的 Android 设备的常规引导序列是由 **P** 主**B**oot**l**loader(PBL)启动的，尽管存在一种称为**E**emergency**D**own**l**oad Mode(EDL)的替代引导模式。后者严格用于 OEM 服务，可用于通过名为“Firehose”的协议使用适当的软件二进制文件[“解锁”设备](https://www.xda-developers.com/oneplus-8-unbrick-tool-msmdownloadtool-edl-available/)。有趣的是，EDL 经常被修补者用来获得低级别的分区访问，这可以被进一步利用来[在一些设备上实现引导加载程序解锁](https://www.xda-developers.com/bootloader-unlock-method-has-been-found-for-the-sprint-oneplus-7-pro-5g/)。基于这一原理以及 Aleph 安全团队之前所做的研究工作，XDA 资深成员 [alexenferman](https://forum.xda-developers.com/member.php?u=10365003) 现在发现了一种通用的方法来解锁一批中兴手机的 bootloader，而不会丢失任何数据。

中兴显然使用“devinfo”分区来存储关键的引导程序状态参数，包括锁定/解锁状态。由于 Firehose 协议提供了读取各个分区的内容，因此可以从锁定引导加载程序的设备中转储“devinfo”分区，更改存储解锁参数的偏移量，并将修改后的映像写回设备以解锁引导加载程序。[与小米](https://www.xda-developers.com/xiaomi-edl-unbrick-authorized-mi-accounts/)和其他一些原始设备制造商不同，中兴甚至没有在 EDL 模式之前设置防范此类“攻击”的保护措施，因此您可以通过一个简单的 ADB 命令轻松触发设备启动到紧急下载模式。唯一的问题是，这种方法无法在使用 Android 8.0 Oreo 或更新版本的中兴手机上运行，也无法在像 [Axon 9 Pro](https://www.xda-developers.com/zte-axon-9-pro-specs-renders-pricing-availability/) 、 [Axon 10 Pro](https://forum.xda-developers.com/axon-10-pro) 、 [Axon M](https://forum.xda-developers.com/axon-m) 等旗舰设备上运行。

 <picture>![zte_bootloader_unlock_devinfo_qfil](img/6dd114a63b9cf98ace759d526553b169.png)</picture> 

Dumping the 'devinfo' partition using QFIL

根据 XDA 公认的开发商 [deadman96385](https://forum.xda-developers.com/member.php?u=4222965) 的说法，该方法适用于以下设备:

### 采用 MSM8909(高通骁龙 210) SoC 的设备

*   中兴 Avid 4 (Z855)(代号:calbee)
*   中兴 Maven 2 (Z831)(代号:chapel)
*   中兴 Maven 3 (Z835)(代号:draco)
*   中兴至尊 Pro Plus (Z899VL)(代号:elden)
*   不知名的中兴通讯(代号:福布斯)
*   中兴 ZMAX One (Z719DL)(代号:gemi)
*   中兴时间 X (N9137)(代号:grayjoylite)
*   中兴 Grand X View 2 (K81)(代号:helen)
*   中兴序曲 3 (Z851)(代号:杰夫)
*   中兴 Fanfare 3 (Z852)(代号:kelly)
*   中兴 ZFive G LTE (Z557BL)(代号:lewis)
*   中兴 ZFive C (Z558VL)(代号:loft)
*   未知的中兴(代号:避难所)
*   中兴 N818S(代号:蓝宝石/蓝宝石 4G)
*   中兴 Blade Vantage (Z839)(代号:sweet)

### 采用 MSM8952(高通骁龙 617) SoC 的设备

*   安卓 5.1.1
    *   中兴 Grand X Max 2 (Z988)(代号:jerry)
    *   中兴帝国 Max (Z963U)(代码-名称:lily)
    *   中兴 Max Duo LTE (Z963VL)(代号:nancy)
    *   中兴 Axon Max (C2016)(代号:兰花)
    *   中兴 Max Duo LTE (Z962BL)(代号:tom)
*   安卓 6.0.1
    *   中兴 ZPAD (K90U)(代号:gevjon)
    *   中兴美国电话电报公司迷航 2 (K88)(代号:茉莉)
    *   中兴 Grand X Max 2 (Z988)(代号:jerry)
    *   中兴 Axon Max (C2016)(代号:兰花)
    *   中兴 ZMAX Pro (Z981)(代号:urd)
*   安卓 7.1.1
    *   中兴美国电话电报公司迷航 2 (K88)(代号:茉莉)
    *   [中兴 Axon 7 Mini](https://forum.xda-developers.com/axon-7-mini) (B2017G)(代号:郁金香)

### 采用 MSM 8920/MSM 8937/MSM 8940/MSM 8953(高通骁龙 427/430/435/625)SOC 的设备

*   中兴 Blade Force/中兴 Warp 8 (N9517)(代号:Warp 8)
*   中兴大 X4 (Z956/Z957)(代号:finacier)
*   中兴 Blade Spark (Z971)(代号:牡丹)
*   中兴 Blade X (Z965)(代号:脯氨酸)
*   中兴 Max XL/中兴 Bolton (N9560)(代号:Bolton)
*   中兴 Blade Z Max (Z982)(代号:crocus)
*   不知名的中兴(代号:火焰)
*   中兴 Blade X Max (Z983)(代号:stollen)
*   中兴 Blade Max View (Z610DL)(代号:紫罗兰)
*   中兴 Max Blue LTE (Z986DL)(代号:花店)
*   中兴通讯美国电话电报公司 prime time(K92)(代号:primerose)

此外，中兴 Avid 4、中兴 Tempo X、中兴 Imperial Max 和中兴 Grand X View 2 也应与此程序兼容。感兴趣的用户应该看看 [deadman96385](https://forum.xda-developers.com/member.php?u=4222965) 的[非官方中兴通讯消防水带回购](https://github.com/programmer-collection/zte)并在摆弄他们的设备之前挑选合适的程序员。一步一步的引导加载程序解锁过程可以在下面链接的线程中找到。

**[高通中兴设备上 Bootloader 解锁— XDA 讨论线程](https://forum.xda-developers.com/android/software/bootloader-unlocking-qualcomm-zte-t4100897)**