# 为您的设备编译 TWRP

> 原文：<https://www.xda-developers.com/compile-twrp-for-your-device/>

我们过去已经谈了很多关于[团队胜利恢复项目](http://www.xda-developers.com/tag/twrp/)的内容。毕竟，拥有一个图形和用户友好界面的漂亮的基于触摸的恢复使根和修改过程更容易，更不容易出错。自从 TWRP2 [问世](http://www.xda-developers.com/android/team-win-recovery-project-updated-to-2-1/)以来，它已经提供了一些最好的功能，无疑是定制恢复选择海洋中最友好的用户界面。

如果你想使用 TWRP，但你的设备没有官方版本，你该怎么办？感谢 XDA 认可的开发人员(和 Team Win 首席开发人员) [Dees_Troy](http://forum.xda-developers.com/member.php?u=912474) ，现在有了一个官方的移植指南。

该指南指导用户完成制作过程，以及 *BoardConfig.mk* 文件中所有参数的含义以及如何调整它们。创建映像后，它将向您展示如何通过在模拟器中引导映像来确保它正常工作，从而保护您的设备免受潜在的损坏。

我不打算对你撒谎；虽然这并不太复杂，但为你自己的设备构建 TWRP 的过程并不简单。换句话说，在坐下来开始之前，你肯定想喝杯咖啡。然而，那些付出努力的人将会得到回报，拥有一个可以工作的 TWRP。

为了开始恢复建筑的乐趣，前往[引导线程](http://forum.xda-developers.com/showthread.php?t=1943625)。在开始之前，一定要喝几杯咖啡。