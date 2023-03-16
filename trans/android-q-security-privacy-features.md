# Android Q:Android 10 中所有新的安全和隐私功能

> 原文：<https://www.xda-developers.com/android-q-security-privacy-features/>

Android 操作系统的每个新版本都带来了从设计、功能、API 等几乎每个方面的改进。在本月早些时候的 Google I/O 上，我们了解了 Android Q 将带来的所有[改进，当然，新的隐私和安全声明也没有被排除在会议之外。平台安全性是操作系统最重要的方面之一，尤其是对于我们随身携带的操作系统。如果 Android 不安全，我们不会相信它有我们一半的功能。NFC 支付将是不可能的，文件共享将是可疑的，连接到其他设备将是彻头彻尾的疯狂。尽管版本分裂的问题由来已久，但谷歌在将安全问题的数量保持在最低水平方面做得非常好。](https://www.xda-developers.com/everything-new-android-q-beta-3/)

Android 已经发展成为一个功能丰富且高度安全的操作系统。但是，当然，总有改进的余地。这种安全性有许多促成因素，其中一些因素正在通过 Android Q 以某种方式得到改善。

* * *

## 加密

作为最基本的安全方法之一，每个设备都支持强加密非常重要。如今，许多原始设备制造商在他们的设备上安装了专用的加密硬件。虽然这是有益的，但也是昂贵的。因此，专用硬件通常仅限于中高端设备。这并不是说低端设备*不能*支持加密，但是如果没有硬件加速加密，整体用户体验会因为缓慢的读/写时间而下降。这就是铁线蕨出现的原因。

### 铁线蕨

二月份，谷歌宣布 Adiantum 作为不支持常规 AES 指令集的低端手机的替代[加密算法。Adiantum 是专门设计的，无需任何专用硬件即可运行。它是 Android 常规 AES 加密的一种更轻便的替代方案。](https://www.xda-developers.com/adiantum-encryption-algorithm-android-pie/)[谷歌的基准测试](https://eprint.iacr.org/2018/720.pdf)告诉我们，它实际上比 AES 快 5 倍，缺点是它在安全性上略有妥协。这使得它成为低端手机的理想候选产品，例如采用 Android Go Edition 的手机。Adiantum 还销售智能手表和各种物联网设备等产品。

到目前为止，铁线蕨是可选的；制造商可以在使用 Android Pie 的设备上启用它，但它不是默认的加密算法。现在，Adiantum 作为 Android Q 的一部分被包含在内，这意味着所有使用 Q 的设备都将被要求加密用户数据，没有例外。因此，无论是否通过 Adiantum，使用 Android Q 的设备肯定会有存储加密。

### Jetpack 安全库

Jetpack 是一组 Android 支持库，而最新添加的一个在 alpha 中:Jetpack 安全库。该库通过处理诸如管理硬件支持的密钥库以及生成和验证密钥之类的事情，简化了保护应用程序的过程。

### TLS 1.3

然而，存储并不是加密得到改进的唯一领域。随着默认情况下 [TLS 1.3 支持](https://www.xda-developers.com/android-q-tls-1-3-support/)的引入，与其他设备的通信得到了很大的改善。TLS 1.3 是最新的网络加密标准，由 IETF 于 2018 年 8 月完成。TLS 1.3 通过对更多的协商握手进行加密，为数据交换提供了更多的隐私。最重要的是，它比 TLS 1.2 更快，因为从连接建立握手中去掉了整个往返过程。再加上更有效的现代算法，这使得速度提高了 40%。

 <picture>![TLS 1.3](img/d29abb60fad7708e305f4f63f1446356.png)</picture> 

TLS 1.3 in Google Chrome. Source: Google.

TLS 现在可以直接从 Google Play 更新，因为它是“Conscrypt”组件的一部分。你可以在这里阅读更多关于那个和项目主线[的内容。](https://www.xda-developers.com/android-q-project-mainline-security/)

鉴于我们每天都信任设备上如此多的敏感交易，升级后的 TLS 比以往任何时候都更加重要。在 Android 上存储登机牌之类的东西，甚至是未来某个时候的数字驾照，意味着所有设备都应该尽可能地加密用户数据。绝热和强制加密将为最敏感的数据存储在最便宜的设备上铺平道路。但是加密并不是谷歌在 Q 版本中增加 Android 安全性的唯一方式。

* * *

## Android Q 中的权限和隐私更改

### 作用域存储

作用域存储是一种新的安全措施，用于限制应用程序读取/写入外部存储中不包含在自己的沙盒应用程序特定目录中的文件。谷歌的目标有三个:更好地确定哪些应用程序可以控制哪些文件，保护应用程序数据，以及保护用户数据。

谷歌在共享音频、视频和图片内容的 MediaStore API 上加倍努力。默认情况下，所有应用程序都可以在 MediaStore 中插入、修改或删除自己的文件。图像，媒体商店。视频和媒体商店。不需要任何权限的音频收藏。Android Q 还增加了新的 [MediaStore。Downloads](https://developer.android.com/reference/android/provider/MediaStore.Downloads) 集合，用于存储用户下载的内容，所有使用 MediaStore API 的应用程序都可以对其进行贡献。虽然存储在沙盒应用程序特定目录中的文件在卸载时会被删除，但所有贡献给 MediaStore 集合的文件在卸载后仍然存在。

要访问由另一个应用程序创建的任何文件，无论该文件是在 MediaStore 集合中还是在它们之外，应用程序都必须使用存储访问框架。此外，除非您的应用程序被授予新的 ACCESS_MEDIA_LOCATION 权限，否则图像的 EXIF 元数据会被编辑。在 Android Q 中，应用程序还可以通过使用 getExternalVolume()查询卷名来控制将媒体放在哪个存储设备上。

谷歌最初对 Android Q 中的所有应用程序施加了范围存储限制，不管它们的目标 API 级别如何，但在反馈后，该公司正在[给开发者更多时间](https://www.xda-developers.com/google-gives-developers-more-time-android-q-scoped-storage/)进行调整。关于限定范围的存储变化的全部细节可以在本页找到[，并且你可以通过](https://developer.android.com/preview/privacy/scoped-storage)[观看这个谷歌 I/O](https://www.youtube.com/watch?v=3EtBw5s9iRY) 演讲，找到更多关于谷歌共享存储最佳实践的建议。

### 针对 API 级别< 23 的应用程序的警告

然而，权限限制并没有到此为止。安装针对低于 23 (Android Lollipop 或更旧)的 API 级别的应用程序时，如果所述应用程序在安装时请求敏感权限，将导致操作系统向用户显示警告。在安装之前，用户将有机会手动指定他们要授予应用程序的权限，然后再继续。因此，Android Q 不再允许应用程序绕过运行时权限。

 <picture>![](img/8b30be33f64b6afc7814c1aa5df8a483.png)</picture> 

Like CopperheadOS, stock Android Q now lets the user disable all requested dangerous permissions before running an app for the first time. This only applies to apps targeting API level 22 or below, which is before runtime permissions were introduced (in Android Marshmallow.)

### 最终 SYSTEM_ALERT_DEPRECATION 支持 Bubbles API

Bubbles API 在运行。来源:谷歌。

Android Q (Go 版)上运行的应用不再可以授予覆盖权限(SYSTEM_ALERT_WINDOW)。对于非 Go 版设备，谷歌正在推动开发者开发新的 Bubbles API。Bubbles API 是 Android Q Beta 2 中引入的一个功能，它允许类似 Facebook Messenger 的聊天头的功能。来自应用程序的通知显示为屏幕边缘的小气泡，当用户点击时会扩大。在气泡中，一个应用程序可以显示一项活动。

这一改变是必要的，因为允许应用程序在其他应用程序上自由绘制覆盖图会带来明显的安全风险。臭名昭著的“[斗篷和匕首](https://www.xda-developers.com/cloak-and-dagger-exploit-uses-overlays-and-accessibility-services-to-hijack-the-system/)”漏洞利用广泛利用了这一弱点。覆盖 API 的功能早在 Android Oreo 时就已经受到限制，但现在 Android Q 的 Go 版本已经完全删除了对该 API 的访问，未来的[版本将完全摒弃它](https://www.xda-developers.com/android-q-system-alert-window-deprecate-bubbles/)。

### 后台活动启动限制

当手机解锁时，后台的应用程序不再能够自动启动活动，无论它们的目标 API 级别如何。有一个完整的列表，列出了应用程序现在可以启动活动的条件，你可以在这里阅读。不满足这些条件并希望紧急启动活动的后台应用程序现在必须通过通知告诉用户。如果通知是以待定全屏方式创建的，则在屏幕关闭时会立即启动该方式，这对于报警或来电非常有用。

### 后台剪贴板访问限制

后台剪贴板访问[不再可能](https://www.xda-developers.com/android-q-blocks-background-clipboard-access/)。任何不在前台或设置为默认输入法的应用程序都不能以任何方式读取您的剪贴板。这对剪贴板管理器这样的应用程序打击尤其大。谷歌表示，这一变化只影响专门针对 Android Q 的应用，但我们的测试表明，这一限制并不歧视；我们尝试的任何应用程序都无法看到剪贴板。

当然，这种变化是有意义的。我们经常将敏感信息复制到剪贴板上——比如密码和信用卡信息——但是看到剪贴板管理器付诸东流仍然是一种耻辱。

### 仅在应用程序正在使用时进行位置访问

 <picture>![Android Q location permission options](img/eb60b104d8e8540c4aa8c1fcb1b1c185.png)</picture> 

New location permission options

新的用户启用设置仅允许应用程序在使用时到达您的位置。最新的 Android Q 测试版还增加了一个通知，提醒你是否已经授权一个应用程序永久访问该位置。

### 角色

 <picture>![Android Q Roles Page](img/18cd62fbdef32e50024db8d17542fce3.png)</picture> 

Roles

添加了一个新的“角色”API。角色本质上是具有预设权限访问的[组。例如，具有画廊角色的应用程序可以访问您的媒体文件夹，而具有拨号器角色的应用程序可以处理呼叫。被用户授予特定角色的应用程序也必须具有所需的组件。例如，具有图库角色的应用必须具有动作意图过滤器 **、安卓 。 意图 。 动作 。 MAIN** 和类别意向过滤器**Android . intent . category . APP _ GALLERY**在设置中显示为图库 app。](https://www.xda-developers.com/android-q-privacy-permission-controls/)

### 传感器关闭快速设置图块

 <picture>![Android Q Sensors Off](img/2b78098f46b2368c48144f98eb45614c.png)</picture> 

Sensors Quick Settings tile

有一个新的“传感器关闭”快速设置磁贴，可以关闭所有传感器(加速度计、陀螺仪等)的读数。)以获得真正的隐私。默认情况下，此快速设置磁贴是隐藏的，但可以通过转到开发人员选项中的“快速设置开发人员磁贴”来启用。

### 对/proc/net 的限制

应用程序不能再访问 proc/net，使得 netstat 这样的服务不再可行。这可以保护用户免受恶意应用程序监视他们连接的网站和服务。需要持续访问的应用，比如 VPN，需要使用**网络统计管理器**和**连接管理器**类。

### 随机 MAC 地址

您的 MAC 地址是网络用来记住哪个设备是哪个设备的唯一标识符。在 Android Q 中，每当你连接到一个新的网络时，你的设备都会使用一个新的随机 MAC 地址。因此，[网络无法通过将您连接的 WiFi 网络与您手机的 MAC 地址进行匹配来跟踪您的位置](https://developer.android.com/preview/privacy/data-identifiers#randomized-mac-addresses)。应用程序仍然可以通过 **getWifiMacAddress()** 命令获得设备的实际出厂 MAC 地址。

* * *

## Android Q 中的平台加固

Android 中的一个漏洞并不意味着攻击者现在可以完全访问操作系统，或者他们可以绕过任何安全系统。这部分是由于大量的安全措施，如进程隔离、攻击面减少、架构分解和漏洞缓解。这些安全措施使得漏洞更加难以甚至不可能被利用。因此，攻击者通常需要大量的漏洞才能实现他们的目标。在过去，我们已经看到了像 DRAMMER 这样的攻击，它们通过将多个漏洞链接在一起来工作。

Android Q 采取了这样的保护措施，并将它们应用于更敏感的领域，如媒体和蓝牙组件以及内核。这带来了一些显著的改进。

*   软件编解码器的受限沙箱。
*   增加杀毒程序的生产使用，以减少处理不可信内容的组件中的各类漏洞。
*   影子调用栈，它提供后向边缘控制流完整性(CFI ),并补充 LLVM 的 CFI 提供的前向边缘保护。
*   使用只执行内存(XOM)防止地址空间布局随机化(ASLR)泄漏。
*   引入了 Scudo 强化分配器，使得大量与堆相关的漏洞更难被利用。

这是一大堆软件术语。其核心是，首先，软件编解码器现在运行在沙箱中，具有更少的权限，这意味着恶意软件不太可能能够运行可能损害您设备的命令，例如 2015 年的 [StageFright](https://www.xda-developers.com/stagefright-explained-the-exploit-that-changed-android/) 事件。

 <picture>![Software codec sandboxing in Android Q](img/eef7aa4c0b5d3cfd58de27f61cf8be23.png)</picture> 

A constrained sandbox for software codecs. Source: Google.

其次，Android 现在检查更多地方的越界数组访问，以及溢出。防止溢出并指示进程安全地失败会显著降低用户空间漏洞的百分比。这意味着，如果一个恶意程序试图通过故意试图访问不存在的数据来导致某个东西崩溃，Android 现在会识别出这一点并退出程序，而不是崩溃。

第三，影子调用栈通过将返回地址存储在单独的影子栈中来保护它们，使它们不能被常规程序访问。返回地址通常是指向函数的指针，因此保护这些地址对于确保攻击者不能访问他们不应该访问的函数非常重要。

第四，ASLR 是一种保护方法，它将程序存储在内存中的位置随机化，使得根据其他程序的位置来找出程序存储在内存中的位置变得更加困难。只执行内存通过使代码不可读来强化这一点。

最后，Scudo 是一个动态堆分配器，它主动管理内存，使得基于堆的漏洞更加难以利用。你可以在这里阅读更多相关信息[。](https://llvm.org/docs/ScudoHardenedAllocator.html)

* * *

## 证明

### Android Q 中 BiometricPrompt 的更新

一年多前，谷歌在 Android P 开发者预览版 2 中引入了新的 BiometricPrompt API。它原本是一个通用的生物识别解锁方法的 Android 提示。这个想法是，不仅仅支持指纹扫描的设备，例如三星 Galaxy S 系列上的虹膜扫描，将能够在应用程序要求验证时使用这些方法。

Android Q 增加了对人脸和指纹验证的强大支持，并扩展了 API 以支持隐式身份验证。显式身份验证要求用户在继续之前以某种方式进行身份验证，而隐式身份验证不需要更多的用户交互。

 <picture>![BiometricPrompt API changes in Android Q](img/f7a8264af771087fae3b53a45552a959.png)</picture> 

BiometricPrompt API implicit and explicit flow. Source: Google.

最重要的是，应用程序现在可以通过一个简单的函数调用来检查设备是否支持生物认证，这样他们就不必浪费时间在不支持生物认证的设备上调用生物认证提示。一个理想的用途是，如果应用程序希望根据设备是否支持生物认证来提供“启用生物认证登录”设置。

### 支持电子身份证的构件

今年早些时候，我们发现有证据表明谷歌正在安卓系统中支持电子身份证。在 I/O 上，谷歌向我们更新了该功能的进展。谷歌表示，他们正在与 ISO 合作，以标准化移动驾照的实施，电子护照也在工作中。对于开发者来说，谷歌将提供一个 Jetpack 库，这样身份应用就可以开始制作了。

* * *

## Android Q 中的项目主线

Project Mainline 是 Google 的一项主要任务，旨在减少某些系统模块和应用程序的碎片化。谷歌将通过 Play Store 控制大约 12 个系统组件的更新。如果您有兴趣阅读更多内容，我们已经在之前的文章中深入讨论了项目主线[。](https://www.xda-developers.com/android-q-project-mainline-security/)

* * *

## 结论

安全性一直是 Android 开发的核心部分。谷歌在让安卓系统与最新的安全功能保持同步方面做得令人印象深刻，同时也做出了一些自己的创新。他们继续 Android Q 的开发过程，使其充满安全特性，以确保您的数据比以往任何时候都更安全。

* * *

[**来源 1:安卓 Q 安全新功能【谷歌】**](https://android-developers.googleblog.com/2019/05/whats-new-in-android-q-security.html)

[**来源二:Android 上的安全:下一步是什么【谷歌】**](https://www.youtube.com/watch?v=0uG_RKiDmQY)

[**来源 3:队列硬化增强功能【谷歌】**](https://security.googleblog.com/2019/05/queue-hardening-enhancements.html)

米莎尔·拉赫曼和亚当·康威参与其中。