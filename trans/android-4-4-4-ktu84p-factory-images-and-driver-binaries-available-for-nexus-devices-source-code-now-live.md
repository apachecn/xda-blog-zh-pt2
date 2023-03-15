# Android 4.4.4 KTU84P 工厂映像和驱动程序二进制文件可用于 Nexus 设备，源代码现已发布

> 原文：<https://www.xda-developers.com/android-4-4-4-ktu84p-factory-images-and-driver-binaries-available-for-nexus-devices-source-code-now-live/>

嗯，这是意想不到的！在几十次导致 Android 4.4.3 最终发布的泄露之后，Android 4.4.4 突然到来了，甚至没有一点通知。更新本身尚未开始推广到实际的最终用户设备，但就像我们在 4.4.3 KTU84M 中看到的那样，大多数当前一代 Nexus 设备的工厂图像已经发布。

今天的 Android 4.4.4 版本以 KTU84P 的形式发布，用于 [Nexus 5](http://forum.xda-developers.com/google-nexus-5) 、 [Nexus 4](http://forum.xda-developers.com/nexus-4) 、 [Nexus 7](http://forum.xda-developers.com/nexus-7) 、 [Nexus 7 (2013)](http://forum.xda-developers.com/nexus-7-2013) 和 [Nexus 10](http://forum.xda-developers.com/nexus-10) 。不幸的是，就像 4.4.3 KTU84M 一样，Nexus 7 (2013)支持 LTE 的版本目前还不可用。根据今天早些时候发布的 Sprint 更新支持文档,这次更新只带来了一个未指明的“安全补丁”~~目前还不知道这个版本是否修复了被 tower root 中的 geohot[利用的 Linux 内核 CVE-2014-3153 漏洞，但如果是这样的话，也不会太令人惊讶。](http://www.xda-developers.com/android/breaking-geohot-roots-the-verizon-galaxy-s5-with-towelroot/)~~显然，早期的合并杀死 Dalvik 并实现 ART 作为缺省运行时编译器还没有发布。

您可以通过 [Nexus Factory Images 页面](https://developers.google.com/android/nexus/images)直接更新您的设备来获得修复。如果构建定制的 rom 是你的事情，抓取 [KitKat MR2.1 源代码](https://android.googlesource.com/platform/build/+/kitkat-mr2.1-release)，然后前往 [Nexus 驱动程序二进制页面开始](https://developers.google.com/android/nexus/drivers)。

**更新:**正如 XDA 资深成员 [phaseL](http://forum.xda-developers.com/member.php?u=3244138) 所指出的，这确实没有实现对 [geohot 的 tower root](http://www.xda-developers.com/android/breaking-geohot-roots-the-verizon-galaxy-s5-with-towelroot/)中利用的 Linux 内核 CVE-2014-3153 漏洞的修复，因为内核构建日期(3 月 13 日)远在补丁可用之前(6 月 3 日)。

*【非常感谢 XDA 论坛版主 [laufersteppenwolf](http://forum.xda-developers.com/member.php?u=4716493) 、公认开发者 [iurnait](http://forum.xda-developers.com/member.php?u=4699427) 以及资深会员 [bilal_liberty](http://forum.xda-developers.com/member.php?u=4817003) 的提醒！]*