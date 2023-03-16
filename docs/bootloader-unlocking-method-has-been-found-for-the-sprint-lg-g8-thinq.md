# 发现了 Sprint LG G8 ThinQ 的引导加载程序解锁方法

> 原文：<https://www.xda-developers.com/bootloader-unlocking-method-has-been-found-for-the-sprint-lg-g8-thinq/>

# 发现了 Sprint LG G8 ThinQ 的引导加载程序解锁方法

您现在可以解锁 LG G8 ThinQ 的 Sprint 变种的引导加载程序，以安装自定义恢复，获得 root 访问权限并修改系统文件。请继续阅读！

LG G8 ThinQ [在 2019 年 12 月收到了稳定的 Android 10 更新](https://www.xda-developers.com/lg-starts-rolling-out-stable-android-10-update-g8-thinq/)。这款手机的 Sprint 版本(型号 **LM-G820UM0** )很快跟进，一个月后[也进行了同样的更新](https://forum.xda-developers.com/lg-g8/how-to/lg-g8-thinq-sprint-rolling-android-10-t4032753)。然而，韩国智能手机 OEM 并没有将这款设备列入[官方引导加载程序解锁](https://developer.lge.com/resource/mobile/RetrieveBootloader.dev)的白名单，因此用户无法在运营商品牌的 LG G8 ThinQ 上安装 LineageOS 等第三方定制 rom，甚至无法闪存[通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)。感谢 XDA 成员 BrandonB1218，j4nn，vlad48，Antintin，路易斯罗萨多和 Brigantti，现在有一个工作的引导加载器解锁方法为 Sprint LG G8 ThinQ。然而，这种方法并不像人们预期的那样简单。

**[LG G8 ThinQ 论坛](https://forum.xda-developers.com/lg-g8)**

该方法依赖于一个特权提升漏洞，XDA 认可的开发者 [j4nn](https://forum.xda-developers.com/member.php?u=4418980) 最近使用该漏洞让[在 LG V50 ThinQ](https://www.xda-developers.com/lg-v50-thinq-root-locked-bootloader-exploit/) 上获得临时 root 访问权限。将该漏洞移植到 LG G8 ThinQ 上是[相当琐碎的](https://forum.xda-developers.com/lg-g8/development/lg-g8-temp-root-exploit-via-cve-2020-t4100333)，因为这两款手机之间的内部相似性。下一步是利用 LG V50 ThinQ 泄露的工程引导程序，允许您解锁引导程序，而无需从 LG 的解锁服务器生成任何令牌。然后，通过用 Magisk 修补股票引导映像，您也可以获得永久的根访问权限。

如果你在你的设备上运行最新的 *20f* 版本的 Android 10 固件，你必须通过[切换到非活动插槽](https://forum.xda-developers.com/lg-g8/how-to/people-trying-beta-want-to-revert-t4011925)来降级到 [*20e* (或更低版本)](https://www.lg.com/us/support/help-library/lg-sprint-g8-g820um0-software-update-CT10000027-20151100901391)，因为根漏洞利用所使用的漏洞已经在更新的版本中得到修补。为了让事情变得简单，社区已经开发了一个包，其中包含执行降级所需的所有组件，一个备份低级引导加载程序相关分区的脚本，以及一个用于 LG G8 ThinQ 的 TWRP 版本。我们强烈建议您完全遵循下面链接的指南，因为对于没有经验的用户来说，篡改设备分区可能不会有好结果。

**[Sprint LG G8 ThinQ boot loader 解锁— XDA 下载讨论线程](https://forum.xda-developers.com/lg-g8/how-to/sprint-lg-g8-bootloader-unlocking-t4107801)**