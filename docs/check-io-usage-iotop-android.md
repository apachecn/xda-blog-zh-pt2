# 使用 Iotop for Android 检查您的 I/O 使用情况

> 原文：<https://www.xda-developers.com/check-io-usage-iotop-android/>

# 使用 Iotop for Android 检查您的 I/O 使用情况

需要在 Android 设备的后台检查哪个进程导致了大量的 I/O 活动？看看这个 Android 的 iotop shell 脚本端口！

曾经需要检查应用程序的 I/O 使用情况吗？如果是这样的话，你可能尝试过搜索一个 *iotop* 端口，一个用于 Linux 的 Python 脚本——却没有找到，要么匆忙编写一个，要么自己手动检查 */proc/* 。

幸运的是，XDA 论坛的主持人和公认的开发者 laufersteppenwolf 已经编写了一个 shell 脚本来复制 iotop 的原始特性。它将允许您检查每个进程的 I/O 负载/使用情况，查看读取和写入的总字节数，甚至当前的读/写速度。

但是，在使用该脚本之前，您必须确保具备以下条件:

1.  根设备。
2.  启用了 I/O 记帐的内核。默认情况下通常不是这样，但是您可以随时要求您的内核开发人员启用必要的配置(或者如果您正在编译自己的内核，您可以自己启用它们——如果没有，很遗憾，您不能做任何其他事情)。

如果您遇到延迟，但 CPU 不是问题所在(在这种情况下，您可以启动 iotop 并检查是否有任何进程在后台导致大量 I/O 活动)，或者如果您试图调试您的应用程序，这将非常方便。如果您想了解更多信息，请立即访问 Android 论坛主题的 [iotop，了解如何安装和使用它。](http://forum.xda-developers.com/android/software-hacking/script-iotop-android-t2910428)