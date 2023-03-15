# 哥伦比亚大学的研究人员将 iOS 应用程序引入 Android

> 原文：<https://www.xda-developers.com/researchers-at-columbia-university-bring-ios-apps-to-android/>

直到几代设备之前，[苹果的 iOS](http://en.wikipedia.org/wiki/Evil) 在应用程序的质量和数量上都比安卓有明显的优势。但最近，Android 应用程序已经赶上来了，在许多方面超过了 iOS 上可用的甚至可能的应用程序。这在很大程度上是因为 Android 现在占据了智能手机市场的绝大部分份额，这反过来又激起了第三方开发者的兴趣。然而，一个很好的交易是由于 Android 给了第三方开发者比 iOS 允许的更多的自由。

尽管应用程序的质量和数量都在增加，但是一些相对重要的程序是特定于平台的并不罕见。例如，如果你有很多使用 iOS 的朋友，你无疑会发现自己被排除在外，无法通过 iMessage 或 FaceTime 进行交流。这就是像苹果酒这样的项目发挥作用的地方。

Cider 由哥伦比亚大学计算机科学系的成员开发，是一种操作系统兼容架构，能够在 Android 上运行 iOS 应用程序。这不是使用严格的虚拟机，而是通过一种新颖的方法来完成，包括编译时代码适配以及外交功能。前者允许现有应用源代码无需修改即可在新架构上使用，而后者允许外来应用挂钩到主机设备库，包括专有软件和硬件接口，如 3D 加速硬件。

苹果酒概念验证的视频可以在下面找到。从视频中可以看出，没有 2D 硬件 UI 渲染，一般的 UI 性能是可以预期的。然而，该演示还包括一个 Passmark 剪辑，该剪辑以良好的帧速率运行 3D 基准测试，并完全访问主机硬件的渲染功能。

//www . YouTube . com/embed/ua ple 0 EC 1dg

尽管有许多法律和技术障碍阻碍这样的项目取得成果，但看到这样的项目甚至可以在 Android 上实现，这令人兴奋。毕竟，这只是进一步证明了 Android 的潜力。

希望这个项目的源代码将在某个时候发布，其他开发人员可以在此基础上进行开发和改进。直到那时，这仍然是相当值得注意的。你可以通过访问[项目页面](http://systems.cs.columbia.edu/projects/cider/)和阅读团队的[完整研究论文(PDF 警告)](http://systems.cs.columbia.edu/files/wpid-asplos2014-cider.pdf)了解更多。

为了能够在您的 Android 设备上运行 iOS 应用程序和游戏，您会怎么做？请在下面的评论中告诉我们。

*【非常感谢 XDA 资深版主 [efrant](http://forum.xda-developers.com/member.php?u=1566190) 的提示！]*