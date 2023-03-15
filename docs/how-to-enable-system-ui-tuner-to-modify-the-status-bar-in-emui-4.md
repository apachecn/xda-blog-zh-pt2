# 如何启用系统 UI 调谐器来修改 EMUI 4+中的状态栏

> 原文：<https://www.xda-developers.com/how-to-enable-system-ui-tuner-to-modify-the-status-bar-in-emui-4/>

经过多年的最小化定制选项，Android Marshmallow 终于通过包含**系统 UI 调谐器引入了一些在定制 rom 中已经存在多年的基本定制功能。**

这项功能包含在所有 Android 6.0+谷歌设备中，为了访问它，你需要下拉状态栏并长按齿轮图标，直到它旋转，之后系统 UI 调谐器菜单将出现在设置中。

在 Android Marshmallow 系统 UI 调谐器中，用户可以修改快速设置磁贴，编辑状态栏，或启动演示模式。对于 Android Nougat，快速设置磁贴编辑器被移动到通知下拉列表，演示模式被移动到开发者选项。此外，Nougat 的 UI 调谐器还引入了勿扰选项，一个支持分屏向上滑动手势的开关，以及电源通知设置。

虽然这些肯定是一些有用的功能，但一些原始设备制造商并不这么认为。HTC、三星和华为等 OEM 厂商取消了对该功能的访问，因为一些可用功能与其软件中的可用功能相冲突。然而，这并不意味着系统 UI Tuner 在非 Google 设备中没有任何用处，尤其是对于非根设备。

幸运的是，至少对于华为/Honor 设备来说，不需要 root 访问就可以**启用系统 UI 调谐器。这是因为 EMUI 只移除了访问 UI 调优器的正常方式，但是活动仍然存在。这意味着我们可以直接启动活动来启动 UI Tuner，即使您必须按住快速设置齿轮图标的普通技巧不再有效。**

虽然这种方法是在运行 EMUI 的华为/Honor 设备上测试的，但它也可能在隐藏了系统 UI 调谐器的其他设备上工作。你必须亲自尝试来验证。

* * *

## 在 em UI 中启用系统 UI 调谐器

如前所述，我们将直接启动一个活动来启动 UI 调谐器(**com.android.systemui/.DemoMode**)。虽然有很多方法可以发起一项活动，但是我写了这个指南来使用一个非常简单的方法。你所要做的就是从谷歌 Play 商店下载[活动启动器](https://play.google.com/store/apps/details?id=de.szalkowski.activitylauncher)。

打开 Activity Launcher，更改查看模式，查看所有活动。”接下来，一直向下滚动到**系统 UI** 。点击它以展开列表并查看所有可用的系统 UI 活动。寻找**演示模式**活动。点击它，它应该会打开隐藏的系统用户界面调谐器。

或者，您可以通过 ADB 命令启用/访问这些设置中的大部分。为了使用 ADB，你需要[下载并解压 ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)到你电脑上的一个文件夹中。接下来，在你的机器上安装[套件](http://consumer.huawei.com/minisite/HiSuite_en/index.html)，这样它就可以为你的手机获取必要的驱动程序。然后，在开发者选项中启用 USB 调试(如果你还没有启用它，进入设置- >关于手机，点击 7 次内部版本号)。在保存 adb 二进制文件的目录中打开命令提示符(在文件夹中右键单击并选择“在此打开命令提示符”)，键入不带引号的“ADB 设备”。你的手机会要求你授予你的计算机 adb 访问权，点击是，当你重新输入“ADB 设备”时，你的手机序列号会出现在命令提示符中

现在您已经设置好了 ADB，下面是您需要的命令:

* * *

启用演示模式:

```
 adb shell settings put global sysui_demo_allowed 1 
```

从状态栏禁用图标:

```
 adb shell settings put secure icon_blacklist "comma-separated-string-of-icons-to-remove" 
```

在音量滑块中显示“请勿打扰”开关

```
 adb shell settings put secure sysui_show_full_zen 1 
```

* * *

无论您使用哪种方法来控制 UI 调谐器，您现在都可以使用它的任何可用选项。我自己已经浏览过这些选项了，根据我的经验(至少对于 Android 7.0 Nougat 版本的系统 UI 调谐器)，这里唯一真正的用途是禁用某些状态栏图标或启用音量滑块中的请勿打扰开关。

其他大部分功能根本不起作用。您不能启用在状态栏时钟中显示秒的切换或启用分屏手势。此外，电池图标不能被修改，你也不能启用电源通知设置，但是，EMUI 原生提供这些功能，所以这不是太大的问题。

* * *

总之，很容易理解为什么华为等原始设备制造商在其软件中禁用系统 UI 调谐器。鉴于有太多的定制选项，提供与他们的股票相冲突的设置菜单是没有意义的。

但是，仍有一些功能可供您利用。对我来说，我喜欢从状态栏中隐藏蓝牙、工作、请勿打扰和其他图标，以获得更干净的 UI 体验。您可能喜欢从音量滑块启用“请勿打扰”的快捷选项。无论你想访问系统 UI 调优器的原因是什么，我希望本教程能帮助你做到这一点。