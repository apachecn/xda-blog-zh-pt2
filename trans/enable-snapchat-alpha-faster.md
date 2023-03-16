# 如何启用新的更快的 Snapchat Alpha [Root]

> 原文：<https://www.xda-developers.com/enable-snapchat-alpha-faster/>

# 如何启用新的更快的 Snapchat Alpha [Root]

Snapchat 在 Android 上的主要重新设计(强调速度)即将到来。最新的 Snapchat Alpha 版本可以启用，如果你有 root 权限！

世界上使用最广泛的社交平台之一 Snapchat 正准备推出其 Android 应用程序的新的更快版本。去年二月，该公司的高管在内部承诺改善 Android 用户的体验。11 月，[公司公开了其意图](https://www.xda-developers.com/snapchat-android-performance-rebuild/) : Snapchat 将从头开始重建，以“提供更高性能的产品体验”和“使其更易于使用”当时，该公司没有提供重新设计的 Snapchat 应用程序何时推出的时间表，但似乎该应用程序的最新测试版现在有了更快设计的主要功能版本。我们[在另一篇文章中启用了这个重新设计](https://www.xda-developers.com/hands-on-snapchat-alpha-faster-cleaner/)来展示它的外观和性能，现在我们也将向您展示如何启用它。**2018 年 8 月 20 日更新:**我们增加了一个额外的步骤(步骤 10)，这是修复 Snapchat Alpha 中许多稳定性问题所需要的。执行这个新步骤可以修复以下错误:

*   消息不发送。
*   从最近打开应用程序会崩溃。
*   无法关闭全屏模式(OnePlus 6)。
*   故事不会自动排序，有时会崩溃。
*   文本框乱七八糟。
*   打开时未收到通知并崩溃

Snapchat Alpha 最初是由[简·满春·王](https://twitter.com/wongmjane/status/1030293566856339456) (@wongmjane)发现的，但随后由 XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) ，[Mighty Quinn Apps 的基隆·奎因](https://kieronquinn.co.uk/)独立启用。

## 如何启用 Snapchat Alpha

**要求**:

在我们开始之前，您需要安装最新版本的 Snapchat 应用程序——10.39 或 10.39.1 测试版。你可以从谷歌 Play 商店下载该应用程序，但如果你没有最新版本，你也可以从 APKMirror 下载 APK。

[**从 APKMirror** 下载最新的 Snapchat 测试版](https://www.apkmirror.com/apk/snap-inc/snapchat/snapchat-10-39-1-0-beta-release/)

现在，按照这些逐步说明来启动和运行 Snapchat Alpha 吧！

1.  下载一个支持 root 的文件浏览器，比如 [FX 文件浏览器](https://forum.xda-developers.com/showthread.php?t=1253399)或者 [MiXplorer](https://forum.xda-developers.com/showthread.php?t=1523691) 。在本教程中，我将使用 MiXplorer。
2.  打开 MiXplorer，向左展开侧边栏。轻击**根**
3.  如果这是你第一次使用 MiXplorer，它会要求你 root 访问。批准吧。
4.  转到**数据**
5.  向下滚动，再次输入**数据**。
6.  找到" **com.snapchat.android** "
7.  打开" **shared_prefs**
8.  打开"**dynamicapconfig . XML**"
9.  查找“ **appFamily** ”字符串，并将“snapchat”值更改为“**蘑菇**
10.  查找“ **previousAppVersion** ”整数，**将当前值增加 1** 。例如，在下图中，我需要将“1775”改为“1776”
11.  保存文件并退出。
12.  长按启动器中的 Snapchat 应用程序图标，进入其应用程序信息页面。
13.  **强制关闭 Snapchat** 。
14.  将你的手机连接到你的电脑，并在开发者选项中启用 USB 调试(如果你还没有这样做的话)。
15.  如果您还没有下载最新的 ADB 二进制文件，请根据本指南下载并安装到您的 PC [上。](https://www.xda-developers.com/install-adb-windows-macos-linux/)
16.  在你的电脑上打开命令提示符，在你保存 ADB 二进制文件的同一个目录下，输入以下命令进入 ADB shell: **Windows 命令提示符**:`adb shell`**Windows PowerShell**:`.\adb shell`**MAC OS/Linux 终端** : `./adb shell`
17.  现在，逐个输入以下 **4 个命令**(输入‘su’后，它会要求您授予 root 访问权限):
18.  `su``pm enable com.snapchat.android/com.snap.mushroom.MushroomMainActivity``pm enable com.snapchat.android/com.snap.mushroom.MainActivity``pm disable com.snapchat.android/.LandingPageActivity`
19.  打开 Snapchat 应用程序，你应该会看到新的、更快的 Snapchat Alpha 重新设计！

这里有一个由 XDA 知名开发者制作的视频教程，可以帮助你解决指南中的任何一个问题。

如果在这个新的 alpha 用户界面的开发过程中有任何变化，我们都会让你们知道。在那之前，请继续关注 XDA 门户网站，获取更多类似的教程！