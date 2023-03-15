# SuperSU 的实验 SUhide Mod 对应用程序隐藏 su 二进制文件

> 原文：<https://www.xda-developers.com/experimental-suhide-mod-for-supersu-hides-su-binary-from-applications/>

XDA 资深公认开发人员 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 无需介绍第三方开发领域，所以我们将为您节省一些时间。

今天，Chainfire 为我们带来了他的最新作品- [suhide](http://forum.xda-developers.com/apps/supersu/suhide-t3450396) 。Suhide 是 SuperSU 的一个实验性 mod，它利用无系统安装来提供一种方法，在每个应用程序级别上对应用程序隐藏 SU 二进制文件。最好的一点是，它目前没有使用 Xposed 框架，所以它应该会吸引那些只想要 root 但不希望涉足 Xposed 方面的用户。

### 你为什么要用 suhide？

如果你有检测 root 存在的应用程序，Suhide 就会出现。最受欢迎的用例之一是 Android Pay，但如果你有 root 用户，还有其他几个应用程序(主要是与银行和企业安全有关的应用程序)将无法工作。这些应用程序确实有合法的理由不工作，但作为一个超级用户，你有自己的理由为什么你想要根。因此，如果你了解相关的风险，并希望两个世界共存，suhide 是你可以通过实现这一点的途径之一。Suhide 在每个应用程序的基础上隐藏 root，所以你根本不需要全局禁用 root。

* * *

Suhide 在目前的状态下有一些局限性。其中一个主要的问题是没有 GUI，所以这使得 mod 远离初学者(在我们看来，这是理所当然的)。接下来，虽然这是 Chainfire 自己的工作，但他将其归类为实验性的，并且不打算正式支持它作为 SuperSU 的一部分。此外，mod 只在少数设备上进行了测试，所以还没有记录所有的异常行为。mod 也仅限于基于 ARM/ARM64 的设备。它也不隐藏 SuperSU GUI，因此检测 GUI 的应用程序仍将检测 root。最后，Chainfire 认为根和以安全为中心的实现共存是一场失败的游戏。这个人在解释他的立场方面做得很好，所以我们建议你继续读一读，了解一下他的立场。

如需安装和使用说明以及下载链接，请前往[论坛主题](http://forum.xda-developers.com/apps/supersu/suhide-t3450396)。请记住在安装和拆卸后重新刷新 SuperSU。

有助于要求安全性的应用程序和要求 root 的应用程序共存的选项当然是一件好事。但最终，你应该做好有一天不能这样做的心理准备。

你试过 suhide 吗？有什么想法和体会？请在下面的评论中告诉我们！