# 脏管道根漏洞可以在 Galaxy S22 和 Pixel 6 Pro 上滥用

> 原文：<https://www.xda-developers.com/dirty-pipe-root-demo-samsung-galaxy-s22-google-pixel-6-pro/>

# PSA: Dirty Pipe，Linux 内核根漏洞，可以在三星 Galaxy S22 和谷歌 Pixel 6 Pro 上被滥用

三星 Galaxy S22 和谷歌 Pixel 6 Pro 上臭名昭著的“Dirty Pipe”漏洞可被利用来获得根外壳访问权限。

当一个同样影响 Android 的 Linux 特权提升漏洞被公开时会发生什么？你猜对了！世界各地的安全研究人员和 Android 爱好者试图利用新发现的问题来创建一个漏洞，该漏洞可用于获得对您设备的高级访问权限(如 root 或刷新自定义图像的能力)。另一方面，设备制造商和少数坚定的第三方开发商迅速承担起尽快修补后门的责任。

这正是发生在 **CVE-2022-0847** 身上的事情，这是一个在 Linux 内核版本 5.8 及更高版本中被称为“脏管道”的漏洞。我们[上周详细讨论了漏洞利用](https://www.xda-developers.com/dirty-pipe-linux-vulnerability-root-android/)，但没有明确涵盖 Android 上的潜在滥用场景。现在，XDA 成员 [Fire30](https://forum.xda-developers.com/m/fire30.5311830/) 展示了一个围绕内核缺陷的漏洞实现，该漏洞可以给攻击者一个三星 Galaxy S22 和谷歌 Pixel 6 Pro 的根外壳。

这里的关键点是，您不需要任何类型的解锁或其他欺骗来使其工作 Dirty Pipe 漏洞利用允许攻击者通过特制的流氓应用程序，通过反向外壳获得目标设备上的根级别访问权限。在撰写本文时，谷歌 Pixel 6 Pro 和三星 Galaxy S22 等旗舰产品即使在最新的软件版本上也容易受到攻击，这表明了该漏洞的潜力。因为它还可以将 SELinux 设置为许可，所以对设备的未授权控制几乎没有障碍。

从 Android 修改场景的角度来看，Dirty Pipe 可能有助于在其他难以找到根的 Android 智能手机上获得临时根访问权限，例如，三星 Galaxy 旗舰产品的一些区域骁龙变体。然而，这个窗口不会持续很长时间，因为该漏洞已经在主线 Linux 内核中得到修补，OEM 可能会在即将到来的每月安全更新中推出该修补程序。尽管如此，为了保护自己，暂时不要安装来自随机来源的应用程序。与此同时，我们预计谷歌将对 Play Protect 进行更新，以防止该漏洞被流氓应用程序利用。

* * *

**来源:** [推特上的 fire 30](https://twitter.com/Fire30_/status/1503422980612923404)

**Via:** [米沙·拉赫曼](https://twitter.com/MishaalRahman/status/1503454863434338305)