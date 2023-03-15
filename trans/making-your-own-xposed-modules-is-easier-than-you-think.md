# 制作您自己的暴露模块比您想象的要容易

> 原文：<https://www.xda-developers.com/making-your-own-xposed-modules-is-easier-than-you-think/>

靠近 XDA 中心的是由 Rovo89 设计的 Xposed 框架。我们大多数人都用过它，但是您可能会觉得模块库缺少了什么。我们的解决方案有几个指南，旨在让您开始构建自己的模块，这可能会令人望而生畏，但只需一点时间和努力，就可以打开一个全新的开发领域。

从哪里开始比一开始更好呢？Rovo89 为 Xposed 的开发创建了一个直接的教程。当开始学习用任何媒介开发时，在相当于“hello world”的程序中，这个[指南](https://github.com/rovo89/XposedBridge/wiki/Development-tutorial)教你如何建立一个基本模块来改变你的时钟的颜色为红色。该页面不仅讨论了您可以开始的过程，还介绍了 Xposed 如何通过“挂钩”方法调用并允许您在方法之前和之后注入代码来在 Android 系统中工作。从更改应用程序的元数据以将其标记为模块开始，到执行代码结束，这实际上包含了理解和实现第一个模块所需的所有基础知识。你可以在这里找到他的向导。

“好吧..您想了解如何为 Xposed 创建一个新模块吗？然后阅读这篇教程(或者让我们称之为“广泛的文章”)，学习如何接近这个“T1”——rovo 89

在 Rovo89 工作的基础上，论坛成员 [hamzahrmalik](http://forum.xda-developers.com/member.php?u=5290145) 对教程做了许多很好的补充，包括为我们这些喜欢学习时使用视觉辅助工具的人提供的 Windows 中的分步图像。相对于原始文章的另一个改进是包含了第二个模块，它可以改变状态栏的高度。在你开始之前，这个线程提供了如何设置你的项目的指导，允许新的和有经验的开发人员开始或温习他们的技能。这一次，这篇文章被分成九个独立的教训，每一个都涵盖了你在旅途中可能面临的新挑战和场景。对于那些希望节省时间的人， [hamzahrmalik](http://forum.xda-developers.com/member.php?u=5290145) 还提供了一个到他的工具的链接，该工具将获取你的类、项目、包和应用程序名称以及你的最低 API 级别，然后为你的模块生成一个 Eclipse 项目。因为它是用 Java 编写的，所以有一定程度的跨平台兼容性，包括 Windows 和 Linux。你可以在这里找到原来的线程[和他的设置工具](http://forum.xda-developers.com/showthread.php?t=2709324)[这里](http://forum.xda-developers.com/xposed/tool-xposed-module-project-auto-setup-t2712825)。

当然这很容易，但是根据你想要你的模块做什么，你可能不得不挂钩许多方法。如果你曾经模仿过 APK 氏症，你就会知道我的意思了

或者，您可能更喜欢在 Android 内部创建模块，以便随时进行开发。这就是为什么 [t2107](http://forum.xda-developers.com/member.php?u=5571346) 的[线程](http://forum.xda-developers.com/showthread.php?t=2637006)在为 Android 集成开发环境 [AIDE](https://play.google.com/store/apps/details?id=com.aide.ui&hl=en) 内部开发。除了你正在开发的操作系统之外，这个教程和 Rovo89 发布的原始教程还有几个不同之处；这些包括删除所有的*。类文件来防止致命错误，并且可能需要增加设备堆大小来防止内存问题，就像在 t2107 的 Galaxy Note 上看到的那样。如果你熟悉 AIDE 或者觉得你可以处理它带来的小问题，你可能会发现从最初的[指南开始会更好。](#rovo)

*“重启你的设备。如果时钟是红色的，那么你应该很开心；您刚刚创建了第一个暴露的模块。现在你可以用 Aide 和 Xposed "-[t 2107](http://forum.xda-developers.com/member.php?u=5571346)来构建模块了*

您现在应该会发现，您已经具备了开始创建自己的模块的方法和知识。只要花一点时间和精力，你应该很快就能改变 Android 和应用程序的外观和功能。一如既往，如果你创造了一些可能对他人有用的东西，请在论坛上分享，让他人从中受益！

你以前创建过 Xposed 模块吗？下面留言评论！