# 如何在播放音乐时向导航栏添加媒体播放控件

> 原文：<https://www.xda-developers.com/how-to-add-media-playback-controls-to-the-nav-bar-when-playing-music/>

自从谷歌首次将软件导航键的概念引入 Android 以来，用户一直在寻求一种定制用户可用键的方法。尽管定制 rom 多年来一直提供这种级别的定制，但只有在第一次 Android O 开发者预览版中，我们才能找到谷歌修改导航条的官方方法。然而，像它之前的许多功能一样，这个导航条调谐器不是凭空出现的，实际上是在秘密测试 Android 牛轧糖。然而，直到最近，我们才发现 Android 牛轧糖[中隐藏的导航条调谐器实际上不需要 root 访问、自定义 ROM 或系统 UI 模块](https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/)就可以访问。因此，一个新的无根定制的途径为许多用户打开了，今天我们将引导你通过一个流行的请求:**如何在播放音乐时添加媒体播放控制到导航条(Android 7.0+，不需要根！)**

正如你在上面的屏幕截图中看到的，我的测试设备(一个在 Android 7.0 Nougat 上的未启动、引导加载程序锁定的 Google Nexus 6 设备)具有标准的导航条键集，直到在 Google Play Music 中启动音乐播放。当音乐播放开始时，两个新键被添加到导航条:一个按钮播放上一首曲目，一个按钮播放下一首曲目。这些键会一直留在导航条上，直到我关闭 Google Play 音乐通知——这样，我仍然可以在保留这些播放控制键的同时使用手机的其他应用程序，直到我决定不再听音乐。

虽然我上面的屏幕截图显示这种设置用于 Google Play 音乐，但这可以很容易地修改为适用于几乎所有的音乐、播客或广播应用程序——只要该应用程序在播放期间显示通知并接受媒体上一页/下一页键(两者都很有可能)。本教程对我的针对 Android O 用户的[原始教程](https://www.xda-developers.com/how-to-enable-media-playback-nav-bar-controls-in-android-o-when-playing-music/)稍作修改，然而，更多的用户将能够利用本教程，因为它不限于运行 Android O 开发者预览版的用户。话虽如此，我们还是开始吧。

* * *

### 要求

**系统** **需求**:你需要一个兼容 AOSP 导航条定制器的 Android 7.0+设备。已知谷歌 Nexus、Pixel 和一些索尼/HTC 手机可以工作。大多数接近库存 Android 的设备很可能没有删除 AOSP 导航条定制器，应该可以工作。这意味着它可能无法在你的 LG、三星或华为/Honor 设备上运行。见本帖第一篇[的“兼容性”部分。(注意:您设备的 OEM 可能没有列在该线程中。要确定你的设备是否兼容，唯一的方法就是试用这个应用程序，我们将在下面告诉你怎么做。)](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)

**App 需求:**

### 设置:自定义导航栏

我们需要自定义导航条的原因很明显——这个应用程序允许我们修改导航条来显示这些媒体播放键。(从技术上来说，我们实际上并不需要这个应用程序来进行这些修改，因为我们可以使用 shell 命令或其他 Tasker 插件，但是为了让我们的用户更容易，我们将展示如何使用这个精彩的应用程序进行设置。)需要通知监听器来监视状态栏上发布了什么通知，这样我们就知道音乐播放开始和结束的时间。最后，Tasker 是一个自动化应用程序，它在通知监听器和自定义导航栏之间架起了一座桥梁——它使用通知监听器来检测音乐何时开始/结束，然后触发自定义导航栏来相应地改变导航栏。

我们需要做的第一件事是确保你可以修改你设备上的导航条。如果你的设备是在[自定义导航栏线程](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967/)中列出的兼容设备之一，那么它很有可能是兼容的。我们可以通过运行这个应用程序附带的简短教程来验证。

从谷歌 Play 商店安装应用[，然后打开应用并继续进入介绍性屏幕。自定义导航栏将要求您授予它一个名为 WRITE_SECURE_SETTINGS 的特定权限，以便继续使用该应用程序。有两种方法可以做到这一点，如申请中所述。](https://play.google.com/store/apps/details?id=xyz.paphonb.systemuituner)

1.  如果您有根设备，自定义导航栏将请求超级用户访问。授予它，应用程序将自动授予自己此权限。
2.  如果您的设备不是根设备，那么您需要通过 ADB 授予许可。在机器上打开命令提示符/终端，然后输入以下命令:`adb shell pm grant xyz.paphonb.systemuituner android.permission.WRITE_SECURE_SETTINGS`

一旦你通过上述两种方法中的任何一种授予应用程序此权限，那么应用程序将继续进行兼容性测试。如果你的导航条没有变化，那么你很不幸的不走运。如果你的导航条变成显示一个右箭头按钮，那么恭喜你的设备是受支持的！我们现在可以继续修改我们的导航栏。

### 设置:通知监听程序

为了让通知侦听器拦截通知，我们必须授予它一个特殊的权限，称为“通知访问”权限。该权限不是通过标准的权限对话框授予的，而是需要由用户通过特殊的设置菜单授予的。幸运的是，这很容易做到。只需打开通知监听器应用程序，该应用程序就会让您启用此权限。只需按下按钮，应用程序将带您到您可以授予应用程序此权限的屏幕。启用应用程序的通知访问。

* * *

### 辅导的

一旦您确认了自定义导航栏与您的设备兼容，并且为通知监听器启用了通知访问，就该进行设置了。我们需要做的第一件事是在自定义导航栏中创建一个新的配置文件，当启用时，将在我们的导航栏中添加一个上一页/下一页键。以下是逐步说明:

1.  打开自定义导航栏，点击自动化部分下的**配置文件**。
2.  点击右上角的 **+** 图标，添加新的个人资料。
3.  点击刚刚创建的个人资料。
4.  在个人资料部分，点击**名称**来命名个人资料。将其命名为**媒体控制**。
5.  在“额外左按钮”部分下，按下**键，输入**。选择**键码**作为类型。
6.  现在，在“额外的左按钮”部分，你会看到两个额外的选项。点击**键码**。
7.  向下滚动并找到**媒体上一个**键。
8.  现在点击“额外左按钮”下的**图标**对于图标，选择**跳过之前的**。
9.  重复步骤 5-8，但“额外的右按钮。”然而，这一次，键码将是**媒体下一个**，图标将是**跳过下一个**。
10.  通过向上滚动并检查**启用**来测试您的档案。如果您在底部看到上一个/下一个导航条键，则此配置文件有效！

现在我们已经设置了自定义导航栏配置文件，我们将创建我们的 Tasker 配置文件，它将在音乐播放时启用/禁用此配置文件。首先，我们将创建当我们的音乐/播客/广播应用程序发布通知时触发的配置文件。以下是逐步说明:

1.  打开 Tasker，点击右下角的+图标创建一个新的个人资料。
2.  选择**事件**上下文。
3.  点击**插件**。
4.  选择**通知监听器**插件。
5.  选择弹出的**通知监听器**动作。
6.  点击铅笔图标打开通知监听器的配置。
7.  将通知事件保留为**已发布**，但在应用程序下选择您想要监控的应用程序。例如，我在这里选择了 Google Play 音乐。完成后，点击右上角的勾号图标。
8.  回到 Tasker，按左上方的返回箭头键返回 Tasker 的主屏幕。
9.  Tasker 会要求您将任务附加到我们刚刚创建的个人资料中。选择以创建新任务。不要为任务命名。
10.  一旦你进入 Tasker 的任务编辑界面，点击底部中间的+按钮添加一个新的动作。
11.  从动作类别中选择**插件**。
12.  选择**自定义导航栏**插件。
13.  再次点击铅笔图标，这一次会将我们带到自定义导航栏的配置页面。
14.  对于该操作，将其保留为“**启用配置文件**”在选择配置文件下，选择**媒体控制**。完成后点击右上角的勾号。
15.  按 back，然后再按一次 back，直到你在 Tasker 的主屏幕。

我们创建的上述 Tasker 配置文件将激活媒体控制自定义导航栏配置文件，以便在媒体播放开始时添加媒体播放键，但现在我们需要在关闭媒体应用程序的通知时禁用媒体控制配置文件。以下是说明:

1.  创建一个新的概要文件并选择**事件**上下文。
2.  进入**插件- >通知监听器- >通知监听器**。
3.  在“通知事件”下这次选择**移除**。再次选择您要监控的相同应用程序。我在这里选择了 Google Play 音乐。完成后轻按勾号。
4.  返回到 Tasker 的主屏幕，它会要求您添加一个任务到这个新的配置文件。添加一个任务，但是不要命名它。
5.  进入 Tasker 的任务编辑屏幕后，添加一个新动作。进入**插件- >自定义导航栏**。
6.  这一次“操作”选择**禁用配置文件**，但再次选择**媒体控制**配置文件。完成后，轻按顶部的勾号按钮。
7.  退出任务，回到 Tasker 的主屏幕。

当您创建了两个 Tasker 配置文件，一个用于发布媒体应用程序的通知，另一个用于删除相同的通知时，您就完成了。每当媒体播放开始时，Tasker 会在你的导航条上显示媒体播放键，当媒体播放结束时，会清除导航条上的这些键！

* * *

### 使用 Shell 命令

鉴于使用 XDA 资深会员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) 的[定制导航栏](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)应用程序是如此简单，我真的不认为有必要提供详细的分步说明，说明如何使用其他 Tasker 插件，如 [SecureTask](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967) 或[自动工具](https://play.google.com/store/apps/details?id=com.joaomgcd.autotools&hl=en)(或 Tasker 中的 run shell 功能)。然而，这当然是可能的，至少我会提供一个不使用 paphonb 的应用程序复制这个设置所需的命令的摘要。

您需要做的第一件事是安装 SecureTask 或 AutoTools。您将需要授予 WRITE_SECURE_SETTINGS 权限来控制您选择的应用程序，以便控制导航栏调谐器。

对于 SecureTask:

```
 adb shell pm grant com.balda.securetask android.permission.WRITE_SECURE_SETTINGS 
```

对于自动工具:

```
 adb shell pm grant com.joaomgcd.autotools android.permission.WRITE_SECURE_SETTINGS 
```

接下来，您需要下载将用于上一个/下一个键的图标。你将需要 PNG 格式的图标，至于大小，你可以通过在 Material.io 上查找你的[设备的显示密度指标并将其与](https://material.io/devices/)[图标大小参考图表](http://iconhandbook.co.uk/reference/chart/android/)相关联来确定你需要的图标大小。IconsDB.com 是免费图标的好资源。将您将要用作 previous.png 和 next.png 的图标保存在存储根目录下的/NavIcons 文件夹中。

最后，您将输入以下命令来显示媒体控制按钮:

```
 settings put secure sysui_nav_bar "key(88:file:///storage/emulated/0/NavIcons/previous.png),back;home;recent,key(87:file:///storage/emulated/0/NavIcons/next.png)" 
```

其中键#88 指[键码 _ 媒体 _ 上一个](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_MEDIA_PREVIOUS)，键#87 指[键码 _ 媒体 _ 下一个](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_MEDIA_NEXT)。

然后将导航条键恢复到默认布局(即当您刷走媒体回放通知时)，请输入以下命令:

```
 settings put secure sysui_nav_bar "space,back;home;recent,menu_ime" 
```

本质上，Tasker 配置文件的设置将与上述通知监听程序的配置完全相同，不会改变。但是如果你选择不使用自定义导航条 app 来控制导航条，那么你可以使用上面两个 shell 命令作为替代。请注意，除非您是 rooted 用户并使用 Tasker 中的“run shell”操作，否则将这些命令导入 SecureTask 或 AutoTools 的过程完全由您决定。这真的不难做到，但许多用户发现只使用 paphonb 的应用程序更容易使用，所以我不会在这里进行更多的细节。

* * *

### 结论

本教程到此为止。在未来的教程中，我将展示更多改变导航条的潜在实际用途，特别是在使用自动化应用程序如 Tasker 的情况下。

请尽你所能支持 XDA 开发者！我们最近发现，有几个博客剪切、复制、粘贴了我们的原始教程和我们的用户在论坛上分享的其他内容。这些博客一直试图将我们在编写这些教程中所做的大量努力归功于自己，而不是自己提供高质量的内容。你不会在我们的[教程类别](https://www.xda-developers.com/category/tutorials/)中找到这样的教程，也不会在其他地方找到来自我们论坛的教程。

在推特、[谷歌+](https://plus.google.com/+xda) 、[脸书](https://www.facebook.com/xda.developers/)或 [YouTube](https://www.youtube.com/user/xdadevelopers) 上关注我们。查看我们的 [XDA 实验室](https://www.xda-developers.com/xda-labs/)应用程序，快速浏览我们的论坛(并考虑获得 [XDA 无广告](https://forum.xda-developers.com/ad-free/)！)上，如果你有一台 OnePlus 3 或 OnePlus 3T，请查看我们最近发布的 [XDA Feed](https://www.xda-developers.com/introducing-xda-feed/) 应用程序！谢谢，请继续关注我们的下一个教程！