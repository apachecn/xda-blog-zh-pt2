# 定制 AOSP 项目 Treble GSI 更新了 2020 年 6 月的安全补丁，网飞高清支持小米 Mi 9 和 Redmi Note 9S 等

> 原文：<https://www.xda-developers.com/custom-aosp-project-treble-gsi-gets-updated-with-june-2020-security-patches-netflix-hd-support-for-the-xiaomi-mi-9-and-redmi-note-9s-and-more/>

# 定制 AOSP 项目 Treble GSI 更新了 2020 年 6 月的安全补丁，网飞高清支持小米 Mi 9 和 Redmi Note 9S 等

XDA 认可开发商 phhusson 为 Project Treble 兼容设备定制的 AOSP GSI 已更新为 2020 年 6 月的安全补丁。

多亏了 Project Treble，Android 用户可以轻松地在任何支持的设备上启动 AOSP 通用系统映像(GSI)。无论是小米的 MIUI 还是三星的 One UI，那些大量定制的 OEM 皮肤甚至可以被社区开发的 GSI 取代，以支持接近库存的 Android 体验。虽然你应该能够在任何支持 Project Treble 的设备上启动谷歌的 AOSP GSI，但你会错过许多有助于正常日常体验的功能。这就是 XDA 认可的开发商 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的定制 GSI 的用武之地。他加入了许多谷歌 GSI 中没有的错误修复和功能添加，以使它们在日常生活中实际可用。开发人员现在已经用最新的【2020 年 6 月安全补丁和许多新的设备特定补丁刷新了他的定制项目 Treble GSI 项目。

**[呱呱 Phh——高音——XDA 螺纹](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/aosp-10-0-quack-phh-treble-t3992559)**

自从[我们的上一篇文章](https://www.xda-developers.com/custom-project-treble-gsi-may-2020-security-patches-dc-dimming-oppo-devices/)以来，phhusson 已经在今天的发布( *v218* )之前发布了一个中间测试版本( *v217* )。各种三星设备上的光学欠显示指纹扫描仪，如 [Galaxy A51](https://www.xda-developers.com/samsung-galaxy-a51-is-now-available-from-att-and-xfinity-mobile-in-the-u-s/) 从现在起应该可以正常工作了。此外，还有一个新的选项，可以正确暴露三星智能手机上的辅助相机传感器。用户现在可以删除 Wi-Fi 专用设备上的电话服务。小米 Mi 9 和 [Redmi Note 9S/Note 9 Pro](https://www.xda-developers.com/xiaomi-redmi-note-9-pro-global-note-9s/) 的用户应该很高兴知道更新的 GSIs 不再中断网飞高清流媒体。

累积的变更日志可以在下面找到:

*   六月安全补丁
*   高音设置的安全选项现在可以在 Magisk 上使用
*   在高音设置中添加“禁用 A2DP 卸载”解决方法
*   为 Vsmart 设备添加双击唤醒功能
*   在小米[米 9](https://forum.xda-developers.com/Mi-9) 和[红米 Note 9S](https://forum.xda-developers.com/redmi-note-9-pro) 上启用网飞高清(可能需要 Securize)
*   修复 gapps 变体中缺失的导航手势
*   在 gapps 变体中包括对讲
*   修正一些 Q 厂商的 exfat
*   在红米设备上启用小米选项(红米 Note 9S)
*   修复 Redmi Note 9S 上的蓝牙、指纹输入和音频中断
*   在 32 位目标上重新启用 Gapps
*   在所有目标上启用 Android Go gapps
*   将光学显示下指纹固定在三星设备上( [Galaxy A51](https://forum.xda-developers.com/galaxy-a51) ， [Galaxy A50](https://forum.xda-developers.com/galaxy-a50) ，...)
*   添加一个选项来曝光三星设备上的所有相机
*   改进运行 [MIUI 12](https://www.xda-developers.com/download-miui-12-closed-beta-xiaomi-redmi-devices/) 厂商的小米设备的显示不足指纹
*   添加一个选项来删除仅 WiFi 设备的电话服务
*   在高音设置中添加了一个解决方法，用于解决某些设备在正常运行一段时间后视频录制中断的问题

**[下载呱呱 Phh-高音 v218](https://github.com/phhusson/treble_experimentations/releases/tag/v218)**

如果您需要帮助为您的设备选择正确的软件包，请安装下面链接的 Treble Info 应用程序。建议用户在安装定制的 AOSP GSI 之前进行完整的设备外备份，因为刷新过程将要求您在工厂重置您的设备。

[app box Google play " tk . hack 5 . treble check "]