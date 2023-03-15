# 使用 AppDowner 降级应用程序

> 原文：<https://www.xda-developers.com/downgrade-applications-with-appdowner/>

# 想降级一个应用程序？AppDowner 来救援

AppDowner 将在几秒钟内降级任何 Android 应用程序，而不会丢失数据。你只需要提供 APK 的原件。

应用程序更新通常会带来各种改进和错误修复，使新更新的应用程序更接近完美。嗯，这里的关键词是“通常”，因为开发人员偶尔会在前进一步时后退两步。这包括诸如瘫痪软件、新的 bug 等等。

避免上述情况的最佳解决方案是降级到旧版本的应用程序。然而，使用 *adb install* 命令是不可能的。因为应用程序数据丢失，移除应用程序并重新安装也不是一个选项。XDA 资深会员[派尔](http://forum.xda-developers.com/member.php?u=5064841)为这一问题找到了解决方案，并制作了 AppDowner。Pyler 的应用程序可以在不卸载或丢失数据的情况下降级其他应用程序。进入技术方面，AppDownren 使用 Unix 系统的 *pm install -r -d file.apk* 命令，它能够在较新的应用程序上安装旧版本的应用程序。它可能对一些 XDA 成员有用(但希望不要太频繁)。

要安装一个应用程序，你需要从你的本地存储器中选择 APK——是的，你显然需要保存旧版本——然后点击*安装 APK* 按钮。AppDowner 会为你做一切。不需要电缆、命令或其他技巧来完成这项工作。

你需要申请降级吗？访问[app downer 线程](http://forum.xda-developers.com/android/apps-games/root-appdowner-downgrade-apps-easy-t2828705)以了解关于该工具的更多信息。