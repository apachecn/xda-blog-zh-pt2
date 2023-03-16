# 安卓派移植到 Honor View 10，华为 Mate 10 Pro 等等

> 原文：<https://www.xda-developers.com/android-pie-honor-view-10-huawei-mate-10-pro/>

Android Pie 是目前 Android 社区中最热门的话题。在发布了谷歌 Pixel [和 Pixel 2](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/) 、 [Essential PH-](https://www.xda-developers.com/essential-phone-android-pie-android-9/) 1 之后，我们论坛上的独立开发者们一直在努力将最新的 Android 版本[从 AOSP](https://www.xda-developers.com/android-pie-source-code-aosp/) 移植到他们的设备上。我们已经看到[小米红米 Note 4、](https://www.xda-developers.com/xiaomi-redmi-note-4-android-pie/)[小米 3、小米 4、红米 4X](https://www.xda-developers.com/xiaomi-mi-3-xiaomi-mi-4-xiaomi-redmi-4x-android-pie-ports/) 、 [ZenFone Max Pro M1](https://www.xda-developers.com/asus-zenfone-max-pro-m1-android-pie-port/) ，以及 OnePlus 2/ [3/3T/X](https://www.xda-developers.com/oneplus-x-oneplus-2-oneplus-3-3t-android-pie/) 获得了 Android 9 Pie 的非官方端口，现在 Honor View 10 和华为 Mate 10 Pro 也加入了移植 Android 9 版本的设备名单。

这要归功于 XDA 论坛版主/认可开发者 [flex1911](https://forum.xda-developers.com/member.php?u=5120185) 和 XDA 认可开发者 [LuK1337](https://forum.xda-developers.com/member.php?u=5075128) 的努力。开发人员从源代码移植了最新版本的 Android，并设法在 Android Pie 公开发布后不到一周就启动了它。我们应该注意到，开发者只在 AOSP 的这个版本中正式支持 Honor View 10，但其他支持三重功能的华为和 Honor 设备也可以启动 AOSP 的相同版本。一些设备需要对 surfaceflinger 二进制文件和 libsurfaceflinger 共享对象库进行修补，而其他设备在没有任何额外修补的情况下也能像 View 10 一样工作。(开发者的[最新版本](https://forum.xda-developers.com/showpost.php?p=77363661&postcount=30)实现了这个补丁，所以你不需要像我一样手动覆盖文件。)因为这是早期版本，所以会有一些 bug。以下是当前的错误列表:

什么不起作用:

*   MTP USB 在 BKL-L04(美国版)上不工作
*   该摄像机在 BKL-L09(以及其他使用 Android 8.0 奥利奥供应商图像的变体)上有问题
*   Wi-Fi 热点不工作
*   [linea geos 15.1 版本的已知问题](https://github.com/berkeley-dev/huawei_quirks/blob/master/TODO.MD)

在我们向您展示兼容设备列表和链接线程之前，让我们先解决一个显而易见的问题:**您需要一个解锁的引导程序来安装这个 ROM。**这对许多人来说似乎是显而易见的，但我们必须解决这个问题，因为[不再可能让任何用户生成新的引导加载程序解锁代码](https://www.xda-developers.com/huawei-honor-request-bootloader-unlock-code/)。如果您的引导加载程序尚未解锁，您现在无法解锁您的引导加载程序来安装这个或任何未来的自定义 ROM。华为关闭 bootloader 解锁表单的决定让我们很难过，因为没有解锁的 bootloader，就不可能安装下一个 Android 版本的早期版本。这些设备可能需要几个月才能收到正式的 Android Pie 更新，其中一些设备可能根本不会收到更新。

## 为 Honor View 10、华为 Mate 10 Pro 等安装非官方的 Android 9 Pie

只需按照下面链接的线程中的说明，在您的设备上安装这个版本的 Android 9 Pie。这是开发人员提供的当前兼容性列表:

*   荣誉观 10
*   华为 P8 Lite 2017
*   荣誉 7X
*   华为 Nova 2i
*   华为 Mate 10 Pro
*   华为 P20 Pro
*   Honor 8 Pro

[**下载 Android 9 派移植到 Honor View 10 和华为 Mate 10 Pro**](https://forum.xda-developers.com/honor-view-10/development/rom-aosp-pie-t3829466)

## 华为/Honor 用户解锁引导程序的提示和技巧

由于拥有解锁引导程序的新华为/Honor 用户的数量最终会减少，所以不会有太多新的华为/Honor 设备指南。对于那些刚刚开始改装华为/Honor 设备并在最后一刻获得引导加载器解锁代码以便安装这样的定制 rom 的人来说，这里有一些关于你的设备的重要信息供你学习。

### 了解您的按钮组合

*   开机时按住**音量调低**和**电源按钮**以及**通过 USB 连接到 PC/电源**，你将启动进入**引导程序**模式。
*   开机时按住**音量增大**和**电源键**，断开**与 USB** 的连接，你将开机进入手机已安装的**恢复**(股票或 TWRP)。
*   开机时按住**音量键**和**电源键**并通过 USB 将**连接到 PC/电源**，将开机进入华为**恢复*** 模式。

*eRecovery 是华为和 Honor 设备上的一项特殊恢复功能，可让您通过 Wi-Fi 完全恢复设备的出厂状态。对于中国以外的用户来说，eRecovery 相当不可靠，所以除非你使用特殊的 DNS/代理服务，比如 [FunkyHuawei.club](https://funkyhuawei.club/) ，否则 Wi-Fi 恢复方法可能对你没用。不过，电子恢复是你解除设备锁定的最后手段之一，所以你应该**永远不要**修改任何电子恢复分区。

### 了解您的分区

有兴趣安装 TWRP 或用 Magisk 给你的手机加根吗？这很酷，但通过了解 TWRP/Magisk 在华为/Honor 设备上修改了哪些分区，可以省去一些麻烦。

*   TWRP 安装到 recovery_ramdisk 分区。(还没有华为/Honor 设备[支持 A/B 分区](https://www.xda-developers.com/list-android-devices-seamless-updates/)，所以这里仍然有一个专用的恢复分区。)
*   Magisk 安装到 ramdisk 分区。(与大多数其他设备将 ramdisk 打包在引导分区不同，华为/Honor devices 将引导分区拆分为专用的 ramdisk 和内核分区。)

### 获取库存分区的备份

如果你安装了 TWRP，你可以备份任何你要修改的分区，比如系统、内存和厂商。安装 TWRP 后，你**应该备份 oeminfo** 。这个分区包括重要的数据，如你的 IMEI 和设备品牌。如果你闪存定制的 rom，你不会(或者不应该)碰这个分区，但是如果你打算重新给你的手机贴牌，你肯定会想要一个这个分区的副本，只是为了安全。

最后，如果你想要额外的安全，从 [Firmware Finder](http://pro-teammt.ru/firmware-database/?firmware_model) 下载你的股票固件的最新版本(“全 OTA”)，并使用本指南从 update.app 文件[中提取分区。当您只能访问引导程序并需要通过快速启动来刷新映像时，请将它们放在身边。(由于安装 TWRP 需要修改 recovery_ramdisk 分区，这实际上也是获得该分区备份的唯一方法。)无论如何，如果你打算闪烁一个项目高音](https://forum.xda-developers.com/mate-10/how-to/guide-extracting-stock-firmware-files-t3756733)[通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)，你会希望通过快速启动来密切熟悉闪烁映像。

* * *

在您的荣誉或华为设备上享受定制 rom，只要它们持续！我在华为 Mate 10 Pro 上用 GSIs 做实验时，通过试错法学会了以上所有内容。我希望这些知识能帮助你节省一些时间，如果出了问题，你不必去 XDA 论坛或 Discord/Telegram 聊天寻求帮助。