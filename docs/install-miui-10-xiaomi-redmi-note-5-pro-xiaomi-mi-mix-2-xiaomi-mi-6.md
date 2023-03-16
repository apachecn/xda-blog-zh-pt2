# 小米红米 Note 5 Pro、小米 Mix 2/2S 和小米 Mi 6 的 MIUI 10 全球测试版 ROM 在这里

> 原文：<https://www.xda-developers.com/install-miui-10-xiaomi-redmi-note-5-pro-xiaomi-mi-mix-2-xiaomi-mi-6/>

# 小米红米 Note 5 Pro、小米 Mix 2/2S 和小米 Mi 6 的 MIUI 10 全球测试版 ROM 在这里

MIUI 10 全球测试版 ROM 在这里，我们有小米 Redmi Note 5 Pro，小米 Mi Mix 2 和小米 Mi 6 的 ROM 链接和安装说明。

虽然大多数小米设备目前都在使用 MIUI 9 ROMs，但该公司最近宣布了 MIUI 10 的全球测试版。据说这次更新带来了大量的速度提升，这在整个操作系统中都可以看到，同时也带来了新的设计。有一个新的最近页面，[增加了散景效果的人工智能肖像](https://www.xda-developers.com/xiaomi-miui-10-single-camera-portrait-mode/)，等等。在宣布的时候，我们得到了一个列表，其中的设备计划接收更新，但我们没有听到任何关于具体的发布日期。今天，小米[宣布](http://en.miui.com/thread-2883296-1-1.html)其 6 款热门智能手机的 MIUI 10 全球测试版 ROM，包括最近宣布的[小米红米 S2/Y2](https://www.xda-developers.com/xiaomi-redmi-y2-launched-miui-10-global-rollout/) 。我们有小米红米 Note 5 Pro、小米 Mix 2、小米 Mix 2S 和小米 Mix 6 的下载链接和安装说明。我们还没有红米 S2/Y2 的链接，但我们会及时更新这篇文章。

## 如何在小米红米 Note 5 Pro、小米 Mix 2/2S、小米米 6 上安装 MIUI 10 全球测试版

1.  在你的电脑上安装 [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) 和 Fastboot，如果你还没有的话。
2.  将您的手机连接到 PC。
3.  为您的手机下载正确的 [TWRP](https://www.xda-developers.com/how-to-install-twrp/) 图像:
    1.  [TWRP 为小米 Mix 2](https://forum.xda-developers.com/mi-mix-2/development/recovery-twrp-3-2-1-0-xiaomi-mi-mix-2-t3780525)
    2.  [TWRP 为小米 Mi Mix 2S](https://forum.xda-developers.com/xiaomi-mi-mix-2s/how-to/recovery-twrp-mix-2s-t3790922)
    3.  [TWRP 为小米 Mi 6](https://forum.xda-developers.com/mi-6/development/recovery-twrp-xiaomi-mi-6-t3619822)
    4.  [TWRP 为小米红米 Note 5 Pro](https://forum.xda-developers.com/redmi-note-5-pro/development/recovery-twrp-3-2-1-0-whyred-t3766113)
4.  下载适合您手机的 MIUI 10 版本:
    1.  [小米 Mix 2 的 MIUI 10](http://bigota.d.miui.com/8.6.14/miui_MIMIX2Global_8.6.14_3a1cbeb56e_8.0.zip)
    2.  [小米 Mix 2S 的 MIUI 10](http://bigota.d.miui.com/8.6.14/miui_MIMIX2SGlobal_8.6.14_9cc38e37db_8.0.zip)
    3.  [小米 6 的 MIUI 10](http://bigota.d.miui.com/8.6.14/miui_MI6Global_8.6.14_6777ad214d_8.0.zip)
    4.  [小米红米 Note 5 Pro 的 MIUI 10(印度- Whyred)](http://bigota.d.miui.com/8.6.14/miui_HMNote5HMNote5ProGlobal_8.6.14_7141e580b7_8.1.zip)
5.  将 MIUI 10 ROM 从 PC 传输到手机。
6.  关闭手机电源，同时按住电源键和音量键，重新启动引导程序。
7.  使用以下命令在您的设备上启动 TWRP:`fastboot boot /path/to/twrp.img`(用实际的文件名和存储位置替换/path/to/twrp.img。)
8.  一旦你启动到 TWRP，点击“擦除”，然后“滑动到工厂重置”进行工厂重置。这可能不是必要的，但在更新主要操作系统升级的测试版时，总是建议这样做。
9.  转到“安装”,找到你存放光盘的地方。选择它并闪烁。
10.  一旦刷新完成，点击“重启系统”,你应该会启动到 MIUI 10！
11.  在您的小米 Redmi Note 5 Pro、小米 Mix 2/2S 和小米 Mi 6 上享受 MIUI 10 全球测试版 ROM

一如既往，我们建议您加入我们在各自的设备论坛，讨论和了解更多关于这些手机和新的更新。

[**小米 Mi Mix 2 论坛**](https://forum.xda-developers.com/mi-mix-2)

[**小米 Mi Mix 2S 论坛**](https://forum.xda-developers.com/xiaomi-mi-mix-2s)

[**小米米 6 论坛**](https://forum.xda-developers.com/mi-6)

[**小米红米 Note 5 Pro 论坛**](https://forum.xda-developers.com/redmi-note-5-pro)