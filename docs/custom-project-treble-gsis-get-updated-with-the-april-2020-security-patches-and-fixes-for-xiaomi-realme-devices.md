# 自定义 AOSP 项目 Treble GSIs 获得 4 月安全补丁更新

> 原文：<https://www.xda-developers.com/custom-project-treble-gsis-get-updated-with-the-april-2020-security-patches-and-fixes-for-xiaomi-realme-devices/>

# 定制项目 Treble GSIs 将于 2020 年 4 月更新小米/Realme 设备的安全补丁和修复程序

XDA 认可的开发商 phhusson 在 Project Treble-enabled 设备上使用的自定义 AOSP GSI 已更新为 2020 年 4 月的安全补丁。请继续阅读！

由于将 Android 操作系统框架与供应商 HALs 和 Linux 内核分离，Project Treble 能够在任何支持的设备上引导 AOSP 通用系统映像(GSI)。虽然谷歌确实在其网站上提供了以开发者为中心的 Android 10 GSI T1 以及方便的 T2 flash 工具 T3，但社区开发者长期以来一直在分发他们自己的基于 T4 流行定制 rom T5 或普通 AOSP 的定制 GSI。这些发行版通常包含特定于设备的修复程序，因此最终用户可以在不破坏 Wi-Fi 或 RIL 等基本功能的情况下，轻松地将手机上大量定制的 Android 皮肤替换为几乎通用的体验。这一领域的先驱，XDA 公认的开发者 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) ，现在已经用最新的[2020 年 4 月安全补丁](https://www.xda-developers.com/google-april-2020-android-security-bulletin-patches-pixel-4-3-3a-2-xl/)以及大量其他修复更新了他的定制项目 Treble GSI。

**[访问 XDA 项目三宝论坛](https://forum.xda-developers.com/project-treble)**

phhusson 基于 Android 10 自编自定义 GSI“嘎嘎 Phh-Treble”的最新版本是 *v215* ，在几款小米手机上都自带双击唤醒手势支持。自 *v214* 以来，开发者还在 Realme 手机上添加了兼容性补丁，以检测指纹扫描仪，包括欠显示传感器。用户还可以在最后几个版本中找到一个远程调试选项(默认情况下禁用)，使开发人员能够通过 ADB 连接到他们的设备进行故障排除。

**[呱呱 Phh——高音——XDA 螺纹](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/aosp-10-0-quack-phh-treble-t3992559)**

嘎嘎 Phh-Treble *v215* 的完整变更日志如下:

*   暂时删除了 32 位目标的 gapps 变体
*   从 pe gapps 迁移到 opengapps
*   可重新启用的 FLOSS 变体(由于 Firefox/Fennec，只能使用 64 位)
*   4 月安全补丁级别
*   修复三星 Galaxy Tab A 10.1 上的 DT2W
*   修复进入“杂项”设置时的崩溃
*   为各种小米设备修复 dt2w
*   修复“三星”设置中的崩溃
*   包括 vr hwcomposer。应该修复华为设备在启动时声明不兼容供应商的错误
*   修复[小米 Mix 3 5G](https://forum.xda-developers.com/mi-mix-3/xiaomi-mi-mix-3-5g-andromeda) 、[红米 Note 8 Pro](https://forum.xda-developers.com/redmi-note-8-pro) 上的音频和指纹行为
*   默认情况下启用导航栏
*   禁用三星预装应用程序
*   修复内部 SU 对根备份/恢复应用程序的支持
*   固定亮度在[真实 C1](https://www.xda-developers.com/realme-2-pro-realme-c1-india-launch-specifications/)
*   禁用关于不兼容 SDK 的祝酒词
*   为所有设备启用多用户
*   修正某些华为设备上的屏幕亮度控制
*   添加 persist . sys . phh . no _ vendor _ overlay 属性以禁用所有供应商覆盖

如果你想尝试 phhusson 的 GSI，你应该使用下面链接的 Treble Info 应用程序来确定你的设备型号。之后从项目的 GitHub 发布页面抓取相应的 build(最新版本可以在[这里](https://github.com/phhusson/treble_experimentations/releases/latest)找到)手动或者使用[XDA 成员](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/treble-gsi-flashing-tool-b-t4040435) [stevegsames](https://forum.xda-developers.com/member.php?u=8390992) 开发的工具刷新[。](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/)

[app box Google play " tk . hack 5 . treble check "]