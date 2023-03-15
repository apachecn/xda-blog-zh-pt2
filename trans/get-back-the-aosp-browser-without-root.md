# 拿回没有 Root 的 AOSP 浏览器

> 原文：<https://www.xda-developers.com/get-back-the-aosp-browser-without-root/>

如果你碰巧拥有从 Galaxy Nexus 开始的任何 Nexus 设备，你肯定会注意到值得信赖的旧 AOSP 浏览器的消失。虽然许多人对 Android 版 Chrome 感到满意，但其他人对替代浏览器相对较差的滚动性能和缺乏 Flash 支持感到不满。这通常没什么大不了的，因为在任何定制恢复中，找回 AOSP 浏览器只是一个 *update.zip* flash away。

如果你没有根，你会怎么做？以前，这意味着接受失败并安装另一个支持 Flash 的替代浏览器。然而，多亏了 XDA 论坛成员 [blackhand1001](http://forum.xda-developers.com/member.php?u=4244043) ，现在可以在没有 Root 权限的情况下找回 AOSP 浏览器了。更重要的是，他还带回了书签同步功能，以便让你与桌面上的 Chrome 共享书签。

开始非常容易。首先，导航到*/系统/应用*并安装 *browserproviderproxy.apk* 并重启。别担心，那部分看起来不会起作用，但它起作用了。不，你不需要 root 权限就可以简单地从*/系统/应用*中*查看*和*执行*。您所需要的只是一个能够对该目录进行只读访问的文件管理器，比如 [EStrongs](https://play.google.com/store/apps/details?id=com.estrongs.android.pop&hl=en) 和许多其他文件管理器。然后重新启动后，安装浏览器和(可选)书签同步应用程序。完成后，您将能够轻松浏览所有支持 Flash 的站点。

转到[原始线程](http://forum.xda-developers.com/showthread.php?t=2385933)开始。如果你这么做是为了在你的移动设备上安装 Flash，别忘了访问 [Adobe Flash Player 档案馆](http://helpx.adobe.com/flash-player/kb/archived-flash-player-versions.html)并下载最新版本。