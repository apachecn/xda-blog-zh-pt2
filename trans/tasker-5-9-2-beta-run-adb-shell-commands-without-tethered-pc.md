# Tasker 5.9.2 测试版让您可以运行 ADB shell 命令，而无需受限于 PC

> 原文：<https://www.xda-developers.com/tasker-5-9-2-beta-run-adb-shell-commands-without-tethered-pc/>

# Tasker 5.9.2 测试版让您可以运行 ADB shell 命令，而无需受限于 PC

最新的 Tasker 测试版更新带来了一个新功能，允许您运行 ADB shell 命令，而无需连接到 PC。

当谈到 Android 上的自动化应用程序时，Tasker 无疑是大多数用户的首选。尽管该应用程序没有初学者友好的用户界面，但 Tasker 是许多高级用户的首选，因为它提供了大量的插件。例如，开发人员[上个月早些时候发布了 Tasker v5.9】，它引入了一个名为 Logcat events 的新特性，开启了自动化可能性的全新领域。现在，该应用程序在测试频道又有了重大更新，带来了更多的东西。](https://www.xda-developers.com/tasker-5-9-brings-logcat-events-media-button-detection-customizable-assistant-and-much-more/)

根据最近在 Reddit 上的一篇帖子，Tasker v5.9.2 beta 现在向用户推出，它带来了一个新功能，让你可以运行 shell 命令，而不必受限于 PC。对于不知情的人来说，这一新功能基本上可以让你在连接到 PC 时运行所有可以在 ADB shell 中运行的操作，允许你做许多大多数常规应用程序无法做的事情。然而，该特性仍然不允许您做许多需要像 root 一样修改系统文件的事情。以下是您可以使用新功能做的几件事:

*   管理其他应用程序的权限(cmd 应用程序)
*   控制覆盖(cmd 覆盖)
*   切换飞行模式、移动数据等。(svc 命令)

虽然这一新功能在最初的 *Reddit* 线程中引起了隐私问题，但我们可以向您保证它的使用是安全的，前提是您只需为 Tasker 授权 RSA 密钥，而不是盲目地为每台请求在您的设备上访问 ADB 的 PC/app 授权。如果你有兴趣了解这个功能到底是如何工作的，你可以点击[这个链接](https://www.reddit.com/r/tasker/comments/epn1nj/dev_tasker_592_root_actions_without_root/felpu6w/)查看 Redditor 提交的精彩解释。TL；DR 版本是，当用户运行“adb tcpip 5555”时，它会导致设备侦听端口 5555 上的 TCP/IP 连接，这允许 Tasker“远程”向 adb 客户端发送命令。通常这个过程是用来让你发送 adb 命令从 PC 到你的手机，而它是无线的，但在这种情况下，Tasker 使用它来保持 ADB 客户端活着，所以它可以发送外壳命令给它。

如果你有兴趣尝试新功能，你可以点击[这个链接](https://joaoapps.com/beta-testing/)注册测试版。如果你已经注册了测试版，不想等待 Google Play 更新，你可以在这里下载更新的应用。

* * *

**来源:[Reddit](https://www.reddit.com/r/tasker/comments/epn1nj/dev_tasker_592_root_actions_without_root/)**