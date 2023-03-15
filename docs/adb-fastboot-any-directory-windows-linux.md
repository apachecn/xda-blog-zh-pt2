# 将 ADB 和 Fastboot 设置为可在 Windows 或 Linux PC 上的任何地方使用

> 原文：<https://www.xda-developers.com/adb-fastboot-any-directory-windows-linux/>

如果你已经按照我们的教程学习了如何在你的电脑上设置 adb 和 fastboot 平台工具，那么每次都必须导航到该文件夹可能会很烦人，尤其是如果你非常频繁地使用这两个工具的话。每当你想在你的设备上闪存东西的时候，不得不将文件复制到平台工具文件夹也是令人讨厌的。对我来说，这是令人沮丧的，因为我使用固态硬盘，我不喜欢将我的文件复制到我的平台工具文件夹，然后删除它们。但是，可以从 Windows 或 Linux PC 上的任何目录运行 adb 或 fastboot 工具，因此您永远不必更改目录来运行任何命令。

* * *

## 什么是 PATH 系统变量？

Windows 使用 PATH 来指定重要可执行文件的位置。通常，这些文件位于系统目录中，如 C:\Windows 和 C:\Windows\system32。这就是为什么你可以在命令提示符下键入“calc”来启动计算器，而不是“chrome”来启动谷歌 Chrome。这个变量有时会在您安装应用程序时被更改，例如 Java。Java 在安装时会将自己添加到 PATH 变量中，这意味着您可以从任何目录使用 Java。这对使用 Java 应用程序的人很有用，这样程序就不必试图硬编码 Java 位置。

我们将修改 PATH 系统变量，以允许我们在 Windows 计算机上的任何地方使用 adb 或 Fastboot。路径也存在于 Linux 上，通常包含 bin 和 sbin 目录。我还将介绍如何将平台工具添加到 Linux PATH 变量中。

注意:这两个教程都需要管理员/sudo 访问权限。添加到 Windows 有两种方法。我强烈建议使用第一种方法，但是两种方法都可以，如果您计划大量使用 PATH 变量，第二种方法会更好。

## 将 adb 和 Fastboot 添加到 Windows 路径(方法 1)

这实际上并不是将它添加到 Windows PATH 变量中，而是将它添加到已经在 PATH 变量中的文件夹中。只需将你的 adb.exe、fastboot.exe、AdbWinApi.dll 和 AdbWinUsbApi.dll 拷贝到 C:\Windows，你就可以开始了。现在，您应该能够从命令行运行 adb 和 fastboot 了。这是迄今为止最简单、最简单的设置方法。如果不管什么原因它不起作用，请遵循方法 2。

## 将 adb 和 Fastboot 添加到 Windows 路径(方法 2)

### 第一步

打开 Windows 资源管理器，右键单击“我的电脑”。选择“属性”，你会看到一个显示一些系统信息的屏幕。

### 第二步

选择“高级系统设置”。

### 第三步

选择“环境变量”

### 第四步

查找名为“Path”的变量，并双击它。

### 第五步

单击“浏览”并导航到您提取 adb 文件的文件夹。在你打开的所有窗口中，下一个“好的”。启动新的 PowerShell 或命令提示符，并键入“adb”以验证位置已被添加。如果没有，重启你的电脑再试一次。

请确保在您单击“浏览”之前没有突出显示任何字段。如果某个字段突出显示，您将最终替换它。单击列表中不包含条目的某处，以确保不会替换字段。

* * *

## 将 adb 和 Fastboot 添加到 Linux 路径

我将在本教程中使用 Ubuntu，只通过命令行。您可以编辑。bashrc 文件，但是您需要导航到您的主目录的根目录并按 Ctrl+H。

### 第一步

请注意您提取的 adb 工具的路径。对我来说，我把它们提取到/home/adam/adb/platform-tools。

### 第二步

你需要编辑你的。bashrc 文件。回到您的主目录并运行以下命令。

```
 sudo nano .bashrc 
```

如果您更喜欢使用 vi 或 gedit，您也可以使用。

### 第三步

将下面一行添加到。bashrc 文件。编辑该文件时要小心，不要添加或更改任何其他内容。

```
 export PATH=${PATH}:/home/YOUR-USERNAME/path/to/adb 
```

和类型

```
 adb 
```

检查它是否工作。如果它给你一个错误(通常在 64 位计算机上)，安装软件包 **glibc.i686** 和 **libstdc++** ，它应该可以工作了。

* * *

## 搞定了。

现在已经完成了，您应该能够在 Windows 或 Linux 计算机上的任何地方简单地执行 adb 或 fastboot 命令。正如我所说的，这是非常有用的，也允许更好的组织，所以你不需要把所有的 flash 文件放在同一个文件夹中。