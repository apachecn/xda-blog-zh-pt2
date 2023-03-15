# 使用 GOptimize 快速优化 APK 和 Classes.dex

> 原文：<https://www.xda-developers.com/quickly-optimize-apk-and-classes-dex-with-goptimize/>

如果您试图通过降低 I/O 时间来最小化加载时间，那么优化应用程序的资源可能是值得考虑的。自然，加载较小的 apk 会减少读取应用程序数据所花费的时间。对于任何形式的压缩数据，在更高级别的压缩中，最终都会在计算时间和读取时间之间进行权衡，但在大多数情况下，应用程序负载和一般设备性能似乎受 I/O 而非计算性能的限制。

为此，XDA 资深会员 [gu5t3r](http://forum.xda-developers.com/member.php?u=4665716) 创建了一个简单的 BASH 脚本来帮助你快速优化你的应用。它主要通过更有效地压缩你的 png 文件来工作。然而，它跳过了讨厌的 [NinePatch](http://www.xda-developers.com/android/tutorial-helps-users-understand-ninepatch-pngs-better/ "Tutorial Helps Users Understand NinePatch PNGs Better") 文件，以防止潜在的强制关闭。对于 PNG 压缩，该工具使用 TruePNG、pngout 和 DeflOpt 的组合，gu5t3r 声称，与更标准的 OptiPNG 压缩相比，它将导致存储空间净减半。

该脚本以基于 Cygwin 的 BASH 脚本的形式出现，并附带了您需要的所有可执行文件，以便轻松入门。该主题中的用户报告了文件大小的显著减小，而功能没有损失。它会对性能产生任何实际的显著影响吗？这取决于许多变量，如设备的 I/O 速度、CPU 能力和应用程序大小。也就是说，试试也无妨。

前往 [实用线程](http://forum.xda-developers.com/showthread.php?t=2358261) 参与其中。

*【感谢资深会员 [ct_moi](http://forum.xda-developers.com/member.php?u=303041) 的提示！]*