# 如何在不擦除数据的情况下在 Google Pixel 上刷新每月安全更新

> 原文：<https://www.xda-developers.com/flash-monthly-security-update-google-pixel/>

人们购买谷歌 Pixel 手机的最大原因之一是及时的更新，无论是每月一次的安全更新，还是 T2 升级系统版本的重大更新。但是谷歌喜欢批量更新，所以你可能要等几天才能获得每月的安全更新。你没有买一个像素等更新吧？他们一发布，你就想把它放在你的手机上。

如果这就是你，好吧，我们会保护你的。我将向你展示如何在你的[谷歌像素](https://forum.xda-developers.com/pixel)、[谷歌像素 XL](https://forum.xda-developers.com/pixel-xl) 、[谷歌像素 2](https://forum.xda-developers.com/pixel-2) 和[谷歌像素 2 XL](https://forum.xda-developers.com/pixel-2-xl) 上手动安装这些更新。你不需要擦你的设备，所以这是一个优点。我们将提供两组说明:一组用于安装快速启动映像，另一组用于安装 OTA 映像。无论你做了多少修改(只要你没有运行定制的 ROM ),快速启动镜像都可以安装在启动加载器未锁定的设备上，而 OTA 镜像更适合启动加载器锁定的设备。

哦，还有一件事:这些指令将适用于任何其他具有快速启动映像的设备(如[谷歌 Nexus 5X](https://forum.xda-developers.com/nexus-5x) 、[谷歌 Nexus 6P](https://forum.xda-developers.com/nexus-6p) 和[谷歌 Pixel C](https://forum.xda-developers.com/pixel-c) )。

## 引导加载程序解锁设备的快速引导映像说明

### Windows 操作系统

1.  好的，首先你需要从[这里](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)下载平台工具。你需要他们使用 adb 和 fastboot 接口。在桌面上下载并解压。
2.  然后你需要从[这里](https://developers.google.com/android/images)为你的设备下载最新的股票图片。
3.  将股票镜像的所有内容解压到 platform-tools(我们之前下载的 adb 和 fastboot 接口)文件夹中。
4.  您将看到一个名为“flash-all.bat”的小批处理文件。这个脚本自动刷新所有压缩图像。您需要更改它，以便它不会擦除您的设备。推荐你用[记事本++](https://notepad-plus-plus.org) 。
5.  在文本末尾附近，删除'-w '(没有引号)并保存文件。
6.  在 Windows 上使用命令提示符导航到平台工具。您可以使用 Windows search 来启动它。要进行导航，您需要使用命令`cd Desktop\platform-tools`注意:如果您在 Windows 10 上使用 PowerShell，那么您需要在以下步骤中的所有命令前加上。\
7.  键入`adb devices`并确保您的设备出现在列表中。
8.  现在你需要把你的设备设置成引导模式。为此，执行命令`adb reboot bootloader`
9.  检查快速启动是否能看到您的设备。输入`fastboot devices`
10.  现在，如果你处于引导模式，快速引导看到你的设备，只需双击“flash-all.bat”并等待几分钟。

### Mac OS/Linux

不使用 Windows 怎么办？我们会掩护你的。

1.  首先，下载用于 Mac OS(T1)或 Linux(T3)的平台工具。在桌面上下载并解压。
2.  然后你需要从[这里](https://developers.google.com/android/images)为你的设备下载最新的股票图片。
3.  将股票镜像的所有内容解压到 platform-tools(我们之前下载的 adb 和 fastboot 接口)文件夹中。
4.  你会看到一个叫做‘flash-all . sh’的小脚本。这个脚本自动刷新所有压缩图像。您需要更改它，以便它不会擦除您的设备。使用您喜欢的文本编辑器。
5.  在文本末尾附近，删除'-w '(没有引号)并保存文件。
6.  使用终端导航至平台-工具。要导航，您需要使用命令`cd Desktop`和`cd platform-tools`
7.  使用命令`./flash-all.sh`执行脚本，并等待几分钟。

您的手机可能需要大约 10 或 15 分钟来安装更新。它甚至可能会挂起，但不要在通过快速启动闪烁时断开 USB 电缆！正如我所承诺的，你所有的应用程序、照片、视频和音乐都在原来的位置。

## 引导加载程序锁定设备的 OTA 映像说明

为了在锁定了引导程序的设备上刷新更新，我们将使用 adb 来加载它。对于任何平台来说，说明都是一样的，所以没有必要把它分成不同的类别。

1.  下载[平台工具](https://developer.android.com/studio/releases/platform-tools)并在你的桌面上解压。
2.  从[这里](https://developers.google.com/android/ota)下载一个 OTA 更新，放在平台工具文件夹里。
3.  在手机上，前往“设置”>“关于手机”。点击 7 次内部版本号，然后进入开发者选项并激活 USB 调试。
4.  在 Windows 上打开命令提示符/PowerShell，在 Mac OS/Linux 上打开终端，输入'`cd Desktop`'和'`cd platform-tools`'。
5.  通过 USB 连接线将您的手机连接到 PC。
6.  现在根据您的操作系统执行以下命令:对于 Windows 命令提示符:`adb reboot bootloader`对于 Windows PowerShell: `.\adb reboot bootloader`对于 Mac/Linux 终端:`./adb reboot bootloader`
7.  现在你进入了引导程序，你需要使用音量按钮找到恢复模式，然后按下电源按钮进入恢复模式。
8.  进入恢复模式后，选择“应用来自 ADB 的更新”
9.  现在，为了最终刷新我们的 OTA 文件，请根据您的操作系统执行以下命令:对于 Windows 命令提示符:`adb sideload filename.zip`对于 Windows PowerShell: `.\adb sideload filename.zip`对于 Mac/Linux 终端:`./adb sideload filename.zip`请注意:您需要用您下载的 OTA 映像的名称替换 filename.zip。比如 sailfish-OTA-OPM 4 . 171019 . 016 . B1-b 387 f 7 b 2 . zip。