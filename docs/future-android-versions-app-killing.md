# 未来版本的 Android 可能会更容易杀死应用程序

> 原文：<https://www.xda-developers.com/future-android-versions-app-killing/>

Android 手机上最令人沮丧的体验之一是应用程序在后台被杀死。通知可能会停止发送，无论你最后在做什么都会消失，这是一种完全随机的行为。一些安卓手机比其他的要好，但是几乎所有的手机都会在某个时候经历这种情况。但是，Android 未来的变化，甚至可能是 Android 13 T1，可能意味着你的应用程序在未来可能不会那么快被淘汰。

这项名为“多代最近最少使用”(或 MGLRU)的功能已经在 Chrome 操作系统上推出了一段时间，该公司在“4.14 至 5.15 之间的许多不同内核”上维护 MGLRU。一位谷歌员工说这已经成为“数千万用户的默认设置”，现在看来这一功能正在向安卓进军。Android Gerrit 上的一个提交显示，谷歌已经合并了 Android 13 的[通用内核映像](https://www.xda-developers.com/google-generic-kernel-image/) (GKI)的更改，另一个提交显示，很快，甚至可能通过 adb 启用它。第二次提交尚未合并，但目前正在审查中。

该特性实现了 Android 用户应该非常感兴趣的两个主要目标。第一个是谷歌发现 kswapd CPU 使用率降低了 40%,第二个是谷歌发现 Android 上 18%的内存不足 (OOM)应用程序查杀减少了[。这位谷歌工程师表示，该公司在“一百万台”Android 设备上测试了 MGLRU，这似乎是指 Chrome OS 虚拟机上的 Android 运行时(ARCVM)，该虚拟机为 Chrome OS 上的 Android 11 提供动力。他们写道:“我们已经看到了 CPU 利用率和内存压力方面的实质性改善，导致了更少的 OOM 破坏和 UI 延迟”。](https://lore.kernel.org/lkml/20210313075747.3781593-1-yuzhao@google.com/)

至于所有这些意味着什么，这相当简单。kswapd 是管理虚拟内存的进程，这意味着如果它的 CPU 使用率降低 40%,就可以释放大量潜在的处理空间。至于内存不足的应用程序杀戮，那是不言而喻的，显然会给最终用户带来立竿见影的好处。我们已经看到很多设备在内存管理、按时发送通知或在后台杀死应用程序方面苦苦挣扎。

目前，还不清楚谷歌是否会在 Android 13 的一些用户身上测试这一功能，更不用说默认启用了，但当它推出时，这对用户来说将是一个好处。我们将密切关注这一发展，看看未来是否会有任何变化。

* * *

**来源:Android Gerrit ( [1](https://android-review.googlesource.com/c/kernel/common/+/2050920) )，( [2](https://android-review.googlesource.com/c/platform/frameworks/base/+/2056441) )**

*感谢 XDA 公认开发者 [luca020400](https://forum.xda-developers.com/m/luca020400.5778309/) 对本文的协助！*