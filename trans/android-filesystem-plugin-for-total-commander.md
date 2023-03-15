# 总指挥官的 Android 文件系统插件

> 原文：<https://www.xda-developers.com/android-filesystem-plugin-for-total-commander/>

那些过去在你的电脑上使用过 Total Commander 的人将会感谢这个小插件可以在你的 Android 设备上使用。总指挥官是一个 windows 资源管理器类型的界面，但内置在一个窗口是 2 个窗口，便于移动文件，而不必打开多个窗口只是为了复制一个文件。XDA 成员 sztupy 为 Total Commander 开发了一个插件，允许应用程序访问你手机的文件系统并编辑它，而不必使用手机或任何第三方专用应用程序。

该插件通过使用 adb (Android 调试桥)外壳来执行简单的 Linux。它需要在你的电脑上安装总指挥官，在你的手机上安装 busybox(不需要 root)，并且必须开启 USB 调试。要了解更多关于这个插件的信息，请查看[讨论主题](http://forum.xda-developers.com/showthread.php?t=801758)并下载到[这里](http://github.com/sztupy/adbfsplugin/downloads)。