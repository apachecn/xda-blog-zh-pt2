# 谷歌和三星开始修补“脏管道”漏洞

> 原文：<https://www.xda-developers.com/google-samsung-dirty-patch-fix/>

本周早些时候，谷歌发布了 4 月份的 Android 安全更新，但该补丁不包括对上个月广为人知的“肮脏管道”安全漏洞的修复。尽管我们可能要等到 5 月份的更新才能修复大多数设备，但一些制造商已经开始为他们自己的设备打补丁，包括谷歌自己。

脏管道(CVE-2022-0847)是在 Linux 内核中发现的一个漏洞，该漏洞允许某人在只读进程中注入和覆盖数据，而无需任何 root 或管理员权限。该漏洞已被用于实现 Android 上的临时 root 访问，但它也可能允许恶意软件和其他未知软件获得系统访问权限。

脏管道现已在 Linux 内核(版本 5.16.11、5.15.25 和 5.10.102)、[以及 Android 版本的 Linux 内核](https://android-review.googlesource.com/c/kernel/common/+/1998671)中得到修复，但该补丁未包含在 4 月的安全更新中。它大概会在五月更新，但不是每个人都想等那么久。Pixel 6 和 Pixel 6 Pro 的一些定制内核包含该补丁，包括 [Kirisakura 内核](https://github.com/freak07/Kirisakura_Raviole/blob/346abdb69c9dde80b84efec417215972a3abe3af/lib/iov_iter.c#L408)。谷歌的 Android QPR3 Beta 2 用于 Pixel 6 和 Pixel 6 Pro，于周四在[发布，有一个](https://www.xda-developers.com/android-12-qpr3-beta-2-released-pixel/)[补丁内核版本](https://android.googlesource.com/kernel/gs/+/refs/heads/android-gs-raviole-5.10-s-qpr3-beta-2/lib/iov_iter.c#410)。

三星似乎是唯一一家在稳定软件上推出手机修复程序的制造商，作为 2022 年 4 月 Galaxy 设备更新的一部分——该公司的安全公告提到了 CVE-2022-0847，该更新已经过[验证](https://github.com/polygraphene/DirtyPipe-Android/issues/3#issuecomment-1086676632)以阻止脏管道攻击。小米 12/12 Pro 仍然[似乎容易受到攻击](https://github.com/MiCode/Xiaomi_Kernel_OpenSource/blob/7d10d738b2c4299f3b8549c61a01ece39f19c788/lib/iov_iter.c#L409)，因为这些手机到目前为止还没有在任何地区获得 2022 年 4 月的安全更新。一加既没有发布 10 Pro 的内核源代码，也没有推出 4 月份的更新。

我们将不得不等待，看看哪些制造商等待 5 月份的更新，哪些公司会提前推出更新(就像三星正在做的那样)。不管怎样，你应该暂时避免安装粗略的 apk。