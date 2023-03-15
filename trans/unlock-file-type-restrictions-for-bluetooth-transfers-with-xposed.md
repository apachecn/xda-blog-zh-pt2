# 使用 Xposed 解锁蓝牙传输的文件类型限制

> 原文：<https://www.xda-developers.com/unlock-file-type-restrictions-for-bluetooth-transfers-with-xposed/>

蓝牙是我们将文件从一个设备传输到另一个设备的最传统的方式之一，随着近几年发布的几乎每个设备都集成了 NFC 技术，这一点变得更加重要。这也有很好的理由——蓝牙方便、相对快速、节能，最重要的是，它可以在过去 10 年的任何技术设备中找到。尽管它有很多优点，但不幸的是，阻碍蓝牙发展的一个因素是对可以接收的文件类型的限制，至少在 Android 操作系统上是这样——这个问题现在可以通过一个 Xposed 模块轻松解决。

由 XDA 论坛成员 [Massi-X](http://forum.xda-developers.com/member.php?u=5576742) 开发的蓝牙解锁摆脱了对文件类型的限制，允许你从你的设备向另一个设备接收*任何你想要的*文件类型。好的，所以可能不是所有的文件类型都存在，但是绝对有很大一部分是存在的。这是因为该模块使您能够选择您想要接收的文件类型，或者从广泛选择的文件类型中选择要阻止的文件类型，这些文件类型分类为简单的类别，例如应用程序、音频和消息等。

蓝牙解锁有英语、意大利语和斯洛伐克语，如果你愿意帮忙，Massi-X 欢迎任何其他翻译。所以如果你想看看这个模块，请访问[原始线程](http://forum.xda-developers.com/xposed/modules/mod-bluetooth-unlock-unlock-receive-t2805347)获取更多信息并下载。