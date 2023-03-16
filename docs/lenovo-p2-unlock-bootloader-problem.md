# 许多联想 P2 用户无法解锁引导程序，联想正在调查

> 原文：<https://www.xda-developers.com/lenovo-p2-unlock-bootloader-problem/>

联想 P2 于 2016 年底推出。它采用了 5.5 英寸的 FHD 屏幕和节能的高通骁龙 625，但最吸引人的是它巨大的 5100 毫安时电池，这在今天有点罕见。它与 Android 6.0 棉花糖一起推出，并正式更新到 Android 7.0 牛轧糖，但该设备不太可能收到 Android 奥利奥。对于目前想要摆脱联想软件的设备所有者来说，P2 有一个可以刷新的[官方 line geos 14.1 ROM](https://forum.xda-developers.com/lenovo-p2/development/rom-lineageos-14-1-p2-t3766140)。然而，有一个重大问题困扰了许多联想 P2 用户一年左右:无法解锁引导程序。

解锁引导加载程序是刷新自定义 ROM 所必需的，因为如果您想要刷新自定义引导映像，例如 LineageOS 等任何基于 AOSP 的 ROM 附带的映像，您需要禁用引导加载程序的引导签名验证。通常，该过程包括在开发人员选项中启用“OEM 解锁”，然后在引导加载程序中运行“fastboot oem 解锁”命令(有或没有解锁代码，取决于设备)。

对于联想 P2，当您尝试启用 OEM 解锁时，您必须首先接受一些条款，声明您将通过解锁引导程序来取消保修。如果你接受这些条款，你就可以用你的联想帐户登录，然后你必须等待 14 天，联想的服务器才会注册你的设备，这样你才能解锁引导程序。然而，正如在[官方联想 P2 论坛](https://forums.lenovo.com/t5/P2-P2a42-Smartphones/Lenovo-p2-unlocking-bootloader/td-p/3642399)上的许多人所发现的，他们无法注册启动加载器解锁等待期，因为有一个错误说他们的联想 ID 电子邮件地址尚未得到验证(尽管它已经得到验证)。)

 <picture>![Lenovo P2 Bootloader Unlock](img/1a7e87fad279ca34b4cfa2a8a300bbc2.png)</picture> 

Lenovo P2 Bootloader Unlock Error. Credits: [phanigondi95](https://forums.lenovo.com/t5/user/viewprofilepage/user-id/1271172)

经过近一年的投诉，公司似乎终于开始调查这个问题了。上周，一位“资深 MotoAgent”在论坛上发布了一条[评论](https://forums.lenovo.com/t5/P2-P2a42-Smartphones/Lenovo-p2-unlocking-bootloader/m-p/4043322/highlight/true#M10444)，称该公司正在调查此事。自从那次评论后，没有关于这个问题的更新被发布，所以我们将不得不等待，看看发生了什么。我们当然希望联想不是故意阻止引导程序解锁，以防止用户刷新定制的 rom。如果这是故意的，也许是为了防止用户禁用某些预装的应用程序(顺便说一下，这可以在没有 root 用户的情况下[很容易做到](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)，那么这对他们来说将是一个愚蠢的举动。

鉴于错误消息，这可能只是他们系统的一个小故障，尽管我不得不说，迫使用户等待 14 天只是为了他们的服务器将设备列入白名单真的没有必要。小米等其他公司实施强制等待期，除了惹恼用户，它什么也没做。我们希望联想能尽快解决这个问题。

[**Via/u/98432 uhefbdfir**](https://www.reddit.com/r/LineageOS/comments/8dw1uv/lenovo_banned_bootloader_unlocking_after/)