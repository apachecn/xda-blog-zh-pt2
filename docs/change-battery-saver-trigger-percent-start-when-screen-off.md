# 如何自定义节电触发百分比或在屏幕关闭时启用它

> 原文：<https://www.xda-developers.com/change-battery-saver-trigger-percent-start-when-screen-off/>

提高设备的电池寿命是用户蜂拥至我们论坛的主要原因之一。在 XDA，你可以找到关于如何提高电池寿命的应用程序、内核、rom 和指南。然而，你很难找到一个通用的电池寿命技巧。

谷歌在 Android 5.0 Lollipop 中推出的一个名为“电池节省器”的功能就是一个电池节省工具的例子，几乎可以在任何 Android 设备上工作。启用电池保护时，会禁用背景数据、定位服务、振动、动画，并在必要时降低 CPU 性能。当你需要延长电池寿命时，这是一个很有用的功能，但默认情况下，该服务只有在电池电量为 5%，10%，15%或手动激活时才会激活。

如果您想要更改触发电池节电功能的电池百分比，该怎么办？或者您可能想在屏幕关闭时自动启用节电模式？当然，你可以使用快速设置开关或快捷方式来启用电池保护，但记住这样做可能是一个麻烦。在本教程中，我将向您展示如何修改电池节省的触发百分比，甚至自动启动功能的基础上，无论你想要的标准。

* * *

# 自定义电池节电器

就像 Android 上几乎所有的设置一样，只要你有适当的权限，这个属性是可以修改的。节电参数在[设置中定义。Global class](https://developer.android.com/reference/android/provider/Settings.Global.html) ，虽然你在那个页面上找不到文档，因为这个特性不能保证在每个设备上都存在。

然而，粗略地看一下 AOSP 或列出您设备上所有可用的设置，就会发现节电参数是在“ **low_power** 常量下定义的。它分别为“关”和“开”保存整数值“0”或“1”。节电模式的触发水平/百分比值由“ **low_power_trigger_level** 常量定义，该值为 1 到 100 之间的一个整数值。通过修改这两个参数中的任何一个，我们可以自己控制电池节电。

## 自定义电池节电触发电平

首先，我们将设置手动节电触发百分比/级别。对此有两种解决方案，第一种涉及修改 low_power_trigger_level 常量本身，以让 Android 系统自己处理启用/禁用电池节省器。为此，您只需发送一个简单的 ADB 命令。如果您的机器上已经安装了 ADB，请跳过下一节。如果没有，请继续阅读。

### 建立亚洲开发银行

首先，[直接从 Google](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/) 为您的特定操作系统下载 ADB 二进制文件，并将其解压缩到您计算机上的一个单独目录中。接下来，[为你的手机安装合适的驱动](https://developer.android.com/studio/run/oem-usb.html)。然后，在设置- >开发者选项中启用“USB 调试”。如果你看不到开发者选项，那么你需要进入设置- >关于手机，然后点击 7 次内部版本号来启用它。最后，通过在与 ADB 二进制文件相同的目录中启动命令提示符(右键单击->“open command prompt here”)并运行以下命令，确保 ADB 正在工作:

```
 adb devices 
```

如果你看到你的设备的序列号(它没有说未经授权)，你是黄金。如果你在手机上看到一个弹出窗口，要求你授予你的计算机 ADB 访问权限，那么就说是。如果你看不到这两种情况，那么试着重启你的电脑/手机，并重新连接到你的电脑上。否则，请尝试重新安装驱动程序。

### 自定义触发级别- ADB 方法

一旦 ADB 设置完毕，就该修改设置了。您所要做的就是输入一个命令，如下所示:

```
 adb shell settings put global low_power_trigger_level TRIGGER_LEVEL 
```

其中 TRIGGER_LEVEL 是您希望 Android 启用电池节电模式的电池电量(1-100%之间)。一旦设置完毕，请注意，如果您进入设置中的电池节电菜单，该值会自动重置(您不需要这样做，因为唯一的选项就是我们正在更改的内容)。

在下一节中，我将向您展示如何使用被称为 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en) 的流行自动化应用程序以及 [AutoTools Beta](https://joaoapps.com/beta-testing/) 插件来设置自定义触发级别。这种方法的好处是你也可以根据你想要的任何条件来启用电池保护，我们将在下面讨论。

* * *

### 自定义触发级别-任务方法

如果你熟悉 Tasker，上面的截图向你展示了我们基本上在做什么。在左边，有两个状态上下文，当满足时，Tasker 将启用电池节电。当这两种状态不再满足时，Tasker 将禁用节电模式。第一种状态是当前的电池电量，当电池电量在 1-25%之间时，此状态将被激活。第二种状态是当手机离开充电器时激活的，以确保无论如何充电时电池保护都不会激活。

上面的两个状态上下文不需要 Tasker 之外的任何东西就可以实现，但是为了让 Tasker 控制 Battery Saver，我们需要使用 AutoTools 插件。特别是，自动工具安全设置功能。但是，默认情况下，AutoTools 没有控制电池保护程序所需的适当权限，因此我们需要首先授予它该权限。

在 Android 的权限管理系统下，应用程序在清单文件中定义它们希望被授予的权限。然后，用户可以授予或拒绝安装权限(前棉花糖)或按需权限(棉花糖+)。但是，有些权限是应用程序即使在清单中请求也不能被授予的，比如 [WRITE_SECURE_SETTINGS](https://developer.android.com/reference/android/Manifest.permission.html#WRITE_SECURE_SETTINGS) 。这是因为授予任何应用程序如此强大的权限都会让该应用程序对您的设备进行大量控制。

但是有一个解决方法，我们可以使用它来授予任何我们想要的应用程序 WRITE_SECURE_SETTINGS 权限。通过使用 ADB 的[包管理器(pm)](https://developer.android.com/studio/command-line/adb.html#pm) 工具，我们可以向任何我们想要的应用程序授予几乎任何权限(假设应用程序在清单文件中请求该权限)。

你需要做的第一件事是[将 ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)安装到你的电脑上，然后为你的设备安装[正确的驱动程序。然后，在开发者选项中启用 USB 调试(进入设置- >关于手机，如果你还没有的话，点击 7 次内部版本号)，将手机连接到电脑上。最后，打开终端后，发送以下命令:](https://developer.android.com/studio/run/oem-usb.html)

`adb shell pm grant com.joaomgcd.autotools android.permission.WRITE_SECURE_SETTINGS`

现在，自动工具将能够更改您设备上的任何全局、安全或系统设置。有各种方法可以使用这些设置，每个类别中的可用设置列表完全取决于您的设备和软件版本，但这一讨论将在其他时间进行。无论如何，我们将继续向您展示如何使用自动工具来控制锁屏超时。

这里有一个逐步的指导，现在有 Tasker 控制电池节省自定义电池水平/百分比，因为我们有所有的先决条件了。

幸运的是，与 ADB 方法不同，我们不必担心输入任何命令。AutoTools 的开发人员编写了触发电池保护程序的功能，该功能会发送包装在用户友好 UI 中的 shell 命令，因此应用程序会处理该命令，而您所要做的只是在应用程序中选择一个选项。

1.  打开 Tasker，按右下角的 **+** 图标，创建一个新的个人资料。将配置文件命名为“Battery Saver - Custom Level ”,并选择**状态**上下文。
2.  转到**电源- >电池电量**。将“从”滑块设置为 1，将“到”滑块设置为您希望触发节电模式的电池电量。
3.  创建一个附加到此配置文件的新任务，并将其命名为“启用节电模式”
4.  按下底部中间的 **+** 按钮，创建一个新动作。进入**插件- >自动工具- >安全设置。**按铅笔按钮进入自动工具配置。
5.  选择**节电器**选项，并将其设置为“**启用”**
6.  回到主屏幕，长按我们之前创建的电池电量状态，以便我们可以向该配置文件添加一个附加的状态上下文。进入**电源- >电源**，对于电源选择“**任意**，检查“**反转**
7.  再次，回到主屏幕，现在长按“启用电池保护”任务，添加一个“退出”任务到这个配置文件，当电池电量大于你的阈值或当设备在充电器上时触发。将此任务命名为“禁用节电模式”
8.  对于操作，再次进入**插件- >自动工具- >安全设置**。这一次设置电池节电选项为“**禁用。”**

接下来，我们将使用 Tasker 在手机进入睡眠/显示屏关闭时触发电池保护。

* * *

### 显示器关闭时启用节电模式

我假设您已经授予 AutoTools 访问上述安全设置的必要权限。如果没有，就回去做。一旦你准备好了，这里有一个逐步的指示。

1.  打开 Tasker，按右下角的 **+** 图标，创建一个新的个人资料。将配置文件命名为“Battery Saver - Display Off ”,并选择**状态**上下文。
2.  进入**电源- >显示状态**。将**设置为【关】**选项。
3.  对于该任务，您可以选择您之前创建的“启用节电”任务。如果您没有遵循这些步骤，那么创建一个名为“启用节电”的新任务
    1.  按下底部中间的 **+** 按钮，创建一个新动作。进入**插件- >自动工具- >安全设置。**按铅笔按钮进入自动工具配置。
    2.  选择**节电器**选项，并将其设置为“**启用”**
4.  回到主屏幕，长按我们之前创建的电池电量状态，以便我们可以向该配置文件添加一个附加的状态上下文。进入**电源- >电源**，对于电源选择“**任意**，检查“**反转**
5.  再次，回到主屏幕，现在长按“启用电池保护”任务，添加一个“退出”任务到这个配置文件，当显示器打开或当设备在充电器上时触发。添加之前的任务“禁用节电模式”,或按照下一步添加。
    1.  对于操作，再次进入**插件- >自动工具- >安全设置**。这一次设置电池节电选项为“**禁用。”**

就是这样！Tasker 现在应该在屏幕关闭和设备不在充电器上时自动启用电池保护，并在屏幕重新打开或设备在充电器上时禁用电池保护。

* * *

试试这些技巧，让我们知道它们对你有什么作用，或者给我们你自己的建议，告诉我们如何改进这个技巧！