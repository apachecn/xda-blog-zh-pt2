# 用一个命令在 Linux、Mac OS X 和 Chrome OS 上设置 ADB 和 Fastboot

> 原文：<https://www.xda-developers.com/set-up-adb-and-fastboot-on-linux-mac-os-x-and-chrome-os-with-a-single-command/>

ADB 和 Fastboot 是几乎每个 Android 用户的无价工具。没有它们，刷新内核或系统映像将会困难得多，甚至是不可能的。如果你是一个有经验的用户，你可以下载 Android SDK，点击几次，将 ADB 和 Fastboot 添加到 *$PATH* 中，然后愉快地用最新的 rom 和内核折磨你的设备，而不用担心一个小错误会导致塑料砖。

如果你是 Linux、ChromeOS 或 Mac 用户，你可能会发现 XDA 论坛成员制作的一个工具非常有用。Nexus Tools 脚本会自动检测您的操作系统，然后下载并配置在您的机器上使用 ADB 所需的几乎所有东西。唯一缺少的是一个 udev 列表，它使设备在调试时“可见”，但这可以通过访问[这个线程](http://forum.xda-developers.com/showthread.php?t=2302780)很容易地修复。

该脚本以 root 用户身份运行，所以当它要求 sudo 并将所有必需的文件复制到 usr/bin 时，不要感到惊讶，这使得它们在系统范围内可用。ChromeOS 支持是实验性的，可能不会像预期的那样工作，所以请记住这一点。

如果你打算将你的电脑设置为使用 Android 设备，Nexus Tools 是一个完美的选择。你所需要做的就是访问[原始线程](http://forum.xda-developers.com/showthread.php?t=2638673)来试一试。