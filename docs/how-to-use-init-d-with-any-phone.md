# 如何在任何电话上使用 Init.d

> 原文：<https://www.xda-developers.com/how-to-use-init-d-with-any-phone/>

*Init.d* 在 Android 中有着特殊的地位。有了它，用户可以安装在开机时运行的脚本和模块，从而修改他们想要的手机的几乎任何方面。有电池的调整，性能的调整，全球定位系统的调整，信号的调整，还有很多其他的调整。然而，要让这些脚本工作，手机必须首先有 *init.d* 支持。通常情况下，Ramdisk 提供 *init.d* 支持，但有时也有可能在不刷新新 Ramdisk，甚至根本不改变 Ramdisk 的情况下获得 *init.d* 支持。

这是 XDA 认可的开发者为许多设备开发的东西。smokin1337 通过一个名为 EZ InitD 的 mod 来帮助用户轻松添加 *init.d* 支持。另外，开发者给出了几个如何使用 mod 的选项。一个版本是供用户通过自定义恢复来闪存，而另一个版本是供 ROM 开发者包含在他们的 ROM 中。最棒的是，这很简单。

在应用了 mod 之后，你的 *init.d* 文件夹中的任何东西都将在引导时运行，就像它通常会做的那样。在 ROM 开发版本中，开发人员实际上可以将目录更改为他们想要的任何内容。换句话说，可以有支持 *init.d* 的 rom，但是没有真正的 *init.d* 文件夹。(艾德:我自己在考虑 */etc/NyanCat* 或者 */etc/bacolicious，*。)该方法已经在 [HTC One S](http://forum.xda-developers.com/forumdisplay.php?f=1528) 和 [HTC One X](http://forum.xda-developers.com/forumdisplay.php?f=1538) 上进行了测试，但实际上应该可以在任何设备上工作。正如许多用户会告诉你的，init.d 支持来自 Ramdisk。这不一定是真的。根据 smokin1337:

> 这个 mod 将增加 init.d 对任何 rom 的支持，甚至不需要编辑内存。相反，它使用 post_boot.sh 文件，该文件存在于大多数(如果不是所有)rom 中。它应该可以在大多数设备上工作，如果它不能在你的设备上工作，请在/system/etc 中查找并发布包含“post_boot.sh”的文件名。

因此，给定这个方法，实际上可以在不切换、编辑或以其他方式接触 Ramdisk 或内核的情况下获得 init.d 支持。欲了解更多信息，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=1710980)。