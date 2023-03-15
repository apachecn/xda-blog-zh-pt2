# LG G Pro Lite:不安全的启动映像和 CWM 恢复

> 原文：<https://www.xda-developers.com/lg-g-pro-lite-unsecured-boot-image-and-cwm-recovery/>

# LG G Pro Lite 不安全引导映像和 CWM 恢复

不安全的引导映像和恢复是定制 ROM/内核开发的第一步。这两种功能现在都可以在带有锁定引导加载程序的 D680 上实现！

LG G Pro Lite D680 是一款经济型手机，于 2013 年与 LG 2013 年旗舰设备 [LG Optimus G Pro](http://forum.xda-developers.com/optimus-g-pro) 一起发布。

不幸的是，到目前为止它还没有得到太多的开发关注…但是 XDA 认可的开发者 [laufersteppenwolf](http://forum.xda-developers.com/member.php?u=4716493) 现在已经发布了一个不安全的 boot.img 和一个 CWM 恢复。这是尽管引导加载程序被锁定(这意味着你没有必要让你的保修无效！)，标志着向设备定制 ROM 和内核开发迈出了第一步。

一个不安全的 boot.img 允许你以 root 用户身份运行 ADB，能够在早期启动时使用 ADB 等等，这在开发获取日志、一般调试和快速修改系统文件时非常方便。

CWM 恢复安装在它自己的分区中，而不是引导，尽管有一个小错误，它仍然是可用的:

*   内部 SD 还不能安装。也就是说，你可以使用外部 SD 卡或第二个分区(sd-ext，通常用于保持应用程序运行)来代替。

感兴趣吗？所有你需要的是一个运行 V10 固件的根设备，ADB 设置并准备在你的计算机上使用，以及一些耐心。前往 V10 论坛线程的 [unsecured boot.img 和锁定 JB bootloader 论坛线程](http://forum.xda-developers.com/optimus-g-pro/d680-development/boot-t3043513)的[CWM recovery 5.5.0.4 开始。](http://forum.xda-developers.com/optimus-g-pro/d680-development/recovery-cwm-recovery-5-5-0-4-locked-jb-t3043659)