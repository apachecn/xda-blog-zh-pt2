# 如何修复某些 KitKat ROMs 中损坏的 ROM 闪存

> 原文：<https://www.xda-developers.com/how-to-fix-a-broken-rom-flash-in-certain-kitkat-roms/>

随着 Android 4.4 KitKat 的发布，谷歌改变了相当多的技术细节。其中一个包括在*更新程序脚本*中设置权限的完全不同的方法。听起来很棘手？不应该， 几个月前[我们写了更新脚本](http://www.xda-developers.com/android/learn-more-about-the-updater-script/)以及如何使用它的各种命令。

简而言之，之前使用的 *set_perms* 方法被弃用，取而代之的是 *set_metadata* 。 不幸的是，大多数可用的恢复不允许用户正确地刷新这些包，这导致了以下错误消息: *set_metadata_recursive:某些更改失败*

针对该错误的解决方案很快在 XDA 知名开发商 [Koush](http://forum.xda-developers.com/member.php?u=617884) 的 clock workmod recovery 和 XDA 资深知名开发商 [Dees_Troy](http://forum.xda-developers.com/member.php?u=912474) 的 TeamWin Recovery 项目中实施。但有时，即使是最新的恢复版本仍然无法刷新基于 KitKat 的 rom，从而产生前面提到的错误 。

XDA 资深会员 [daniel_hk](http://forum.xda-developers.com/member.php?u=4948627) 做了一些研究和 发现用 替换*更新二进制*补丁修复了闪烁程序，让大家现在可以享受这些以前难以安装的 Android 4.4 版本。他写了一个指南，一步一步地指导如何修复 update.zip 文件。这个过程非常简单，比替换你的*更新脚本*中的行要容易得多。

如果你在刷新 KitKat 版本时遇到了错误，去看看[原始线程](http://forum.xda-developers.com/showthread.php?t=2532300)并学习如何修复它们。