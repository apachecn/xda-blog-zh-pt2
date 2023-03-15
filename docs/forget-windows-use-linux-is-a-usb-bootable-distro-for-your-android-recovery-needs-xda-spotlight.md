# “忘记 Windows 使用 Linux”是一个 USB 引导的发行版，可以满足你的 Android 恢复需求[XDA 聚焦]

> 原文：<https://www.xda-developers.com/forget-windows-use-linux-is-a-usb-bootable-distro-for-your-android-recovery-needs-xda-spotlight/>

几十年来，微软的 Windows 平台一直是最广泛使用的桌面操作系统，直到最近才下滑至第二位，仅次于 Android，成为用于浏览互联网的最受欢迎的操作系统。尽管这两个平台很受欢迎，但不幸的是仍然存在互通问题，这可能会让任何拥有 Windows 电脑和 Android 手机的用户(数百万)感到沮丧。这些问题在处理[亚行和 Fastboot](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/) 时尤为突出。Android 爱好者对修补并不陌生，他们试图用各种方法来弥补这一点。但有时，无论你启动多少次安全模式，重新安装驱动程序，安装新的驱动程序，或者修改系统设置，你就是无法让你的 Windows 电脑识别你的 Android 手机。为此，XDA 资深成员[standover x](https://forum.xda-developers.com/member.php?u=5545101)发布了“**忘记 Windows 使用 Linux**”(FWUL)——一个可引导的 GNU/Linux ISO，专门面向需要更可靠地与 Android 通信的 Windows 用户。

基于 [Arch Linux](https://www.archlinux.org/) 发行版，忘记 Windows 使用 Linux 是一个 USB 可引导的 GNU/Linux 发行版，旨在帮助修补 Android 的 Windows 用户过渡到 GNU/Linux 环境。你再也不用为 Windows 上的驱动程序问题而苦恼，也不用为了在另一个 USB 引导的 GNU/Linux 发行版上下载合适的工具而手忙脚乱。有了 FWUL，您需要的一切触手可及。你的 Android 手机将毫不费力地被你的电脑识别，所有你可能需要与你的智能手机交互的工具——无论是哪个品牌的——都已经预装了。

在以 Windows 10 为主题、基于 GNU/Linux 的操作系统中嵌入了专门的工具，如 [Simple ADB](https://forum.xda-developers.com/android/software/revive-simple-adb-tool-t3417155) ，这是一个基于 GUI 的 ADB/Fasboot 程序，由 XDA 资深会员 [mhashem6](https://forum.xda-developers.com/member.php?u=5157399) 提供； [JOdin](https://forum.xda-developers.com/showthread.php?t=2598203) ，三星 Odin 软件的 Java 版本——由 XDA 知名开发者 [AdamOutler](http://forum.xda-developers.com/member.php?u=3682533) 、 [Benjamin Dobell](http://forum.xda-developers.com/member.php?u=2710388) 和 [Ralekdev](http://forum.xda-developers.com/member.php?u=2918486) 与 XDA 资深成员 [Loglud](http://forum.xda-developers.com/member.php?u=4194371) 和 [jrloper](http://forum.xda-developers.com/member.php?u=4193553) 合作完成； [Heimdall](https://forum.xda-developers.com/showthread.php?t=755265) ，三星 Galaxy 设备上闪存 ROM 的开源工具，由 XDA 知名开发者 [Benjamin Dobell](https://forum.xda-developers.com/member.php?u=2710388) 开发；以及用于更新 LG、索尼和联发科设备的工具，以及在最初的开发线程中列出的其他工具。可以说，FWUL 装载了强大而有用的工具。

 <picture>![](img/a29ff6f8653b738c8259104e06cdc16a.png)</picture> 

Screenshot of FWUL showing its "start menu" (bottom left), Heimdall (top right), MediaTek Flash Tool (top left), Team Viewer (bottom right), and JOdin (center) running concurrently in multiple windows

设置 FWUL 非常简单。指令可以在[原始线程](https://forum.xda-developers.com/android/software-hacking/live-iso-adb-fastboot-driver-issues-t3526755)中找到，但是所需要的只是一个

干净的闪存驱动器(意味着你可以轻松擦除的闪存驱动器)-任何超过 1GB 的东西都足够了-ISO 镜像，以及一个程序，如 [ISO 转 USB](http://www.isotousb.com/) ，用于镜像带有 FWUL ISO 的闪存驱动器。一旦映像被刻录到 USB，只需将其插入您的 Windows 设备，并选择 USB 驱动器作为您的启动设备。选择这个选项因电脑制造商而异，所以如果你不熟悉一次性启动菜单，谷歌搜索是你的好朋友。启动后，选择“Arch Linux archiso x86_64 UEFI USB”使用用户名“android”和密码“Linux”——不要大写字母。嘣。你被录取了。桌面上将是所有上述工具，准备就绪，等待出发。请注意，其中一些图标是安装程序，因此您可以选择要安装的内容。

确实存在一些 bug，但问题通常会在几周内得到解决，并且可以直接报告给 Github 链接。例如，1.3 版本的网络浏览器有一些问题，但是今天早些时候开发者更新了 FWUL 到[版本 1.4](https://forum.xda-developers.com/showpost.php?p=72144325&postcount=102) ，并且带来了一个新的网络浏览器。虽然 FWUL 并不是万能的操作系统替代品，但它选择了强大的预装 Android 工具，为您的 Android 调整需求提供了一个轻量级和方便的补充，甚至可能是 Windows 的替代品。

* * *

你试过 FWUL 或类似的项目吗？请在下面的评论中告诉我们！

**关注 FWUL，测试平台[这里](https://forum.xda-developers.com/android/software-hacking/live-iso-adb-fastboot-driver-issues-t3526755)！**