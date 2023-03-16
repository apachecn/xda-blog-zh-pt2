# 如何在 Project Treble 支持的设备上闪现通用系统映像(GSI)

> 原文：<https://www.xda-developers.com/flash-generic-system-image-project-treble-device/>

如果你只是顺便听说过 Project Treble，但没有深入研究过它，那么你可能听说过它被认为有助于 Android 的主要更新更快地推出。在 XDA，还有另一个我们已经详细讨论过的好处:能够在任何支持的设备上启动 AOSP 通用系统映像(GSI)。这意味着曾经运行大量定制 Android 版本的设备，如[三星 Galaxy S9](https://www.xda-developers.com/samsung-galaxy-s9-s9-plus-hands-on/) 上的[三星 Experience](https://www.xda-developers.com/samsung-experience-9-0-beta-android-oreo-features/) 或[华为 Mate 10 Pro](https://www.xda-developers.com/huawei-mate-10-pro-porsche-official/) 上的 [EMUI 8](https://www.xda-developers.com/official-changelog-huawei-mate-9-android-oreo-update/) ，可以选择运行更接近于[谷歌 Pixel 2](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 的软件。

售后定制 rom(由通常不隶属于某公司的独立开发人员制作的定制版本的 Android 软件)对 XDA 论坛来说是一个很大的吸引力，由于 Project Treble 需要对 Android 进行更改，支持 Treble 的设备将更容易基于 Android 开源项目(AOSP)更新定制 rom。没有 Project Treble，开发人员不得不采用许多技巧和方法来让他们的定制 rom 工作，虽然 Treble 支持不能解决所有问题，但它肯定有助于启动进程。

像[华为 Mate 9](https://www.xda-developers.com/stock-android-oreo-huawei-mate-9-project-treble/) 、 [Honor View 10](https://www.xda-developers.com/lineageos-honor-view-10-huawei-mate-10-pro-project-treble/) 、[华为 Mate 10 Pro](https://www.xda-developers.com/project-treble-aosp-android-oreo-huawei-mate-10-pro/) 、Honor 7X、 [Exynos 三星 Galaxy S9](https://www.xda-developers.com/samsung-galaxy-s9-aosp-android-8-1-oreo/) 或 [Allview V3 Viper](https://www.xda-developers.com/obscure-mediatek-phone-kernel-source-android-oreo-project-treble/) 这样的设备要么由于缺乏开发者兴趣而没有基于 AOSP 的定制 rom 可用，要么 rom 缺乏一些基本的硬件功能。但正如我们在这些设备的情况下看到的那样，由于 Treble 支持，可用的 rom 大多是功能性的(在哪些有效哪些无效方面存在一些差异，社区已经[整理了一个 wiki 页面](https://github.com/phhusson/treble_experimentations/wiki)您应该查看以找到该信息)。

由于 Treble 对用户来说是如此之新，而且与通常的定制 rom 相比，闪存的过程略有不同，所以关于如何将 GSI 闪存到 Treble 兼容设备上，存在很多困惑。本教程将大致引导你如何刷新这样一个 ROM。根据设备的不同，可能会涉及一些不同的步骤，但一般来说，过程应该是相似的。以下是如何在兼容高音的安卓设备上闪现 GSI 的方法。

* * *

## 如何在支持项目高音的设备上闪烁通用系统图像

**要求:**

*   你的设备**必须**有一个**可解锁的引导程序**。
*   您的设备**必须**与**项目高音兼容**。这意味着您的设备符合以下标准之一:
    *   您的设备**安装了安卓 8.0 奥利奥或更新版本**(例如安卓 8.1 奥利奥)**，并通过了 [Google Play 认证](https://www.xda-developers.com/how-to-fix-device-not-certified-by-google-error/)** 。(如果你对你的设备进行了 rooted 刷新了另一个定制的 ROM，结果你的设备在 Google Play 中被列为未认证，那么不要担心。我们只关心设备发货时的状态。)
    *   您的设备升级到 Android 8.0 Oreo 或更高版本，并由制造商使**与 Project Treble 兼容。参见[这篇文章](https://www.xda-developers.com/list-android-devices-project-treble-support/)获取此类设备的列表。**
    *   您的设备不符合上述任何一个标准，但可以通过一种非官方的方式实现高音兼容。同样，请参考本文中的[以获取此类设备的列表。](https://www.xda-developers.com/list-android-devices-project-treble-support/)
*   您的设备不需要任何重大修改，例如 Xposed Framework、SuperSU 或 Magisk。您可以在以后重新安装这些程序，但是在继续之前，请确保您使用的是普通的 boot/ramdisk。

三星 Galaxy S8/S8+ ( [Exynos](https://www.xda-developers.com/how-to-install-android-oreo-on-the-samsung-galaxy-s8-s8-exynos/) 或[骁龙](https://www.xda-developers.com/install-android-oreo-galaxy-s8-snapdragon/))、三星 Galaxy Note 8 ( [Exynos](https://www.xda-developers.com/install-android-oreo-samsung-galaxy-note-8-exynos/) 或[骁龙](https://www.xda-developers.com/samsung-galaxy-note-8-android-oreo-verizon-sprint/))、 [LG V30](https://www.xda-developers.com/lg-v30-android-oreo-update-south-korea/) 、[索尼 Xperia XA1 系列](https://www.xda-developers.com/sony-xperia-xa1-series-android-oreo/)等设备不符合这些标准中的任何一项，因此无法遵循本指南。虽然 [2018 诺基亚品牌的设备](https://www.xda-developers.com/nokia-8-sirocco-nokia-7-plus-nokia-6-nokia-1-8110-reloaded/)和[骁龙三星 Galaxy S9](https://www.xda-developers.com/samsung-galaxy-s9-and-galaxy-s9-are-official-specifications-features-prices-and-availability/) 与 Android Oreo 一起推出，并支持 Treble，但它们没有可解锁的引导加载器，因此无法刷新 GSI。

请确保，即使您的设备被列为 Treble-compatible，除非您已经正式或非正式地收到 Android Oreo 更新,否则您不会遵循本指南**。如果你的设备符合上述标准，那么你几乎准备好闪光 GSI。我们需要说的最后一件事是，刷新 GSI 将需要您在工厂重置您的设备，所以请确保您在继续操作之前准备好丢失应用程序数据！我们建议您进行设备外备份(例如在您的 PC 或 SD 卡上)，以防出现任何问题。**

* * *

### 支持 Project Treble 的设备上的 flash GSI 指南

#### 为正式支持高音的设备做准备

1.  解锁您的设备的引导加载程序。您在此采取的步骤因设备而异。我们在门户网站和论坛上都有许多指南供您阅读。只要在谷歌上快速搜索“XDA 解锁引导程序”+你的设备名，你就会找到很多指南。
2.  将您选择的 GSI 下载到您的 PC 上。你可以闪存一个纯 AOSP ROM，如 phh-Treble，或者如果你喜欢更多的功能，你可以抓取其他 ROM，如 LineageOS 15.1 或复活混音 GSIs。我将这些线程链接如下。下载适合您的设备类型(大多数人使用 ARM64)和分区类型的映像。如果你的设备支持无缝更新(这种设备的列表[可以在这里找到](https://www.xda-developers.com/list-android-devices-seamless-updates/)，然后下载 A/B 镜像，否则下载 A-only 镜像。

#### 为非正式支持高音的设备做准备

1.  解锁您的设备的引导加载程序。您在此采取的步骤因设备而异。我们在门户网站和论坛上都有许多指南供您阅读。只要在谷歌上快速搜索“XDA 解锁引导程序”+你的设备名，你就会找到很多指南。
2.  通过闪烁本文中提到的帖子中链接的适当文件[，使您的设备高音兼容。你必须在闪现 GSI 之前做到这一点！](https://www.xda-developers.com/list-android-devices-project-treble-support/)
3.  将您选择的 GSI 下载到您的 PC 上。你可以刷新纯 AOSP ROM，如 phh-Treble，或者如果你喜欢更多的功能，你可以抓取 LineageOS 15.1 或复活混音 GSIs。我将这些线程链接如下。下载适合您的设备类型(大多数人使用 ARM64)和分区类型的映像。如果你的设备支持无缝更新(这种设备的列表[可以在这里找到](https://www.xda-developers.com/list-android-devices-seamless-updates/)，然后下载 A/B 镜像，否则下载 A-only 镜像。

以下步骤取决于您的设备是否有您可以使用的功能性 TWRP。如果你的设备有 TWRP，那么我们强烈建议你先安装它。我们在这里有一个[指南。](https://www.xda-developers.com/how-to-install-twrp/)

#### 与 TWRP 一起闪现 GSI

1.  在 TWRP 境内执行工厂重置。
2.  将 GSI 从您的 PC 传输到 TWRP 可以访问的设备内部存储器。
3.  点击“安装”
4.  将类型从“zip”更改为“image”
5.  找到并选择您下载的 GSI。
6.  选择刷新到系统分区。
7.  完成后，重启你的设备。

希望你的设备能在几分钟的等待后启动。如果没有，请跳过以下部分，转到故障排除提示。

#### 没有 TWRP 的闪光 GSI

1.  在您的设备上执行出厂重置。您有两种选择:
    *   打开手机上的设置应用，寻找恢复出厂设置选项。通常在与备份相关的设置下。
    *   在启动时使用按钮组合或在 Android 中启动时发出以下 ADB 命令来重新启动设备的股票恢复:`adb reboot recovery`。到达这里后，使用音量键进行导航，使用电源按钮选择恢复出厂设置选项。
2.  一旦您的设备恢复出厂设置，在启动时使用按钮组合或在 Android 中启动时发出以下 ADB 命令，重新启动设备的引导加载程序:`adb reboot bootloader`
3.  将您的设备连接到 PC，在您下载所选 GSI 的同一目录中打开命令提示符或终端窗口。
4.  输入以下命令:`fastboot erase system`
5.  按以下格式输入命令:`fastboot -u flash system name_of_system.img`
6.  让图像闪烁，这可能需要几分钟时间。完成后，通过电源键或输入`fastboot reboot`手动重启设备。

希望你的设备能够启动到你选择的 GSI。如果没有，这里有一些故障排除技巧。

#### 故障排除提示

*   在一些设备上，如谷歌像素 2/2 XL T2，安卓验证启动(AVB)需要被禁用。你可以通过将[这个镜像](https://drive.google.com/open?id=1ifnXCIdkqKnk_a1HII9RqQd5CVFWz1xR)刷新到 vbmeta 分区来实现(命令:`fastboot flash vbmeta name_of_vbmeta.img`)
*   在 **OnePlus 6** 上，你需要遵循一些[特殊的闪烁指令](https://forum.xda-developers.com/oneplus-6/how-to/treble-mistery-solved-developer-t3800716)。
*   dm-verity 可能会阻止您的设备使用 GSI 启动。在这种情况下，请继续闪存 Magisk，然后看看它是否启动。举例来说，我被告知这是 Razer 手机所必需的。
*   作为最后的手段，您可以在引导加载程序中通过从命令提示符/终端窗口输入`fastboot -w`来尝试数据分区的完整格式(**警告:这将清除所有的**)。我不得不在我的华为设备上这样做，然后它才能工作。

* * *

### 刷新通用系统映像后要做什么

默认情况下，没有任何应用程序来管理超级用户权限。你可以通过从谷歌 Play 商店安装 phh 的超级用户[来解决这个问题。或者，你可以闪现](https://play.google.com/store/apps/details?id=me.phh.superuser) [Magisk](https://forum.xda-developers.com/apps/magisk) 或[SuperSU](https://forum.xda-developers.com/apps/supersu)——由你决定。

接下来，如果你想进一步修改的话，你可以为主题或者[暴露的框架](https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/)安装[底层。Magisk 存储库中有大量简洁的模块，您也可以尝试一下。LineageOS 15.1，尤其是复活混音已经提供了大量开箱即用的功能，所以我们不认为你真的需要修补大量额外的好东西，但选择是存在的。](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)

现在，享受股票 Android 的世界！我们建议您关注[Treble-Enabled Device Development](https://forum.xda-developers.com/project-treble/trebleenabled-device-development)论坛，了解有关您的 ROM 的任何更新。此外，请关注 XDA 门户网站，了解与 Treble 项目相关的所有最新进展。最好的方法是为[高音标签](https://www.xda-developers.com/tag/project-treble/)设置一个馈送。

最后，请向 [Treble Experimentations wiki 页面](https://github.com/phhusson/treble_experimentations/wiki)投稿，这样其他人就会知道 ROM 的任何潜在问题(这样开发者就知道该修复什么！)