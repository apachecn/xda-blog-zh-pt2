# Android Oreo 通过新的救援队功能保存 Bootloops 中的设备

> 原文：<https://www.xda-developers.com/android-oreo-rescue-party-bootloop/>

# Android Oreo 通过新的救援队功能保存 Bootloops 中的设备

Android Oreo 的一个名为 Rescue Party 的新功能将自动尝试修复智能手机或平板电脑检测到的崩溃/重启 bootloop。

自从公司发布了 Android O 的第一个开发者预览版以来，Android Oreo 的大多数新功能都已经为人所知。我们已经在 XDA 这里谈论了[几个月的新功能，然而一旦完整更新发布，总会有新的好东西被发现。其中一个新功能叫做 Rescue Party，它的目标是帮助你恢复遇到 bootloop 问题的 Android Oreo 智能手机或平板电脑。](https://www.xda-developers.com/android-o-ota-update-streaming/)

几乎我们所有在 XDA 的人都曾经去过那里。我们试图安装一个不兼容或有问题的修改，或者只是遇到一点运气不好，然后我们的设备卡在引导循环中。这通常是一个字面上的引导循环，它会导致设备引导到某个时间段，然后简单地重新启动。其他时候，人们会看到他们的设备在引导周期中被卡住，这通常也称为社区中的引导循环。

谷歌指定了两种不同的方法和触发救援队的情况，所以这只会在特定情况下发生，不会是万能的。尽管如此，这还是很有意思的，并且可以在很大程度上防止人们提交保修查询的支持票。这对原始设备制造商来说也是一件好事，因为救援方功能可以解决客户遇到的问题，从而使他们的员工不必处理这些问题。

当 system_server 在 5 分钟内重新启动超过 5 次或持续系统应用程序在 30 秒内崩溃超过 5 次时，将触发救援方。因此，一旦 Android Oreo 检测到崩溃循环，它就会升级一系列行动来恢复设备。这从处理与该级别相关联的任务开始，并试图让设备从该情况中恢复。每一级都越来越激进，会清除/重置某些东西。

当设备最终正常启动时，或者设备直接启动到恢复模式以便您可以执行出厂重置时，整个过程结束。

* * *

[**来源:谷歌**](https://source.android.com/devices/tech/debug/rescue-party)