# 如何在没有 Root 的情况下禁用 Android 上的任何系统应用膨胀软件

> 原文：<https://www.xda-developers.com/disable-system-app-bloatware-android/>

我们对“膨胀软件”的定义取决于个人偏好，但我认为我们都同意，一些制造商和运营商比其他制造商和运营商更应该在他们的智能手机上安装它。根据你的观点，膨胀软件可以是像脸书这样的预装应用，也可以是普通的非谷歌照片库应用。一个人讨厌的膨胀软件是另一个人喜爱的功能，但不幸的是，对于将某些预装应用程序归类为膨胀软件的人来说，他们通常无法卸载它。有时您可以停用系统应用程序，但并不是每个系统应用程序都会让您停用它。

不过，还是有办法绕过这些限制的。不久前，我们写了一篇指南，教你如何在 Android 智能手机或平板电脑上“卸载”任何预装的系统应用。这种方法的问题是双重的:它实际上并没有完全卸载应用程序，并把空间还给用户，恢复更改需要你要么从侧面加载 APK(如果你能找到的话)，要么重置出厂设置。不过，这种方法非常有用，我们已经看到许多论坛帖子和用户脚本利用它来为他们的新 Android 设备解除屏蔽。为了帮助用户以更安全的方式解除设备锁定，我们希望将您的注意力转向另一种方法，这种方法不仅可以禁用您选择的预安装膨胀软件，还可以在您方便的时候非常容易地重新启用它们，使任何错误都更容易恢复。我们仍然会使用 ADB 命令来扰乱系统应用程序，所以请确保您不要禁用任何绝对关键的东西(使用您的最佳判断)，但这种方法更友好，以防您禁用错误的应用程序。

* * *

## 禁用任何没有 Root 权限的安卓系统预装应用

1.  按照本教程在你的 Windows、Mac 或 Linux 电脑上安装并运行 ADB。ADB 或 Android Debug Bridge 是一款开发工具，可以让您发出一些强大的命令来控制您的设备。在我们的教程中，我们经常使用它来做一些没有根设备就不能做的事情。
2.  从谷歌 Play 商店下载类似 [App Inspector](https://play.google.com/store/apps/details?id=com.ubqsoft.sec01) 的应用。
3.  使用“应用程序检查器”获取您想要停用的应用程序的包名称。以下截图向您展示了如何操作:
4.  在存储 ADB 二进制文件的目录中启动命令提示符/PowerShell (Windows)或终端(Mac/Linux)。对于 Windows 用户，这可以通过按住 shift 键，然后在文件夹中右键单击来完成。在菜单中，选择“在此打开命令窗口”或“在此打开 PowerShell 窗口”选项。<picture>![](img/0e597be4d46e7b7955f6c71ea545cb90.png)</picture>

    在 Windows 10 上打开命令窗口

5.  进入命令提示符或终端后，根据您的操作系统输入以下命令: **Windows 命令提示符:**`adb shell pm disable-user --user 0 <package_to_disable>`**Windows PowerShell:**`.\adb shell pm disable-user --user 0 <package_to_disable>`**Mac/Linux 终端:** `./adb shell pm disable-user --user 0 <package_to_disable>`
6.  例如，如果你想删除小米 Mix 2S 上作为 miui 的一部分预装的 clean master(com . MIUI . clean master)，它看起来是这样的: **Windows 命令提示符:**`adb shell pm disable-user --user 0 com.miui.cleanmaster`**Windows PowerShell:**`.\adb shell pm disable-user --user 0 com.miui.cleanmaster`**Mac/Linux 终端:** `./adb shell pm disable-user --user 0 com.miui.cleanmaster`

我们完事了。该应用程序应立即被禁用，并将从您的启动器中消失。请注意，在极少数情况下，如果系统有重新启用的功能，一些应用程序可能会自动重新启用。例如，禁用中国华为或 Honor devices 上的股票 [EMUI 9 启动器将导致股票启动器在一段时间后自动重新启用。如果这困扰着你，试试“](https://www.xda-developers.com/huawei-honor-chinese-emui-9-blocks-third-party-launchers/)[卸载](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)的方法。

## 重新启用任何禁用的预装系统应用程序

如果您禁用了一个应用程序并想要恢复它，该怎么办？重新启用 app 非常容易！首先，进入**设置>应用**并查看“所有应用”列表(它可能位于您设备上的其他地方。)通常，您可以在此处过滤，查看所有禁用的应用的名称。一旦您知道要重新启用的应用程序，请按照以下步骤操作:

1.  打开命令提示符或终端窗口，运行以下命令: **Windows 命令提示符:**`adb shell pm list packages -d`**Windows PowerShell:**`.\adb shell pm list packages -d`**Mac/Linux 终端:** `./adb shell pm list packages -d`
2.  此命令列出所有禁用的软件包。找到与您要重新启用的应用程序对应的包名称。现在，只需运行以下命令重新启用其中一个: **Windows 命令行提示:**`adb shell pm enable <package_to_enable>`**Windows PowerShell:**`.\adb shell pm enable <package_to_enable>`**Mac/Linux 终端:** `./adb shell pm enable <package_to_enable>`
3.  如果您有任何问题，请在重新启用应用程序后尝试重新启动。

## 我们做了什么？

首先，重要的是区分这个命令做什么，以及为什么它优于我们在之前的[膨胀软件移除教程](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)中使用的方法。在该教程中，我们在用户级别卸载了一个应用程序，这意味着它仍然安装在设备的系统分区中，但不是为主要用户(用户 0)安装的。这就是为什么要拿回来，你要么需要工厂重置或侧装 APK。在本教程中，我们*为主要用户禁用*该应用程序，而不是卸载它，这意味着我们可以启用它，而无需再次重新安装。

pm disable-user 命令已经存在很多年了，但是由于支持 pm disable 而被忽略了。您可能认为 pm disable-user 和 pm disable - user 0 应该是相同的，但是您错了。出于某种原因，disable-user 命令可以让你禁用任何你想禁用的应用程序，而常规的 disable 命令是非常有限的。

这种方法最好的一点是，如果你弄糟并禁用了一个不应该禁用的应用程序，这是一个非常简单的修复方法。你仍然会收到 OTA 更新，因为你实际上并没有修改任何系统文件。这就是为什么我们需要命令中的“- user 0”部分，它指定该应用程序仅对当前用户禁用，而不是所有用户，这将需要 root 访问权限。