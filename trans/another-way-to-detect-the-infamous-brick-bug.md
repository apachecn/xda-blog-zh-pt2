# 另一种检测臭名昭著的砖块错误的方法

> 原文：<https://www.xda-developers.com/another-way-to-detect-the-infamous-brick-bug/>

我们一直在报道影响大量用户的[三星硬件故障](http://www.xda-developers.com/android/hard-brick-bug-on-galaxy-s-ii-and-note-leaked-ics-kernels/)。对于那些不熟悉的人来说，硬砖错误会对 eMMC 存储设备造成完全且不可修复的损坏。它发生在各种三星设备上的第一批 IC 泄漏被发布时，从那时起它们就一直是一个问题。

用户跟踪他们是否有 brick bug 的一种方式是 Chainfire 的 Got Brickbug 应用程序，它可以确定你的硬件是好是坏。如果你有[三星 Galaxy S II](http://forum.xda-developers.com/forumdisplay.php?f=1055) ，还有另一种方法来确定你是否有砖块错误。XDA 资深成员[钨文迪](http://forum.xda-developers.com/member.php?u=4322181)发布了一个脚本，帮助进一步确定用户是否有砖块错误。据 XDA 精英公认的开发者 [Entropy512](http://forum.xda-developers.com/member.php?u=591147) 称，它的功能与 Chainfire 的应用程序不同，他一直站在对抗 brick bug 的最前沿。Entropy512 声明:

> 它检测一个不同的组成部分的 brickbug - Chainfire 的检测坏芯片，这将检测一些内核，允许危险的命令通过印章。

然而，并非一切都好。由于它的检测方式，它很有可能会产生假阳性*和假阴性*。同样，Entropy512 解释道:

> 它可能会产生一些误报和漏报，因为它检查的是编译后的二进制文件，而不是源代码。例如，如果 MMC_CAP_ERASE 位置附近的任何内容发生变化，可能会导致误报。

因此，虽然它是一个非常有用的工具，但严格根据该应用程序的内容来宣布您的设备是安全还是危险是不明智的。考虑到它有传递假阳性和假阴性的能力，即使你有砖块错误，它也可能出现干净。它最好与 Chainfire 的应用程序(上面有链接)一起使用，以进行双重检查。如果在两次测试后你仍然不确定——这种危险的 bug 很可能是你应该有的——那么最好的办法就是假装你有砖块错误。安全总比后悔好。

钨文迪帖子的第二部分解释了如果你确实有这个问题，该如何解决。虽然这有工作的能力，Entropy512 再一次说出了至理名言:

> 如果补丁失败，可能会导致用户认为他们是安全的，而实际上他们并不安全。不是修补代码段以使内核安全，而是可能只是修补内核的某个其他部分，引入一个错误而不使内核安全。此外，由于修改将触发闪存计数器/修改检测机制，与从源代码构建内核相比，这样做没有太大意义。

所以，再一次，如果你决定尝试一下，一定要非常小心。测试和补丁都可能失败，如果发生这种情况，您可能会以失败告终。这不应该被误认为是不好的发展。这绝对是一个不错的开发，该脚本可以很好地用于帮助确定是否存在 brick bug。然而，使用最大限度的谨慎从来不是一个坏主意。目前，Entrop512 和其他公司正在与三星直接联系，以永久修复该问题。

更多信息，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=1807995)。

【图片摘自 egzthunder1 关于砖头虫的[奇幻文章](http://www.xda-developers.com/android/hard-brick-bug-on-galaxy-s-ii-and-note-leaked-ics-kernels/)。此外，非常感谢 Entropy512 的咨询。]