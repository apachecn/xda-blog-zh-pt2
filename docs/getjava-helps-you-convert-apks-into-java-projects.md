# GetJava 帮助您将 apk 转换成 Java 项目

> 原文：<https://www.xda-developers.com/getjava-helps-you-convert-apks-into-java-projects/>

Android 是一个使用了大量编程语言的操作系统。最常见的语言是 Java(或者 Android Java，如果你喜欢的话)、C、XML、Bash 以及其他一些语言。Android 应用程序可以被 APKTool 和一些类似的工具反编译，它们的输出很小。我知道你们中的许多人不同意我的观点，但是 Smali 是一种非常复杂的语言——比 Java 复杂得多。

有两个工具可以将 Smali 转换回 Java: Dex2Jar 和 JAD。不过，它们很难使用，需要一些经验才能正确使用。幸运的是，XDA 认识到开发人员 [broodplank1337](http://forum.xda-developers.com/member.php?u=4354408) 创建了一个简单的 bash 脚本，它为我们做了所有的工作。这个脚本可以获得所有必要的依赖项，也可以直接从 APK 获得 Java 代码。它只能在 Linux 上工作，但是我很确定它可以在非 UNIX 类系统上使用，比如带有 Cygwin 的 Windows。开发人员建议您将文件放在~/bin 中，并使其可执行。线程中有进一步的说明。

有时候脚本可以让生活变得简单很多。如果您对这个项目感兴趣，请访问[原始线程](http://forum.xda-developers.com/showthread.php?t=2564386)以获得更多信息，并学习如何将汇编代码转换成 Java。

注意:像这样的工具应该用于教育目的。从应用程序(付费或免费)中“借用”代码是不道德的，不应该发生。他们关闭源代码是有原因的。记住这一点。