# 使用暴露模块修复外部存储处理

> 原文：<https://www.xda-developers.com/fix-external-storage-handling-with-xposed-module/>

在最近的 Android 版本中，谷歌越来越不愿意迎合使用外置 SD 卡。一直不太清楚谷歌为什么决定在 Nexus 设备中放弃 SD 卡支持，但许多人认为这是因为移除另一个存储区域更加简单。

虽然谷歌在自己的设备上取消了这个想法，但各种原始设备制造商决定在他们的设备上保留 SD 卡插槽。为了正确使用它们，需要对 Android 的源代码进行一些修改。由于一些较新版本的 Android 处理 SD 卡的方式发生了变化，许多应用程序失去了访问外部 SD 卡的能力。幸运的是，Xposed Framework 允许用户修改操作系统的各个方面，而不需要修改文件本身。

XDA 资深成员 [defim](http://forum.xda-developers.com/member.php?u=4501300) 对外部存储的情况感到恼火，于是创建了一个模块来解决上述问题。要应用这个补丁，唯一需要做的就是在根设备上成功安装这个模块后，在 Xposed 安装程序中启用它。

如果您的 Android 4.0.3+设备遇到了外部存储处理问题，请使用[原始线程](http://forum.xda-developers.com/showthread.php?t=2693521)并尝试一下这个模块。