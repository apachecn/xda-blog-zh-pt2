# 开发者为小米 Redmi Note 4 带来完整的项目三重兼容性

> 原文：<https://www.xda-developers.com/xiaomi-redmi-note-4-project-treble/>

如果你一直关注 XDA 门户网站，那么你就会知道我们对谷歌的 Treble 项目有多兴奋。简而言之， [Project Treble](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/) 可能是近年来 Android 框架最重大的底层变化。它涉及将厂商硬件抽象层(HALs)从 Android 框架分离到一个新的厂商分区中，并让 HALs 通过一个新的厂商接口经由所谓的 HAL 接口定义语言(HIDL)与 Android 框架进行通信。这样做理论上会加速未来的软件更新，因为设备制造商，也被称为 OEM，将不再需要等待像高通这样的供应商升级他们的二进制文件，然后他们才能开始工作在下一个版本的 Android 上(像 [Android P](https://www.xda-developers.com/tag/android-p/) )。

所有使用 Android 8.0 Oreo **的 Android 设备必须**兼容 Project Treble(这意味着它们必须通过供应商测试套件【VTS】)，然而，升级到 Android Oreo 的设备不需要。(你可以通过[按照我们这里的指南](https://www.xda-developers.com/project-treble-android-oreo/)来检查你的设备是否是高音兼容的。)虽然谷歌[一直在与一些原始设备制造商](https://www.xda-developers.com/project-treble-android-o-exist-flagship/)合作，以确保一些设备的三重兼容性，但设备制造商如[一加](https://www.xda-developers.com/oneplus-project-treble-android-oreo/)、[诺基亚](https://www.xda-developers.com/why-current-oneplus-nokia-phones-wont-be-project-treble-certified/)和[三星](https://www.xda-developers.com/samsung-galaxy-s8-android-oreo-project-treble/)已经推出了不具备三重兼容性的奥利奥更新。

这在我们的社区成员中尤其令人失望，因为三重兼容性给定制 ROM 开发带来了潜在的问题。在理论化了它如何使定制 ROM 社区受益之后，我个人能够在我的华为 Mate 9 上[启动一个通用的 AOSP Android 8.0 Oreo build](https://www.xda-developers.com/stock-android-oreo-huawei-mate-9-project-treble/) (谷歌称之为通用系统映像【GSI】)。这个[打开了以 GSI 为中心的 ROM 开发](https://www.xda-developers.com/how-project-treble-revolutionizes-custom-roms-android-oreo/)的闸门，其他设备如[华为 Mate 10](https://www.xda-developers.com/project-treble-aosp-android-oreo-huawei-mate-10-pro/) 、 [Honor 8 Pro、Honor 9](https://www.xda-developers.com/honor-8-pro-honor-9-aosp-android-oreo-rom-project-treble/) 等都可以作为日常驱动运行 AOSP Android Oreo 的稳定版本。我个人正在我自己的华为 Mate 10 Pro 上运行一个所谓的“Treble ROM”，由于一些项目，如带有 [GravityBox 模块](https://www.xda-developers.com/all-in-one-xposed-module-gravitybox-android-oreo/)的 [Xposed 框架](https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/)、主题的[底层](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)和我自己的[框架叠加](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/overlay-enable-night-light-adaptive-t3741965)，我没有错过太多功能。

因此，尽管 Treble 似乎给定制 ROM 开发带来了很多好处，但用户想知道是否有可能“移植”Treble 兼容性。这对开发人员来说是一个挑战，因为这意味着他们必须首先找到空间用作临时供应商分区(在还没有分区的设备上)，然后将所有 Hal 从系统分区移到这个新的供应商分区，然后在 HIDL 中自己创建供应商接口。一如既往，XDA 社区的开发者们迎接了这一挑战，XDA 资深成员[abhishek 987](https://forum.xda-developers.com/member.php?u=6070905)[刚刚宣布](https://forum.xda-developers.com/showpost.php?p=75527103&postcount=2233)他能够成功完成上述所有工作，从而为小米红米 Note 4 (mido)带来**完整的项目三重兼容性。**

* * *

## 在小米红米 Note 4 上投射高音

他是怎么做到的？他使用设备上的“cust”分区作为临时供应商分区。cust 分区通常保存了很多来自 MIUI 的特定于设备的东西，所以在 AOSP 版本中这基本上是浪费空间。利用大约 830MB 未使用的分区，他将供应商 HALs 从 system 迁移到 cust，而无需重新分区——这是诺基亚和一加等原始设备制造商在声明中使用的理由，说明他们为什么不为他们的设备带来三倍的兼容性。

*小米红米 Note 4 上的全项目高音兼容性*

经过一番努力让供应商界面正常工作后，他不费吹灰之力就启动了 XDA 资深会员 phhusson 的 Android 8.1 奥利奥 GSI。(注意:phhusson 告诉我，由于缺乏“版本化的 VNDK”，abhishek987 必须改变一些东西才能工作。详细解释这一点需要另一篇关于高音的文章，这是我正在做的！)

如果你想在你的骁龙红米 Note 4 上安装这个 LineageOS 15.1 ROM，那么你会想要彻底阅读 abhishek987 的公告帖子，因为它包含了关于新闪存指令的重要信息。

[**在小米红米 Note 4(骁龙)**](https://forum.xda-developers.com/showpost.php?p=75527103&postcount=2233) 上安装全项目高音支持的 LineageOS 15.1

* * *

## 结论

这无疑是高音相关定制 ROM 开发的一个重要里程碑。一旦开发人员发布了他的设备树，其他定制 ROM 开发人员可以在这项工作的基础上重新开发他们的 ROM——这意味着你将看到的不仅仅是 Redmi Note 4 上完全三倍兼容的 LineageOS。而且，现在这已经被证明是可能的，我们肯定会看到更多的开发者在其他设备上尝试这样做。事实上，我已经看到 XDA 资深公认开发者 [codeworkx](https://forum.xda-developers.com/member.php?u=3208754) [试图在 OnePlus 5/5T 上实现完全的高音兼容性](https://twitter.com/MishaalRahman/status/960208026471936000)。

至于这意味着什么，红米 Note 4 用户有很多值得兴奋的事情。由于高音支持，一旦源代码可用，Redmi Note 4 应该会更容易启动和运行 Android P。Treble 应该使它成为一个设备，比如说，Android 8.1 供应商能够在其上运行 Android P 系统，但由于 Android P 尚未上市，我们无法自己测试这一说法。但是当 Android P 真的出现时，我们一定会试用它，并有可能在定制 ROM 开发方面迈出下一大步。

如果您对 Project Treble 的所有内容感兴趣，请通过我们的 [Project Treble 标签](https://www.xda-developers.com/tag/project-treble/)或使用 XDA 实验室应用程序关注 XDA 门户网站。此外，请考虑订阅我们的三重设备开发论坛，了解更多此类新闻。

[**加入我们的高音设备开发论坛**](https://forum.xda-developers.com/project-treble/trebleenabled-device-development)

*感谢 XDA 成员 Shreesha。Murthy，MyNameIsRage，feherneoh 和 AbhishiktH 给我们发来了一条消息！*