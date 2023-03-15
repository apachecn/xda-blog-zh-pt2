# TWRP 2.8 带来了 MTP 本地支持和更多！

> 原文：<https://www.xda-developers.com/team-win-recovery-project-2-8-brings-native-mtp-support-and-more/>

# 团队胜利恢复项目 2.8 带来了本地 MTP 支持和更多！

TWRP 获得了 2.8 版本的巨大更新，开发人员准备了许多新功能，并增加了对新分辨率的支持。

团队胜利恢复项目，简称为 TWRP，是最受欢迎的安卓定制恢复项目之一。它有一个很好的布局，在它的易于使用的用户界面上有大量的功能，它让我们能够潜入自定义的 ROM 世界。这种恢复适用于大多数流行的设备——无论它们是大还是小。开发了大部分功能的 XDA 高级认证开发者 [Dees_Troy](http://forum.xda-developers.com/member.php?u=912474) 和 XDA 认证开发者 [bigbiff](http://forum.xda-developers.com/member.php?u=2638973) 已经更新了恢复版，将其版本提升到 2.8。这是一个重要的版本，所以变化是巨大的。

最新的 TWRP 有什么新内容？UI 布局没有改变，但恢复获得了相当多的新功能，你们中的许多人肯定会喜欢。可能最重要的一个是基于 C++的 MTP 实现，它允许将文件传输到 microSD 卡和模拟存储。如果您是专业用户，您也会喜欢在恢复过程中执行 ADB 命令的能力，而无需触摸屏幕和使用 GUI。最新版本的 TWRP 也将原生支持智能手表中使用的 QHD 屏幕和更小的屏幕。

这是最新版本的完整变更日志:

*   > 增加命令行功能——你现在可以通过 adb 执行各种 TWRP 功能，而不是触摸屏

*   > 在控制台中增加颜色支持，给错误、警告和高亮线条不同的颜色

*   > 根据文件大小跟踪备份和恢复进度，以提供更准确的进度指示

*   > 得益于 mdmower

    改善/杂项处理
*   > 通过【螺母】

    改进高通设备的时间设置
*   > 感谢塔萨达

    允许在 slidervalue GUI 对象上使用图像
*   > 允许在变量中使用变量和加减运算，以便于主题化

*   > 增加对 1440x2560、280x280、320x320 分辨率的支持，更新 240x240

*   > 允许 ui.xml 文件包含额外的 xml 文件，以帮助分解主题并使 TWRP 更易于维护

*   > 其他小修正和改进

如果您想要升级您的恢复，请从 [TeamWin 的网站](http://teamw.in/project/twrp2)下载镜像文件，将您的设备重新启动到快速启动模式并刷新镜像。如果你不想弄乱命令行，你可以使用像 XDA 公认的开发者 [jmz](http://forum.xda-developers.com/member.php?u=1219335) 的 [TWRP 经理](http://forum.xda-developers.com/showthread.php?t=2331735)这样的应用。您也可以在您的设备论坛中寻求指导。