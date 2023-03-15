# Android 获得 X11 支持

> 原文：<https://www.xda-developers.com/android-gains-x11-support/>

1984 年，马萨诸塞州理工学院发布了被称为 X Windows 系统的开源窗口系统。1987 年，X11 协议最终确定。展望未来 25 年，Linux 已经经历了几次变化，但是[仍然在最初的 X11 协议上运行](http://en.wikipedia.org/wiki/X.Org_Server)它的图形系统。虽然 X Window 系统已经经历了几次变化，包括 X.Org[取代 X Window，X11 背后的惊人发展让它存活了许多年。今天，我们有许多新的输入设备和驱动程序，包括 Android。](http://www.x.org/wiki/)

是的，没错。Android 现在可以通过 X.org 输入驱动程序充当 X.Org 的输入设备。GIMPUSERS 公司的开发人员已经开发了一个 Android 应用程序，你可以简单地把它作为一个应用程序安装在设备上，还可以为你的桌面提供一个配套的驱动程序。这一发展归功于 [redforce](http://www.gimpusers.com/users/redforce) 。

> 他首先开发了 X.org 输入驱动程序，用于桌面 PC(在这种情况下运行 Linux，运行 X display 服务器)接收 Android 的触摸事件。
> 
> 然后，他制作了一个原生的 Android 4.0 应用程序，作为 PC 的输入设备。平板电脑的压力敏感度(如果支持，例如在 Galaxy Note 10.1 上使用手写笔)也会传输到 PC。

使用这个名为“XorgTablet”的新应用程序，您可以将平板电脑用作 X 服务器的压敏触摸输入设备。如果你想为这个正在进行的开发做出贡献，你可以从 GitHub 获得[应用程序源](https://github.com/rfc2822/XorgTablet)和[驱动程序源](https://github.com/rfc2822/xf86-networktablet)，进行测试，并给出反馈。

[来源:[金普斯文章](http://www.gimpusers.com/news/00462-use-android-tablet-as-graphics-tablet-with-gimp)