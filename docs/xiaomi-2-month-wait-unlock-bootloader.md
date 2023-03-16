# 用户需要等待 2 个月才能解锁他们的小米引导程序

> 原文：<https://www.xda-developers.com/xiaomi-2-month-wait-unlock-bootloader/>

# 一些用户需要等待 2 个月才能解锁他们小米设备上的引导程序

一些用户看到解锁他们的小米设备的引导程序需要很长的等待时间——长达 2 个月的时间。不清楚这是否是故意的。

虽然解锁运行 MIUI 的小米手机的引导程序是可能的，但这不像谷歌 Pixel 2 或 OnePlus 6 这样的手机那么容易。除了 Android One 智能手机([米 A2](https://www.xda-developers.com/xiaomi-mi-a2-mi-a2-lite-kernel-source-code/) ，米 A2 Lite，米 A1)，你不能用开箱后的标准 fastboot 命令解锁小米设备的 bootloader。相反，你需要使用他们的 Mi 解锁工具。为了打击试图销售带有修改软件的设备的经销商，小米在引导加载程序解锁过程中增加了检查，其中包括在发出初始请求后的等待时间。最初，等待时间为 3 天，但今年早些时候，等待时间增加到 15 天。现在，一些用户看到等待时间长达 **2 个月**。

XDA 论坛[上的几个用户](https://forum.xda-developers.com/redmi-note-5-pro/help/1440hr-to-unlock-t3836157)、上的[、](https://www.reddit.com/r/Xiaomi/comments/9bmb60/1440_hours_to_unlock_redmi_note_5_bootloader/)[上的【Reddit】](https://www.reddit.com/r/Xiaomi/comments/9bnwip/xiaomi_in_a_nutshell/)和 MIUI 论坛上的[报告看到消息，告诉他们在最初的引导程序解锁请求后等待 2 个月。人们可以忍受 3 天甚至 15 天的等待时间，但在你能摆弄你的手机之前不得不等待 2 个月是令人不快的。考虑到 Poco](http://en.miui.com/thread-3701225-1-1.html) [宣布](https://www.xda-developers.com/xiaomi-poco-f1-developer-community/)他们将支持 Poco F1 上的开发社区，长时间的等待令人担忧。

![Xiaomi bootloader unlock](img/02baa846b564a3083826d66753d4e874.png) *一些用户看到的 2 个月等待期。这个特定用户拥有红米 Note 5 (vince)。*

我们希望这是一个错误，而不是有意的改变。小米手机是我们定制 rom 论坛上最受欢迎的设备之一。拥有一个解锁的引导加载程序允许您刷新未签名的引导映像，这样您就可以安装自定义恢复、修补引导映像以使用 Magisk 为设备安装根，以及安装自定义的基于 AOSP 的 rom。如果你还没有解锁你的小米设备的引导加载程序，并打算这样做，[一些用户报告](https://www.reddit.com/r/Xiaomi/comments/8mfgor/for_anyone_having_trouble_bypassing_the_360hr/)使用旧的小米解锁版本可能会缩短等待时间。我们已经联系了小米来澄清这一情况，当我们得到回复时，将更新您的信息。