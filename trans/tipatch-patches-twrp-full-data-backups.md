# Tipatch 修补 TWRP 以允许完整数据备份

> 原文：<https://www.xda-developers.com/tipatch-patches-twrp-full-data-backups/>

我们 XDA 社区的许多人使用最流行的定制恢复，TWRP。主要用来闪存，但也有人用来备份数据。当然，你可以备份你的应用程序数据，启动，系统等。但是，它有一个问题:默认情况下，您不能备份整个内部存储(/data/media)。因此，TWRP 的用户使用其他方法来备份他们的照片、视频等。这些方法很可能是亚行或 MTP。

有人可能会认为，包含整个内部存储是对所谓的完整备份的必要补充。XDA 资深成员 [kdrag0n](https://forum.xda-developers.com/member.php?u=7291478) 也这么认为，并做了一个名为 Tipatch 的有用应用，给 TWRP 打补丁，允许完整的数据备份，包括内部存储。您可能知道，TWRP 已经备份了没有/data/media 的数据分区，因此使用 Tipatch 您现在可以进行真正的完整备份。

请记住，使用 Tipatch 后，擦除/data 分区也会擦除您的内部存储，其中可能包含您的 TWRP 备份。此外，恢复备份可能会导致您正在处理的文档未完成或版本较旧。一些应用程序和游戏甚至将数据保存在内部存储器上，因此它们也可能是不完整的。但是，如果您无法摆脱 bootloop，并且希望轻松备份所有内容，它仍然是一个很好的工具。

更有趣的是，该应用程序可以在根设备和非根设备上运行。如果您是根用户并且已经安装了恢复，应用程序将一键为您修补恢复。但是，如果你没有 root，这个应用程序会修补 TWRP 的图像，你可以从官方网站下载。

开发者表示，该应用程序几乎适用于所有设备。他在所有可能的片上系统上测试了一些设备，包括骁龙、Exynos、麒麟和联发科。如果你对应用程序有任何问题，你可以在 XDA 论坛的帖子中报告错误并寻求帮助。你可以从 Google Play 和 XDA 实验室下载这个应用程序。这两个链接都在下面。

[appbox xda com.kdrag0n.tipatch]

* * *

[**在 XDA 论坛上下载 Tipatch**](https://forum.xda-developers.com/android/apps-games/app-twrp-tipatch-backup-internal-t3831217)