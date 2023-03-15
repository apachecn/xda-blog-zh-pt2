# 如何访问 Facebook Messenger 的隐藏内部菜单

> 原文：<https://www.xda-developers.com/facebook-messenger-internal-menu/>

Facebook Messenger 中隐藏的内部菜单被脸书的开发者用来在测试期间修改应用程序的某些方面。用户通常无法打开它，因为隐藏的菜单活动无法在应用程序中直接访问。然而，如果你的设备有 root 权限，那么就可以进入这个内部菜单，使用脸书工程师使用的一些隐藏的开发/调试工具。以前，访问内部菜单可以用来[禁用信使日](https://www.xda-developers.com/disable-facebook-messenger-day-android/)，尽管脸书意识到人们正在这样做，因此禁用了关闭信使日的功能。

 <picture>![](img/9747f0435e251333f18e4ff95a574fb6.png)</picture> 

Error message when attempting to disable Messenger Day in "MobileConfig"

尽管如此，该应用程序的其他方面并不在 MobileConfig 中，我们可以尝试一下。我们将向您展示如何访问该菜单，以便您可以查看可以更改的内容，我们还将提供一些示例，说明您可以在 Facebook Messenger 的内部菜单中执行的一些操作。

您需要在设备上安装 Android 调试桥(ADB)或终端应用程序，如 [Termux](https://play.google.com/store/apps/details?id=com.termux&hl=en) 才能继续。如果使用 ADB，需要在手机上启用 USB 调试。要这样做，打开设置，然后导航到“关于手机”，并反复点击建立号码，直到它告诉你是一个开发者。按下返回按钮，你现在将有“开发者选项”在设置列表中。向下滚动并启用 USB 调试。

本指南需要 root 用户。解锁设备的引导程序后，你可以通过闪烁 [Magisk](https://forum.xda-developers.com/apps/magisk) 或 [SuperSU](https://forum.xda-developers.com/apps/supersu) 来获得 root。如果你的设备没有 root，你可以使用来自 XDA 成员 [evilwombat](https://forum.xda-developers.com/member.php?u=5029215) 的[这款修改过的 APK](https://forum.xda-developers.com/android/apps-games/bullshified-version-facebook-okay-to-t3586318) ，它可以让你直接在应用程序中访问内部菜单。但是，如果你想使用的不仅仅是 Messenger，这样做需要你卸载你已经安装的任何现有的脸书应用，而是使用来自同一个开发者的所有修改过的脸书应用。

* * *

### 使用亚行

下载 adb，要么在 XDA 下载"[最小 ADB & Fastboot](https://forum.xda-developers.com/showthread.php?t=2317790) ，要么下载谷歌发布的[官方二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)。提取它们，在包含 adb 的文件夹中，按住 shift +右键单击文件夹，然后单击“在此打开命令窗口”。将您的电话连接到 PC，并授予调试权限。

接下来，在命令提示符下键入以下命令。

```
 adb shell 
```

```
 su 
```

出现提示时授予超级用户访问权限。

```
 am start -n "com.facebook.orca/com.facebook.messaging.internalprefs.MessengerInternalPreferenceActivity" 
```

然后向下滚动。

### 使用终端

打开您选择的终端应用程序。我用的是 [Termux](https://play.google.com/store/apps/details?id=com.termux&hl=en) ，但是任何能接入终端的都可以正常工作。接下来键入以下命令。

```
 su 
```

出现提示时授予超级用户访问权限。

```
 am start -n "com.facebook.orca/com.facebook.messaging.internalprefs.MessengerInternalPreferenceActivity" 
```

* * *

执行完命令后,“内部菜单”应该会显示如下所示的菜单。

向下滚动到“网关守护设备覆盖”点击它，在下面的菜单中点击“搜索门卫”。键入“ **internal** ”(不带引号)并点击显示“messenger _ internal _ prefs _ Android”的字段。它应该改变说是。

就是这样！现在，您可以永久访问该菜单，位于下面的屏幕截图中。

### 说明

我们使用 adb 或终端来启动`MessengerInternalPreferenceActivity`，它是隐藏的内部菜单活动。然后，我们在内部菜单中编辑应用程序设置，以永久显示用于访问该活动的菜单项。我们需要 root 访问权限的原因是，这个活动是在 Facebook Messenger 应用程序的 AndroidManifest 中定义的未导出活动。未导出的活动需要提升权限才能启动，但一旦启动，我们就可以从菜单中启用它。

* * *

### 猛撞

如果出于某种原因你想让应用程序崩溃(也许你正在测试你所做的一些系统编辑)，内部菜单在“**性能和配置”下包含 4 种崩溃类型。**

### 语言

如果你想在 Facebook Messenger 中自己选择语言，在内部菜单根目录的“**子系统**”下有一个选项，可以将应用程序语言更改为你想要的任何语言。

### 总是启用聊天头

当您打开 Facebook Messenger 时，您当前打开的聊天标题会消失。如果您希望在已经使用 Facebook Messenger 的情况下也能使用聊天标题，您可以启用“功能”下的“**不要隐藏 messenger** ”。

就是这样！浏览一下设置，看看你是否能在 Facebook Messenger 中找到一些东西，如果有，请在下面的评论中告诉我们！