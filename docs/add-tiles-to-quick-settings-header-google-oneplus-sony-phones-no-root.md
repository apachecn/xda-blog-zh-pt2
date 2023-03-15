# 如何在谷歌、一加和索尼手机的快速设置标题中添加更多磁贴[无根]

> 原文：<https://www.xda-developers.com/add-tiles-to-quick-settings-header-google-oneplus-sony-phones-no-root/>

如果你下拉你的 Android 手机的状态栏，你可能会在单行快速设置磁贴下看到一些通知。这一行被称为快速设置标题，因为它仅显示完整的 QS 图块集中可用的前几个图块。再向下拉一次，您将看到您添加的 QS 互动程序的完整列表。从 Android 5.0 Lollipop 开始，AOSP 正式添加了快速设置(尽管三星等 OEM 厂商在 Lollipop 之前的几个版本中都有自己的通知切换形式)。

虽然我们已经可以通过重新排列图标来定制 QS，并在 QS 列表中添加第三方磁贴，但仍然没有官方方法来定制显示多少磁贴(同样，[三星在这方面已经击败了谷歌](https://www.xda-developers.com/customize-size-quick-settings-button-layout-samsung-galaxy/))。然而，通过使用一个隐藏的首选项，我们可以通过 ADB 设置，这是有可能的**添加更多的瓷砖到快速设置标题**。

*感谢 Eli Irvin 为我收集这些截图！*

**此修改不会改变当您在状态栏上向下滑动两次(或用两个以上的手指下拉)时，在整个 QS 面板中显示的列数或行数。据我所知，唯一的方法是通过修改 SystemUI 这显然需要 root 用户或解锁的引导程序。**

修改快速设置头**不需要 root 访问**，尽管它不会在所有设备上工作。如果你的设备运行的是 **Android 7.0+** ，并且底层软件没有从 AOSP 进行太大的修改，那么这个技巧应该可以在你的手机上使用。这是因为它依赖于 SystemUI 包中定义的设置首选项(在 QuickQSPanel.java 的[中可以找到 AOSP 列出的首选项)。](https://android.googlesource.com/platform/frameworks/base/+/master/packages/SystemUI/src/com/android/systemui/qs/QuickQSPanel.java)

**QuickQSPanel.java**

```
 /**
* Version of QSPanel that only shows N Quick Tiles in the QS Header.
*/
public class QuickQSPanel extends QSPanel {
public static final String NUM_QUICK_TILES = "sysui_qqs_count"; 
```

这段代码摘自我上面链接的 AOSP 页面。字符串 NUM_QUICK_TILES 定义了在标题中显示多少个 QS 图块。NUM_QUICK_TILES 从[设置中获取其值。安全](https://developer.android.com/reference/android/provider/Settings.Secure.html)首选项“sysui_qqs_count ”,这是我们将要修改的内容。为了使这种修改生效，您手机上的软件必须具有这种偏好设置。

谷歌 Nexus 和 Pixel 手机可以使用这种修改，索尼 Xperia 和一加手机也可以。LineageOS 之类的定制 rom 可以工作，至少在我的 Nextbit Robin 上是这样。三星和华为手机无法适应这种偏好变化，尽管如前所述，你可以按照我之前的教程定制三星手机上的 QS 面板尺寸。

* * *

### 辅导的

如前所述，您需要 ADB 访问权限来使用该命令。直接从谷歌为你的机器下载最新的 ADB 二进制文件。确保你安装了正确的[驱动程序](https://developer.android.com/studio/run/oem-usb.html)，这样你的手机才能被你的机器识别。进入设置- >开发者选项，启用 USB 调试。然后在您的机器上打开命令提示符或终端，并输入以下命令:

```
 adb devices 
```

您的机器将尝试启动 ADB，并查看它是否识别任何连接的设备。您可能会在手机上看到一个提示，要求允许 ADB 访问您的机器-接受它。如果您现在看到您的设备的序列号在命令提示符中返回，那么您是黄金。

现在，您需要输入以下命令来修改 QS 标题中显示的图块数量:

```
 adb shell settings put secure sysui_qqs_count N 
```

其中 N 是您希望在标题行中显示的图块数量。例如，如果我想只显示 3 个单幅图块:

```
 adb shell settings put secure sysui_qqs_count 3 
```

或者，如果我想显示 7 个图块:

```
 adb shell settings put secure sysui_qqs_count 7 
```

如果您想返回默认配置，只需为 n 输入“5”

* * *

虽然无可否认这是一个相当小的调整，但即使没有 root，仍然有一些方法可以修改 UI。我不知道谷歌为什么让我们更改这个设置，尽管你甚至不知道它是可用的，除非你在 AOSP 挖来挖去，因为当你把可用的安全设置转储到你的设备上时，这个设置不会被列出来。我希望谷歌像三星一样增加一个原生的方法来调整整个 QS 面板的大小，但这可能仍然是我一厢情愿的想法。

这一调整归功于 XDA 资深成员 paphonb T1，他在 12 月 T3 在 T2 的一个隐藏帖子中发布了这一消息。他是[定制导航条](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)应用的开发者，该应用允许你[在许多没有根](https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/)的 Android 7.0+设备上调整导航条。他和我正在开发一个新的应用程序，它将包含这个调整和许多更多的调整，这样非 root 用户就可以探索他们设备上所有隐藏的调整。