# 将 Sprint 一加 7 Pro 5G 更名为欧盟固件，以试用 OxygenOS 测试版

> 原文：<https://www.xda-developers.com/rebrand-sprint-oneplus-7-pro-5g-eu-firmware-oxygenos-open-betas/>

一加凭借 T-Mobile 品牌的一加 6T 在美国市场正式亮相。从那以后，原始设备制造商[继续](https://www.xda-developers.com/t-mobile-oneplus-7-pro-us/)与 T-Mobile 的[合作](https://www.xda-developers.com/oneplus-7t-pro-mclaren-edition-5g-t-mobile/)，并与 Sprint 合作开发一加 7 Pro 5G。虽然一加手机在美国的可用性增加是一个优点，但缺点是对软件更新频率的负面影响。更糟糕的是，美国 5G 一加手机没有资格参加 OxygenOS Open Beta 计划。XDA 资深成员[谁是你](https://forum.xda-developers.com/member.php?u=2727149)现在一石二鸟:他想出了一个在不解锁引导程序的情况下将 Sprint 一加 7 Pro 5G 转换为国际/欧洲固件的方法，他还移植了 4G 版本的开放测试版固件。

**[一加 7 场职业 XDA 论坛](https://forum.xda-developers.com/oneplus-7-pro)**

虽然 Sprint 还没有为一加 7 Pro 5G 提供官方的引导加载器解锁工具，但手机用户可以选择[一种非官方的方法](https://www.xda-developers.com/bootloader-unlock-method-has-been-found-for-the-sprint-oneplus-7-pro-5g/)，这种方法早些时候由某个希望匿名的人创建，但由 whoay 分享给社区。之后可以刷新修改过的欧盟固件，但这样做[会破坏安全网认证](https://www.xda-developers.com/magisk-no-longer-hide-bootloader-unlock-status/)，因此来自网飞和 Prime Video 等流媒体服务的受 DRM 保护的高清视频无法访问。

另一方面，最新版本的“黑客”不会攻破安全网。Sprint 用户可能会面临一些与 APN 相关的问题，并且关于电话的部分被破坏了，但是除此之外，转换过程是非常无缝的。这些步骤如下所述。

1.  拔下并完全关闭手机电源。
2.  [下载](https://www.mediafire.com/file/dqyna0n5fx64q8s/guacamoles_to_guacamoleg_21_E.09_190925_repack.rar/file)，打开修改后的 MSM 下载工具。
3.  取消选中 SHA256 检查。
4.  将 USB 电缆连接到 PC。
5.  同时调低和调高音量。
6.  握住这些钥匙，插入 USB。
7.  按住这些键，单击工具中的“枚举”。
8.  点击“开始”。
9.  等待大约 5-10 分钟，通过 Wi-Fi 设置，接受 Android 10 OTA，就大功告成了。

**[将 Sprint 一加 7 Pro 5G 转换为欧洲固件— XDA 线程](https://forum.xda-developers.com/oneplus-7-pro/how-to/discussion-oneplus-7-pro-5g-rom-gsi-t4042583)**

谈到开放测试版端口，它是基于普通一加 7 Pro 的最新[开放测试版 11 构建](https://www.xda-developers.com/oneplus-7-pro-oxygen-os-open-beta-11-oneplus-7t-beta-2/)。该软件包可以安装在欧洲一加 7 Pro 5G 设备(型号为 *GM1920* )和 Sprint 设备(型号为 *GM1925* )上。*关于手机*部分将不会被正确填充，并且[威瑞森的可视 MVNO](https://www.xda-developers.com/oneplus-7-pro-oxygenos-9-5-13-verizon-visible/) 不受该移植固件的支持，但用户最终可以体验到前沿功能，如[即时翻译](https://www.xda-developers.com/oneplus-instant-translation-oxygenos-oneplus-7/)服务。

**[一加 7 Pro 5G 氧气 OS 公测— XDA 线程](https://forum.xda-developers.com/oneplus-7-pro/how-to/port-oxygen-os-beta-oneplus-7-pro-5g-t4075597/)**

要恢复出厂固件，请参考设备特定的 unbrick 线程: [EU](https://forum.xda-developers.com/oneplus-7-pro/how-to/op7pro-5g-eu-unbrick-tool-to-restore-t4078827) ， [Sprint](https://forum.xda-developers.com/oneplus-7-pro/how-to/sprint-msmdownloadtool-unbrick-t3989841) 。

* * *

*感谢 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 的提示！*