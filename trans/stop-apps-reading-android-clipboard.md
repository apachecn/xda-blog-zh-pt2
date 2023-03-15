# Android 剪贴板隐私-如何阻止应用程序读取剪贴板

> 原文：<https://www.xda-developers.com/stop-apps-reading-android-clipboard/>

有时，剪切、复制和粘贴一些文本比在键盘上打字或敲击更容易。如果你想输入一些长的文本，如地址、密码或网站链接，使用 Android 的复制粘贴功能肯定比必须精确地键入每个字符要好。但 Android 的剪贴板是出了名的不安全，因为你手机上的任何应用程序都可以在未经你允许的情况下读取它，所以一般建议你永远不要复制任何敏感数据。今天，我将向你展示如何通过阻止应用程序读取 Android 剪贴板来保护你的隐私。

举例来说，Android 的[复制粘贴框架](https://developer.android.com/guide/topics/text/copy-paste.html)允许任何应用程序读取或写入设备的剪贴板。使用这个框架，许多开发者已经在 Play Store 上提供了第三方剪贴板管理器[。虽然这些应用程序以及 Google Translate 等其他一些应用程序很好地利用了剪贴板框架，但绝对不知道其他应用程序可能会对你的剪贴板做什么。一些请求许可的应用程序对它们如何处理你的剪贴板数据是透明的，但是你会惊讶于你的手机上有多少应用程序能够读取你的剪贴板！这就是为什么 Android 上这么多密码管理器应用程序建议你在输入密码时使用他们自己的键盘——他们想保护你免受可能从你的剪贴板上窃取你的密码的应用程序的攻击！](https://play.google.com/store/apps/collection/search_results_cluster_apps?clp=ggELCgljbGlwYm9hcmQ%3D:S:ANO1ljJMs-k)

但你再也不用担心什么可以复制什么不可以复制了，因为我们将向你展示如何控制哪些应用程序可以读取你的 Android 剪贴板。如果没有隐藏的命令行选项，这不是你可以在手机上做的事情，但是我们会指导你如何做。一旦你遵循了这个教程，你应该能够安全地复制你想要的任何数据，而不用担心一些流氓应用程序可能会记录你复制和粘贴的每一个东西。

注意:从应用程序中移除此权限后，在该应用程序中输入文本时，您将无法再使用“粘贴”功能。这对于游戏等应用来说应该不是问题，但可能会给其他应用带来不便。

* * *

## 阻止应用程序读取 Android 剪贴板

1.  你首先需要为你的[手机或](https://developer.android.com/studio/run/oem-usb.html)平板电脑下载并安装 USB 驱动程序。这可能只有在 Windows 上才有必要。
2.  接下来，下载适用于您的操作系统的 [Android Debug Bridge (ADB)二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/),然后将文件从 zip 存档文件解压缩到您计算机上的任何文件夹中。
3.  然后，打开手机上的设置应用程序，找到“关于手机”选项——通常在底部附近。
4.  向下滚动并查找“内部版本号”点击该值 7 次以启用开发者模式。
5.  回到设置中的主菜单，进入新的开发者选项菜单。
6.  启用 USB 调试模式。
7.  将您的设备连接到 PC，并将 USB 模式从“仅充电”更改为“文件传输(MTP)”。
8.  在您的计算机上，导航到之前在步骤 2 中提取 ADB 二进制文件的位置。
9.  对于 Windows 用户，在此 ADB 目录中打开命令提示符。最简单的方法是按 Shift+右键，然后在出现的上下文菜单中选择“在此打开命令窗口”选项。对于 Mac 或 Linux 用户，打开终端。
10.  输入以下命令:`adb devices`。如果您使用的是 Mac 或 Linux，您可能需要在命令前面加上 ADB 存储位置的整个目录。所以比如说，`/home/user/downloads/adb devices`。如果是这样，您需要记住在本教程中以同样的方式为任何进一步的命令添加前缀。
11.  在任何情况下，输入该命令都将启动 ADB 守护程序。如果这是您第一次使用 ADB，您将在设备上看到一个提示，要求您授权连接。允许它。
12.  从步骤 10 重新运行命令，您将在输出中看到设备的序列号。如果是，那么继续下一步。否则，请重新安装驱动程序。
13.  现在发送以下命令:`adb shell`
14.  这将使您进入设备的外壳环境。现在，我们需要弄清楚哪些应用程序能够读取剪贴板。输入这个:`cmd appops query-op --user 0 READ_CLIPBOARD allow`<picture>![Stop Android Apps from Reading the Clipboard](img/cec6d2ac88b4494be0229ad342494881.png)</picture>

    例子:可以读取我的剪贴板的应用

15.  正如你所看到的，在输出中你会看到一个可以读取你的剪贴板的包列表。这里列出的一些内容可能对你来说是显而易见的，但如果不是，安装 [App Inspector](https://play.google.com/store/apps/details?id=com.ubqsoft.sec01) ，然后在每个应用名称下找到包的名称。
16.  一旦您知道要阻止哪个(些)应用程序读取剪贴板，请输入以下内容:`cmd appops set <package> READ_CLIPBOARD ignore`<picture>![](img/4f58341329ddc3d20eb9a96f55e2b171.png)</picture>

    示例:阻止任务者读取您的剪贴板

17.  如果您没有看到错误消息，那么该命令起作用了！重复上述步骤的任何其他应用程序，你想停止读取你的剪贴板。
18.  如果你想撤销你刚才所做的，将第 16 步中的“忽略”改为“允许”。或者，您可以卸载然后重新安装该应用程序，它将重置所有权限。

如果步骤 14 和 16 中的命令对您不起作用，请尝试在前面没有“cmd”的情况下运行它们。我听说这可能是一些运行 Android 6.0 棉花糖或以下版本的手机所必需的。

* * *

## 说明

任何在其`AndroidManifest.xml`文件中声明权限`android.permission.READ_CLIPBOARD`的应用程序在安装时都会被自动授予该权限，这意味着它们可以读取 Android 剪贴板。虽然许多设备都可以访问设置中的权限管理控制系统，但用户无法从应用程序中限制`READ_CLIPBOARD`，除非你是 LineageOS 等某些自定义 rom 的用户。

然而，实际上有一个隐藏的方法来限制应用程序读取你的剪贴板的权限，这就是我们刚才所做的。我们使用了隐藏的“appops”命令行界面，它允许我们限制比设置中显示的更多的权限。我们做的第一个命令是`query-ops`，提取已安装的、被授予 Android 剪贴板读取权限的应用程序列表。使用该列表，我们可以决定要阻止哪些应用程序读取您的剪贴板。如果您决定限制安装在您设备上的每个用户/第三方应用程序的权限，那么您甚至可以开始安全地复制和粘贴您的密码，而不必担心另一个应用程序可能会监听并窃取您的密码！

在我们的[教程类别](https://www.xda-developers.com/category/tutorials/)中查看其他类似的优秀教程。通过 [XDA 实验室](https://www.xda-developers.com/xda-labs/)应用程序了解最新消息。