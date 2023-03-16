# 小米 Redmi Note 7 获得非官方 Ubuntu Touch 端口

> 原文：<https://www.xda-developers.com/developer-ports-ubuntu-touch-to-the-xiaomi-redmi-note-7/>

曾经有一段时间，你可以在神话般的 HTC HD2 上安装任何操作系统，无论是 [Android](https://forum.xda-developers.com/showpost.php?p=68623703) 、 [Ubuntu](https://forum.xda-developers.com/showthread.php?t=889433) ，甚至是 [Windows RT](https://www.xda-developers.com/htc-hd2-refuses-to-die-now-runs-windows-rt/) 。三星 Galaxy S III 和 Galaxy Note II 正在逐渐继承这一衣钵，因为只需很小的努力就可以在它们上面安装常规的 GNU/Linux 发行版。虽然你可以通过购买 [Librem 5](https://www.xda-developers.com/purism-kde-crowdsource-free-smartphone/) 或 [PinePhone](https://www.pine64.org/pinephone/) 来满足拥有一部“真正的 Linux 手机”的渴望，但不幸的是，它们的硬件配置已经过时了。几个社区驱动的项目，如 [UBports](https://www.xda-developers.com/ubuntu-to-show-off-community-ports-on-oneplus-one-sony-xperia-z1-at-mwc-2016/) 和 [postmarketOS](https://www.xda-developers.com/postmarketos-touch-optimized-linux-distro/) ，正在试图弥合普通消费者 Android 设备和主流 Linux 发行版之间的差距，而 [Project Halium](https://www.xda-developers.com/halium-is-an-open-source-project-working-towards-a-common-base-for-non-android-mobile-operating-systems/) 在这一开发场景中扮演着巨大的角色。现在，XDA 公认的开发者 [erfanoabdi](https://forum.xda-developers.com/member.php?u=6298645) 决定涉足这一特定领域，因为他已经将 Ubuntu Touch 移植到小米 Redmi Note 7 上。

**[小米红米 Note 7 XDA 论坛](https://forum.xda-developers.com/redmi-note-7)**

erfanoabdi 是 Android modding 社区中一个著名的名字，他因在[通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI) [端口](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/pie-erfan-gsi-ports-t3906486)以及为各种摩托罗拉手机维护[线路地理](https://www.xda-developers.com/tag/lineageos/)方面的工作而闻名。据开发者称，Halium 开发者 [NotKit](https://github.com/NotKit) 为 [F(x)tec Pro1](https://www.xda-developers.com/fxtec-pro1-slider-phone-physical-keyboard/) 提供的 Ubuntu Touch 现有端口帮助他开始了“黑客”工作。[之前将](https://github.com/Danct12) [Ubuntu Touch 移植到小米 Redmi 4X](https://forums.ubports.com/topic/3682/xiaomi-redmi-4x-santoni) 上的 Danct12 ，负责创建 erfanoabdi 在这次旅程中使用的初步设备树。Danct12 还发布了一个预告图，显示 Ubuntu Touch 将在 Redmi Note 7 上启动。

erfanoabdi 已经上传了[预建的图像](https://build.lolinet.com/file/halium/lavender/)，但是此时此刻该端口只不过是一个概念证明。触摸和硬件合成器(带加速功能的显示器)正在工作，你甚至可以利用 Wi-Fi，但仅此而已。如果你想咬紧牙关，那么你必须先从前面提到的镜像中闪存 [erfanoabdi 为红米 Note 7](https://build.lolinet.com/file/lineage/lavender/lineage-16.0-20200226-UNOFFICIAL-lavender.zip) 自编译的 LineageOS 16.0 build 来填充供应商分区，然后是预编译的 system.img、dtbo.img 和 hallium-boot.img。之后，你必须使用 [Halium 安装脚本](https://gitlab.com/JBBgameich/halium-install)安装。如果一切顺利，在这个阶段，您应该能够 SSH 到您的手机。然而，设置适当的挂载点和启动 LightDM(即图形显示管理器)仍然需要一些 shell 命令。

由于引入了[项目 Treble](https://forum.xda-developers.com/project-treble) ，这是对 Android 的一次重大重组，旨在将 Android 框架代码从硬件供应商实现中分离出来，Halium 开发人员不得不重写 *libhybris* 的主要部分(一个重用现有 Android 驱动程序的兼容层)。尽管如此，正如 erfanoabdi 所暗示的，这种重塑可能有助于在不久的将来将 Ubuntu Touch 发行版转变为 GSI。

* * *

**来源:推特( [1](https://twitter.com/RealDanct12/status/1239745207660212225) ， [2](https://twitter.com/Khode_Erfan/status/1239911295496998914) )**