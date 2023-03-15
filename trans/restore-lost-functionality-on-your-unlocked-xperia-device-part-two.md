# 在解锁的 Xperia 设备上恢复丢失的功能-第 2 部分

> 原文：<https://www.xda-developers.com/restore-lost-functionality-on-your-unlocked-xperia-device-part-two/>

你可能已经注意到，不久前，我们发表了一篇文章，详细介绍了如何在解锁的索尼 Xperia 设备上找回丢失的功能。概括地说，一个简单的系统修改可以让你重新获得在解锁最新 Xperia 设备的引导加载程序时丢失的大部分功能。功能减少的原因是，当解锁引导加载程序时，您会丢失设备的内部 DRM 密钥，这些密钥对于受保护的流媒体以及 BIONZ 图像处理器或 Bravia 引擎等高级技术都是必需的。

在与 mod 的作者[进一步讨论此事后，发现修改后的文件欺骗了 DRM 系统，并假装随时可以获得有效的 DRM 密钥。幸运的是，一些丢失的特性只检查 DRM 密钥的可用性，实际上并不要求它们有效。你可以把它想象成一辆汽车(特定功能)和一把汽车钥匙(DRM 钥匙)。在这种情况下，汽车不需要*的特定按键*，它只需要*的任何按键*就能工作。可以说，它甚至不需要匹配汽车的制造商。](http://forum.xda-developers.com/member.php?u=4699816)

虽然这最初听起来完全是好消息，但它也带来了一些重要的问题。只有索尼能回答的问题，但大家应该都清楚。

****如果一个(大部分)简单的软件修改可以恢复索尼所说的需要有效 DRM 密钥才能工作的功能，那么为什么这些功能甚至可以在没有 DRM 密钥的情况下工作？****

 *在这一点上，看起来你肯定不需要有效的 DRM 密钥来使某些功能工作，这些功能在解锁后最初不会工作。各种成员已经发布了对比图像(例如这里的，或者 OP 中的[)，这些图像显示了 BIONZ 图像处理器和 Bravia 引擎在刷新修改后的文件后的工作情况。虽然不是所有的东西现在都可以工作了，但是作者一直在努力改进结果。毕竟，即使我们今天得到的结果也表明，没有有效的 DRM 密钥也可以重新激活这些功能。他们告诉我们，所有的问题充其量都是人为的。](http://forum.xda-developers.com/showpost.php?p=56541777&postcount=1)

 <picture>![xperia_comparision_bionz_off_on](img/a56ec1d84ba3a462f1f014eea173b07b.png)</picture> 

*The left image has the BIONZ image processor disabled while it's enabled on the right*

***如果这些功能不需要有效的 DRM 密钥才能工作，那么索尼为什么还要移除它们呢？***

显然，这一点只是猜测，但它肯定看起来像是索尼试图通过人为杀死重要功能来阻碍引导加载程序解锁，作为解锁设备的权衡。另一方面，这可能更像是索尼的一次意外失误，因为毕竟他们确实倾向于与开发社区紧密合作。

在这两种情况下，未来将揭示哪个是正确的答案，索尼有机会改善和消除这些限制，或者他们可能会加强安全措施，使其更难找回失去的功能。让我们等待棒棒糖 OTA 们，发现索尼为我们准备了什么。

请务必查看[第一部分](http://www.xda-developers.com/android/restore-lost-functionality-unlocked-xperia/)和[主题](http://forum.xda-developers.com/crossdevice-dev/sony/xperia-z1-z2-z3-series-devices-drm-t2930672)了解更多信息，并在下面的评论中告诉我们你的想法。*