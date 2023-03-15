# Pterodon 恢复项目，一个定制的恢复与优化的图形用户界面

> 原文：<https://www.xda-developers.com/pterodon-recovery-project-is-a-new-custom-recovery-for-android-devices-with-an-optimized-gui-and-more-features/>

Android 设备上的“恢复”环境是一种轻量级运行时模式，通常与实际的 Android 用户界面相分离。在大多数情况下，恢复由独立的内核驱动，这意味着即使主 Android 操作系统无法启动，设备也可以启动到恢复模式。这种设计使得恢复环境对于安装 OTA 更新和执行维护作业(例如清理缓存或擦除用户数据)特别有用。

后来，售后改装商扩大了 Android 恢复机制的范围。传奇开发者 Koushik Dutta，在 Android power 用户社区中更好地被称为 [Koush](https://forum.xda-developers.com/member.php?u=617884) ，介绍了[clock work mod Recovery](https://www.xda-developers.com/tag/clockworkmod/)(CWM)，它可以用于执行系统备份和恢复，在不安全模式下运行 adbd，安装自定义内核和 rom，以及一系列其他事情。Koush 确实[在 CWM](https://www.xda-developers.com/clockworkmod-touch-recovery-for-galaxy-nexus-nexus-s/) 中加入了触摸屏支持，但是是 Team Win Recovery Project (TWRP)让触摸恢复普遍流行起来。 [TWRP](https://www.xda-developers.com/tag/twrp-recovery-t/) 及其分叉，如 [OrangeFox 恢复](http://orangefox.tech/)、[红狼恢复](https://redwolfrecovery.github.io/index.html)、[天鹰恢复](https://shrp.team/)等。是目前 Android 修改圈最受欢迎的自定义恢复解决方案，但现在我们又有了一个竞争者。认识一下 **Pterodon 回收项目**！

XDA 的资深成员 ATG·德罗伊德·T1 曾经是红狼恢复的首席开发者，他是新恢复解决方案的幕后主脑。值得一提的是，Pterodon Recovery 不仅仅是另一个 TWRP 分叉，它的整个代码库都是从头开始编写的。例如，GUI 部分是由 [libaroma 引擎](http://amarullz.github.io/libaroma/)处理的——这是支持粉丝最喜欢的 [AROMA 安装程序](https://forum.xda-developers.com/showthread.php?t=2409951)的东西。状态栏工作区用户界面可以在存在缺口的情况下进行动态调整，同时恢复还支持兼容设备上的开箱即用双击进入睡眠(dt2)。除了常规的定制选项外，您还可以选择按住音量按钮来改变亮度，按住电源按钮来打开手电筒。

请记住，在现阶段，Pterodon Recovery**根本不适合日常使用。一些重要的模块，比如分区管理，还没有被开发者实现。[但是源代码是开放的](https://github.com/PterodonRecovery)，这意味着其他社区成员可以免费提交补丁，开发新功能，修复现有的 bug(有很多！).如果你想把 Pterodon Recovery 移植到你的设备上，看看这个清单[。](https://github.com/PterodonRecovery/manifest) [ATG Droid](https://forum.xda-developers.com/member.php?u=8393345) 还公布了两款小米设备的 Pterodon Recovery 编译版本，可以在下面找到:**

**Pterodon 恢复项目:[小米红米 Note 3](https://forum.xda-developers.com/redmi-note-3/development/recovery-pterodon-recovery-project-t4130011)| |[小米红米 Note 6 Pro](https://forum.xda-developers.com/redmi-note-6-pro/development/recovery-pterodon-recovery-project-t4130665)**

**[红米 Note 3 XDA 论坛](https://forum.xda-developers.com/redmi-note-3) ||| [红米 Note 6 Pro XDA 论坛](https://forum.xda-developers.com/redmi-note-6-pro)**

* * *

*截图摘自电报上的[翼龙复原讨论组。](https://t.me/joinchat/FZlpFBdO4Hypy6oVASltqA)*