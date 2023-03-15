# 使用 Android API 的内部/隐藏类

> 原文：<https://www.xda-developers.com/using-internalhidden-classes-of-the-android-api/>

嘘...在这里。是的，你知道隐藏的机器人类吗？嘘...这是个秘密。他们让你做你本来做不到的事情。你可以读取内部数据，比如储存在手机上的短信数据库。您还可以获得对硬件的较低级别的访问权限，以便将应用程序的访问权限扩展到触摸屏输入值或 WiFi 无线电使用等方面。为了得到这种违禁品，你需要在 Android SDK 中做一些探索，并制作一些...变化...Eclipse ADT 插件的工作方式。

这条信息引起了我们的注意，因为 XDA 认出了开发者 [E:V:A](http://forum.xda-developers.com/member.php?u=4372730) 从一年前的默默无闻中推出了他自己的帖子，但是我们很高兴他这么做了。如果你喜欢做一些你不应该做的事情，那就值得你花时间去阅读这个指南。前往[他的原始线程](http://forum.xda-developers.com/showthread.php?t=1711653)了解全部细节。

E:V:A 的工作归结于几年前 Inazaruk 发布的关于主题的[信息的雪崩。同义地称为隐藏类或内部类的 Java 类受到保护，不能直接使用，并且在 Java 文档中隐藏显示(使用@hide 指令)。使用它们只需破解 android.jar 文件并调整 IDE 设置，就能阻止你通往禁果的道路。](https://devmaze.wordpress.com/2011/01/18/using-com-android-internal-part-1-introduction/)

我认为 Inazaruk 和 E:V:A 都忽略了一件事，那就是对隐藏类的可能应用的简单解释。在本文中阅读更多关于[的内容。](http://developer.sonymobile.com/2011/10/28/code-examples-using-hidden-android-apis/)