# 使用 Dex Manager 轻松编辑 Classes.dex

> 原文：<https://www.xda-developers.com/edit-classes-dex-manager/>

# 使用 Dex Manager 轻松编辑 Classes.dex

这个 Windows 工具允许您以简单有效的方式反编译和编译 classes.dex 文件。

Android 应用程序可以通过多种方式进行编辑。最方便的方法当然是在您最喜欢的 IDE 中更改源代码，并用提供的工具进行编译。不幸的是，并非所有适用于 Android 的应用程序都是开源的，因此很容易通过 Android Studio 或 Eclipse with ADT 进行编辑。

没有公开源代码的应用程序也可以被修改。众所周知的 ApkTool 是做出一些改变的一个选择，但是如果你使用 Windows 作为你的操作系统，XDA 论坛成员 [Jasi2169](http://forum.xda-developers.com/member.php?u=5439231) 创建了一个很好的工具，能够直接从 APK 或 JAR 文件反编译 classes.dex 文件。使用这个工具，用户可以简单地用喜欢的归档管理器(如 7-Zip)提取 classes.dex，并将 classed.dex 文件拖到 Dex Manager。一切都将被反编译，并作为 Smali 文件提取到源文件夹中。这些文件可以编辑并重新编译为 classes.dex，用于替换 APK 中的原始文件。

如果出错，用户会在错误框区域得到一个错误日志。这应该有助于调试项目并修复潜在的构建问题。一个漂亮的图形用户界面和简单性使 Dex Manager 成为基于命令行的 ApkTool 的一个有趣的替代品。

你可以通过从 [Dex Manager v1.0 下载来试用这个应用程序——它是为玩 Classes.dex](http://forum.xda-developers.com/android/software/tool-dex-manager-v1-0-designed-to-play-t2988532) 论坛线程而设计的。