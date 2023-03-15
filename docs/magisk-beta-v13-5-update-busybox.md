# Magisk Beta v13.5 提供了稳定性和兼容性修复程序

> 原文：<https://www.xda-developers.com/magisk-beta-v13-5-update-busybox/>

# Magisk Beta v13.5 更新增加了内部使用的 Busybox、Samsung 内核工作区等等

Magisk beta 频道的新更新推出了 13.5 版本，包括内部使用的 Busybox、三星内核解决方案等。

上个月，我们看到 XDA 公认的贡献者和开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 发布了一个新的 Magisk 稳定更新。这是 13.3 版本，它允许[绕过谷歌最新的安全网限制](https://www.xda-developers.com/magisk-v13-3-is-now-available-bypasses-googles-latest-safetynet-protections/)，并为 Magisk Manager 添加了滚动日志屏幕功能。从那时起，大量的工作已经进入新的测试版更新，这是提供给公众的权利。这个新的测试版更新于 8 月 12 日发布，重点是提高设备的稳定性和兼容性。

最大的变化与 Busybox 有关，Busybox 之前已经从 Magisk 中移除。这样做是因为它会导致问题，而且开发人员需要做大量的工作来构建。然而，自从它被删除后，出现了许多兼容性问题。拥有一个可靠的、功能丰富的命令行工具使得修复这些问题变得更加容易，所以我们已经做了一些工作，通过 v13.5 beta 更新将 Busybox 重新引入 Magisk。

为了帮助将 Busybox 的源代码集成到 Magisk 中，开发人员创建了 [ndk-busybox-kitchen](https://github.com/topjohnwu/ndk-busybox-kitchen) 来自动处理基于配置的头文件的生成，将这些文件解析到 Android.mk 中，以支持使用 ndk-build 命令进行构建。值得注意的是，这一变化意味着 Busybox 的安装仅供内部使用，您将需要手动安装或通过回购通过 XDA 认可的开发者/认可的贡献者 [osm0sis](https://forum.xda-developers.com/member.php?u=4544860) ' Busybox Magisk 模块安装。

在这个测试版更新中做了一些工作，包括一些关于三星股票内核的变通办法。这是对 Magisk 模块模板的更新(现在是版本 5，在另一个分支上运行)，但是模块开发者应该认为这是一个开发者预览版，因为使用它的模块不会安装在运行最新稳定版本(版本 13.3)的用户上。说到版本 13.3，那个更新有一个 bug 在版本 13.5 beta 中被修复了，这个 bug 阻止了股票图像的 SHA1 被获取。

由于这个错误，库存图像恢复(当你卸载它时触发)会失败，只能通过 ramdisk 备份来恢复你的设备。

* * *

[**在我们的 Magisk 论坛**](https://forum.xda-developers.com/apps/magisk/beta-magisk-v13-0-0980cb6-t3618589/post73379475#post73379475) 查看新的测试版更新