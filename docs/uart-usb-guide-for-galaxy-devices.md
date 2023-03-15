# Galaxy 设备的 UART USB 指南

> 原文：<https://www.xda-developers.com/uart-usb-guide-for-galaxy-devices/>

很久以前，一个穿着闪亮盔甲的白色骑士，名叫 XDA 精英公认开发者 [AdamOutler](http://forum.xda-developers.com/member.php?u=3682533) 为我们带来了大量关于三星 Galaxy Captivate 和其他一些相关设备硬件规格的知识。他和其他一些开发人员，如 XDA 论坛成员和公认的开发人员 [UberPinguin](http://forum.xda-developers.com/member.php?u=2933674) 也给我们带来了打开硬件恶作剧之门的钥匙，反过来也为有抱负的开发人员和最终用户揭示了一个充满可能性的世界。并非每种设备都是相同的，当然，设置 UART 会有一系列的问题，包括但不限于将设备搞乱到不可挽回的地步(也称为完全阻塞)。

XDA 公认的开发人员 bhundven 决定尝试帮助那些有抱负的硬件开发人员铺平道路，这些人不怕打开他们的设备，看看他们午餐吃了什么。以这种方式设置 USB UART 应该可以让你轻松地使用大多数 Galaxy S(而不是 SII 或 SIII)设备。该指南将教你如何设置，使用什么程序，你需要什么硬件，以及某些命令，一旦你掌握了你正在做的事情，你就可以从中得到一些乐趣(如彻底清除 SBL 分区)。

请，请，确保您在尝试执行任何操作之前，已将所有内容阅读了 2 次、3 次或多次。你会弄乱设备的内部，所以很容易把事情弄糟。既然免责声明已经过时，那就来吧，祝你好运！

> 你好，欢迎来到我的 usb uart 指南——也就是如何完全关掉你的手机，如果你没有先思考的话！

您可以在[导丝](http://forum.xda-developers.com/showthread.php?t=1901376)中找到更多信息。

想在门户网站上发表什么吗？联系任何新闻记者。