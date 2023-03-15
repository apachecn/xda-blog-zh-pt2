# 导航条定制一直隐藏在库存牛轧糖中...它从来不需要根

> 原文：<https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/>

请举手:你们中有多少人实际上正在运行第一个 [Android O 开发者预览版](https://www.xda-developers.com/google-announces-android-o-developer-preview-1-available-for-supported-devices/)？开发者预览版不仅仅对少数谷歌设备可用，而且真的不适合作为日常驱动。当然，它从来没有打算被普通用户使用，而是作为开发人员的测试平台，以确保他们的应用程序在 Android O 正式发布时能够工作。然而，这并不意味着我们不能为自己找点乐子，看看里面有什么。Android O 设备最令人兴奋的功能之一是位于系统 UI 调谐器中的[导航条定制](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)。但是，如果我们告诉你，这个了不起的导航条定制不仅仅适用于 Android O 开发者预览版的用户呢？没错，这个功能其实**已经在 Android 7 上运行了。x 牛轧糖，而且也不需要 root 访问。**

*Facepalm* 。当我写关于在 Android O 上根据上下文修改导航条的[教程时，我曾假设我发送的这些 shell 命令只能在 Android O 上运行。事实证明这不是真的——这些命令实际上在 Android Nougat 上运行得很好。现在，](https://www.xda-developers.com/category/tutorials/)[我们已经知道近 9 个月](https://www.xda-developers.com/android-nougat-how-to-enable-hidden-navigation-bar-tweaks/)可以在 Android Nougat 中启用导航条定制，然而，最初的发现要求用户[修改系统界面 APK](https://forum.xda-developers.com/nexus-6p/themes-apps/mod-navbar-tuner-android-nougat-t3446791) 以[显示导航条调谐器偏好](https://forum.xda-developers.com/nexus-6p/themes-apps/mod-enable-navbar-tuner-nougat-t3447478)。对于许多用户来说，这显然是一个需要克服的主要障碍，因为它不仅需要 root 访问权限，还需要对 SystemUI APK 进行反编译，并为每个更新打补丁。然而，你甚至不需要*修改 SystemUI 来暴露这个导航条调谐器活动，你可以通过 shell 命令手动修改导航条！*

警告:我们从一些用户那里得知，在谷歌 Pixel 的最新 Android 7.1.2 测试版上，自定义导航条不起作用。尝试这些命令需要您自担风险。为了安全起见，我建议使用下面发布的 paphonb 开发的应用程序而不是 ADB 命令来尝试这种定制[。如果它不能与他的应用程序一起工作，那么不要尝试 ADB 命令！](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)

我们可以确认 Android Nougat 中的隐藏导航条定制可以在以下设备上运行:

*   谷歌 Nexus 6
*   谷歌 Nexus 5X
*   谷歌 Nexus 6P
*   谷歌像素
*   谷歌像素 XL
*   一加 3
*   OnePlus 3T
*   索尼 Xperia 手机

导航栏定制器似乎可以在任何没有删除 AOSP 实现的设备或 ROM 上工作，因此大多数设备都有或接近有基于 Android 7 的固件。x 牛轧糖应该有效果。

* * *

## 隐藏在 Android 牛轧糖中的导航条定制

在 Android Nougat 中手动修改导航栏的工作方式与它在 Android O 上的工作方式非常相似。您可以发送 ADB shell 命令来修改特定设置，或者将 WRITE_SECURE_SETTINGS 权限授予某个应用程序，如 [SecureTask](https://play.google.com/store/apps/details?id=com.balda.securetask&hl=en) 或 [AutoTools](https://play.google.com/store/apps/details?id=com.joaomgcd.autotools&hl=en) ，以便他们可以控制修改设置。控制导航栏按钮的安全首选项。使用[任务器](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en)，你也可以根据上下文修改导航栏。

向 SecureTask 或 AutoTools 授予 WRITE_SECURE_SETTINGS 非常简单，因为您所需要做的就是输入以下 ADB shell 命令之一，这不需要您成为 rooted 用户。

对于 SecureTask:

```
 adb shell pm grant com.balda.securetask android.permission.WRITE_SECURE_SETTINGS 
```

对于自动工具:

```
 adb shell pm grant com.joaomgcd.autotools android.permission.WRITE_SECURE_SETTINGS 
```

然后修改导航栏的语法如下:

```
 settings put secure sysui_nav_bar "key(KEYCODE_CONSTANT:file:///path/to/icon.png),back;home;recent,key(KEYCODE_CONSTANT:file:///path/to/icon.png)" 
```

你可以重新安排按键布局，向左或向右添加空格来移动按钮(输入`space`会在导航条上添加一个空槽)，选择自定义图标，更改键码，等等。如你所愿，遵循这个语法。例如，下面是我用来在导航栏上添加一个[键码 _ 菜单](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_MENU)按钮和一个[键码 _ 前进](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_FORWARD)按钮来增强我的 Chrome 浏览体验的命令:

```
 settings put secure sysui_nav_bar "key(82:file:///storage/emulated/0/NavIcons/menu.png),back;home;recent,key(125:file:///storage/emulated/0/NavIcons/forward.png)" 
```

命令引用的图标路径是我从 [IconsDB](http://www.iconsdb.com/) 下载的自定义图标。我通过在 [Material.io](https://material.io/devices/) 上查找我的设备的显示密度，然后使用参考图表将该密度与[适当的图标尺寸相关联，从而获得了适当的图标尺寸。](http://iconhandbook.co.uk/reference/chart/android/)

如果我想将导航条恢复到默认布局，我可以输入以下命令:

```
 settings put secure sysui_nav_bar "space,back;home;recent,space" 
```

如果你一直关注我的 Android O 教程，那么这个语法对你来说应该很熟悉。如果没有，那也不用担心。有一个应用程序可以解决这个问题。

* * *

## 自定义导航栏

XDA 资深会员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) 开发了一款名为[的定制导航条](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)的应用，它可以为你做所有的跑腿工作，并改变导航条按钮。这款应用非常容易使用，因为它基于 Android O 的导航栏定制器。然而，该应用程序已经被编码为允许你使用自定义图标([很像我的教程](https://www.xda-developers.com/how-to-add-custom-icons-to-the-navigation-bar-in-android-o/))，包括创建可以快速切换的配置文件的能力，此外还有 Tasker 支持，所以你可以根据你想要的任何标准根据上下文改变导航栏。

您只需安装应用程序，然后通过在 ADB 中发出以下命令授予其 WRITE_SECURE_SETTINGS 权限:

```
 adb shell pm grant xyz.paphonb.systemuituner android.permission.WRITE_SECURE_SETTINGS 
```

然后当你打开应用程序时，应用程序将确定你的设备是否支持修改导航栏。它会尝试在你的导航条中间显示一个“下一页”键。如果它出现了，那么你可以修改你的导航条。如果没有，应用程序会告诉你，你运气不好。

该应用程序**是免费的**，但如果你想创建 2 个以上的个人资料，你需要购买一个专业版。这个应用程序当然可以更容易地修改你的导航栏，所以我个人认为这个价格是值得的，但如果你知道如何做，你可以通过 Tasker 和 SecureTask/AutoTools 执行这个应用程序提供的所有功能。

* * *

## 定制可能性

用这个 app + Tasker 可以做很多事情。我已经在我的教程中概述了许多这样的案例[，但是这里有一些你可以尝试的事情的快速列表:](https://www.xda-developers.com/category/tutorials/)

这些是我在玩 Android O 中的导航条调谐器时想到的，但它们应该与 Android Nougat 中隐藏的导航条调谐器一样工作。

我真的很惊讶，花了这么长时间才有人发现这个导航条调谐器可以在没有 root 的 Android Nougat 上工作。回过头来想想，它在没有根的情况下工作是完全有道理的。毕竟，SystemUI mod 只暴露了 preferences 片段来启动导航栏调谐器活动，这并不像 mod 实际上向 SystemUI 添加了该功能-它一直都在那里。shell 命令只是允许我们改变导航条，而不暴露这个 SystemUI 活动，paphonb 的应用程序只是让这一切变得更容易。

* * *

您希望如何自定义您的导航栏？请在下面的评论中告诉我们！