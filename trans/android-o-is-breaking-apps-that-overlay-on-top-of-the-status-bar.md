# Android O 正在打破覆盖在状态栏顶部的应用程序

> 原文：<https://www.xda-developers.com/android-o-is-breaking-apps-that-overlay-on-top-of-the-status-bar/>

由于用户已经花了数周时间在他们的设备上测试该软件，概述在 Android O 中发现的面向用户的新功能的帖子开始减少。然而，有很多很多的改变正在慢慢被发现。前几天我们发布了一个这样的变化，关于运行 Android O [的 Nexus 和 Pixel 设备采用 SDCardFS](https://www.xda-developers.com/nexus-pixel-devices-migrate-to-sdcardfs-in-android-o/) 。但是今天，我们想讨论一个会影响某些应用开发者的变化，特别是那些**覆盖在状态栏**顶部的应用。这些应用程序似乎在 Android O 开发者预览版中**被破坏了，乍一看你可能会认为这是一个简单的错误，但是深入研究参考文档，这可能是**谷歌有意的改变**。**

* * *

## Android O 打破状态栏覆盖

我最喜欢 Android 的一点是它的可定制性。根用户或运行自定义 rom 的用户可以在本地设置系统状态栏的主题，基本上没有任何限制，但是如果你的设备没有根，你的选择就更少了。幸运的是，在谷歌 Play 商店上有许多应用程序允许你改变状态栏的基本外观。这是可能的，这要归功于系统覆盖窗口的巧妙组合，以在现有窗口上显示自定义状态栏，通知监听器以显示通知，以及可选的可访问性服务以允许根据上下文着色自定义状态栏。

上面两张截图显示了我的通知栏在使用 Play Store 上众多状态栏覆盖应用中的一个时的样子。这些截图是在一台运行 EMUI 5.0 的未 root 华为 Mate 9 上拍摄的。对于那些不熟悉 EMUI 的人来说，状态栏看起来一点也不像上面的截图。相反，它看起来像这样:

如果你不介意你的股票状态栏的外观，那么像[状态](https://play.google.com/store/apps/details?id=com.james.status)或[材料状态栏](https://play.google.com/store/apps/details?id=com.treydev.msb)这样的应用程序就是天赐之物。但是如果，或者当你的设备更新到 Android O 的时候，这些应用可能就不再起作用了。下面是这两个应用在运行 Android O 开发者预览版的 Google Pixel 上的样子:

不是覆盖图挡住了原来的状态栏，而是看起来覆盖图*与原来的状态栏*重叠，这导致了巨大的混乱。

不幸的是，这实际上使这些应用程序变得毫无用处。受此影响的不仅仅是典型的状态栏主题应用程序- **所有需要在状态栏顶部显示覆盖图的应用程序都会受到影响**。

以下是一些可能变得无用的流行应用程序列表:

*   [状态](https://play.google.com/store/apps/details?id=com.james.status)(50-100 万次安装)
*   [物料状态栏](https://play.google.com/store/apps/details?id=com.treydev.msb)(100 万-500 万安装)
*   [酷工具-系统统计](https://play.google.com/store/apps/details?id=ds.cpuoverlay) (500，000 - 1，000，000 次安装)
*   [电视电影](https://play.google.com/store/apps/details?id=com.jakewharton.telecine) (5 万- 10 万安装)
*   [清理状态栏](https://play.google.com/store/apps/details?id=com.emmaguy.cleanstatusbar&hl=en)(10-50 万次安装)
*   Tinycore (10 万- 50 万安装)

以及一些可以工作的应用程序的列表，但不能再覆盖在状态栏的顶部(限制以前的功能):

*   [暮光之城](https://play.google.com/store/apps/details?id=com.urbandroid.lux)(500 万-1000 万安装)
*   [抬头](https://play.google.com/store/apps/details?id=com.achep.headsup)(10-50 万安装)
*   [小型资源监视器](https://play.google.com/store/apps/details?id=info.kfsoft.android.MemoryIndicator) (50，000 - 100，000 个安装)
*   [迷你网络监视器](https://play.google.com/store/apps/details?id=info.kfsoft.android.TrafficIndicator)(100 万-500 万台)

Play Store 上有更多的应用在状态栏上使用某种覆盖，但你已经可以看出这样的变化将影响许多潜在数百万用户使用的应用。这是怎么回事？

* * *

## TYPE_SYSTEM_OVERLAY 已被否决

随着 Android 的每一次新的迭代，谷歌都引入和摒弃(指定为过时和将被删除)各种功能。这一次，砧板上的特征是 TYPE_SYSTEM_OVERLAY。引用[参考页面](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#TYPE_SYSTEM_OVERLAY)中的话来说明这个特性给开发者带来了什么:

> #### **类型 _ 系统 _ 覆盖图**
> 
> #### 窗口类型:系统覆盖窗口，需要显示在所有其他窗口之上。这些窗口不能获得输入焦点，否则会干扰键盘保护。在多用户系统中，只在拥有用户的窗口上显示。

本质上，这种窗口类型允许应用程序在屏幕上的任何元素上绘图——包括状态栏。然而，从 Android O 开始，这种窗口类型已被弃用。对于非系统应用，Google 建议开发者改用 TYPE_APPLICATION_OVERLAY。引用[参考页](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#TYPE_APPLICATION_OVERLAY)中关于这种新窗口类型的内容:

> #### **类型 _ 应用 _ 覆盖**
> 
> #### 窗口类型:应用程序覆盖窗口显示在所有活动窗口的上方(类型在`[FIRST_APPLICATION_WINDOW](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#FIRST_APPLICATION_WINDOW)`和`[LAST_APPLICATION_WINDOW](https://developer.android.com/reference/android/view/WindowManager.LayoutParams.html#LAST_APPLICATION_WINDOW)`之间)，但在状态栏或 IME 等关键系统窗口的下方。
> 
> #### 系统可以随时改变这些窗口的位置、大小或可见性，以减少用户的视觉混乱，并且还管理资源。
> 
> #### 系统将调整具有该窗口类型的进程的重要性，以减少低内存杀手杀死它们的机会。
> 
> #### 在多用户系统中，仅在拥有用户的屏幕上显示。

正如你所看到的，这种新的窗口类型允许应用程序将内容覆盖在所有其他活动窗口*的顶部，除了*“像状态栏或 IME 这样的关键系统窗口”(IME 指的是键盘)。这对于像 Facebook Messenger 这样的应用程序来说是没问题的，因为该应用程序提供的聊天头没有任何目的地位于状态栏的顶部，但这对我前面提到的大多数应用程序都有负面影响。

此外，目前似乎没有可供开发人员使用的变通办法。人们可能会认为，为了避免 Android O 上的这一问题，开发人员只需针对 SDK 25 (Android 7.1.1)构建他们的应用程序。然而，正如 Reddit 上 Status 的[开发者所指出的，Google 已经*用 TYPE_APPLICATION_OVERLAY 替换了* TYPE_SYSTEM_OVERLAY，并且变化是**独立于目标 SDK** 版本。使用 TYPE_SYSTEM_OVERLAY 的开发人员目前必须使用 TYPE_APPLICATION_OVERLAY 来保持兼容性，因此，无论特定应用程序基于什么目标 SDK 版本，它都不能在 Android 上使用 TYPE_SYSTEM_OVERLAY。](https://www.reddit.com/r/androiddev/comments/6363f3/android_o_dev_preview_breaks_my_app/)

* * *

## 对此能做些什么？

尚不清楚谷歌为什么做出这一改变，因为他们尚未提供官方解释。我的猜测是，它试图通过防止不知情的用户意外安装恶意阻止或替换他们的状态栏的应用程序来提高 Android 的安全性。不幸的是，这一变化捕捉到了许多使用 TYPE_SYSTEM_OVERLAY 的完全合法的应用程序。

利用这一功能的开发者已经在 Android 的问题跟踪器( [#260787](https://code.google.com/p/android/issues/detail?id=260787) 和 [#36574245](https://issuetracker.google.com/issues/36574245) )上公开了错误报告，以抗议这一变化，并要求提供替代 API，但一名谷歌人在跟踪器上发表了如下声明[:](https://issuetracker.google.com/issues/36574245#comment14)

> #### *状态:无法修复(预期行为)*
> 
> #### 我们与产品和工程团队进行了跟进，并得到建议，开发人员可以使用 SHOW_WHEN_LOCKED 活动来显示设备何时锁定，但有意不再可能通过锁屏/通知阴影来显示

目前，这些开发者似乎不太走运，因为开发者指出，FLAG_SHOW_WHEN_LOCKED 仍然不允许窗口覆盖在状态栏的顶部。目前还不清楚这些应用的开发者能做什么，除了祈祷谷歌改变事情，或者为此大吵大闹。

由于这只是 Android O 的第一个开发者预览版，谷歌仍然有可能改变主意，为不针对 Android O 的应用程序提供这一功能，或者谷歌恢复 TYPE_SYSTEM_OVERLAY。但是如果事情保持现状，你可以**和这些应用吻别**。那真是太可惜了。

* * *

*感谢 Eli Irvin 为我测试了许多应用程序！*