# 移动 ODIN 更新到版本 4，新功能和设备

> 原文：<https://www.xda-developers.com/mobile-odin-updated-to-version-4-new-features-and-devices/>

两年多前，我们第一次报道了 XDA 资深知名开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 的移动 ODIN 应用[。从一开始，移动 ODIN 就允许用户直接从设备上刷新 ODIN-flash 固件，而不需要连接到一台完整的计算机。](http://www.xda-developers.com/android/mobile-odin-lets-you-flash-firmware-from-device/ "Mobile ODIN Lets You Flash Firmware from Device")

在应用程序的各种更新过程中，移动 ODIN 已经发生了很大的变化——既增加了对新设备的支持，也增加了对 T2 的新能力。现在，随着版本 4 的更新，该应用程序获得了更多的功能，以及与更多设备的兼容性。

第 4 版最显著的新特性与它刷新调制解调器映像的能力有关。由于这些分区受到保护，某些设备上的闪存可能会不稳定。为了防止这种情况，添加了新代码来检测保护，如果启用，则跳过刷新受影响的分区。也就是说，仍然有可能通过移动 ODIN 来刷新完整的固件和调制解调器。现在，它采取了一种更安全的方法，检查可能导致问题的保护措施。

另一个版本 4 独有的新功能是它能够在移动 ODIN 闪存后自动重启手机进入下载模式。如果您希望刷新 bootloaders、trustzone 和其他未通过 Mobile ODIN 刷新的分区，这将非常有用。借助 EverRoot，您可以在保存 root 的同时刷新 Android 更新，自动引导下载，并刷新跳过的特定分区。

SuperSU 的内置版本更新到了 1.89，该版本旨在支持最新的三星 Android 4.4 固件。最后，这次更新带来了对各种版本的 [Galaxy S 4](forum.xda-developers.com/galaxy-s4) 和 [Galaxy Note 3](http://forum.xda-developers.com/galaxy-note-3) 的支持。

前往 [手机奥丁线程](http://forum.xda-developers.com/showthread.php?t=1347899) 和 [Chainfire 的 Google+公告](https://plus.google.com/+Chainfire/posts/MPmRtxjxGgf)开始使用。