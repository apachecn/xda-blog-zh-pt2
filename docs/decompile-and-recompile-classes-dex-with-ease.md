# 轻松反编译和重新编译 Classes.dex

> 原文：<https://www.xda-developers.com/decompile-and-recompile-classes-dex-with-ease/>

公平地说，除非你花了一些时间在 APK 文件中挖掘，并对应用程序或 Android 操作系统本身进行了一些大规模的修改，否则你很可能没有在. smali 文件的自然环境中见过它。它们是许多最受欢迎的 Android 调整和修改中的常见组件，例如添加开关、扩展电源菜单和添加 CRT 屏幕关闭动画。

文件本身通常可以在 apk 中找到，一旦特定的文件被诸如 [APKTool](http://www.xda-developers.com/android/apktool-to-receive-updates-once-again/) 这样的实用程序反编译，就可以对其进行修改。不幸的是，这些 smali 文件有时倾向于将自己隐藏在 JAR 文件的 *classes.dex* 中，使自己变得更加笨拙和费时。在他最近的 ADB 命令指南之后，XDA 资深成员 [iamareebjamal](http://forum.xda-developers.com/member.php?u=4782403) 组装了一个点击式工具，可以让你轻松地从任何 APK 或 JAR 文件中反编译 *classes.dex* 。

只需将相关文件放在输入文件夹中，反编译，对新的可用文件进行必要的更改，重新编译，并检查输出文件夹中的修改版本。就这么简单。显然，这需要一些先决条件，即某种运行 Windows、Java(理想情况下以软件**和**液体形式)的个人计算设备，相关的文件和工具(notepad++和存档管理器等)，以及你希望最终实现的一些想法。如果你拥有所有这些，这将证明是一个很好的节省时间的小方法，值得一游[原始线程](http://forum.xda-developers.com/showthread.php?p=40451202)。