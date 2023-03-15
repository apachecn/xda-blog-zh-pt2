# Andromeda Add-on for Substratum 为 Android Oreo 带来定制主题

> 原文：<https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/>

谷歌 Android 操作系统最常要求增加的功能之一是主题支持。索尼、华为和三星等公司的 Android 设备都支持自定义主题。然而，谷歌 Nexus 和 Pixel 系列设备上的股票 Android 粉丝一直无法对他们的设备进行主题化，至少没有 root 或自定义 ROM 是不行的。但正如我们上个月末发现的那样，对索尼设备中相同主题引擎的完全支持实际上在 Android Oreo 的官方版本中也可以得到。在过去的两周里，流行的 Substratum 主题引擎背后的团队一直在努力工作，在无根的 Android Oreo 设备上获得自定义主题，我们自豪地宣布**Android Oreo 中的无根自定义主题支持现已对所有**可用。

* * *

## 欢迎来到“仙女座”，Substratum 的安卓奥利奥无根插件

### 仙女座菌株是什么？

仙女座菌株(不要与传言中的 Android/Chrome OS 合并混淆)是 Substratum 主题引擎新附加包的官方名称。它既是一个必须安装在手机上的 Android 应用程序，也是一个配套的桌面客户端，以便 Substratum 应用程序能够工作。Andromeda 桌面客户端使用脚本和 ADB 访问来提升手机上 Andromeda 应用程序的权限，以匹配 ADB 外壳的权限。一旦发生这种情况，Substratum 应用程序就可以使用它需要的命令，如“ [cmd overlay](https://www.xda-developers.com/android-oreo-command-line-themes/) ”和“pm install”，以便在你的手机上编译和安装主题。

迷茫？别担心。开发者已经使安装变得足够简单，以至于你不需要真正理解它是如何工作的。无论如何，您可能只关心最终结果，结果可能是这样的:

*之前:安卓奥利奥的股票，轻 UI*

*After: Android Oreo 通过底层使用深色 UI*

### 这是如何工作的？

如果你真的有兴趣了解这是如何工作的，我推荐你通读一下[原始文章](https://www.xda-developers.com/android-oreo-rootless-system-theme/)，在那里我们非常详细地描述了这个开发的构建。此外，我们还整理了一份[冗长的 FAQ](https://www.xda-developers.com/video-rootless-substratum-theme-engine-android-oreo/) (常见问题)，应该可以回答你关于这个项目的任何问题。

### 我能做什么主题？

我已经在一个封闭的测试中测试了无根底层，结果非常棒。下面是我在运行 Android Oreo 的非 root 设备上定制的一个小清单:

*   [**全系统黑暗主题**](https://www.xda-developers.com/install-dark-theme-android-oreo-without-root/) ，包括设置、快速设置磁贴、通知、提醒/对话框/吐司窗口等。
*   **每个应用的主题**，比如黑暗商店/Twitter/Messages，或者将 Hangouts 应用中的所有绿色改为蓝色
*   [**最小锁屏**](https://www.xda-developers.com/minimal-lock-screen-rounded-recent-app-more-quick-setting-columns-android-oreo/) **，**它允许我隐藏状态栏和所有快捷图标来炫耀我漂亮的锁屏壁纸
*   [**自定义导航条图标**](https://www.xda-developers.com/customize-navigation-bar-icons-android-oreo/) ，我能够挑选出大量可用的导航条图标包，比如三星 Galaxy S8/S8+上的那种
*   [**Whatsapp/Telegram blob 表情符号**](https://www.xda-developers.com/blob-emojis-whatsapp-telegram-android-oreo/) ，换句话说，可以根据应用程序改变字体/表情符号
*   [**Whatsapp 聊天泡泡主题**](https://play.google.com/store/apps/details?id=com.thepsycraft.wabubblesub)**因为为什么不呢？底层主题的强大之处在于，你甚至可以定制单个应用的小方面。**
***   [**圆角最近的**](https://www.xda-developers.com/minimal-lock-screen-rounded-recent-app-more-quick-setting-columns-android-oreo/) **，**可以圆角最近的 app 屏幕缩略图。*   [**改变快速设置磁贴的列数**](https://www.xda-developers.com/minimal-lock-screen-rounded-recent-app-more-quick-setting-columns-android-oreo/) ，而不是只有 3 列我可以自定义它有更多或更少。**

 ***底层调整前/后截图。请阅读末尾，了解如何获得这些主题的指南！*

这正是我，一个相对来说对底层主题化世界的新手，所能尝试的。多亏了 Substratum，现在非 root 用户可以使用的主题化的可能性大大增加了。Substratum 是一个相当小众的项目，因为它需要用户安装一个自定义的 ROM 来支持它，但现在 Android 8.0 Oreo 已经内置了自定义主题支持，这将会改变。

一个全新的定制主题世界将为任何一个有幸在自己的设备上安装了 Android Oreo 的用户打开。随着用户数量的增加，越来越多的开发者会对这个项目感兴趣，给用户越来越多的主题选择。我们很高兴看到这个项目的未来，并将在未来很长一段时间内对它进行更新。

### 什么设备支持新的无根底层主题引擎？

任何现有的 Android 8.0 Oreo 设备都可以使用这个新版本的无根底层来主题化他们的设备。目前包括谷歌 Nexus 5X、谷歌 Nexus 6P、谷歌 Pixel 和谷歌 Pixel XL。任何拥有安卓奥利奥非官方端口的[设备都可以在没有 root 的情况下享受自定义主题。在未来，我们怀疑来自摩托罗拉、HTC、](https://www.xda-developers.com/list-android-oreo-unofficial-ports/)或索尼等原始设备制造商的许多设备在推出他们对 Android Oreo 的官方软件更新时，也会支持 Substratum 主题引擎。像三星或 LG 这样的其他制造商更是一个谜，因为不能保证他们会进行必要的改变。然而，这并不意味着它不会发生。

至于仙女座桌面客户端，它支持任何 **Windows、Mac、**或 **Linux** 电脑。你不需要**已经安装了 ADB**来工作，因为桌面客户端已经预打包了 ADB 二进制文件。

### 要花多少钱？

当我们第一次宣布这个新版本的 Substratum 将是一个付费的附加软件时，我们没有想到会有如此多的支持。许多人高度期待这个定制主题引擎的发布，相信它会值 10-20 美元。但它的成本不会接近这个数字。带来无根底层自定义主题支持的仙女座附加组件将只需****2.49 美元，限时 1.99 美元！****

 **这么低的价格不是你们中的许多人所期望的，而且考虑到你们所得到的价值，这看起来像是一笔大买卖。那是因为它是——如果你不相信我的话，就向上滚动看看你可以用 Substratum 实现的调整列表。

### 我能在哪里得到它？

Andromeda 桌面客户端的官方 XDA 论坛主题是这个新项目的主页，在这里你可以找到桌面客户端的最新安装文件。至于 Substratum 和 Andromeda 附加 Android 应用程序，您可以通过下面的链接找到它们:

### 我如何安装和使用 Andromeda 的基质？

我们已经写了一份官方指南，一步一步地引导你完成这个过程。您可以在下面的列表中找到该指南，以及我们为定制您的手机而编写的其他指南:

### 我在哪里可以获得自定义主题？

在谷歌 Play 商店寻找[底层](https://play.google.com/store/apps/collection/search_results_cluster_apps?clp=ggEMCgpzdWJzdHJhdHVt:S:ANO1ljKAR64)。宣传支持 Substratum 或提及“OMS”(覆盖管理器服务)的主题可能适用于您的设备。

此外，如果你正在寻找主题设置/系统用户界面，请确保你专门寻找定制主题，声明它们是为 Android Oreo 构建的。你必须这样做的原因是，许多底层假设的自定义主题是为 Android Nougat 的系统 UI 设计的，然而，Android 8.0 的系统 UI 非常不同，因此需要主题更新他们的主题。你可以在这个[论坛的帖子](https://forum.xda-developers.com/apps/substratum/android-o-ready-themes-t3666473)中找到一份 Android 奥利奥主题的不错列表。

### 哪些主题不兼容？

提及“legacy”或“RRO”(运行时资源覆盖)的自定义主题在您的设备上不起作用。此外，您将无法使用 Play Store 上现有的底层主题进行以下操作:

*   更改启动动画
*   在系统范围内改变字体(尽管每个应用的字体/表情符号都可以改变)

基本上任何绝对需要 root 权限才能更改的事情都做不到，因为很明显你的手机没有 root。否则你一开始就不会用这个。

### 这在将来会继续得到支持吗？

是啊！底层从早期开始就经历了疯狂的发展。开发团队[非常专注于项目](https://www.xda-developers.com/an-interview-with-the-team-behind-the-substratum-theme-engine/)，由于这一新方向，对底层感兴趣的人数急剧增加。我们期待这个项目在未来会有很大的作为，也期待新的主题进入底层家庭。

喜欢这个项目？考虑捐给开发商！你可以通过这个链接找到尼古拉斯·查姆，通过这个链接找到伊万·伊斯坎达尔[。](https://www.paypal.me/IvanIskandar)

了解未来发展的最佳方式是关注[官方底层 XDA 论坛](https://forum.xda-developers.com/apps/substratum)。如果你喜欢被即将到来的特性戏弄，你也可以关注底层团队的个人开发者，比如首席开发者[尼古拉斯·查姆](https://plus.google.com/116845249995235969561)。最后，如果你只关心项目的主要更新，跟踪 Substratum 新闻的最好地方是 XDA 门户网站，最好通过移动设备上的 XDA 实验室应用程序阅读。****