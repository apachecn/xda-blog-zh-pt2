# 借助 F2FS 加快老化的 Nexus 7 2012 存储速度

> 原文：<https://www.xda-developers.com/speed-up-your-aging-nexus-7-2012s-storage-with-f2fs/>

众所周知，尽管总体来说是一款很棒的设备，但谷歌 Nexus 7(2012)的闪存性能并不理想。虽然通过使用 TRIM ，这个问题已经[在一定程度上得到了缓解，但是文件系统性能仍然经常是设备的致命弱点。正因为如此，任何提高设备存储性能的措施都将极大地改善整体用户体验。](http://www.xda-developers.com/android/yet-another-reason-to-update-to-android-4-3-trim-support/ "Yet Another Reason to Update to Android 4.3: TRIM Support")

XDA 资深成员 [legolas93](http://forum.xda-developers.com/member.php?u=2743057) 决定通过使用 F2FS 来提高 Nexus 7 的存储性能，F2FS 是一种不同的文件系统，旨在更好地优化闪存设备中 NAND 内存的特性。但是在我们继续之前，重要的是要注意，当改变你的文件系统时，你*将*丢失你所有的数据。因此，请确保您进行了完整备份，然后在执行所需步骤时将备份传输到您的计算机。

首先，您必须下载支持 F2FS 的内核和一个修改过的 TWRP，它能够用 F2FS 重新格式化平板电脑。然后，您通过当前的自定义恢复来刷新内核，并通过快速启动来刷新 TWRP 的修改版本。接下来，您访问修改后的 TWRP 并格式化到新的文件系统。最后，您可以在将备份从 PC 复制回平板电脑后进行恢复。

更详细的说明和所有下载可以在[原始线程](http://forum.xda-developers.com/showthread.php?t=2664392)中找到。如果你是一个 SlimKat 用户，你可能想试试[这个版本](http://forum.xda-developers.com/showthread.php?t=2678142)修改后完全兼容 F2FS。