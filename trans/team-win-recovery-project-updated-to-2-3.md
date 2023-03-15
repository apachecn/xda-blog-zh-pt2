# 团队胜利恢复项目更新至 2.3

> 原文：<https://www.xda-developers.com/team-win-recovery-project-updated-to-2-3/>

上一次我们带给你关于 TWRP 的消息，是宣布 [TWRP 2.2.2 已经发布](http://www.xda-developers.com/android/twrp-2-2-2-update-brings-several-improvements-and-bug-fixes/)。它修复了最初[发布的 TWRP 2.2](http://www.xda-developers.com/android/team-win-recovery-project-updated-to-2-2/) 中的许多错误，并增加了一些新功能。最近，TWRP 又被更新到 2.3 版本。

TWRP 2.2 有一大堆令人敬畏的改进，也有许多独特和全新的功能。TWRP 2.3 承诺不会更少。官方变更日志包括:

> 重新基于 AOSP 果冻豆源代码
> 
> 用 C++类重写了备份、恢复、擦除和挂载代码，以便将来更容易维护
> 
> 注意:TWRP 早期版本的备份仍然与 2.3 兼容
> 
> AOSP 的 ADB 侧载功能包含在 2.3 中，更多信息请参见此链接
> 
> 完全用 C++重写了修复权限，运行时间从几分钟缩短到几秒钟(感谢 bigbiff)
> 
> OpenRecoveryScript 中 zip 查找的改进(应该会减少很多 GooManager 自动化问题)
> 
> 更快的启动时间
> 
> 增加了恢复中的充电指示灯(每 60 秒更新一次)

此外，XDA 知名开发商 [Dees_Troy](http://forum.xda-developers.com/member.php?u=912474) 报告称，现在支持在备份名称中使用空格。以前，如果您在备份名称中添加空格，它将不会恢复。现在用户可以使用他们想要的任何命名约定。

不过，最大的变化之一是所有的 TWRP 都用 C++重写，并转移到恢复 API 3 而不是 API 2。随着代码重写，它将允许 TWRP 更新更快，更稳定。随着 API 3 的变化，这意味着一些可闪存的 zip 文件可能会停止工作，因为开发人员需要更新更新二进制文件。如果你不想等待开发商，或者开发商已经停止了该项目的工作，你可以在 [TWRP 的官方网站](http://teamw.in/project/twrp2)上找到一个来使用。要安装最新的 TWRP，可以使用[的 Goomanager 应用](http://www.xda-developers.com/android/easily-obtain-and-distribute-your-goo-ds-with-goomanager-beta/)。只需打开应用程序，点击菜单，并安装开放恢复。

如果您想为您的设备检查最新的 TWRP 恢复，请检查下面的链接之一。