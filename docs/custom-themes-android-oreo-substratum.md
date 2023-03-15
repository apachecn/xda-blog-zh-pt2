# 如何在 Android Oreo 上安装自定义主题

> 原文：<https://www.xda-developers.com/custom-themes-android-oreo-substratum/>

在经历了大量的[戏弄](https://www.xda-developers.com/video-rootless-substratum-theme-engine-android-oreo)之后，Substratum 团队和 XDA 开发者自豪地宣布发布了[Andromeda add-on for Substratum](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)，它为**带来了对任何没有 root** 的 Android 8.0 Oreo 设备的完全定制主题支持。我们意识到许多人对这个项目感到兴奋，但也有许多人觉得这个消息对他们来说是压倒性的，因为我们一直在转播大量的技术细节。对于这些人，我们想让你放心，最终产品对你的普通用户来说是足够简单的，并且不需要你理解如何使用复杂的脚本或 ADB 命令。本教程旨在向您展示如何设置和安装新的无根底层，然后使用主题引擎安装自定义主题。

* * *

## 如何使用 Substratum 在 Android Oreo 上安装自定义主题

要求:

*   安卓 8.0 奥利奥设备
*   访问 Windows、Mac 或 Linux PC

### 先决条件

您需要下载并在手机上安装两个应用程序。首先，下载安装底层主题管理应用程序。这个应用程序是免费的，需要用来管理你的主题。

接下来，下载仙女座附加组件。本应用为**付费**应用。

最后，从这个 XDA 论坛的帖子中为你的特定操作系统下载仙女座桌面客户端(可以在 **Windows、Mac** 和 **Linux** ) [上下载)。提取。zip 文件，并将存档的内容保存到 PC 上的任何文件夹中。为了苹果电脑。dmg 文件，保持原样。](https://forum.xda-developers.com/apps/substratum/andromeda-desktop-clients-release-notes-t3668682?styleid=18)

### 第 1 部分-如何安装仙女座菌株

1.  启用**开发者选项**然后 **USB 调试**
    1.  打开手机上的**设置**应用程序。
    2.  向下滚动并点击“**系统**”
    3.  点击**关于电话**
    4.  向下滚动并点击**“Build number”7 次**，直到你看到一条提示信息，上面写着“**你现在是一名开发人员了！**
    5.  回到“系统”设置，你会看到一个新的“**开发者选项**菜单。
    6.  进入**开发者选项**。注:它可能会要求您输入设备的 pin/密码。
    7.  找到并启用 **USB 调试**
2.  打开手机上的**仙女座菌株应用程序**。“连接状态”应该是“**断开**
3.  **使用支持的 USB 数据线将手机连接到 PC** 。
4.  在你之前下载的 PC 上运行 **Andromeda 客户端**。
    1.  在你的电脑上，打开 start_andromeda.bat 文件。它可能会要求您提供“管理员”权限。如果是这样，那么授予它，您将看到一个命令提示符打开。按回车键后，您将看到一串 ADB 命令被发送。这些命令正在设置 Andromeda 加载项，以便它可以独立于您的 PC 运行。
    2.  **Mac: **Click on AndromedaClient.app. It will ask you to select the "disk image of the mounted Andromeda client." Press continue, then when your file browser pops up, look for "Andromeda" under the "Devices" list. Select it and click continue. Here is a quick video showing these steps:
    3.  **Linux:** 点击 start_andromeda.sh 脚本文件。您应该会看到一个终端窗口打开，一些命令正在运行，很像上面显示的 Windows 版本。
5.  一旦你运行了上面的仙女座桌面客户端，你会立即看到底层应用程序在你的手机上打开。如果是这样的话，那么这个脚本就成功了，Substratum 现在可以在没有 root 用户的情况下管理主题，也不需要绑定到你的 PC 上！为了验证脚本工作，再次打开 Andromeda 应用程序，连接状态现在应该显示绿色的“**已连接**

现在 Andromeda 服务已经在你的手机上运行了！每当你重启手机时，这项服务就会被关闭，所以如果你想在未来改变任何主题，你只需简单地插入手机，然后再次运行桌面客户端。不过，不要担心，如果你重启手机，你设置的任何自定义主题都不需要重新启用。请查看我们关于底层的[FAQ 文章](https://www.xda-developers.com/video-rootless-substratum-theme-engine-android-oreo/#faqs)来了解更多关于这是如何工作的！

### 第 2 部分——如何安装定制主题

首先，你需要为你的手机找到一个自定义主题。在谷歌 Play 商店中寻找[底层](https://play.google.com/store/apps/collection/search_results_cluster_apps?clp=ggEMCgpzdWJzdHJhdHVt:S:ANO1ljKAR64)或者看看这个帖子中列出的[中的一些。寻找提到支持底层或“OMS”的主题，因为这些主题很可能在你的设备上运行。提及“legacy”或“RRO”的主题在您的设备上不起作用。](https://forum.xda-developers.com/apps/substratum/android-o-ready-themes-t3666473)

作为一个例子，我们将向你展示如何为底层安装波罗的海用户界面。请注意，如果你不喜欢这个主题，那么你可以自由选择任何其他主题。我选择这个主题仅仅是为了演示，因为它是免费的，并且使用了 Substratum 的许多特性，是展示 Substratum 工具的绝佳选择。

从下面的 Play Store 链接下载到您的手机上。

安装完成后，请按照以下步骤进行安装:

1.  打开**底层应用**。
2.  在列表中查找“**波罗的语用户界面**”。选择它。
3.  有两种方法来安装这个主题。您可以点击顶部附近的切换按钮“**select to toggle all overlays**”，这将检查列表中的每个覆盖，或者您可以逐个选择每个覆盖。*注意:主题者目前建议你**不要选择列表中的“系统 UI QS 磁贴图标”或“系统 UI 状态栏图标”覆盖**，直到他能够修复它们。总是检查你安装的任何主题的 Play Store 描述，以获得特定主题的说明！*
4.  注意一些应用程序下面列出的一些**选项。例如，在“Android 系统”下有 3 个下拉菜单，分别是 Android 框架的强调色、基色和背景色。如果您展开下拉菜单，您可以从许多选项中选择自定义主题。**
5.  一旦你选择了你想要的应用程序，点击右下角的**油漆桶浮动按钮**。
6.  点击**构建&启用**您将看到一个屏幕，告诉您正在编译和安装哪些主题。过一会儿，它应该会无错地完成。

几秒钟后，主题将被编译、安装并立即应用。享受你的新主题吧！

### 第 3 部分-如何卸载主题

1.  如果你注意到一些看起来奇怪的东西，或者你想禁用主题来尝试另一个，那么回到主底层页面，在侧边栏菜单中打开“**恢复**”。
2.  点击**恢复主题**。
3.  选择**禁用所有已启用的覆盖**或**卸载所有已安装的覆盖**。选择禁用选项将使您的主题保持编译和安装状态，但不会再被应用。选择卸载选项会将它们从您的设备上完全删除。如果你想修复一个损坏的主题，这两种方法都可以！

### 第 4 部分-我可以用底层做什么？

我们有一系列的教程，旨在展示一些你可以用 Substratum 做的不仅仅是主题的很酷的事情。现在你已经知道了如何设置仙女座服务和安装一个主题，试着按照这些指南去做吧！

### 结论

《底层》最棒的地方在于，你不仅仅局限于一个单一的主题。如您所见，我们能够启用主题包中的一个或所有覆盖。你可以利用这一点，甚至混合和匹配游戏商店的底层主题。因此，举例来说，你可以用一个主题包调整视频链接，而用另一个主题包调整 Gmail。这完全取决于你想如何主题你的手机！

Substratum 应用程序中甚至还有其他漂亮、更高级的选项，如[浮动 UI](https://www.xda-developers.com/substratum-introduces-floatui-a-per-app-theming-solution/) 和设置主题优先级的能力。你可以玩其中的一些，但它们是针对那些想要完全控制他们的设备主题的铁杆主题玩家。如果这就是你，那就试试吧！

通过我们的[底层论坛](https://forum.xda-developers.com/apps/substratum)或使用 XDA 实验室应用程序关注 XDA 门户网站，了解最新的底层新闻。