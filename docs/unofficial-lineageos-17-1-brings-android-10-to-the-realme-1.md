# 非官方的 LineageOS 17.1 将 Android 10 带到了 Realme 1

> 原文：<https://www.xda-developers.com/unofficial-lineageos-17-1-brings-android-10-to-the-realme-1/>

# 非官方的 LineageOS 17.1 将 Android 10 带到了 Realme 1

基于 Android 10 的 LineageOS 17.1 的非官方版本现在可用于 Realme 1，这是由 XDA 高级成员无敌毒液提供的。

你们大多数人应该已经知道，Realme 品牌的根源在于 OPPO，而 OPPO 本身就是步步高电子的子公司。Realme 1 是该公司从 OPPO 剥离之前 Realme 品牌下的第一款智能手机，运行的是由 OPPO 自己设计的定制 Android 软件 ColorOS。为了将他们的设备与母公司区分开来，Realme 引入了一个名为“[Realme UI”](https://www.xda-developers.com/coloros-7-for-realme-phones-will-be-closer-to-stock-android/)的新界面，该界面建立在 Android 10 之上。然而，原始设备制造商[没有计划向 Realme 1 提供 Realme UI/Android 10 更新](https://www.xda-developers.com/realme-1-u1-c1-and-realme-2-will-not-be-updated-to-coloros-7-and-android-10/)，尽管这款手机仍然在其基于 Android 9 Pie 的 ColorOS 6 固件上获得定期安全更新。

**[Realme 1 XDA 论坛](https://forum.xda-developers.com/realme-1)**

然而，正如预期的那样，XDA 的售后市场开发社区已经前来救援。开发者[无敌毒液](https://forum.xda-developers.com/member.php?u=8592239)、 [Naveen56](https://forum.xda-developers.com/member.php?u=9791495) 、 [vishalk17](https://forum.xda-developers.com/member.php?u=7968806) 努力为 Realme 1 带来非官方的 LineageOS 17.1 端口，为这款手机的用户提供接近库存的 Android 10 体验。内核源代码的[可用性以及](https://www.xda-developers.com/realme-3-2-pro-1-u1-kernel-sources/)[官方引导加载程序解锁方法](https://www.xda-developers.com/realme-1-bootloader-unlocking/)的存在无疑帮助了开发者。除了一些奇怪的地方，比如 USB 连接中断和 SELinux 设置为许可(这是一个主要的安全问题，我们希望很快得到解决)，目前的版本可以用作日常驱动程序。

值得一提的是，LineageOS 的这个特殊版本是一个源代码构建的 ROM，而不是一个[通用系统映像](https://www.xda-developers.com/custom-project-treble-gsi-may-2020-security-patches-dc-dimming-oppo-devices/) (GSI)，尽管可以说现在许多定制的 ROM 都源自 GSI。Realme 1 的 **CPH1859** 和 **CPH1861** 变种都得到开发者的支持。你需要刷新最新版本的库存固件([*cph 1861 ex _ 11 _ c . 49*](https://download.c.realme.com/osupdate/CPH1861EX_11_OTA_0490_all_sWtP8RDIvyoU.ozip))并使用[TWRP 编译的同一个开发者](https://sourceforge.net/projects/realme1/files/twrp-9.0/)才能安装这个 ROM。Magisk 存在一些已知的不兼容问题，因此建议用户继续使用 Magisk 版本 20.1 或 20.3。

**非官方 line geos 17.1 for the Realme 1:[下载](https://sourceforge.net/projects/realme1/files/lineage-17.1/) ||| [XDA 讨论帖](https://forum.xda-developers.com/realme-1/development/rom-lineageos-17-1-t4107019)**

GitHub 上有相关的设备树和供应商树[。一个内置的 OTA 更新程序最初也是计划好的，但是](https://github.com/CPH1859)[开发者暂时放弃了它](https://github.com/CPH1859/OTA)。现在，LineageOS 17.1 的一个相对稳定的 Realme 1 版本已经发布，我们希望在不久的将来社区能够看到这一成果。