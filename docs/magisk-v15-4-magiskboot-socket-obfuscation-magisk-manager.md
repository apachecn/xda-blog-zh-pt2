# Magisk v15.4 更新了 MagiskBoot 改进、套接字混淆等功能

> 原文：<https://www.xda-developers.com/magisk-v15-4-magiskboot-socket-obfuscation-magisk-manager/>

上个月，Magisk 收到了一个更新，修复了一些错误，并增加了对[指纹认证的 SU 访问](https://www.xda-developers.com/magisk-manager-v5-4-4-fingerprint-authentication-root-access/)(在 Android 6.0+设备上)的支持。自那以后，Magisk 的稳定和测试分支已经得到了许多改进，因为 XDA 认可的开发人员和贡献者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 继续完善根实用程序。本周标志着最新测试版 Magisk v15.4 的发布，它带来了 Magisk 管理器优化、套接字混淆和改进的 MagiskBoot。

首先是对 MagiskBoot 的大规模改进。这些变化，其中一些是 XDA 公认的开发者和贡献者 [osm0sis](https://forum.xda-developers.com/member.php?u=4544860) 的工作，意味着它支持更多的引导镜像。topjohnwu 说，现在，MagiskBoot 可能是“处理 Android 启动映像的最强大的单一二进制文件”，并计划在未来的版本中进一步开发它。

接下来是对 Magisk Manager 应用程序(v5.6.0)的优化。根据 topjohnwu 的说法，Chainfire 的 zipadjust 工具最初来自于 [OpenDelta](https://www.xda-developers.com/easily-add-opendelta-functionality-to-almost-any-rom-to-save-bandwidth/) 项目，经过调试，完全重写为 Java，允许在 Magisk Manager 中删除 JNI，并大大简化了 Magisk 构建系统对 ZIP 文件的签名。另外，Magisk Manager 处理 root 的部分已经迁移到 libsu，这是一个为 root 应用程序开发人员设计的 Android 库 topjohnwu，Magisk Manager 的超级用户数据库管理在稳定性方面得到了“大幅改善”。

Magisk v15.4 的最后一个重大变化涉及套接字混淆。在 Magisk 的早期版本中，守护程序侦听特定的 Unix 套接字，这允许通过套接字发送请求，从守护程序远程启动根 shell，并将 STDIN/OUT/ERR 连接到当前终端或进程。使用这种方法，任何应用程序都可以发现 Magisk 的套接字条目，并检测或请求 root 访问权限——即使启用了 MagiskHide。随着更新，这种情况正在改变:现在，每次你的设备启动时，插座名称都会被随机分配。

Magisk v.5.6.0 可通过稳定渠道获得，Magisk v15.4 处于测试阶段。

* * *

[**在我们的 Magisk 论坛**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/post75545948#post75545948) 查看 Magisk v15.4