# OnePlus 5 和 OnePlus 5T 现在在最新的 OxygenOS 测试版上支持 Project Treble

> 原文：<https://www.xda-developers.com/oneplus-5t-project-treble-oxygenos-beta/>

一加以及谷歌、小米和诺基亚等其他几家智能手机供应商提供了一个公共测试程序。一加的 OxygenOS Open Beta 计划让您在稳定版本发布之前很久就可以收到新功能和安全补丁的更新。OnePlus 5 和 OnePlus 5T[分别获得了新的](https://forums.oneplus.com/threads/oxygenos-open-beta-13-for-the-oneplus-5-and-open-beta-11-for-oneplus-5t.865027/) OxygenOS Open Beta 13 和 Open Beta 11，它们带来了一些令人惊讶的东西:项目高音兼容性。

Project Treble 是在 Google I/O 2017 之前宣布的，当时我们甚至还不知道 Android Oreo 中的大多数新平台功能。Treble 背后的想法是[模块化 Android 操作系统](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/),这样制造商更容易对软件进行更新。通过将供应商 HALs 从 Android 框架中分离出来，并在框架和 HALs 之间提供标准接口，谷歌使设备制造商能够更快地推出新版本的 Android。这反过来让设备制造商有更多的时间来开发软件功能，使用户体验更加愉快，谷歌直接将 Android P 引入[如此多新软件功能](https://www.xda-developers.com/android-p-beta-3-google-pixel-2-xl/)的原因归功于 Project Treble，而不是 Android Oreo。最后，高音支持在非谷歌设备如 OnePlus 6、小米 Mix 2S、索尼 Xperia XZ2、诺基亚 7 Plus 和更多[提前获得](https://www.xda-developers.com/android-p-beta-program-is-now-available/)Android P 测试版的原因中发挥了重要作用。

对于任何推出 Android 8.0 Oreo 及更高版本设备的设备制造商来说，三重支持是强制性的，但对于任何升级到 Android Oreo 的设备来说，这不是一项要求。我们已经看到[华为等公司的几款设备获得了三重支持](https://www.xda-developers.com/list-android-devices-project-treble-support/)，而一加和诺基亚此前表示，不考虑为三重提供支持。一加给我们的理由是，他们[觉得通过 OTA 更新重新划分 OnePlus 5 和 OnePlus 5T 会有风险](https://www.xda-developers.com/why-current-oneplus-nokia-phones-wont-be-project-treble-certified/)。然而，正如独立 ROM 开发人员所展示的[，每个设备上都有大量未使用的空间，可以重新用于适合移动 Hal 的供应商分区。我们还没有检查运行最新 OxygenOS 开放测试版的 OnePlus 5 和 OnePlus 5T 的分区表，以确认他们如何处理这个过程，但至少这对于这些设备的所有者来说仍然是一个令人兴奋的消息。](https://www.xda-developers.com/oneplus-5-oneplus-5t-project-treble/)

**更新:**这里是运行最新公测版的 OnePlus 5 的分区表。如您所见，现在有一个供应商分区。

### OxygenOS Open Beta 13 上的 OnePlus 5 分区列表

```

drwxr-xr-x 2 root root 1480 1970-11-28 23:34:41.249999999 -0500 .
drwxr-xr-x 4 root root 1640 1970-11-28 23:34:41.249999999 -0500 ..
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 LOGO -> /dev/block/sde18
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.249999999 -0500 abl -> /dev/block/sde16
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 ablbak -> /dev/block/sde17
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 apdp -> /dev/block/sde31
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.249999999 -0500 bluetooth -> /dev/block/sde24
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 boot -> /dev/block/sde19
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 boot_aging -> /dev/block/sde20
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 cache -> /dev/block/sda3
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 cdt -> /dev/block/sdd2
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 cmnlib -> /dev/block/sde27
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 cmnlib64 -> /dev/block/sde29
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 cmnlib64bak -> /dev/block/sde30
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 cmnlibbak -> /dev/block/sde28
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.209999999 -0500 config -> /dev/block/sda12
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 ddr -> /dev/block/sdd3
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 devcfg -> /dev/block/sde39
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 devinfo -> /dev/block/sde23
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.209999999 -0500 dip -> /dev/block/sde14
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.249999999 -0500 dpo -> /dev/block/sde33
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.219999999 -0500 dsp -> /dev/block/sde11
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.219999999 -0500 frp -> /dev/block/sda6
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.249999999 -0500 fsc -> /dev/block/sdf4
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.249999999 -0500 fsg -> /dev/block/sdf3
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 fw_4g9n4 -> /dev/block/sde45
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 fw_4j1ed -> /dev/block/sde43
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 fw_4t0n8 -> /dev/block/sde46
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 fw_8v1ee -> /dev/block/sde44
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.219999999 -0500 hyp -> /dev/block/sde5
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 hypbak -> /dev/block/sde6
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 keymaster -> /dev/block/sde25
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 keymasterbak -> /dev/block/sde26
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.219999999 -0500 keystore -> /dev/block/sda5
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 limits -> /dev/block/sde35
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.249999999 -0500 logdump -> /dev/block/sde40
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 logfs -> /dev/block/sde37
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.239999999 -0500 md5 -> /dev/block/sdf5
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 mdtp -> /dev/block/sde15
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.219999999 -0500 mdtpsecapp -> /dev/block/sde12
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.219999999 -0500 mdtpsecappbak -> /dev/block/sde13
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 minidump -> /dev/block/sde47
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 misc -> /dev/block/sda4
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 modem -> /dev/block/sde10
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.239999999 -0500 modemst1 -> /dev/block/sdf1
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.239999999 -0500 modemst2 -> /dev/block/sdf2
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.249999999 -0500 msadp -> /dev/block/sde32
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.219999999 -0500 oem_dycnvbk -> /dev/block/sda7
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 oem_stanvbk -> /dev/block/sda8
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.229999999 -0500 param -> /dev/block/sda9
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.239999999 -0500 persist -> /dev/block/sda2
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.249999999 -0500 pmic -> /dev/block/sde8
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.239999999 -0500 pmicbak -> /dev/block/sde9
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 recovery -> /dev/block/sde22
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.249999999 -0500 reserve -> /dev/block/sdd1
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 reserve1 -> /dev/block/sda10
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.209999999 -0500 reserve2 -> /dev/block/sda11
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.229999999 -0500 reserve3 -> /dev/block/sdf7
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.239999999 -0500 rpm -> /dev/block/sde1
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 rpmbak -> /dev/block/sde2
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.239999999 -0500 sec -> /dev/block/sde7
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 splash -> /dev/block/sde34
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.229999999 -0500 ssd -> /dev/block/sda1
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 sti -> /dev/block/sde38
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.249999999 -0500 storsec -> /dev/block/sde41
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.239999999 -0500 storsecbak -> /dev/block/sde42
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:40.559999999 -0500 system -> /dev/block/sde21
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.229999999 -0500 toolsfv -> /dev/block/sde36
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.219999999 -0500 tz -> /dev/block/sde3
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.219999999 -0500 tzbak -> /dev/block/sde4
lrwxrwxrwx 1 root root 16 1970-11-28 23:34:41.219999999 -0500 userdata -> /dev/block/sda13
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:40.559999999 -0500 vendor -> /dev/block/sdf6
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 xbl -> /dev/block/sdb1
lrwxrwxrwx 1 root root 15 1970-11-28 23:34:41.209999999 -0500 xblbak -> /dev/block/sdc1

```

我们已经深入讨论了 Treble 为基于 AOSP 的定制开发带来的[好处，但鉴于 OnePlus 5/5T 背后已经有一个强大的开发社区，Treble 的好处在这一领域不会被感受到。相反，三重兼容性将使一加](https://www.xda-developers.com/how-project-treble-revolutionizes-custom-roms-android-oreo/)[更容易推出安全补丁更新](https://www.xda-developers.com/linux-kernel-long-term-support-google/)，以便像[最近承诺的那样](https://www.xda-developers.com/oneplus-software-maintenance-schedule/)更好地长期支持设备。我们必须等待，看看将 Project Treble 支持引入 OnePlus 5 和 OnePlus 5T 是否会为这些设备带来真正的好处，但我们相信它会有所帮助。

关于高音支撑已经说得够多了。最新的 OxygenOS Open Betas 带来的不仅仅是高音。以下是完整的变更日志:

## 适用于 OnePlus 5/OnePlus 5T 的 OxygenOS Open Beta 13/11

*   系统
    *   全新的用户界面
    *   支持的强调色(设置-显示-自定义)
    *   支持项目 Treble
*   发射者
    *   改进了应用抽屉中的搜索标签
    *   在应用抽屉中添加了“新安装”类别标签
    *   改进了隐藏空间和工具箱的应用列表
*   电话
    *   联系人页面的优化逻辑
*   天气
    *   全新设计，改善了用户体验
    *   所有预测都集成在一个界面下，带来完全沉浸式的体验

我们可以从变更日志中看到，一加仍在改善启动器体验，在应用程序抽屉中添加了搜索标签，一个“新安装”类别，以及一个改进的应用程序列表。天气应用程序和系统也有了新的外观。我们还不确定“全新的用户界面”是什么意思，因为更新还没有向用户推出。变更日志还提到了新的强调颜色，尽管还不清楚这是否意味着完全的强调颜色定制[，就像 OnePlus 6 上最新的](https://www.xda-developers.com/oneplus-6-android-p-beta-2-google-lens-face-unlock/) Android P beta 一样。

**更新:**我们可以确认最新的 beta 版带来了全强调色定制。至于“全新的用户界面”，我们确实注意到一些图标的变化，但我们没有看到太多的风格变化。这里有几张最新公测的截图。

一加警告用户在新的更新之前先刷新更早的 OxygenOS 开放测试版(OnePlus 5T 为 10，OnePlus 5 为 12)，以避免数据丢失。如果你没有这样做，并决定从系统的稳定版本更新，你必须事先做一个干净的闪存。这意味着从恢复中清除缓存和数据(始终建议使用 TWRP)。

你可以从这里的链接下载公测版本[。那些已经在公开测试版上的人将会收到 OTA 更新，而不必手动刷新 zip 文件。你也可以跳过这一行，通过使用氧气更新应用程序来获得更新，就像我们在这里的教程中提到的](https://downloads.oneplus.com/)。

一旦更新在服务器上可用，我们将更新文章的更多细节和截图。更多详情敬请关注。