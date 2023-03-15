# 如何在运行 EMUI 的华为和 Honor 设备上设置自定义屏保

> 原文：<https://www.xda-developers.com/how-to-set-a-custom-screen-saver-on-huawei-and-honor-devices-running-emui/>

Android 4.2 Jelly Bean 引入了一个名为 daydream 的功能，它本质上只是一个[交互式屏幕保护程序](https://android-developers.googleblog.com/2012/12/daydream-interactive-screen-savers.html)，在设备对接和/或充电时激活。第三方开发者可以[制作自己的屏保](https://developer.android.com/reference/android/service/dreams/DreamService.html)，用户可以在设置→显示中访问屏保。不幸的是，并不是每个 OEM 都允许他们的用户设置自定义屏幕保护程序。例如，华为及其子品牌 Honor 只给用户提供了一个单一的屏幕保护选项——可以播放幻灯片的照片表格选项。

*(注:从 Android 7.0 牛轧糖发布开始，谷歌将 daydreams 重命名为屏幕保护程序，这样用户就不会将该功能与 Daydream VR 平台混淆。然而，华为和 Honor devices 在设置中仍然将屏幕保护程序称为“白日梦”，所以我将这两个术语互换使用。)*

我不知道为什么 EMUI(在华为和 Honor 的 Android 智能手机上运行的软件)不允许用户在设置中设置自定义的屏幕保护程序，但我知道可以手动设置自己的屏幕保护程序。以下是方法。

* * *

## 教程-在 EMUI 中手动设置自定义屏幕保护程序

## 建立亚洲开发银行

由于这种方法涉及到发送 ADB 命令，我们首先需要确保在接触其他任何东西之前我们已经设置好了。下载[独立的 ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)，并将其保存在你的台式机/笔记本电脑的存储器中的任何地方(专业提示:对于 Windows，将所有内容放入`C:\Windows`中，以便 ADB 在系统范围内工作)。接下来运行 [HiSuite](http://consumer.huawei.com/minisite/HiSuite_en/index.html) ，看看它是否能识别你的手机，确保你已经为你的手机安装了合适的驱动程序。如果没有，让 HiSuite 为您安装驱动程序。

现在，在你的手机上，进入设置→关于手机，点击“内部版本号”7 次，直到你看到一个弹出窗口，说明你现在是一名开发人员。回到“设置”,会出现一个名为“开发者选项”的新菜单项。输入这个并查找“USB 调试”启用它，然后将您的手机连接到您的 PC。

在 PC 上打开命令提示符/终端，输入以下命令:

```
 adb devices 
```

回到手机上，您应该会看到一个弹出窗口，要求您授权您的计算机使用 USB 调试。授权吧。现在，在您的计算机上，上述命令的输出应该显示您的手机的序列号。如果是这样，那么你已经准备好继续前进了。

### 设置自定义屏幕保护程序

接下来你需要做的是进入设置→显示，打开屏幕保护程序(在 EMUI 中称为白日梦)。不要担心它下面的任何设置，当我们设置自己的自定义屏幕保护程序时，所有这些都无关紧要。

接下来，你需要从谷歌 Play 商店下载并安装一个定制的白日梦/屏幕保护程序。我在[谷歌时钟](https://play.google.com/store/apps/details?id=com.google.android.deskclock)、[清醒白日梦屏保](https://play.google.com/store/apps/details?id=de.j4velin.ultimateDayDream)和[夜钟](https://play.google.com/store/apps/details?id=com.firebirdberlin.nightdream)上测试了这个方法。你还需要一些方法来手动找出你的自定义屏保应用程序的“梦想服务”的名字。这是你在设置→显示→白日梦中设置时，安卓系统启动的屏保服务的名称。然而，由于 EMUI 不显示提供这项服务的应用程序列表，我们必须挖掘应用程序的服务，找出它的名称。

我将向您展示如何做到这一点的两种不同方法。方法 1 不太精确，但更容易做到。方法 2 将保证你得到正确的名字。

从 Play Store 下载并安装[我的 Android 工具](https://play.google.com/store/apps/details?id=cn.wq.myandroidtools)。打开应用程序，展开左侧的侧边栏。点击组件信息下的“服务”,调出已安装应用程序及其所有服务的列表。在列表中查找您安装的 daydream/屏保应用程序。选择它，你会看到每个应用程序的服务列表。

寻找一些听起来像是白日梦/屏保服务的东西。对于谷歌时钟来说，那将是`com.android.deskclock.Screensaver`。对于 Lucid 来说那就是`de.j4velin.ultimateDayDream.DreamWrapper`。对于夜钟来说那是`com.firebirdberlin.nightdream.NightDreamService`。一旦你有了这些信息，我们就可以设置自定义的屏幕保护程序了。跳过“发送 ADB 命令以设置自定义屏幕保护程序”部分。

### 方法 2 -检查 Android 清单文件

下载 Play Store 上能够检查应用程序的 Android 清单文件的任何应用程序。为此，我使用了[开发者](https://play.google.com/store/apps/details?id=tursky.jan.settings)，但其他任何应用程序也可以。查看你的屏幕保护程序的清单文件，搜索包含权限“`android.permission.BIND_DREAM_SERVICE`”的<服务>标签

 <picture>![](img/7f54e657b450491f1c1ce8237ee0fc87.png)</picture> 

Snippet of Android Manifest file from Google Clock

 <picture>![](img/4320569bbb4f648db2c07e88f5f9013e.png)</picture> 

Snippet of Android Manifest file from Lucid DayDream

 <picture>![](img/84a72b7a6c257c7759591c260e2e0275.png)</picture> 

Snippet of Android Manifest file from Night Clock

找到之后，记下服务名。对于谷歌时钟来说，那将是`com.android.deskclock.Screensaver`。对于 Lucid 来说那就是`de.j4velin.ultimateDayDream.DreamWrapper`。对于夜钟来说那是`com.firebirdberlin.nightdream.NightDreamService`。

### 发送 ADB 命令以设置自定义屏幕保护程序

在计算机上打开命令提示符或终端，输入以下命令:

```
 adb shell 
```

然后，输入以下命令:

```
 settings put secure screensaver_components YOUR.CUSTOM.SCREENSAVER.COMPONENT 
```

你的。CUSTOM.SCREENSAVER.COMPONENT 是屏幕保护程序的包名，后跟屏幕保护程序的服务名。包名和服务名应该用正斜杠分隔。

例如，如果我想将谷歌时钟设置为我的屏幕保护程序:

```
 settings put secure screensaver_components com.android.deskclock/.Screensaver 
```

可以看到，组件的第一部分 com.android.deskclock 是 Google Clock 的包名。如果您遵循方法 1，那么可以通过查看所有服务的公共前缀来找到包名。如果您遵循方法 2，包名会列在清单文件的最顶端。无论哪种方式，你都可以假设在最后一个句点之前的是包名。

对于组件名的第二部分，。屏幕保护程序，这实际上是一个快捷符号，允许我们跳过写出完整的组件名`com.android.deskclock/com.android.deskclock.Screensaver`。

作为另一个例子，下面是我如何将 Lucid 设置为我的屏幕保护程序:

```
 settings put secure screensaver_components de.j4velin.ultimateDayDream/.DreamWrapper 
```

最后，下面是我如何将夜间时钟设置为屏幕保护程序:

```
 settings put secure screensaver_components com.firebirdberlin.nightdream/.NightDreamService 
```

一旦你通过 ADB 命令设置了你的自定义屏幕保护程序，你就可以开始了。只需将手机插入或对接，等待屏幕自行超时。你现在应该看到你的华为或 Honor 手机开始播放你的自定义屏保！如果你想自定义屏幕保护程序，你必须进入应用程序的设置。

* * *

关注 [XDA 教程 RSS 源](https://www.xda-developers.com/category/tutorials/feed/)获取更多类似的内容。下载 [XDA 实验室](https://www.xda-developers.com/xda-labs/)，快速了解 XDA 门户网站上发布的所有最新新闻和原创专题。