# 学习使用 Logcat 来诊断和修复您的问题

> 原文：<https://www.xda-developers.com/learn-to-use-a-logcat-to-diagnose-and-fix-your-issues/>

前段时间，我们介绍了一个快速教程，旨在帮助用户学习如何[生成 logcat](http://www.xda-developers.com/android/help-your-developers-pull-a-logcat-when-issues-arise/ "Help Your Developers; Pull a Logcat when Issues Arise") 。我们还[介绍了](http://www.xda-developers.com/android/take-logging-to-the-next-level-with-logcat-extreme/ "Take Logging to the Next Level with Logcat Extreme")和[的一些工具](http://www.xda-developers.com/android/simplify-logging-with-aio-logcat-manager/ "Simplify Logging with AIO Logcat Manager")，它们可以帮助您轻松地从这个非常重要的诊断工具中获得输出。然而，我们过去介绍的大部分材料都是为了向您提供信息，当某些东西不正常时，您可以将这些信息发送给您最喜欢的开发人员。

如果您学会了如何阅读输出，以便更好地诊断您自己的问题，会怎么样呢？这正是 XDA 论坛版主 [Stryke_the_Orc](http://forum.xda-developers.com/member.php?u=3053298) 想要通过他的指南帮助你完成的事情。尽管这不是一项过于复杂的任务，但是在 logcat 输出中发现错误通常比听起来要困难。

该指南首先向您展示了如何在 Windows 和 Linux/Mac 上获得 logcat。同样，有相当多的工具、指南和方法可以做到这一点。但是，Stryke_the_Ork 介绍了如何使用 *Android SDK\Platform Tools* 文件夹手动完成。他甚至向您展示了如何在 bootloop 情况下获得 logcat。一旦你已经有了你的 logcat，该指南将向你展示如何通过应用程序来过滤你的 logcat，这样你就可以只看到你想看到的内容。

为了让这个方便的工具的输出更有意义，我们来看看[引导线程](http://forum.xda-developers.com/showthread.php?t=2274119)。