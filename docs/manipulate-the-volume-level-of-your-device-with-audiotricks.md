# 使用音轨控制设备的音量

> 原文：<https://www.xda-developers.com/manipulate-the-volume-level-of-your-device-with-audiotricks/>

Android 有一个方面肯定需要改进，那就是麦克风。不幸的是，音频管理几乎不存在，这在像 Android 这样成熟和流行的操作系统中是不应该存在的。但是尽管这已经被谷歌遗忘了，ti 还没有被 XDA 的论坛成员遗忘。

如果你曾经在 Android 中寻找改变麦克风设置的方法，我们有一个好消息给你。XDA 公认的开发者[Mike reidis](http://forum.xda-developers.com/member.php?u=3575078)([Spirit FM](http://forum.xda-developers.com/showthread.php?t=1059296)的创造者)开发了一个应用程序，允许你修改 Android 中一些隐藏的音频偏好。应用程序使用基于填补的技术拦截对原始 HAL 的调用。修改完成后，用户可以改变麦克风的音量。mod 还允许你调整输出的音量。

该解决方案可能不限于使用 HAL 垫片。可以使用 ALSA(常见于 Linux)，它有几十个配置选项。该应用程序仍处于非常早期的阶段，在适当的时候肯定会变得更加成熟。目前，它只能在运行 AOSP 衍生的 KitKat 和 root 的设备上运行，但开发者承诺在漏洞被清除后会降低要求。

您可以通过访问[应用程序线程](http://forum.xda-developers.com/showthread.php?t=2756320)来试验您设备的音频。