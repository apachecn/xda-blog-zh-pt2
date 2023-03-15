# 保护您的隐私:应用运营、隐私保护和 XPrivacy

> 原文：<https://www.xda-developers.com/protecting-your-privacy-app-ops-privacy-guard-and-xprivacy/>

继[昨天的文章](http://www.xda-developers.com/android/play-store-permissions-change-opens-door-to-rogue-apps/)关于谷歌最近对 Play Store 进行的更改为用户带来了许多隐私问题之后，今天我们将看看用户在 Android 设备上保护自己隐私的三个最受欢迎的选项。首先，让我们看看它们是如何工作的，以及它们的用途。

## 我为什么要在乎？

从一开始，安卓就有一个权限系统，允许用户控制应用程序在他们的设备上可以做什么。安装应用程序后，系统会提示用户同意应用程序所需的权限。安卓操作系统确保应用程序不能使用他们没有请求的权限，用户有责任决定是否可以安装应用程序。

起初这很有效，因为用户可以看到应用程序可以访问什么数据。然而，不幸的是，开发者发现很少有用户关注权限提示，开发者使用越来越多的权限变得越来越常见——大概是为了改善用户体验或使他们的应用货币化。

## 那又怎样？大不了？

有鉴于此，今天我们到达了一个点，来自 Play Store 的[首页特色游戏](https://play.google.com/store/apps/details?id=com.ftbsports.BeALegendFootball2)使用以下权限:

*   检索正在运行的应用程序
*   在设备上查找帐户
*   精确定位(全球定位系统和网络定位)
*   大概位置(基于网络)
*   修改或删除 USB 存储设备的内容
*   测试对受保护存储的访问
*   查看 Wi-Fi 连接
*   读取电话状态和身份
*   从互联网接收数据
*   完全网络访问
*   查看网络连接
*   防止设备休眠

所有这些都是为了一个让你玩梦幻足球的游戏？在这一点上，我必须向读者提出几个问题(请在下面的评论中自由讨论):大约一半的权限有任何可能的正当理由吗？这个应用程序有必要查看用户正在使用的其他应用程序吗？或者查看用户在他/她的设备上有哪些帐户？或者使用 GPS 获取您在世界上的确切位置？或者读取你的 IMEI 号码，以及与你通话的人的电话号码？这不是孤立的事件。这只是我在 Play Store 首页选择的第一个应用。再选一个，自己看看！因为现在绝大多数应用程序都在使用我所说的过度权限，越来越多的用户觉得仅仅不使用使用过度权限的应用程序是不够的。这引发了一个常见的请求，即让用户选择应用程序可以访问哪些权限。这将权力的天平向用户倾斜，用户的手机正在运行应用程序，而不是开发者，开发者以前可以自由规定应用程序运行所需的权限。对于技术社区来说，显而易见的解决方案是开发对应用程序能够做什么有更大控制的方法，并防止他们使用他们请求的所有权限。三种最常见的撤销权限的方法是 App Ops、Privacy Guard 和 XPrivacy。

## 应用运营

获得对设备更多控制的第一种方法是通过一个称为“App Ops”的功能这原本是

[introduced by Google in Android 4.3](http://www.xda-developers.com/android/app-ops-brings-granular-permissions-control-to-android-4-3/)

作为隐藏功能。随着 KitKat 的发布，谷歌使访问 App Ops 变得更加困难，但继续

[introduce new improvements to the feature](http://www.androidpolice.com/2013/11/25/new-app-app-ops-lives-on-in-android-4-4-can-be-unleashed-with-app-ops-from-color-tiger-and-enhanced-with-root/)

。最终在 Android 4.4.2 中，谷歌

[removed access to App Ops.](https://www.xda-developers.com/android/source-code-commits-in-android-4-4-2-kot49h-reveal-flash-sms-attack-fix-and-app-ops-removal/)

然而，它仍然

[possible to access with root and an Xposed modification](https://www.xda-developers.com/android/xposed-module-brings-back-app-ops-to-android-4-4-2-and-gives-your-control-of-your-application-permissions/)

或者定制 ROM。App Ops 的主要局限性在于，它是由谷歌开发的，只能让你屏蔽他们愿意让你屏蔽的内容。值得注意的是，App Ops 不提供任何控制应用程序是否应该访问互联网的能力。也不可能阻止应用程序通过你的第三方账户唯一地识别你的设备或你的用户身份。这意味着一个应用程序仍然可以将你设备上的所有帐户身份绑定在一起，并通过适当的权限访问你的 IMEI 和其他唯一的设备标识符，使用 App Ops 不可能阻止这一点。愤世嫉俗者可能会认为，谷歌阻止用户阻止应用程序访问互联网是别有用心的。毕竟，谷歌有动力推动他们的应用内广告，并为谷歌分析收集用户信息。同样，谷歌擅长创建用户档案，这就解释了为什么不能通过你的账户名在应用程序中屏蔽你的身份。访问唯一设备标识符的能力只会有助于允许其他应用程序跟踪您的使用(从而允许 Google 跨应用程序跟踪您的使用)。出于这个原因，我们认为尽管 App Ops 比没有好得多(你可以控制对你的联系人、消息、位置等的访问)，但它绝对不是保护你隐私的最佳解决方案。有许多类型的数据不能被屏蔽，这似乎与谷歌跟踪和收集用户数据的动机有关。因此，我们建议您寻找替代方案。

## 隐私卫士

Privacy Guard 是 CyanogenMod 最初开发的一项功能，用于在 App Ops 上放置一个简单的用户界面，通过一个“开/关”开关来控制它。因此，隐私卫士在局限性方面受到了与 App Ops 相同的批评。它还会在运行受隐私卫士保护的应用程序时发出通知，以提醒用户它正在运行。然而，不幸的是，Privacy Guard 没有试图匿名化用户或阻止应用程序通过设备标识符或互联网访问跟踪他们的会话。然而，有了一个开关控制，对于初学者来说肯定很容易使用，默认设置应该相当好。唯一的缺点是缺乏粒度，这意味着需要访问你的位置的应用程序不能被允许，同时仍然阻止联系人和日历访问。尽管如此，作为一个一键式解决方案，它工作得很好。不过，它确实需要用户安装一个定制的固件，这破坏了一键式吸引力的好处。

## 表达方式

[XPrivacy](http://forum.xda-developers.com/xposed/modules/mod-xprivacy-1-11-8-ultimate-privacy-t2320783)

是安卓隐私保护的瑞士军刀。与我们在这里看到的其他解决方案相比，XPrivacy 的可定制性更强，但结果也更复杂。如果你不熟悉 Android 权限，XPrivacy 可能不是最好的起点。它需要 Xposed 框架，这意味着您还需要一个根设备。然而，XPrivacy 几乎可以在任何 ROM 上工作。XPrivacy 相对于替代产品的主要优势在于您可以对应用程序施加的限制的广度和粒度。您可以将应用程序限制为只能访问和查看您设备上的特定帐户，阻止访问您的剪贴板(以阻止应用程序访问复制的数据)，甚至阻止访问互联网，包括直接访问和通过 web 浏览器访问(以防止任何形式的秘密数据从您的设备泄漏)。如果你想限制什么，XPrivacy 几乎肯定可以限制它。尽管 XPrivacy 是一个非常强大的工具，但它背后有一个很大的学习曲线。我建议通读 XDA 认可开发商 m66b 的所有文档

[Github repository](https://github.com/M66B/XPrivacy)

(我提到过它是完全开源的吗？)，和他的线程

[XDA forums](http://forum.xda-developers.com/xposed/modules/mod-xprivacy-1-11-8-ultimate-privacy-t2320783)

，了解更多信息。总的来说，如果你想绝对控制你的私人数据，我建议你看看 XPrivacy。这需要花很多时间去适应，但它给了你无与伦比的选择。如果你不太确定自己在做什么，使用 App Ops 会给你很好的控制，尽管无法控制互联网接入和识别你是设备用户的数据。App Ops 和 XPrivacy 都可以通过 Xposed 插件在任何 ROM 上获得。Privacy Guard 对于那些只想要一次点击解决方案的人来说是很好的，但是安装定制 ROM 来实现它的需要在这方面是一个限制，因为你不能(目前)在股票固件上找到一个实现。