# 轻松备份三星 Galaxy Note 3 上的 EFS 分区

> 原文：<https://www.xda-developers.com/easily-backup-the-efs-partition-on-the-samsung-galaxy-note-3/>

任何拥有三星设备的人无疑都知道 EFS 分区的重要性。该分区控制许多重要的无线电功能，并且当被破坏时，会导致各种问题，例如可能失去网络连接。因此，备份 EFS 分区非常重要，以防将来闪存出现任何问题。

为了让备份过程变得简单一点，XDA 高级成员 [A.S._id](http://forum.xda-developers.com/member.php?u=2976903) 创建了一个 Windows 批处理文件，让用户可以选择备份 EFS 分区，以及运行 Odin、DD 和 Tar.GZ 恢复。伴随批处理的是脚本所需的所有二进制文件，包括 Odin3、adb、tar 和 Cygwin DLLs。

该实用程序目前官方仅支持 Note 3 的 N900 和 N9005 版本。然而，用户报告称，N9005 版本[在中国 N9008](http://forum.xda-developers.com/showpost.php?p=46063408&postcount=11) 型号上运行良好，T-Mobile N900T [在 T4](http://forum.xda-developers.com/showpost.php?p=46246255&postcount=25)也运行良好，尽管我们假设这是 N900 版本的实用程序。无论如何，即使你的设备还不被支持，尝试运行备份也不会有什么坏处。但是，我们不建议在不支持的设备上运行恢复功能，直到该实用程序更新为支持您的型号。

转到[实用线程](http://forum.xda-developers.com/showthread.php?t=2447342)开始。