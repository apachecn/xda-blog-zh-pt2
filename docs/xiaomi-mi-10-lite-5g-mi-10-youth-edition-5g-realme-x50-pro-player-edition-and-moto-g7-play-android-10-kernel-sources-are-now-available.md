# 小米 Mi 10 Lite 5G，Realme X50 Pro Player 版，Moto G7 Play Android 10 内核源码现已上市

> 原文：<https://www.xda-developers.com/xiaomi-mi-10-lite-5g-mi-10-youth-edition-5g-realme-x50-pro-player-edition-and-moto-g7-play-android-10-kernel-sources-are-now-available/>

# 小米 Mi 10 Lite 5G/Mi 10 青春版 5G、Realme X50 Pro Player 版、Moto G7 Play Android 10 内核源码现已上市

小米 Mi 10 Lite 5G/Mi 10 青春版 5G、Realme X50 Player Edition 和 Moto G7 Play 的 Android 10 版本的内核源代码现已提供。

除了旗舰智能手机 [Mi 10](https://www.xda-developers.com/xiaomi-mi-10-review/) 和 [Mi 10 Pro](https://www.xda-developers.com/xiaomi-mi-10-pro-review/) 之外，小米还提供了一种更实惠的产品线变体，称为 [Mi 10 Lite 5G](https://www.xda-developers.com/xiaomi-mi-10-lite-5g-announced/) 。基于骁龙 765g(T7)的设备开箱即可在 Android 10 上运行 MIUI 11，而其 MIUI 12 更新(T8)现在正在欧洲逐步推出。该公司还在他们的祖国销售类似规格的 [Mi 10 青春版 5G](https://www.xda-developers.com/xiaomi-mi-10-youth-edition-5g-snapdragon-765g-periscope-camera-china-launch/) ，尽管中国版本的后置摄像头设置略有不同。如果你已经带了这两款手机中的任何一款，并希望开始构建 TWRP 或移植基于 AOSP 的 ROM，那么你会很高兴地知道，小米已经发布了每款手机各自的 Android 10 版本所附带的 Linux 内核二进制文件的内核源代码。

**[米 10 Lite 5G XDA 论坛](https://forum.xda-developers.com/xiaomi-mi-10-lite)**

小米为米 10 Lite 5G(代号:“莫奈”)和米 10 青春版 5G/ [米 10 Lite Zoom](https://blog.mi.com/en/2020/04/27/newsxiaomi-launches-mi-10-lite-zoom-edition-and-miui-12/) (代号:“凡高”)维护了两个不同的固件包，但它们的内核源代码是统一的。你可以在小米的 Github repo 的“vangogh-q-oss”分支下找到设备 duo 的内核源代码树。

**[米 10 Lite 5G/米 10 青春版 5G/米 10 Lite 变焦内核来源](https://github.com/MiCode/Xiaomi_Kernel_OpenSource/tree/vangogh-q-oss)**

摩托罗拉还发布了 Moto G7 Play 的 Android 10 内核源代码，刷新了他们的 Github repo。该手机最近[以软件版本 *QPY30.52-22* 的形式获得了其稳定的 Android 10 更新](https://www.xda-developers.com/motorola-starts-rolling-out-android-10-stable-update-moto-g7-play/)。新发布的这款手机的内核源代码(代号“channel”)也对应于完全相同的版本。

**[Moto G7 Play Android 10 内核来源](https://github.com/MotorolaMobilityLLC/kernel-msm/releases/tag/MMI-QPY30.52-22) || [Moto G7 Play XDA 论坛](https://forum.xda-developers.com/g7-play)**

最后，我们有[Realme X50 Pro Player Edition](https://www.xda-developers.com/realme-launch-flagship-5g-65w-fast-charging-china-may-25/)，这是一款中国独家旗舰手机，支持 5G 和 65W 快充。与前两个版本不同，这个版本不是*的新版本*，因为内核源代码已经在几周前上传了。请注意， [Realme X50 Pro 5G](https://forum.xda-developers.com/realme-x50-pro) 和它的“播放器”变种不共享一个通用固件，因此下面链接的源代码可能与普通版不兼容。

**[Realme X50 Pro 5G 播放器版内核来源](https://github.com/realme-kernel-opensource/realmeX50Pro-5GPlay_AndroidQ-kernel-source)**