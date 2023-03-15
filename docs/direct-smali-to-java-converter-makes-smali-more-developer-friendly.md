# Smali 到 Java 的直接转换器使得 Smali 对开发者更加友好

> 原文：<https://www.xda-developers.com/direct-smali-to-java-converter-makes-smali-more-developer-friendly/>

Android 应该是开源的。大多数组件，尽管受 Apache 许可证保护，都有公开的源代码。不幸的是，令人难过的事实是，只有 Nexus 设备所有者可以在不钻研 Smali 汇编语言的情况下修改 Java，Smali 汇编语言并不简单，而且需要比 Java 多得多的努力。另外，反编译的应用程序不能导入 Eclipse 或 Android Studio。

有一些像 [GetJava](http://www.xda-developers.com/android/getjava-helps-you-convert-apks-into-java-projects/) 这样的工具已经可以完成这项工作，但在大多数情况下，结果并不是 100%准确，一些文件仍然需要翻译成 Java。XDA 资深会员 [darkguy2008](http://forum.xda-developers.com/member.php?u=4031980) 决定启动一个项目，旨在提供一个比 JAD 或 JD-GUI 更好的解决方案。

这个项目仍处于非常早期的阶段，但大部分事情已经开始运作了。这个项目是用 C#写的，需要 Visual Studio 2012 和。安装了. NET Framework 4.5 才能正常工作。希望在未来，它将有可能在其他操作系统上使用，如 Linux 或 Mac OS X。毫无疑问，这个项目有很大的潜力，在其他开发者的帮助下，Android 开发可以得到显着改善。

关于这个转换器的更多信息可以在[原始线程](http://forum.xda-developers.com/showthread.php?t=2592266)中找到，所以不要犹豫去那里给开发者一些输入。当然，你也可以通过向 [Github](https://github.com/darkguy2008/smali2java) 库推送一些补丁来做出贡献。

请记住，像这样的工具不应该被用来从付费应用程序中获得一些免费的东西，并以你的名义重新发布。开发者出售他们的作品是有原因的，所以你应该只把它用于教育目的。