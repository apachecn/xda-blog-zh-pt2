# 亚行、Logcat 和 DDMS 使用指南

> 原文：<https://www.xda-developers.com/guide-on-using-adb-logcat-and-ddms/>

如果你是一个安卓用户，你几乎没有理由不知道如何使用 ADB 和拉一个 *logcat* 的一些基本知识。毕竟，有什么更好的方式来回报帮助我们的移动设备变得更好的开发人员，而不是给他们所需的工具来有效地诊断出现的问题呢？虽然在 Dalvik Debug Monitor 服务被正式添加到 Android 用户界面之前，大多数普通用户都使用该服务来截图，但该工具还可以做更多的事情。

现在，你应该对*logcat*T3[的重要性并不陌生。我们在过去用各种工具](http://www.xda-developers.com/android/help-your-developers-pull-a-logcat-when-issues-arise/)多次讨论过[这个话题，来帮助开发人员解决他们的应用问题。然而，即使有工具供您使用，知道如何手动完成同样的过程也是很好的。亚行的一般知识也是如此。它非常有用，我们强烈推荐这里的一些东西。手动操作的能力更是锦上添花。](http://www.xda-developers.com/android/log-all-the-things-with-aiologger/)

本着这种精神，XDA 资深会员[-全球先生-](http://forum.xda-developers.com/member.php?u=5199314) 创建了一个简单的入门到中级水平的指南来帮助你完成上面列出的所有任务。该指南主要面向 Windows 用户，涵盖的主题从安装 Java JDK 和 Android SDK，一直到通过 ADB 实际连接、拉取 logcat，以及使用 DDMS 执行各种与监控相关的任务。关于 ADB 命令，给出的示例命令将教您如何完成任务，例如从本地计算机安装和卸载 APK，将设备推入和拉出您的设备，以及使用 *adb shell* 通过命令行访问您的设备。

前往[导丝](http://forum.xda-developers.com/showthread.php?t=2303834)开始