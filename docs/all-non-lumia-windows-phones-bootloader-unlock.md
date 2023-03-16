# 所有非 Lumia Windows 手机现在都可以解锁引导程序

> 原文：<https://www.xda-developers.com/all-non-lumia-windows-phones-bootloader-unlock/>

如果你仍然拥有一台 Windows Phone 设备，并且以任何方式参与了修改社区，你可能听说过 Windows Phone Internals 工具。该工具最棒的一点是它可以在所有 Lumia Windows 手机上禁用 SecureBoot，相当于在典型的 Android 智能手机上解锁 bootloader。对于其他手机，如 HTC One M8，过去的情况是你运气不好。这种情况不再存在，现在有一种方法可以解锁*所有* Windows 手机，包括所有基于高通的设备。

目前，唯一可用于解锁你的设备的指令有点难以遵循。该漏洞之所以成为可能，要感谢一个 developermenu.efi 的泄漏。developermenu.efi 是微软以前用来测试智能手机的工具，它允许你在设备上做许多事情，包括直接在手机上进入大容量存储模式，而不用电脑。这只是修改设备的前奏，还需要很多步骤，包括从 GitHub 存储库中修改 Windows Phone Internals 应用程序。

如果你想试一试，你可以查看下面的源代码链接。请记住，现在您只能通过您安装的新 developermenu.efi 来访问设备存储。如果你不小心的话，很容易损坏你的手机。然而，这个黑客可以让你在阿尔卡特 Idol 4S，惠普 Elite x3 和 HTC One M8 上禁用 SecureBoot，为安装 Windows RT 等替代操作系统打开了大门。一旦你设置好一切，SecureBoot 将被关闭，不管操作系统实际上说什么。

鉴于微软已经将他们的移动重点转移到推广他们的各种服务上，我们几乎不可能看到任何 Windows Phone 的继任者。尽管 Windows 10 Mobile 现在处于维护模式，但这并不意味着一群专注而热情的开发人员不能尽可能长时间地保持现有 Windows Mobile 设备的可用性。我们看到同样的事情一直发生在 Android 方面，所以如果一年后这些设备上仍有工作要做，我们也不会感到惊讶。

* * *

[**来源:gus 33000**](https://gus33000.me/2019/01/05/secureboot-flaw-for-all-wp-devices-literally/)[**Via:MSPowerUser**](https://mspoweruser.com/wpinternals-now-supports-all-non-lumia-windows-phones/)