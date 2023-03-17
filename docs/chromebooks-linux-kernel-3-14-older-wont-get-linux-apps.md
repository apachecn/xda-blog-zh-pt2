# 采用 Linux 内核 3.14 及更低版本的 Chromebooks 不会获得 Linux 应用程序支持

> 原文：<https://www.xda-developers.com/chromebooks-linux-kernel-3-14-older-wont-get-linux-apps/>

当谷歌宣布 Chrome OS 上的 Linux 应用程序时，每个人都很兴奋。我们[发表了一篇文章](https://www.xda-developers.com/linux-app-support-older-chrome-os-devices/)，其中我们列出了所有将获得 Linux 应用支持的旧 Chromebooks，因为开发人员已经在努力向后移植基本的内核模块，如 vsock。嗯，我们在技术上并没有错，因为开发者[确实尝试过](https://bugs.chromium.org/p/chromium/issues/detail?id=763970)让 vsock 向后兼容。但是，事实证明，vsock 不能被反向移植到 Linux 内核 3.14。

无法将 vsock 反向移植到 Linux 内核 3.14 或更早版本，这意味着使用该版本内核的设备将无法安装 Linux 应用程序。以下是使用 Linux 内核 3.14 或更低版本且无法运行 Linux 应用的 Chromebooks 列表:

| 

设备

 | 

出厂日期

 | 

内核版本

 | 

体系结构

 |
| --- | --- | --- | --- |
| Acer Chromebase | 2015 年 8 月 1 日 | 3.10 | 手臂 |
| 惠普 Chromebook 14 G3 | 2014 年 10 月 18 日 | 3.10 | 手臂 |
| 宏碁 Chromebook 13 (CB5-311) | 2014 年 9 月 7 日 | 3.10 | 手臂 |
| 宏碁 C670 Chromebook 11 | 2015 年 2 月 28 日 | 3.14 | x86_64 |
| 华硕 Chromebook Flip C100PA | 2015 年 7 月 1 日 | 3.14 | 手臂 |
| 华硕 Chromebook C201 | 2015 年 5 月 1 日 | 3.14 | 手臂 |
| 宏碁 Chromebox CXI2 | 2015 年 5 月 1 日 | 3.14 | x86_64 |
| 宏碁 Chromebase 24 | 2016 年 4 月 1 日 | 3.14 | x86_64 |
| 东芝 Chromebook 2 (2015 版) | 2015 年 9 月 22 日 | 3.14 | x86_64 |
| 联想 ThinkCentre Chromebox | 2015 年 6 月 2 日 | 3.14 | x86_64 |
| 谷歌 Chromebook Pixel (2015) | 2015 年 3 月 11 日 | 3.14 | x86_64 |
| 宏碁 Chromebook 15 | 2015 年 4 月 30 日 | 3.14 | x86_64 |
| 戴尔 Chromebook 13 7310 | 2015 年 8 月 13 日 | 3.14 | x86_64 |
| 华硕 Chromebox CN62 | 2015 年 8 月 3 日 | 3.14 | x86_64 |
| AOpen Chromebase Mini | 2017 年 2 月 28 日 | 3.14 | 手臂 |
| 华硕 Chromebit CS10 | 2015 年 11 月 2 日 | 3.14 | 手臂 |
| AOpen Chromebox Mini | 2017 年 2 月 28 日 | 3.14 | 手臂 |

正如你所看到的，这个列表中有很多 Chromebooks，其中一些还相当新。就连 2015 年发布的谷歌自家原创 Chromebook Pixel 也榜上有名。请记住，由于 32 位基础架构，那些使用 ARM 处理器的用户已经失去了支持。虽然这些旧的 Chromebooks 有可能在更新中获得新的内核版本，但你不应该指望这种情况会发生。

你是否足够幸运，拥有一台使用 Linux 内核 3.18 或更新版本的 Chromebook 设备？[以下是支持 Linux 应用程序或即将支持的设备列表](https://www.xda-developers.com/chromebooks-linux-app-support/)。你很快就可以在上面运行 Linux 应用了。但是，对于那些运气不好的人来说，斗争还在继续。

* * *

[**来源:Chromium Gerrit**](https://chromium-review.googlesource.com/c/chromiumos/docs/+/1181782)[**Via:/r/Crostini**](https://www.reddit.com/r/Crostini/comments/99gpkw/chromebooks_with_314_kernel_will_not_get_linux)

本文在美国中部时间晚上 11:03 更新，删除了 Linux 内核的扩展 LTS 可以防止这种情况发生的措辞。LTS 分公司看不到功能备份，只有错误修复和安全补丁。