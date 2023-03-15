# 在大多数三星设备上，轻松将内部 SD 卡目录绑定到外部 SD 卡

> 原文：<https://www.xda-developers.com/easily-bind-internal-sd-card-directories-to-external-sd-card-on-most-samsung-devices/>

许多在手机上玩大量重度游戏的 Galaxy S II 和 III 用户已经耗尽了内部存储的游戏数据空间。虽然这两种设备都支持外部 SD 卡，但没有官方方法可用于存储。幸运的是，现在有一个简单的免费工具 DirectoryBind 来解决这个问题。

DirectoryBind 最初是由 XDA 论坛成员 [slig](http://forum.xda-developers.com/member.php?u=1212457) 为 SGS II 构建的，已经被许多人证实可以在 SGS III 和 Galaxy Tab 2 上工作，并且也可以在更多设备上工作，只要它们是根设备并且具有类似的分区结构。顾名思义，DirectoryBind 将设备上一个位置的目录绑定到另一个位置。虽然其背后的概念类似于符号链接，但它使用 bind 命令，这使得它可以跨文件系统工作。这一点尤其重要，因为外部 SD 卡上使用的文件系统通常是 FAT 或 FAT32，而内部文件系统是 Ext 3/4，这使得符号链接不可能。

该应用程序有一个不错的 GUI，可以轻松地创建新的目录对，管理现有的目录对，手动安装或卸载它们，选择在系统启动时自动安装它们，甚至可以设置它们在 USB 存储模式激活时自动卸载，在停用时重新安装。

可以下载 app，在[应用线程](http://forum.xda-developers.com/showthread.php?t=1410262)了解更多。