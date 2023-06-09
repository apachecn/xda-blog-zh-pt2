# 谷歌贴出 Pixel 4a 的工厂图片、Android 11 测试版和内核源代码

> 原文：<https://www.xda-developers.com/google-pixel-4a-android-11-beta-factory-image-kernel-source/>

本月早些时候，谷歌推出了该公司第二款中端 Pixel 智能手机 [Pixel 4a(代号“sunfish”)](https://www.xda-developers.com/google-pixel-4a-specs-features-pricing-availability/)。售价 349 美元，你可以获得 5.81 英寸有机发光二极管显示屏，高通骁龙 730 克，6GB 的 LPDDR4X 内存，128GB 的 UFS 2.1 存储，3140 毫安时电池，3.5 毫米音频插孔，以及谷歌出色的摄像头和软件支持。上周晚些时候，这款手机正式上市销售，今天，谷歌已经上传了对运行定制软件感兴趣的开发者所需的所有工具、文件和文档。

**[谷歌像素 4a 论坛](https://forum.xda-developers.com/pixel-4a)**

当谷歌发布 Android 11 Beta 3 时，他们承诺最终将为 Pixel 4a 提供测试版。如果你有设备，你现在可以选择加入 Android 测试程序，允许你接收最新 Android 测试版本的 OTA 更新。如果你不想等待测试版推出，你可以选择刷新 Android 11 Beta 3 工厂映像或下载完整的 OTA 文件。内部版本号为 rpb3.200720.005，与目前符合 Android 11 测试版资格的其他 Pixel 手机的内部版本相匹配。

**为谷歌 Pixel 4a** 下载 Android 11 Beta 3:[选择进入 Android Beta 计划](https://www.google.com/android/beta) ||| [工厂镜像](https://dl.google.com/developers/android/rvc/images/factory/sunfish-rpb3.200720.005-factory-0c21828c.zip) ||| [OTA](https://dl.google.com/developers/android/rvc/images/ota/sunfish-ota-rpb3.200720.005-56e4a437.zip)

如果您想返回到 Pixel 4a 上的库存软件，您可以从下面的链接中提取并刷新最新的出厂映像固件。最新版本的内部版本号为 QD4A.200805.003，对应于 2020 年 8 月的 Android 安全补丁级别。有两套工厂图像可用:一套用于日本/威瑞森机组，另一套用于解锁机组。

最后，Google 已经上传了设备树和内核源代码。对于任何对构建自定义内核来引导 TWRP 和/或基于 AOSP 的自定义 ROM 感兴趣的开发人员来说，这些都是很有帮助的起点。

**[工厂画面](https://developers.google.com/android/images#sunfish)**| |**|[设备树](https://android.googlesource.com/device/google/sunfish/)**

**内核源代码** : [安卓 10.0.0 版本 0.87](https://android.googlesource.com/kernel/msm/+/refs/tags/android-r-beta-3_r0.6) ||| [安卓 10 Beta 3 版本 0.6](https://android.googlesource.com/kernel/msm/+/refs/tags/android-r-beta-3_r0.6) ||| [预建二进制](https://android.googlesource.com/device/google/sunfish-kernel)