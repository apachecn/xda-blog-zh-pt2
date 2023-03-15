# 如何在没有 Root 用户的情况下启用全系统沉浸式模式

> 原文：<https://www.xda-developers.com/how-to-enable-system-wide-immersive-mode-without-root/>

随着手机屏幕变得越来越大，有时我们希望隐藏状态栏和导航栏，这样我们就可以使用整个清晰、漂亮的高清屏幕来查看我们的内容。

从 Android 4.4 开始，应用程序可以实现[沉浸式模式](https://developer.android.com/training/system-ui/immersive.html)，真正为最终用户带来全屏体验。不幸的是，谷歌和原始设备制造商从来没有让用户手动控制何时启用沉浸式模式。一个名为 [GMD 全屏沉浸式模式](https://play.google.com/store/apps/details?id=com.gmd.immersive&hl=en)的第三方应用程序已经提供了几年的解决方案，但使用这个应用程序的最大问题是它会破坏软键盘。

用户使用 ADB 命令触发系统范围的沉浸式模式已经有一段时间了，但多年来人们一直认为，从 ADB 终端上拔下插头时使用该命令需要 root 访问权限。然而，去年年底用户发现，如果应用程序有一定的权限，某些 ADB 命令实际上可以在没有 root 访问权限的设备**上触发。这意味着你可以根据需要**启用全系统沉浸式模式****。例如，你可以创建一个牛轧糖磁贴来切换沉浸式模式，甚至可以基于每个应用程序设置沉浸式模式。****

 *** * *

## 切换无根的沉浸式模式

正如你在上面的视频中看到的，我已经创建了一个牛轧糖磁贴，当我按下它时，它会切换沉浸式模式。这是在我的非 root 华为 Mate 9 上，但它应该可以在几乎所有 Android 4.4+设备上工作。你只需要两个应用程序就能完成这项工作: [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en) 和 [AutoTools Beta](https://joaoapps.com/beta-testing/) 。如果你想用这个做一块牛轧糖砖，你还需要安装[自动通知](https://play.google.com/store/apps/details?id=com.joaomgcd.autonotification&hl=en)，但这不是必需的。

一旦您安装了这两个应用程序，您将需要授予自动工具 **WRITE_SECURE_SETTINGS** 权限，以便能够切换沉浸式模式(在其他令人敬畏的设置中，我们将在稍后介绍)。这是因为沉浸式模式的命令是在**设置下定义的。Global** 类，尽管该命令的确切语法隐藏在 AOSP。我们将首先讨论如何向自动工具授予必要的权限，然后讨论如何在 Tasker 中使用该命令。

* * *

在 Android 的权限管理系统下，应用程序在清单文件中定义它们希望被授予的权限。然后，用户可以授予或拒绝安装权限(前棉花糖)或按需权限(棉花糖+)。但是，有些权限是应用程序即使在清单中请求也不能被授予的，比如 [WRITE_SECURE_SETTINGS](https://developer.android.com/reference/android/Manifest.permission.html#WRITE_SECURE_SETTINGS) 。这是因为授予任何应用程序如此强大的权限都会让该应用程序对您的设备进行大量控制。

但是有一个解决方法，我们可以使用它来授予任何我们想要的应用程序 WRITE_SECURE_SETTINGS 权限。通过使用 ADB 的[包管理器(pm)](https://developer.android.com/studio/command-line/adb.html#pm) 工具，我们可以向任何我们想要的应用程序授予任何权限(假设应用程序在清单文件中请求该权限)。

你需要做的第一件事是[将 ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)安装到你的电脑上，然后为你的设备安装[正确的驱动程序。然后，在开发者选项中启用 USB 调试(进入设置- >关于手机，如果你还没有的话，点击 7 次内部版本号)，将手机连接到电脑上。最后，打开终端后，发送以下命令:](https://developer.android.com/studio/run/oem-usb.html)

`adb shell pm grant com.joaomgcd.autotools android.permission.WRITE_SECURE_SETTINGS`

现在，自动工具将能够更改您设备上的任何全局、安全或系统设置。有各种方法可以使用这些设置，每个类别中的可用设置列表完全取决于您的设备和软件版本，但这一讨论将在其他时间进行。无论如何，我们将继续向您展示如何使用自动工具来切换沉浸式模式。

* * *

### 使用 Tasker 通过牛轧糖磁贴切换沉浸式模式

通过磁贴切换沉浸式模式显然需要 Android 牛轧糖，所以如果你没有牛轧糖，那么跳过这一部分，了解如何在每个应用程序的基础上切换它。如果您还没有，请从谷歌 Play 商店下载 AutoNotification 并授予其通知访问权限。这个 Tasker 插件是我们将用来制作自己的定制通知磁贴的。

这是对熟悉 Tasker 的人的简介描述。如果你对 Tasker 不太熟悉，请继续阅读逐步说明。

### 牛轧糖瓷砖沉浸式模式切换

```
 Profile: Toggle Immersive Mode (30)
Event: AutoNotification [ Configuration:Event Behaviour
Filter: immersivemode ]
Enter: Immersive Mode (33)
A1: AutoNotification Tiles [ Configuration:Tile: 1
Command: immersivemode
Label: Immersive mode
Icon: /storage/emulated/0/Tasker/immersive.png
State: 999 Timeout (Seconds):60 ]
A2: AutoTools Secure Settings [ Configuration:Immersive Mode: Toggle Timeout (Seconds):60 ] 
```

打开 Tasker，按下右下角的 **+** 按钮。创建一个**事件**上下文并选择**插件- >自动通知。**点击铅笔图标打开自动通知的配置页面。在**命令过滤器**下输入 **immersivemode** 。这就是当我们点击一块牛轧糖砖时发出的确切命令。

现在创建一个附加到这个概要文件的新任务(使用任何名称)，第一个操作是进入**插件- >自动通知- >图块**。对于图块编号，选择第一个图块。对于**命令**，输入**沉浸模式**完全按照写的。标签将显示在磁贴下，因此将其命名为“沉浸式模式”对于**图标**，将我在本节开始时附加的图标保存到您的内部存储器中并使用。最后对于**状态**选择**切换激活/非激活。**

完成后，运行该任务一次(按下任务创建屏幕左下角的播放按钮),以便填充图块。现在，一旦您展开可用通知窗口列表，您应该会看到新的沉浸式模式切换。

* * *

### 使用 Tasker 在每个应用程序的基础上切换沉浸模式

在每个应用程序的基础上切换沉浸式模式非常简单，我们需要做的就是在 Tasker 中创建一个应用程序上下文，当应用程序启动或关闭时，它将触发，当它这样做时，沉浸式模式将被切换。为了让 Tasker 监控应用程序，您需要启用它的**辅助功能服务**。

这是对熟悉 Tasker 的人的简介描述。如果你对 Tasker 不太熟悉，请继续阅读逐步说明。

### 每应用沉浸式模式

```
 Profile: Per-App Immersive Mode (192)
 Application: Chrome or XDA Labs
Enter: Anon (199)
 A1: AutoTools Secure Settings [ Configuration:Immersive Mode: Toggle Timeout (Seconds):60 ] 

Exit: Anon (204)
 A1: AutoTools Secure Settings [ Configuration:Immersive Mode: Toggle Timeout (Seconds):60 ] 
```

您首先要打开 Tasker，因为我们将创建一个配置文件，以便在某些应用程序打开时启动沉浸式模式。打开 Tasker，按右下角的 **+** 按钮，创建一个新的个人资料。对于上下文类型，选择**应用**，并选择您希望沉浸式模式处于活动状态的所有应用。

完成后，按 back，Tasker 会要求您创建一个任务。不需要命名任务，所以只需按下复选标记就可以开始创建任务。一旦进入任务创建屏幕，您只需要添加一个操作。按下底部的 **+** 按钮，进入**插件- >自动工具- >安全设置**。按铅笔图标配置自动工具。在这里，转到**显示屏**，然后点击**沉浸式模式**，选择**切换**

我们还需要做最后一件事，那就是在退出应用程序时禁用沉浸式模式。回到 Tasker 的主屏幕，在你刚刚创建的任务上长按，这样你就可以创建一个**退出任务**。当您创建一个退出任务时，只需添加您在第一个任务中添加的相同动作——这将切换沉浸式模式。

* * *

### 微调沉浸式模式

正如我之前提到的，强制沉浸式模式可用的确切命令可以从 AOSP 收集[。通过发出以下命令之一，您可以将沉浸式模式设置为仅隐藏通知栏或仅隐藏导航栏:](https://android.googlesource.com/platform/frameworks/base.git/+/master/services/core/java/com/android/server/policy/PolicyControl.java)

`settings put global policy_control immersive.status=*`

设置将全局策略控制融入其中。navigation=*

当然，AutoTools 实际上并不允许您像这样直接发送 shell 命令，而是使用它的接口发送命令。只需在 AutoTools 安全设置中选择“自定义设置”，将设置类型设置为“全局”，将“输入类型”设置为“字符串”，对于名称，您必须输入“policy _ control immersive . status = *”或“policy _ control immersive . navigation = *”。如果您更喜欢沉浸式模式，隐藏状态栏或导航栏，您可以使用此命令来代替我们用于 Nougat Tile 或每个应用程序控件的命令。

* * *

## 下载并导入 Tasker

一如既往，我们提供了脚本的 XML 文件，您可以下载和导入。只需从下面的链接下载文件，并将其保存在您的内部存储的任何地方。打开 Tasker，在首选项中禁用初学者模式。然后，回到主屏幕，长按顶部的“个人资料”标签。您应该会看到一个弹出窗口，其中一个选项是“导入”点击它，浏览到保存. prf.xml 文件的位置，并选择要导入的文件。

如果您选择导入通知磁贴 1，请确保将沉浸式模式图标保存为 Immersive，并将其保存到/sdcard/Tasker。如果您选择导入每个应用程序的配置文件，那么请确保您进入并自定义它将触发的应用程序，因为我的示例设置为仅在使用 Chrome 或 XDA 实验室时触发。

[**下载通知平铺沉浸式模式切换**](https://www.androidfilehost.com/?fid=457095661767138543)

[**下载每个应用的沉浸式模式切换配置文件**](https://www.androidfilehost.com/?fid=673368273298932602)

我们希望这个提示对你有用。如果这对你有用，请在下面的评论中告诉我们！**