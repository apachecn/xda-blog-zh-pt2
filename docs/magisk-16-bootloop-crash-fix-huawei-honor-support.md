# Magisk v16.0 发布，具有 Bootloop 崩溃修复、华为/Honor 高音支持等功能

> 原文：<https://www.xda-developers.com/magisk-16-bootloop-crash-fix-huawei-honor-support/>

本月早些时候，XDA 知名开发者和贡献者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 向公众发布了[Magisk 15.4 版本。该更新包括 MagiskBoot 改进、用于更好地隐藏 Magisk 的套接字混淆以及对 Magisk 管理器的一些优化。今天，流行的无系统根工具又发布了另一个版本，这次是 16.0 版本，这次重大更新增加了对运行 Android Oreo 的华为和 Honor 设备的支持，修复了一些之前报告的 bootloop 问题，等等。](https://www.xda-developers.com/magisk-v15-4-magiskboot-socket-obfuscation-magisk-manager/)

对于很多人来说，Magisk 最新版本的最大变化是增加了对运行 Android Oreo 的华为和 Honor 设备的支持。上周早些时候，我们告诉你, [topjohnwu 能够让 Magisk 在 Pixel XL 之外的第一个高音设备](https://www.xda-developers.com/magisk-honor-view-10-huawei-mate-10-pro/)上运行。这个成绩是在 Honor View 10 上取得的，也让 Magisk 可以在华为 Mate 10 系列上工作。

版本 16 中的另一个重大变化是，导致引导循环的 NDK 编译器错误已被修复。以前，一些安装 Magisk 15.4 版本的人遇到了引导循环，但这个问题在 16 版本中已经解决了。

topjohnwu 还宣布，他为 root 应用程序开发人员提供的 Android 库 libsu 已经完全记录在案，并准备好进行适当的发布。该库旨在整个应用程序中轻松共享一个交互式根 shell。对于那些感兴趣的人来说，Android 库的教程、示例代码和完整的 Javadoc 现在都可以在这里获得。

[**从 XDA 论坛**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/post75648916#post75648916) 下载 Magisk v16

最后一点信息对社区来说非常重要，是对 topjohnwu 个人有影响的东西。他宣布，由于他即将于 2 月 22 日开始的强制兵役，他将在接下来的 4 个月内基本上无法参加比赛。在接下来的 4 个月里，他将完全脱离互联网。因此，提交速度会变慢，但 topjohnwu 希望他到目前为止所做的大量工作会让社区满意。我们个人祝愿吴振伟一切顺利，社会也一定会怀念他！