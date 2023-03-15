# 利用通用工具简化 ADB 的使用

> 原文：<https://www.xda-developers.com/adb-universal-utility/>

# 利用通用工具简化 ADB 的使用

这个批处理脚本允许您执行简单的 ADB 命令，而无需输入它们。

Android Debug Bridge(或简称 ADB)是 Android SDK 包中包含的一组工具。它由相互通信的客户端和服务器端程序组成。要正确使用 ADB，您的 PC 必须有正确的二进制文件、命令工具(如终端或命令提示符),并且必须在 yoru 设备上启用 USB 调试。

ADB 的使用并不太困难，但有时输入长命令是一项非常繁琐的任务。如果你以前没有机会使用 ADB 或者只是想让命令的使用更有效，你绝对应该看看 XDA 论坛成员 [Lars124](http://forum.xda-developers.com/member.php?u=5225151) 制作的工具。通用 ADB-Helper 是一个 Bash 脚本，帮助您以最方便的方式使用 ADB。它有使协议工作所需的 ADB 二进制文件，所以您不必担心自己获得它们。使用此实用程序，您可以将设备重新启动到某个模式(快速启动、恢复)，安装应用程序，拉一个 logcat，或者删除 CyanogenMod ROMs 上的 PIN 码/模式。如果您经常更改密码，并且无意中更改了一个您不再记得的密码，这可能会派上用场。

通用 ADB-Helper 可以在根设备和非根设备上使用。在使用它之前，请确保在手机的开发者选项中启用 USB 调试，并向您的 PC 授予 ADB 权限。像往常一样，您可以通过在“关于手机设置”页面轻按几次“内部版本号”来启用开发者选项(启用 USB 调试所必需的)。

这个工具非常适合那些以前完全没有 ADB 经验的人，或者那些厌倦了手动输入命令的人。您可以通过前往 [ADB 通用实用程序线程](http://forum.xda-developers.com/android/software/utility-universaladb-helper-1-0-t2969165)了解更多信息。