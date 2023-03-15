# 使用 Flatline 为原始 Nexus 7 和其他华硕平板电脑生成 Nvflash Blobs

> 原文：<https://www.xda-developers.com/generate-nvflash-blobs-for-2012-nexus-7-and-other-asus-tablets-with-flatline/>

用于 Nvidia Tegra 驱动的华硕设备的 Blob 文件非常有用。这是因为它们允许我们以极低的级别使用 Nvflash 轻松地将映像闪存到我们的设备上。

鉴于 [APX (Nvflash)模式](http://forum.xda-developers.com/wiki/APX_mode)运行的级别较低，并且这比引导至标准 Android 恢复分区要原始得多，具有适当 blobs 的设备实际上是不可分的。因此，blob 文件可以用来让我们摆脱严重的棘手情况，否则不进行大的设备手术是无法恢复的。

自然，你会希望你的设备有适当的斑点，以防出现任何问题。多亏了 XDA 公认的开发者[雷曼](http://forum.xda-developers.com/member.php?u=962182)(以及 [AndroidRoot.mobi 团队](https://www.androidroot.mobi/pages/about-us/)的其他工作人员)，这现在在[(原版)谷歌 Nexus 7](http://forum.xda-developers.com/forumdisplay.php?f=1673) ，以及[华硕 Transformer Prime](http://forum.xda-developers.com/forumdisplay.php?f=1411) 、 [TF300T](http://forum.xda-developers.com/forumdisplay.php?f=1578) 和 [TF700](http://forum.xda-developers.com/forumdisplay.php?f=1661) 上成为可能。

Flatline 为上述设备创建了这些斑点。自定义恢复映像用于刷新自定义引导加载程序，以及生成适当的 blobs。该解决方案与其他 Nvflash 解决方案的独特之处在于，它不需要用于映像存储的工作*/数据*分区。相反，可以从 */tmp/AndroidRoot* 中检索 blobs，如下面链接的指南中所述。

你可以通过访问[原始线程](http://forum.xda-developers.com/showthread.php?t=2455927)来参与讨论。要在自己的设备上开始，请访问开发团队的[完整指南](https://www.androidroot.mobi/pages/guides/tegra3-guide-nvflash-jellybean/)，其中包含修改后的恢复映像和所有其他必需的文件。

感谢 OEM 关系经理 jerdog 的提示。]