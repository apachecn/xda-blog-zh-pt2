# Zip Builder 是一个 Windows 工具，可以帮助您轻松创建可刷新的拉链

> 原文：<https://www.xda-developers.com/zip-builder-windows-tool-flashable-zips/>

# Zip Builder 是一个 Windows 工具，可以帮助您轻松创建可刷新的拉链

Zip Builder 是一个新的 Windows 工具，它使得为 Android 创建可刷新的、易于使用的 Zip 安装程序变得轻而易举。

 <picture>![zip builder](img/dd16158656a25eccdc28e1daf2fd2181.png)</picture> 

A Samsung Electronics Co. Galaxy Note Edge smartphone running the Android mobile operating system is arranged for a photograph in New York, U.S., on Tuesday, July 28, 2015\. A researcher at a security firm revealed a hole in Android's source code that hackers can exploit, if they have a phone's number, with a text. Photographer: Chris Goodney/Bloomberg

为 Android 创建一个 mod 比计算出哪些代码需要修改要花费更多的工作。大多数使用 mods 的人更喜欢易于刷新的 ZIP 文件，但是为 Magisk 模块或 AnyKernel2 git repo 创建和签名 ZIP 文件需要一定的努力。这就是为什么[PA GApps](https://www.xda-developers.com/get-the-latest-gapps-with-0-day-pa-gapps-compilation/)fame([Open GApps](https://www.xda-developers.com/open-gapps-adds-option-to-enable-google-assistant-during-installation/)的前身)的 XDA 资深成员 [TKruzze](https://forum.xda-developers.com/member.php?u=2777334) 发布了一款名为 Zip Builder 的 Windows 工具。Zip Builder 可以在 shell 脚本和 edify 脚本安装程序上使用，它从 Windows 文件夹中构建并签名基于 Android Zip 的安装程序，自动检测安装类型，并包括构建和签名 ZIP 安装程序所需的所有组件，而无需其他软件。它甚至支持自定义命令，让您生成一个 MD5 校验和文件，包括。git 文件夹和相关文件，在输出文件中添加构建日期，等等。你需要的只是最新版本的 Java。

* * *

[**在我们的安卓软件和黑客论坛**](https://forum.xda-developers.com/android/software-hacking/tool-zip-builder-v4-2-1-build-sign-t3739556) 查看 Zip Builder