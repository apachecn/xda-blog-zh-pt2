# 如何下载索尼固件并创建 FTF 文件

> 原文：<https://www.xda-developers.com/how-to-download-sony-firmwares-and-create-ftf-files/>

Xperia 用户无疑熟悉 FTF 文件，这是一种用于 Xperia 设备上官方固件包的文件扩展名。我们在论坛上看到很多，但并不是每个人都确切知道它们是如何创建的。有些人可能因为好奇而想知道这个，或者只是想与社区分享某个版本。为了解决这个问题，XDA 的资深会员 Apollo89 创建了一个教程来指导你完成这个过程。

这是一个相当简单的程序，指南附有丰富的图片，分为四个不同的部分。每一部分都详细介绍了一个主要步骤，它们是:

1.  *更改您设备的定制号*:可选的初始步骤，这允许您通过对 build.prop 进行一些简单的更改来下载另一台 Xperia 设备的固件，因此需要 root 访问权限。
2.  *下载固件*:这个步骤需要一个锁定的 bootloader，Apollo89 详细介绍了两种情况，可能适用于你。情况 A 是有新的更新时，情况 B 是没有更新时。
3.  *创建实际的 FTF 文件*:然后需要 Flashtool 将固件文件转换成 FTF 文件。这可能是整个过程中最复杂的一步，但实际上仍然非常简单，因为只需要建立对工具的理解。
4.  *分享 FTF 文件*:这是结束本指南的一个很好的收尾步骤。这一步将提供一些提示，告诉你哪种文件托管服务适合你，以及 FTF 文件发布在 [XDA 论坛](http://forum.xda-developers.com/)时应该附带哪些信息。

所以现在你已经掌握了它的要点，如果你想了解更多，一定要访问[原始线程](http://forum.xda-developers.com/showthread.php?t=2334653)。