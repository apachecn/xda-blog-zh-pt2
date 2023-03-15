# Android 牛轧糖的自由形式窗口模式:它是什么以及开发者如何利用它

> 原文：<https://www.xda-developers.com/android-nougats-freeform-window-mode-what-it-is-and-how-developers-can-utilize-it/>

 <picture>![](img/071f2be601e6cff563b1e08d56a4d1c2.png)</picture> 

Freeform window mode, as first demonstrated by [Ars Technica](http://arstechnica.com/gadgets/2016/03/this-is-android-ns-freeform-window-mode/)

当 Android 7.0 牛轧糖在 2016 年初首次发布时，它为 Android 平台带来了一个备受期待的功能——多窗口支持。大多数人都知道所有 Android 牛轧糖手机和平板电脑默认启用的分屏多窗口支持。安装了 Android Nougat 的 Android 电视设备支持画中画多窗口支持。

然而，Android Nougat 中还有第三种多窗口模式，没有多少人知道:**自由形式窗口模式**。这种模式允许 Android 将应用程序呈现为浮动窗口，用户可以随意移动和调整大小。它本质上是 Android 的一个[堆叠窗口管理器](https://en.wikipedia.org/wiki/Stacking_window_manager)的实现。

在 [Android SDK 文档](https://developer.android.com/guide/topics/ui/multi-window.html)中，它指出:

> #### 大型设备的制造商可以选择启用自由模式，在这种模式下，用户可以自由调整每个活动的大小。如果制造商启用此功能，则除了分屏模式之外，设备还提供自由形式模式。

还有，在[安卓 7.0 CDD](https://static.googleusercontent.com/media/source.android.com/en//compatibility/7.0/android-7.0-cdd.pdf) :

> #### 屏幕尺寸为 xlarge 的设备实现应该支持自由模式。

这表明，任何搭载 Android 7.0 的新大屏幕 Android 设备都可能有制造商支持的自由形式窗口模式。

但是，这绝对不是硬性要求。可以使用两种不同方法中的一种来强制任何 Android 牛轧糖设备(启用了开发人员选项)支持自由形式窗口模式:

* * *

## 在任何 Android 牛轧糖设备上启用自由形式窗口模式

 <picture>![](img/23cc927c505bf992c37307ea47ee14d4.png)</picture> 

Turning on the “Force activities to be resizable” option allows apps to run in freeform mode on any device

### 方法 1(需要一台带 adb 的计算机)

确保在开发人员选项中启用了 USB 调试。然后，将您的设备连接到安装了 adb 的计算机，并执行以下命令:

```
 adb shell settings put global enable_freeform_support 1 
```

### 方法 2(无额外要求)

启用开发者选项底部的“强制活动可调整大小”选项。

**这两种方法都需要重启系统 UI 才能生效。**最简单的方法是重启你的设备(或者，如果你的设备是根设备，你可以简单地终止`com.android.systemui`进程)

* * *

## 好了，自由模式被启用了…现在做什么？

如果您使用方法 1 启用了自由形式模式，那么在总览菜单中的应用条目上将有一个新按钮，用于将应用启动到自由形式窗口模式。

然而，使用方法 2，无法通过 Android 本身将应用程序启动到自由模式。幸运的是，**任何第三方启动器都可以使用作为 API 级别 24 的一部分最终确定的标准 Android APIs 将应用程序启动到自由形式窗口模式**。

在自由模式下启动应用程序的关键是调用 [`ActivityOptions.setLaunchBounds()`](https://developer.android.com/reference/android/app/ActivityOptions.html#setLaunchBounds%28android.graphics.Rect%29) 方法。该方法将一个 [`Rect`](https://developer.android.com/reference/android/graphics/Rect.html) 作为参数，包含应用程序启动时使用的窗口边界。

然后可以用 [`startActivity(Intent, Bundle)`](https://developer.android.com/reference/android/content/Context.html#startActivity%28android.content.Intent,%20android.os.Bundle%29) 启动 app。如果您还没有一个`ActivityOptions`包，您可以使用 [`ActivityOptions.makeBasic()`](https://developer.android.com/reference/android/app/ActivityOptions.html#makeBasic%28%29) 创建一个包，然后在新创建的包上调用`setLaunchBounds()`。

请注意，默认情况下，如果概览屏幕中已经有应用程序的任务，那么 Android 会简单地将您重定向到用户之前启动的现有(全屏)任务。在尝试将应用程序启动到自由形式窗口之前，您需要在概览中清除该应用程序的任何任务。(对于具有以`standard`或`singleTop`模式启动的活动的应用程序，您可以在调用`startActivity()`之前，通过将 [`Intent.FLAG_ACTIVITY_MULTIPLE_TASK`](https://developer.android.com/reference/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK) 标志添加到意图来强制打开一个新窗口。)

* * *

## 自由模式是如何工作的？

有一篇[写的很棒的文章](http://qiangbo.space/2016-09-26/AndroidAnatomy_Multi-Window/)解释了多窗口模式，包括自由形式模式，是如何在 Android Nougat 中实现的。(注意:文章是用中文写的，所以一定要通过谷歌翻译来运行)

简而言之，自由模式下的应用程序运行在一个独立于系统其余部分的堆栈中(想象一下:虚拟桌面)。因此，自由形式的应用程序不可能在启动程序或另一个全屏应用程序上运行。

在自由模式下运行的应用程序(没有将`android:windowIsFloating`设置为 true)有一个 [`DecorCaptionView`](https://android.googlesource.com/platform/frameworks/base/+/android-7.1.1_r6/core/java/com/android/internal/widget/DecorCaptionView.java) 作为顶层`DecorView`的子节点。这个视图包含一个`LinearLayout`，定义了移动、最大化和关闭窗口的标题栏。虽然我个人并不推荐，但是可以通过使用 [`Window.getDecorView()`](https://developer.android.com/reference/android/view/Window.html#getDecorView%28%29) 获得`DecorView`，将其转换为`ViewGroup`，然后访问其子视图，来访问和定制这个视图。

任何设计为在 Android 标准分屏多窗口模式下表现良好的应用程序都可以在自由模式下工作。对于在自由模式下运行的应用程序， [`isInMultiWindowMode()`](https://developer.android.com/reference/android/app/Activity.html#isInMultiWindowMode%28%29) 将返回 true。还有一些其他公开可用的类和方法，应用程序可以使用，它们专门与自由形式模式相关:

* * *

## 自由形式窗口模式的实例

 <picture>![](img/25560096f83fa4e9c9eaa3948fff7722.png)</picture> 

Taskbar adds a start menu and recent apps tray to compliment freeform window mode

2016 年夏天，当 Android Nougat 仍然是开发者预览版时，我发布了一个名为 **Taskbar** 的应用程序，它在系统叠层中提供了一个类似 Windows 的开始菜单和最近的应用程序列表。它允许 Nougat 上的用户以自由形式窗口模式启动应用程序——而且，由于任务栏使用覆盖，它可以在自由形式窗口环境中停留在屏幕上。任务栏和自由形式模式的结合给任何 Android 设备，尤其是平板电脑，一种类似 PC 的感觉。

你可以[在 Google Play 上下载任务栏](https://play.google.com/store/apps/details?id=com.farmerbb.taskbar)，或者[自己在 GitHub 上查看源代码](https://github.com/farmerbb/Taskbar/)。除了本文中提到的概念之外，我还使用了一些技巧来保持自由模式环境活动，即使屏幕上没有显示自由模式窗口。用户还可以选择将任务栏设置为他们的默认启动器，以允许他们的设备自动引导到自由模式环境。

由于还没有任何设备正式提供 OEM 支持的自由形式窗口，我建议开发人员使用任务栏作为工具，在不支持自由形式窗口的设备上测试他们的应用程序。

除了任务栏，我还修改了 AOSP 的 Launcher3 源代码，让它可以以自由模式启动应用程序。这是对 Android 7.1.1 启动器的直接克隆，只做了最少的必要修改，就可以启动自由形式的应用程序。我提供了这个修改过的启动器，希望其他开发人员能够在他们的定制启动器中实现对启动自由形式窗口的支持。你可以[在 GitHub 上查看源代码](https://github.com/farmerbb/Launcher3-Freeform)，或者[下载一个样本 APK](https://github.com/farmerbb/Launcher3-Freeform/raw/freeform-mode-example/Launcher3-Freeform-aosp-debug.apk) 。

我希望自定义启动器的开发人员可以利用这些代码，并支持为那些希望在大屏幕设备上更灵活地管理窗口的用户启动自由形式的窗口应用程序。