# 高通能够在 6 周内发布骁龙 845 源代码

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-845-kernel-source-code/>

[高通](https://www.xda-developers.com/tag/qualcomm/)的最新高端片上系统，[高通骁龙 845](https://www.xda-developers.com/tag/qualcomm-snapdragon-845/) ，[在去年 12 月的骁龙科技峰会上发布了](https://www.xda-developers.com/qualcomm-snapdragon-845-news/)。[芯片组提供了](https://www.xda-developers.com/qualcomm-2018-snapdragon-tech-summit-roundup/) 4 个 Kryo 385 (A75“性能”)和 4 个 Kryo 385 (A55“效率”)CPU 内核、最新的 Adreno 630 GPU、Spectra 280 ISP、Hexagon 685 DSP、骁龙 X20 LTE 调制解调器和一个新的安全处理单元(SPU)。骁龙 845 SoC 是基准测试中的[发电站，它已经在](https://www.xda-developers.com/qualcomm-snapdragon-845-hands-on-benchmarks-first-impressions/)[三星 Galaxy S9/S9+](https://www.xda-developers.com/tag/samsung-galaxy-s9/) 、[小米 Mi Mix 2S](https://www.xda-developers.com/xiaomi-launches-xiaomi-mi-mix-2s-qualcomm-snapdragon-845/) 和 [OnePlus 6](http://xda-developers.com/tag/oneplus-6) 等设备中可用。我们论坛上的开发人员一直渴望得到一台拥有高通最新最棒的设备，但只有一件事让一些开发人员担心该平台的发展前景:在 [CodeAurora 论坛](https://www.codeaurora.org/)上缺乏公开可用的内核、Hal、框架分支等源代码。

* * *

## 高通和 CodeAurora 论坛

如果你想知道为什么我们论坛上的开发者喜欢使用高通芯片组的设备，而不是使用来自[海思](https://www.xda-developers.com/tag/huawei/)、[三星](https://www.xda-developers.com/tag/samsung/)、[联发科](https://www.xda-developers.com/tag/mediatek/)和其他公司的芯片组的设备，原因是高通对定制开发社区的友好。定制 ROM 开发者构建的 Android 基于 Android 开源项目(AOSP)。谷歌发布了 AOSP 的[公共部分，但他们也私下开发 Android 的部分内容(这就是为什么如果你今天从 AOSP 构建一个 ROM，你将不会得到](https://source.android.com/) [Android P](https://www.xda-developers.com/tag/android-p/) 中任何[花哨的新功能](https://www.xda-developers.com/everything-new-android-p-developer-preview-2/)。)对于定制 ROM 开发者来说，他们所拥有的融合 Android 最新平台特性的唯一选择就是等待 Google 发布最终版本的源代码。然而，芯片组供应商与谷歌达成了[协议，以提前获得下一版本的 Android](https://www.xda-developers.com/qualcomm-snapdragon-android-p/)——他们从私人 AOSP 仓库中获取，修改他们的芯片组代码以兼容，然后将这些代码分发给原始设备制造商，以构建和分发他们设备的 rom。

*安卓各版本的一般更新流程。来源:[谷歌](https://android-developers.googleblog.com/2017/05/here-comes-treble-modular-base-for.html)。*

为了遵守 Linux 内核的 GNU 通用公共许可证(GPL ),芯片组供应商和原始设备制造商需要发布内核源代码，但这是他们需要发布的全部内容。例如，高通骁龙 845 [三星 Galaxy S9/S9+](https://www.xda-developers.com/samsung-galaxy-s9-kernel-source/) 、[小米 Mix 2S](https://www.xda-developers.com/xiaomi-releases-kernel-sources-for-the-xiaomi-mi-mix-2s/) 和 [OnePlus 6](https://www.xda-developers.com/oneplus-6-kernel-source-code/) 的内核源代码已经可用。这足以让开发人员开始在这些设备上移植基于 AOSP 的定制 rom，但仅仅访问内核源代码并不意味着将 [LineageOS 15.1](https://www.xda-developers.com/tag/lineageos/) 移植到这些设备上很容易(尽管由于[项目 Treble](https://www.xda-developers.com/tag/project-treble/) ，这种情况正在改变)。新芯片组特性的所有芯片组特定代码通常在这些内核源代码版本中不可用，这是意料之中的，因为代码将揭示专有芯片组特性是如何工作的。开发人员可以以预编译二进制文件(称为二进制大型对象或 BLOB)的形式访问这些代码，但几乎不可能将这些 BLOB 与他们在 AOSP ROM 上的工作结合起来，因为没有关于如何工作的文档。

对开发者来说幸运的是，这正是高通的 CodeAurora 论坛(CAF)派上用场的地方。在 CAF 上，高通发布了他们的芯片组特定代码的公共部分，这种方式使得 ROM 开发者不必知道新的芯片组特性是如何工作的，就可以很容易地为平台进行构建。开发人员只需要派生出新平台库的[公共部分(比如 hardware/qcom/display 和 vendor/qcom-open source/bluetooth)并将其与预编译的二进制文件结合起来，基本上就能完成大部分工作。高通已经在 CAF 上发布了之前 SOC 的芯片组特定代码，如](https://source.codeaurora.org/quic/la/)[高通骁龙 820](https://www.xda-developers.com/tag/qualcomm-snapdragon-820/) / [821](https://www.xda-developers.com/tag/qualcomm-snapdragon-821/) 和 [Snapdragon 835](https://www.xda-developers.com/tag/qualcomm-snapdragon-835/) ，通常在芯片组发布的几天内！然而，自从骁龙 845 宣布以来已经过去了 **5 个月**，我们还没有[看到该公司通常的源代码下降到 sdm845 分支](https://wiki.codeaurora.org/xwiki/bin/QAEP/release)下。

*在 CAF 中搜索与高通骁龙 835 SoC 相关的源代码*

CAF 中 sdm845 源代码的延迟发布导致一些开发人员担心高通会放弃该论坛，实际上变得像联发科一样，只与合作伙伴而不是社区共享源代码。我们采访的开发者担心，这将有损于小米等公司设备上的定制 rom 开发，因为 CAF 资源通常是为小米的骁龙设备构建稳定的 ROM 所必需的。我们联系了高通，了解发生了什么，我们终于有了一些好消息要分享: **CAF 并没有被抛弃**，只是高通骁龙 845 代码下降不会发生，直到高通宣布他们的新移动平台。原因？因为[泄密](http://xda-developers.com/tag/exclusive)。

* * *

## CodeAurora 论坛和高通芯片泄漏

当高通的工程师为他们的芯片组开发新的平台功能时，他们很少会只为一个芯片组开发这些功能。未发布的芯片组有可能使用已经发布的芯片组中的相同软件，如骁龙 845。虽然公司经常使用代号来防止泄密，但即使这样也不能完全防止泄密的发生。例如，未发布的[高通骁龙 670 的细节是来自 *WinFuture 的罗兰·匡特在*](https://www.xda-developers.com/qualcomm-snapdragon-670-kernel-source/)咖啡馆发现的。我们后来从咖啡馆得知，高通骁龙 670 被[更名为高通骁龙 710](https://www.xda-developers.com/qualcomm-snapdragon-710-xiaomi-devices/) 。高通还没有证实骁龙 670/骁龙 710 的存在，但由于在咖啡馆的参考，我们已经知道了很多关于即将到来的芯片组。

因此，为了防止这样的泄密事件发生，高通选择推迟发布骁龙 845 的源代码。我们被告知，在新的移动平台发布之前，该公司不会发布芯片组的源代码。在**大约 6 周后**，该公司将能够在 CAF 上发布 sdm845 源代码。一名高通代表对源代码发布的延迟表示歉意，称该公司正在审查代码中的芯片组命名约定，以便他们可以为已经发布的芯片组发布代码，同时仍然避免泄漏。