# Magisk v14.3 引入了“无敌模式”等等

> 原文：<https://www.xda-developers.com/magisk-v14-3-invincible-mode-running/>

# Magisk v14.3 引入了“无敌模式”，以确保 Magisk 始终运行

Magisk 收到了 v14.3 的测试版更新，增加了无敌模式，确保 Magisk 守护进程始终运行，等等！

Magisk 是由 XDA 公认的开发者/公认的贡献者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 开发的广受好评的无系统界面和根解决方案，在过去几周内已经获得了稳定和频繁的测试版和稳定更新。[14.0](https://www.xda-developers.com/magisk-v14-receives-update-install/)版本支持安装它而不需要自定义恢复，随着 [v14.1 和 v14.2](https://www.xda-developers.com/magisk-14-1-official-google-pixel-support/) ，我们获得了对 Google Pixel A/B 分区方案的官方支持，这将有助于未来证明它，因为越来越多的设备采用该分区方案进行无缝更新。现在，在 v14.3 中，进一步的改进和功能被添加进来，以增强用户的 Magisk 体验。

Magisk v14.3 增加了开发者所说的“无敌模式”，旨在一劳永逸地结束所有根丢失问题。由于 Magisk 守护程序负责接口的每个部分，崩溃可能会使 root 完全停止工作，直到设备重新启动。当无敌模式被启用时，系统将确保守护程序无条件地一直工作，并且如果守护程序由于某种原因被杀死/停止工作，将自动重启。更新还包括一些底层的变化，比如 Magisk 处理 logcats 的方式的重写。

在这次更新中，Magisk Manager 也得到了大量的改进，将专有组件(用于安全网检查)模块化，这意味着该应用程序现在是 100%自由/开源软件，并准备在 F-Droid 仓库上发布。管理器现在还拒绝模板版本低于 4 的所有存储库，以尽量减少过时模块导致的引导错误。如果你想试试 Magisk 的最新版本，你可以在我们的论坛上找到它并安装到你的设备上。根据开发者的说法，如果这个版本没有任何问题，那么它将在接下来的几天内进入稳定分支，所以稳定用户也应该关注他们手机即将到来的更新。

* * *

[**立即查看 Magisk v14.3！**](https://forum.xda-developers.com/showpost.php?p=74158225&postcount=31)