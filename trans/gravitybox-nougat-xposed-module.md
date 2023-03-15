# nougat-Ready gravity box V7 x 曝光模块现已推出！

> 原文：<https://www.xda-developers.com/gravitybox-nougat-xposed-module/>

随着通过 abforce 的艺术子模块的 Xposed 的突然而不完整和非官方的[回归，开发人员和爱好者都开始探索流行的修改框架在 2017 年可能带来的可能性。虽然我们仍在等待 rovo89 的完整 Xposed 版本(以及随之而来的所有好处)，但最近的解决方案再次引发了 Xposed XDA 论坛的活力，现在我们看到了一个受欢迎的模块的回归:GravityBox。](https://www.xda-developers.com/art-submodule-for-aosp-7-1-2-adds-xposed-functionality-to-custom-roms/)

如果你以前用过 Xposed，*你可能已经知道 GravityBox* 。它是 Xposed 中最大的一个调节盒，具有广泛的兼容性和大量的功能以及定制潜力。主题选项，声音设置，自定义动画，调整各种 UI 元素行为的能力，在你的 ROM 中添加有用的信息显示- GravityBox 有一个很长的功能列表，以至于许多人认为它贬低了自定义 ROM，因为它允许用户挑选他们最喜欢的调整，并让他们在他们最喜欢的 ROM 库中设置它们。GravityBox 是少数几个可以阻止用户更新设备或以其他方式离开 Xposed 的单一 mod 之一，围绕其[回归棒棒糖](https://www.xda-developers.com/gravitybox-makes-massive-return-to-lollipop/)和[棉花糖](https://www.xda-developers.com/gravitybox-for-marshmallow-xda-xposed-mods/)的宣传表明它对许多爱好者来说有多重要。

XDA 公认的贡献者 [C3C076](https://forum.xda-developers.com/member.php?s=82eac66f8ad079156322129f7a210df2&u=5008415) 再次施展了他的魔法，他现在为 Android 牛轧糖 rom 带来了 GravityBox。他警告用户，该模块是在一个非官方版本的 Xposed 上开发和测试的，该版本本身就有缺陷。这个版本还缺少各种功能，要么是因为它们需要额外的工作，要么是因为它们现在是 AOSP 的一部分。例如，指纹发射器仍然需要额外的工作，发射器的调整不会被添加回来。添加清除所有最近事件触发器的功能也不存在，因为这是 Android 的默认功能。GravityBox 也不再提供其旧的 quicksettings 磁贴重新排序界面，尽管它允许您启用或禁用特定文件。你可以在 GravityBox github 查看[完整的迁移历史。此版本的突出功能包括:](https://github.com/GravityBox/GravityBox/compare/v6.3.7_mm...v7.0.0-alpha-01_n)

*   锁屏调整
*   快速设置带附加图块的图块管理
*   Statusbar tweaks
*   导航栏调整
*   饼图控件
*   电源调整
*   显示调整
*   电话调整
*   媒体调整
*   硬件/导航键操作
*   重力盒操作-第三方应用程序的界面

如果你忘了，GravityBox 是为足够接近 AOSP 的**ROM 设计和测试的，它应该可以在任何有普通 Android ROM 或没有经过彻底修改的设备上运行。具体来说，牛轧糖的 GravityBox 已经在 Nexus 5 (AOSP 7.0 & 7.1，奥斯帕 7.2)和 OnePlus 3T (OxygenOS 4.1.6)上进行了设计和测试。不支持 TouchWiz、Sense、MIUI、LeWa、Xperia 和联想的 VibeUI 等 OEM ROMs，您的里程数可能会有所不同-如果您认为您想要启用的功能会与您的 ROM 冲突，请小心谨慎。如果你对兼容性有任何疑问，请务必在提问前搜索 XDA 主题，并完整阅读开篇文章。如果您遇到错误，请通过提供详细信息和日志来帮助解决。**

通过[点击线程](https://forum.xda-developers.com/xposed/modules/app-gravitybox-v7-0-0-tweak-box-android-t3653953)的链接查看 GravityBox，在那里你会找到更多信息和 APK 下载。

* * *

在牛轧糖上试用 GravityBox，你兴奋吗？请在评论中告诉我们！

在我们的公开论坛中查看牛轧糖的重力盒！