# 在 Android 上安装 Curl 和 OpenSSL 的迷你指南

> 原文：<https://www.xda-developers.com/mini-guide-to-install-curl-and-openssl-on-android/>

你曾经使用 Linux 命令 *curl* 通过终端从服务器下载文档或文件吗？你想从你的 Android 设备上得到同样的功能吗？当然，对于大多数任务，您总是可以使用 wget，但是 curl 与所支持的协议更加兼容，并且还支持双向传输。然而麻烦的是，Android 默认不支持 curl。

如果你想要一个简单的方法来自己安装 curl T1，XDA 论坛成员 T2 r3pwn T3 有一个简单的迷你指南来帮助你开始。该指南首先指导用户从 haxx.se 下载用于 curl 和 OpenSSL 的[预编译二进制文件。将它们提取出来后，只需将它们复制到适当的文件夹中，并设置适当的权限。之后，可以从您选择的](http://curl.haxx.se/download.html)终端仿真器访问这些命令。

如您所见，安装非常简单，最多只需要几分钟。这要归功于来自 haxx.se 的预编译二进制文件，根据 r3pwn，运行 OpenSSL 需要 root 访问权限，但 curl 不需要提升权限。

那些希望开始的人可以通过前往[导丝](http://forum.xda-developers.com/showthread.php?t=2362386)来开始。