# 任务栏 6.0 为 Android 10+带来了类似三星 DeX 的桌面模式

> 原文：<https://www.xda-developers.com/taskbar-samsung-dex-desktop-mode-android-10/>

Android 10 现在已经推出近 9 个月了，但它最好的功能之一桌面模式仍然广泛不为人知。这是因为它在技术上隐藏在 Android 10 中，需要启用一个开发标志，并支持内置到股票启动器应用程序中。令人欣慰的是，任务栏的开发者已经找到了一种方法，使 Android 10 的桌面模式更加有用，为一些设备带来了类似三星 DeX 的体验。

出于某些背景，Android 10 为 Launcher3 添加了一个“二级启动器”活动，Launcher 3 是 AOSP 启动器应用程序，谷歌的 Pixel Launcher 和其他许多 OEM 启动器应用程序都是从它派生出来的。当支持显示输出的 Android 设备连接到外部显示器时，这个辅助启动器活动会显示在外部显示器上。然而，因为这个二级启动器非常简单，所以作为一个生产力工具是没有用的。第三方应用程序开发者发现，他们自己的启动器应用程序可以取代外部显示器上的股票启动器，这正是 XDA 高级成员 [farmerbb](https://forum.xda-developers.com/member.php?u=4289533) 在任务栏 6.0 中实现的内容。

任务栏是一个开源的 Android 应用程序，可以在任何屏幕上放置一个浮动的开始菜单和最近的应用程序托盘。由于它支持在自由形式的多窗口中启动 Android 应用[，它甚至预装在](https://www.xda-developers.com/android-nougats-freeform-window-mode-what-it-is-and-how-developers-can-utilize-it/) [Bliss OS](https://forum.xda-developers.com/android/software/bliss-os-x86-pc-s-12-x-development-t4004419) 上，这是一个面向 x86 PCs 的流行 Android 端口。早在 11 月初，farmerbb 发布了开源 Lawnchair launcher 的一个分支，其中集成了任务栏。这让我们提前看到了[通过一些开发工作，Android 10 的隐藏桌面模式看起来会是什么样子](https://www.xda-developers.com/make-android-10-desktop-mode-useful/)，但是有一些明显的问题需要解决。桌面模式用户体验需要修复，以便自由形式的多窗口行为如您所预期的那样工作，设置过程需要清理，以便您可以在不需要另一个应用程序的情况下控制 DPI/UI，并且必须找到更好的解决方案，以便您不必更改您的默认启动器。现在，farmerbb 已经将任务栏更新到 6.0 版本，以解决所有这些问题。

## 带有任务栏 6.0 的桌面模式

设置任务栏的桌面模式非常简单:

1.  在开发者选项中，打开“启用自由形式窗口”和“强制桌面模式”，然后重新启动设备。(后者可能在一些 OEM 软件如 ZenUI/ROG UI 上不可用，但如果不存在也不用担心。)
2.  从 Google Play 安装任务栏 6.0(旧版不行)。
3.  打开任务栏的设置，进入“桌面模式”启用它并授予应用程序“在其他应用程序上显示”的权限，因为这是应用程序的浮动开始菜单出现所必需的。然后，将该应用程序设置为默认的家庭应用程序。不过，不要担心，因为下一个提示会要求你设置你的首选/主启动器应用程序，所以任务栏不会劫持你的主屏幕。(注意，在某些设备上，更改默认启动器会禁用 Android 10 的全屏导航手势。)
4.  接下来，我强烈建议您按照说明为桌面模式“启用附加设置”。这将允许你降低 DPI，这样 UI 元素在外部显示器上就不会太大，隐藏导航栏，甚至在连接到外部显示器时将手机屏幕调暗以节省电池寿命。你必须在你的电脑上设置 ADB 访问并运行以下命令:

    ```
     adb shell pm grant com.farmerbb.taskbar android.permission.WRITE_SECURE_SETTINGS 
    ```

    (如果你使用的是任务栏的“捐赠”版本，在上面的命令中用“com.farmerbb.taskbar . payed”替换“com . farmerbb . Taskbar”。)
5.  最后，检查以确保任务栏启用了“使用访问”。这样做将允许应用程序在开始菜单中显示一行您最近使用的应用程序。
6.  现在，只需使用 USB Type-C 转 Type-C 电缆(如果您的外部显示器支持 Type-C 输入)或通过 USB Type-C 转 HDMI 适配器将您的手机连接到外部显示器。

连接后，您可以使用“开始”菜单来启动应用程序、搜索应用程序、将应用程序图标添加到主屏幕、打开一些系统菜单等等。您可以点击“开始”菜单旁边的图标来添加/显示小工具。你可以启动多个 windows 实例，在某些情况下，如谷歌浏览器，有多个标签。

任务栏 6.0 中有很多其他选项和变化，所以我建议你在这里阅读完整的更新日志。

## Android 上的显示输出——遗憾的是仍然有限

这对谁有用？三星、华为/Honor 和 [LG](https://www.xda-developers.com/lgs-android-10-update-desktop-mode-interface/) 都提供自己的桌面模式体验，所以如果你拥有这些品牌的智能手机，你不会发现任务栏的桌面模式有多大用处。华硕、一加、Essential、谷歌和小米都不提供自己的桌面模式体验，所以如果你在这些品牌的设备上至少运行 Android 10，那么你可能会发现任务栏的桌面模式功能很有用。如果你想让桌面模式的体验更有效率，那么我建议你使用蓝牙键盘和鼠标。如果你有一个像 [NexDock 2](https://nexdock.com/) 这样的便携式外部显示器/笔记本电脑机箱，那么你会有更好的任务栏体验。

请记住，为了真正利用这一功能，您的智能手机**必须支持显示输出**。高通最新的 Snapdragon 800 和 700 系列芯片组原生支持通过 USB 3.1 Type-C 端口的 DisplayPort 备用模式，但一些供应商(如谷歌)已经在其智能手机上禁用了这一功能。如果你的设备不支持 DisplayPort 替代模式，那么你可能会幸运地使用一个 [DisplayLink 认证的适配器](https://www.displaylink.com/)和 [DisplayLink Presenter 应用程序](https://play.google.com/store/apps/details?id=com.displaylink.presenter)来镜像手机的显示。使用 DisplayLink 适配器的屏幕镜像不如通过标准连接器的本机桌面模式理想，但总比*没有*任何显示输出要好！幸运的是，如果你只是镜像手机的显示屏，只要应用程序被设置为默认启动器，任务栏仍然可以使用，但你必须使用开发者的 [SecondScreen 应用程序](https://play.google.com/store/apps/details?id=com.farmerbb.secondscreen.free)来改变分辨率和密度。

Android 桌面模式目前最大的缺点是有限的应用支持。尽管三星和华为多年来一直提供桌面模式体验，每年销售数百万部智能手机，但用户对支持桌面模式的需求并不多。这意味着很多安卓应用并没有针对大屏幕进行优化。谷歌希望改变这一点，因为更广泛的 Android 应用程序对更大屏幕的支持也将有利于 Chromebooks，但遗憾的是，在大多数 Android 应用程序支持更大屏幕之前，还有很长的路要走。因此，在使用任务栏的时候，你可能会注意到一些应用程序拒绝运行或者看起来很糟糕，而你对此无能为力。

## 下载任务栏 6.0

如果你有以下智能手机之一，我建议试试这个应用程序:

你可以从下面的谷歌 Play 商店链接下载任务栏 6.0，或者从 GitHub 上的源代码编译这个应用程序。该应用程序完全免费使用，但如果你想支持 farmerbb 的开发工作，可以提供 1.99 美元的捐赠版本。

**[任务栏论坛线程 XDA](https://forum.xda-developers.com/android/apps-games/app-taskbar-freeform-window-enabler-t3517608)| |**|**任务栏源代码 GitHub**