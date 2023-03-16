# OnePlus 3 的最佳 rom、内核和 mod

> 原文：<https://www.xda-developers.com/oneplus-3-best-stuff/>

OnePlus 3 带来了一种设计革新，它摒弃了前两款手机的标志性砂岩背面，并通过软化曲线和边缘以及改变所用材料来改变设计语言。

虽然 OnePlus 2 引入了坚固的镁框架来补充砂岩背部，但全金属 OnePlus 3 由单一铝块制成，最终仍然令人惊讶地坚固。事实上，虽然 OnePlus 3 缺乏其前身的重量，但它最终看起来相当耐用，[的测试表明](https://www.youtube.com/watch?v=8PZ8W_g6Vvk)它可能不会像类似的手机一样弯曲。[](http://static1.xdaimages.com/wordpress/wp-content/uploads/2016/11/oneplus_3_launch.jpg)

| 安卓版本 | 6.0.1(氧气只读存储器) | 显示 | 5.5 英寸 1080 像素 AMOLED(401 像素 ppi) |
| 芯片集 | 骁龙 820，四核 2x 2.15GHz 2x 1.6GHz，Adreno 530 GPU | 电池 | 3000 毫安时，快速充电(5V 4A) |
| 随机存取存储 | 6GB LPDDR4 | 传感器 | 指纹、冰雹、加速度计、陀螺仪、接近度、环境光、电子罗盘 |
| 储存；储备 | 64GB UFS 2.0 | 连通性 | USB 2.0 Type C，双 nano-SIM 卡插槽，3.5 毫米音频插孔 |
| 规模 | 152.7 x 74.7 x 7.35 厘米(屏幕与机身的比例约为 73%) | 后置摄像头 | 16MP 索尼 IMX 298 传感器，1.12μm，OIS，EIS，PDAF，f/2.0，原始支持，4K 30FPS / 720p 120FPS 视频 |
| 重量 | 158 克 | 前置摄像头 | 800 万像素索尼 IMX179，1.4μm，EIS，定焦，f/2.0，1080p 30FPS 视频 |

## rom/mod/内核/指南

### OnePlus 3 的最佳内核

**渲染内核**

来自开发者 [RenderBroken](https://forum.xda-developers.com/member.php?u=5438598)

*   采用 LINARO 6.x 构建
*   更新了洛杉矶咖啡馆。嗯. 5.5
*   IO 调度程序- FIOPS、CFQ、BFQ、ROW、DEADLINE、NOOP 和 ZEN 调度程序
*   Flar 声音控制
*   通过@savoca 完成颜色校准
*   超频
*   F2FS 支持
*   肾上腺素增强

[**线程**](https://forum.xda-developers.com/oneplus-3/development/kernel-render-kernel-t3505956)

**佛朗哥内核**

来自开发商 [franciscofranco](https://forum.xda-developers.com/member.php?u=3292224)

*   传奇的电池寿命
*   一闪而过
*   典型的界面，像显示调节、声音控制、振动控制，以及所有那些无聊的东西
*   绕过 Android Pay 兼容性的验证启动标志(root 仍然会破坏 Android Pay，但那是你自己的问题)
*   空闲功耗降至绝对最低(如果你有来自第三方应用的唤醒锁，显然你只能靠自己了)
*   支持 FKUpdater 的性能配置文件
*   后台应用程序限制从 32 个增加到 60 个(我们有 6Gb 内存，废话！)
*   神奇的支持，我每天都在这里，几乎每小时检查帖子，随时准备提供帮助(嗯，除非你没有阅读 OP，它包含了你需要的大部分信息)
*   与我的应用 FKUpdater 无缝集成
*   可能更多，查看我的 github 了解所有细节——代码本身就说明了一切

[**线程**](https://forum.xda-developers.com/oneplus-3/development/kernel-franco-kernel-r1-28th-november-t3508904)

**带 CM13 的 OP#的 Arter97 内核**

Arter97 内核来自开发者 [arter97](http://forum.xda-developers.com/member.php?u=4898097) 。

*   最新利纳罗 LSK 内核完全合并
*   自适应 LMK 禁用
*   使用最新的 Linaro GCC 工具链和最新的 Linux H.G 链接器构建
*   内置 O2 速度优化
*   启用高能效工作队列
*   从主线 Linux 反向移植随机驱动程序(快 12 倍)
*   Westwood 作为默认 TCP 网络拥塞控制
*   移除存储上的熵挂钩
*   带有 noatime 的默认文件系统挂载选项
*   默认使用 CFQ I/O 调度程序(这是 3.18 内核中最快的 I/O 调度程序)
*   NVIDIA 的电源效率改进承诺得到应用
*   Galaxy S7 移植的 sd 卡文件系统(稳定)
*   支持 f2fs 格式的系统分区

[**线程**](http://forum.xda-developers.com/oneplus-3/development/arter97-kernel-oneplus-3-running-t3439266)

**基于 OP3 CM 的 rom 的元素 x**

来自开发者 [flar2](http://forum.xda-developers.com/member.php?u=4684315) 。

*   使用 Aroma 安装程序轻松安装和设置
*   唤醒手势支持(sweep2wake 和 doubletap2wake)
*   通知 LED 控制
*   声音控制
*   高级颜色控制
*   清扫睡眠
*   背光调光器
*   超频或欠频 CPU
*   调整或禁用振动
*   FIOPS、BFQ、CFQ、deadline、noop 和 SIO i/o 调度程序
*   NTFS 读/写支持
*   禁用 fsync 的选项
*   性能和功耗优化
*   USB OTG 支持
*   短跑费用
*   支持 MultiROM
*   不强制加密
*   与无系统根目录兼容

[**线程**](http://forum.xda-developers.com/oneplus-3/development/kernel-elementalx-op3-0-01-t3404879)

**blu_sp★rk r18 混合定制 rom**

这个内核来自开发者 [eng.stk](http://forum.xda-developers.com/member.php?u=3873953) 。

*   由 Ubuntu 16.04.1 x86_64 支持
*   增强了对设备和目标标志的全面 O3 支持，改进了 linaro 构建，等等
*   少即是多:stockish OP3/OP3T 混合构建基于 OnePlusOSS/Android _ kernel _ oneplus _ MSM 8996
*   无系统安装程序(OTA 友好)
*   删除了一些调试和日志选项
*   ARM 增强的性能和电池补丁
*   一般上游和 CAF 修复
*   可用超频(使用默认频率启动)，设置 300HZ 基本定时器频率
*   msm_performace 输入升压开关(默认禁用)，调整 cpu_boost 驱动程序
*   增强的 TCP 方法(westwood 是默认的)，网络和 Wifi 调整和更新的驱动程序
*   几个 I/O 控制调整，添加调度 FIOPS 和 ZEN v2 是默认的，调整文件系统(F2FS，ExFAT，NTFS 和 CIFS)
*   删除了验证和强制加密
*   默认情况下，库存热量驱动器(提供自定义可调参数)
*   优化的 RWSEM、AES 和 SHA1 例程(支持 NEON)
*   默认关闭交换和自适应 LMK
*   振动器强度可调和手势触觉反馈控制
*   KGSL 修复并重新制作了 GPU 驱动程序(使用 133MHz 最小频率以节省电量，在 100MHz 时进入空闲状态)
*   sRGB 和 KCAL -高通 MDSS v2 的高级色彩控制(RGB 校准和后处理功能)
*   DASH charge 和 USB 快速充电(MTP 开启时 USB 模式最高可达 900mA)
*   电池/通知 LED 控制
*   Multimount fstab(您可以将数据和缓存分区用作 f2fs 或 ext4)
*   FS fsync 开关
*   海量存储上的 CDROM 仿真(与 DriveDroid 0.10.18+兼容)
*   init.d 支持(将您的脚本放在/system/su.d 或/su . su . d[无系统 SuperSU])中

[**线程**](http://forum.xda-developers.com/oneplus-3/development/kernel-t3404970)

### OnePlus 3 的最佳牛轧糖 rom

**crDroid 安卓**

crDroid 旨在为您的设备提高性能和可靠性，同时试图带来当今存在的许多最佳功能。我们主要基于 CyanogenMod，所以使用与它们兼容的自定义内核！

[**线程**](https://forum.xda-developers.com/oneplus-3/development/rom-crdroid-android-beta-builds-t3483640)

**BJ-RR 复活混音 N**

复活混音 ROM 基于 CM，slim.omni 和原始混音 ROM 构建，这创造了性能，定制，功能和最新功能的可怕组合，直接带到您的设备上

[**线程**](https://forum.xda-developers.com/oneplus-3/development/rom-resurrection-remix-m-t3399960)

**CypherOS 3.1.3 芝士蛋糕**

这是塞弗。对纯 Android 的扩展。Cypher 试图保持 Android 的纯洁性，同时为用户提供有用的功能。目标是在实现简单性的同时提供最高水平的性能。

[**线程**](http://forum.xda-developers.com/oneplus-3/development/rom-cypheros-3-1-cheesecake-t3500074)

**OP3 官方复活 Remix-N v 5 . 8 . 0**

复活混音版基于 CM，slim.omni 和原始混音版。这创造了性能、定制、功能和最新功能的完美结合，直接带到您的设备上。许多在以前版本中被修改的东西，现在都默认包含在 ROM 中，所以，请欣赏！

[**线程**](http://forum.xda-developers.com/oneplus-3/development/rom-resurrection-remix-n-v5-8-0-oneplus-t3507292)

**CM14.1 牛轧糖 7.1.x 夜宵**

CyanogenMod 是一款定制的售后固件发行版，适用于多种 Android 设备。基于 Android 开源项目，CyanogenMod 旨在提高谷歌、T-Mobile、HTC 等供应商和运营商发布的基于 Android 的 rom 的性能和可靠性。CyanogenMod 还提供了目前这些版本的 Android 中没有的各种功能和增强。

[**线程**](http://forum.xda-developers.com/oneplus-3/development/unofficial-cm14-1-root-nightlies-t3490551)

### OnePlus 3 的最佳棉花糖 rom

**Arter97 定制的 CyanogenMod 13**

*   强制启用优化编译器和优化一切过滤器的艺术，第一次启动(或更新后)将非常慢
*   用 GCC 代替 Clang 构建，以避免稳定性和性能退化
*   采用甲骨文 JDK 7u121 构建
*   合并了 AOSPA 的仿生(libc)优化
*   为了更好的优化，合并了 AOSPA 的构建环境
*   对 apk 和 jar 进行半强制 0 压缩以获得更好的性能
*   更新的内存分配器(jemalloc)
*   更新的 SQLite
*   Privacy Guard 上的 CyanogenMod 12.1 的前转“唤醒”控制
*   实现了状态栏老化保护

[**线程**](https://forum.xda-developers.com/oneplus-3/development/arter97-s-custom-built-cyanogenmod-13-t3439217)

**用于 OP3 的 MIUI 8**

这个帖子列出了你的 OnePlus 3 的九个不同版本的 MIUI ROMs。这些 rom 基于 Android 棉花糖 6.0.1。

MIUI 是我们自己的基于 Android 的用户界面，受到全球数百万人的喜爱。在过去的五年里，我们开发了无数的功能和优化，将提高您使用手机的方式。MIUI 很直观，很有用，也很容易使用。

[**线程**](http://forum.xda-developers.com/oneplus-3/how-to/rom-miui-8-multiple-editions-t3479362)

**带有 OP3 和 OP3T 定制内核的非官方 CM13】**

这是一个统一的 CyanogenMod 13.0 ROM，可以在 OnePlus 3 和 OnePlus 3T 上工作。它基于稳定的 CyanogenMod 分支，而不是 nightly 分支，主要目标是稳定性和整体良好的用户体验。这个 ROM 带有一个高度定制的内核，以及一些其他非常定制的修改。

[**线程**](http://forum.xda-developers.com/oneplus-3/development/rom-kernel-unofficial-cyanogenmod-13-0-t3444221)

**FreedomOS CE 1.10**

FreedomOS 允许你通过安装一个极简的 Android 体验来解除 ROM 的屏蔽。这个 ROM 是完全可定制的，你将得到一个完全加载的 ROM 的所有最好的特性，没有任何膨胀。

[**线程**](http://forum.xda-developers.com/oneplus-3/development/rom-freedomos-ce-1-7-t3470660)

显示屏肯定比我们以前的一加手机要好。我确实发现 OnePlus One 的 LCD 和 OP3 的 OAMOLED 的色彩饱和度有点奇怪，但这是一个非常漂亮的显示器。

今天刚拿到手机，已经玩了几个小时了。在某些方面，这不是我的 Moto X Pure 的大升级，但就速度而言，它绝对是一种享受。一切都非常爽快和流畅。

目前的 6p 和 HTC 10 用户在这里，我甚至不能开始说我对这个 OP3 印象有多深刻。承认吧，我只吃了半天，到目前为止，我完全被弄糊涂了！！现在快 3 小时了，电池电量只有 50%😃我喜欢它的一切。唯一平庸的是外部扬声器。惊人的相机，漂亮的屏幕，完美的尺寸，握在手中感觉很好，拍出来甚至看起来很棒！哦，指纹阅读器比 10 和 6p 都要快。但是给我印象最深的还是皮肤。我仍然是骨头股，我从来没有离开手机股票..它有谷歌应该有的所有东西..也没有腌制品..只是一个令人印象深刻的手机和所有的 400 美元！

**OnePlus One XDA 官方审核**

在这篇评论中，我们将深入探讨 OnePlus 3。该功能试图提供与我们的读者群相关的内容，而不是列出规格和谈论体验感受。在 XDA，我们的评论不是为了告诉用户一部手机是否值得购买——相反，我们试图通过我们的话语把手机借给你，并帮助你自己做出决定。

[**阅读更多**](https://www.xda-developers.com/oneplus-3-xda-review/)

### OxygenOS 的提示和技巧

**如何安装谷歌拨号器(电话)和联系人**

使用谷歌的 [Phone](https://play.google.com/store/apps/details?id=com.google.android.dialer) 应用程序，你可以屏蔽垃圾邮件和其他不需要的电话。它还具有增强的来电显示功能。这些只是 OP3 的默认拨号器缺少的一些功能。不幸的是，谷歌不允许在 OP3 等非 Nexus 设备上安装该应用程序。为了解决这个问题，我创建了一个 flashable zip 来安装 Google Dialer(电话)应用程序和必要的 Dialer 框架。

[**线程**](http://forum.xda-developers.com/oneplus-3/how-to/guide-how-to-install-google-dialer-phone-t3443006)

**仪表板充电速度分析**

更快的充电速度已经成为原始设备制造商幸灾乐祸的一个常见规格，推动他们自己的标准和实施，以立即给你充电。如今，当一部手机充电速度不快时，它就会突出来，让人头疼。

[**阅读更多**](https://www.xda-developers.com/dash-charge-speed-analysis-even-with-heavy-usage-your-phone-will-charge-rapidly-and-stay-cool/)

**OnePlus 3 的长期性能**

几天前，我们快速浏览了一下 [OnePlus 3](http://forum.xda-developers.com/oneplus-3) 的 RAM 管理背后的问题[，这是一个围绕手机性能的热门话题。这款手机的骁龙 820 处理器的性能似乎不是什么大话题，*也不是热门话题*。](http://www.xda-developers.com/how-to-fix-the-oneplus-3s-memory-management-almost-double-the-apps-in-memory/)

[**阅读更多**](https://www.xda-developers.com/oneplus-3-performance-throttling-and-thermals-analysis-redeeming-the-oneplus-2/)

### 如何修复砖砌的 OnePlus 3

**一加 3s 硬质砖的 Mega Unbrick 指南**

一个硬砖 OP3 除了黑屏什么都没有(屏幕上什么都没有，甚至没有启动标志)，当电源按钮被按下并保持 20 秒时，它可能会振动，没有恢复分区，没有 adb 模式，也没有快速启动分区(它可能是一个闪烁的一加标志)。在 Linux 中可以检测到这个设备，你甚至可以向它发送命令。在 Windows 下，被砖化的 OP3 应该检测为 QHUSB_BULK，未知设备，高通什么的。您可能会因为刷新一个用于不同设备的内核(或一个用于另一个包含内核的设备的 ROM)、修改引导徽标或引导加载程序，或者尝试解锁引导加载程序导致引导分区损坏而导致 OP3 被阻塞。大多数情况下，这是必要的，因为 OEM 解锁被禁用，手机无法启动和没有恢复。

[**线程**](http://forum.xda-developers.com/oneplus-3/how-to/guide-mega-unbrick-guide-hard-bricked-t3405700)

### OnePlus 3 的最佳曝光改装

**自定义滑块**

我向您展示我的自定义滑块应用程序，它可用于在 Oneplus 3、Oneplus 2 和 Oneplus X 上自定义您的提醒滑块。支持基于 OOS 和 AOSP 的 rom，但目前不支持 OOS 社区版本 3.5+!

[**线程**](http://forum.xda-developers.com/oneplus-3/themes/app-custom-slider-root-xposed-required-t3439672)

**操作按钮模块**

OP3 按钮模块目前在按钮操作中增加了缺失的“打开/关闭菜单”。我正计划添加一个选项来替换菜单按钮的单按行为，尽管这不会出现在第一版中。安装这个 mod 有两个选项:Xposed module 或者 modded Settings.apk。

[**线程**](http://forum.xda-developers.com/oneplus-3/themes/mod-op3-button-mods-t3411524)

**OnePlus 3 的最佳调整**

OnePlus 3 很棒。你可能已经看到了 XDA 上发布的广泛评论，但今天我们将讨论如何让 OnePlus 3 变得更好。让我们回顾一下人们对手机最常见的一些抱怨，以及一些可以解决这些抱怨的方法。

[**阅读更多**](https://www.xda-developers.com/best-mods-for-the-oneplus-3/)

### OnePlus 3 的最佳外壳、屏幕保护器和外壳

**VOOC 和 DASH 充电配件**

根据 OPPO 的 VOOC(OP Dash 充电系统)的早期评论，这似乎远远优于市场上的任何 QC 甚至 iPhone 充电系统。通过将热量带到实际的充电器块，大约 20 瓦，超过 7 个引脚，它比 QC2.0 更快，更冷，比 Moto 的 QC2.0+更冷。

[**线程**](http://forum.xda-developers.com/oneplus-3/accessories/vooc-dash-charging-accessories-t3398938)

* * *

**解锁你的引导程序，闪烁 TWRP 和寻根的指南**

这个设备的根实际上是一个非常简单和容易的过程。在您开始之前，建议您至少尝试理解该过程的每个部分将会做什么。虽然本指南将延长每个步骤，以显示所有的细节，所使用的方法可以分为 3 个主要步骤:解锁引导加载程序，安装自定义恢复，最后根。

[**线程**](http://forum.xda-developers.com/oneplus-3/how-to/oneplus-3-how-to-unlock-bootloader-t3398733)

[**从 Swappa**](https://swappa.com/buy/oneplus-3-unlocked) 买一台 330 美元起的二手 OnePlus 3

* * *

*嘿！感谢你阅读这篇文章。这是我们想出的新东西，如果你喜欢，我们会做更多(更多手机)，或者，如果你认为它可以更好，告诉我们如何做！或者，如果我们错过了什么，请在评论中告诉我们。无论哪种方式，我们都希望得到您的反馈。*