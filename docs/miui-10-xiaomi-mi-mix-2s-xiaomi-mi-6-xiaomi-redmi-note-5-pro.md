# 如何在小米米 Mix 2/2S、小米米 6/5、小米红米 Note 5 Pro 和小米米 Note 2 上安装 MIUI 10

> 原文：<https://www.xda-developers.com/miui-10-xiaomi-mi-mix-2s-xiaomi-mi-6-xiaomi-redmi-note-5-pro/>

小米 Mi 8、Mi 8 探索版和 Mi 8 SE 最近在中国的一次活动中发布。随着三款智能手机的发布， [MIUI 10 中国开发者 ROM](https://www.xda-developers.com/miui-10-announcement-ai-features/) 也发布了。小米在发布会上强调的新“人工智能”功能包括人工智能预加载和人工智能人像。MIUI 10 还为系统 UI 的几乎每个方面带来了[变化](https://www.xda-developers.com/miui-9-xiaomi-mi-mix-2s-redmi-note-5-pro-redesigned-ui/)，比如重新设计的锁屏、通知、最近的应用、快速设置、音量面板等等。新 UI 的部分内容[让人想起了 Android P 中的设计](https://www.xda-developers.com/everything-new-android-p-developer-preview/)，如果你想尝试这个新版本的 MIUI，你可以等待小米发布全球测试版 ROM，或者现在就下载中国测试版 ROM，只要你有小米 Mix 2、小米 Mix 2S、小米 Mi 5、小米 Mi 6、小米 Redmi Note 5 Pro 或小米 Note 2。不要担心，你可以将语言从普通话改为英语，你也可以安装谷歌应用程序！

为什么只有这些设备？嗯，MIUI 10 还没有公开发售。这些设备的 ROM 已经在网上泄露，这就是我们现在能够安装它们的原因，但如果你拥有一台准备接收 MIUI 10 更新的其他设备，你必须等待 ROM 泄露或小米发布版本。提醒一下，下面的设备现在正在进行 ROM 的封闭测试，本月晚些时候会有一个公开测试。

**2018 年 6 月 4 日更新**:增加了小米米 5 和小米米 Note 2 的下载链接。其他设备的下载链接已经更新为 MIUI 10 的最新版本。

### 符合 MIUI 10 中国开发者 ROM 的设备

7 月下旬，将为以下设备提供公开测试版:

### 7 月 MIUI 10 中国开发者 ROM 合格设备列表

截图鸣谢:@ [小蜜](https://t.me/xiaomiui)上电报

小米 5、小米 6、小米 Mix 2、小米 Mix 2S 和小米 Note 2 的版本基于 Android 8.0 Oreo，而小米红米 Note 5 Pro 的版本基于 Android 8.1 Oreo。一旦你刷新了这些版本，你就应该安装了最新的[5 月安全补丁](https://www.xda-developers.com/android-security-patches-for-may-are-now-available-with-ota-and-factory-images/)。我们不确定您是否会收到稳定版本的 OTA 更新，但应该很容易像安装这些版本一样下载未来的更新。最后要注意的是，小米红米 Note 5 Pro build 其实来自中国小米红米 Note 5(不要和在印度发布的被称为中国小米红米 5 Plus 的小米红米 Note 5 混淆)；根据我们论坛上[用户的说法，它应该还能正常工作。](https://forum.xda-developers.com/redmi-note-5-pro/how-to/miui-10-close-beta-released-8-5-31-t3798176)

## 如何在小米米 Mix 2、小米米 Mix 2S、小米米 6、小米红米 Note 5 Pro 上安装 MIUI 10

侧装 MIUI 10 需要一个解锁的引导程序，你可以[在这里](http://en.miui.com/unlock/)申请。解锁引导加载程序将擦除设备。尝试升级之前，请备份您的所有数据！

1.  在你的电脑上安装 [ADB 和 Fastboot](https://www.xda-developers.com/install-adb-windows-macos-linux/) 如果你还没有的话。
2.  将您的手机连接到 PC。
3.  为您的手机下载合适的 TWRP 图像:
    1.  [TWRP 为小米 Mix 2](https://forum.xda-developers.com/mi-mix-2/development/recovery-twrp-3-2-1-0-xiaomi-mi-mix-2-t3780525)
    2.  [TWRP 为小米 Mi Mix 2S](https://forum.xda-developers.com/xiaomi-mi-mix-2s/how-to/recovery-twrp-mix-2s-t3790922)
    3.  [TWRP 为小米 Mi 5](https://forum.xda-developers.com/mi-5/development/recovery-twrp-xiaomi-mi-5-t3412123)
    4.  [TWRP 为小米 Mi 6](https://forum.xda-developers.com/mi-6/development/recovery-twrp-xiaomi-mi-6-t3619822)
    5.  [TWRP 为小米红米 Note 5 Pro](https://forum.xda-developers.com/redmi-note-5-pro/development/recovery-twrp-3-2-1-0-whyred-t3766113)
    6.  [TWRP 为小米 Mi Note 2](https://forum.xda-developers.com/mi-note-2/development/recovery-twrp-3-2-0-0-touch-recovery-mi-t3713441)
4.  点击下载[谷歌应用套件。](https://forum.xda-developers.com/mi-mix-2/themes/gapps-miui-10-8-x-t3798402)
5.  下载适合您手机的 MIUI 10 版本:
    1.  [小米 Mix 2 的 MIUI 10](https://bigota.d.miui.com/8.6.4/miui_MIMIX2_8.6.4_9ad7c1e29b_8.0.zip)
    2.  [小米 Mix 2S 的 MIUI 10](https://bigota.d.miui.com/8.6.4/miui_MIMIX2S_8.6.4_47d2ee80ac_8.0.zip)
    3.  [小米 5 的 MIUI 10](https://bigota.d.miui.com/8.6.4/miui_MI5_8.6.4_1420c8419d_8.0.zip)
    4.  [小米 6 的 MIUI 10](https://bigota.d.miui.com/8.6.4/miui_MI6_8.6.4_e972c05f94_8.0.zip)
    5.  [小米红米 Note 5 Pro 的 MIUI 10](http://bigota.d.miui.com/8.5.31/miui_HMNote5_8.5.31_1ae494c33e_8.1.zip)
    6.  [小米 Note 2 的 MIUI 10](https://bigota.d.miui.com/8.6.4/miui_MINote2_8.6.4_61ed9c46c4_8.0.zip)
6.  将 MIUI 10 ROM 和 GApps 包从 PC 传输到手机。
7.  关闭手机电源，同时按住电源键和音量键，重新启动引导程序。
8.  使用以下命令在您的设备上启动 TWRP:`fastboot boot /path/to/twrp.img`(用实际的文件名和存储位置替换/path/to/twrp.img。)
9.  一旦你启动到 TWRP，点击“擦除”，然后“滑动到工厂重置”进行工厂重置。如果你已经在 MIUI 9 中国版或开发者版上，这可能没有必要，但如果你在 MIUI 9 全球版上，这很可能是必要的。
10.  进入“安装”，找到你存放 MIUI 10 ROM 的地方。选择它并闪烁。
11.  点击“返回”,然后闪现谷歌应用套件。
12.  一旦刷新完成，点击“重启系统”,你应该会启动到 MIUI 10！
13.  享受 miui 10 对你的小米混音 2、小米 Mi Mix 2S、小米 Mi 5、小米 6、小米 Redmi 评分 5 Pro、小米评分 2！

想要分享您对这些 rom 的想法并关注您设备的所有最新消息吗？查看以下每种设备的 XDA 官方论坛！

[**小米 Mi Mix 2 论坛**](https://forum.xda-developers.com/mi-mix-2)

[**小米 Mi Mix 2S 论坛**](https://forum.xda-developers.com/xiaomi-mi-mix-2s)

[**小米米 6 论坛**](https://forum.xda-developers.com/mi-5)

[**小米米 6 论坛**](https://forum.xda-developers.com/mi-6)

[**小米红米 Note 5 Pro 论坛**](https://forum.xda-developers.com/redmi-note-5-pro)

[**小米 Mi Note 2 论坛**](https://forum.xda-developers.com/mi-note-2)