# Android Oreo 上的无根底层主题引擎演示，并解决误解

> 原文：<https://www.xda-developers.com/video-rootless-substratum-theme-engine-android-oreo/>

# Android Oreo 上的无根底层主题引擎演示，并解决误解

Android Oreo 上无根底层主题引擎的视频演示。还有，关于即将到来的主题管理器的常见问题。

昨天，我们发表了一篇[独家文章](https://www.xda-developers.com/android-oreo-rootless-system-theme/)，详细介绍了许多 Android 爱好者一直渴望的东西:完整的、全系统的无 root 主题支持。这个主题支持是由 Team Substratum 提供给我们的，但是昨天，这个团队还没有准备好展示他们的作品。然而，这种情况已经改变了，因为尼古拉斯·查姆为 XDA 制作了一个视频，向你展示使用新的无根底层主题引擎在 Android Oreo 上应用主题覆盖会是什么样子。

* * *

## Android Oreo 上的无根底层主题引擎演示

**注意:“仙女座菌株”只是该团队在 Android 8.0 上使用的无根底层的代号。与传闻中的 [Google Andromeda 无关。](https://www.xda-developers.com/exploring-andromeda-a-look-at-the-challenges-awaiting-googles-next-voyage/)**

我建议您观看这个简短的 2:30 视频，演示主题管理器应用程序在 Android Oreo 8.0 上无 root 用户的情况下工作，这样您就可以真正地*看到*它是多么流畅，但以下是您应该从该视频中吸取的要点:

*   在视频中，他的手机与电脑没有关联。在他运行了一个**一键式**桌面工具(团队 Substratum 制作的)来启用 Substratum 的提升权限后，这是可能的。他不需要手动输入任何 ADB 命令。
*   一旦启用，底层应用程序可以很容易地**安装，启用，禁用，或卸载**底层主题-所有这些都在后台默默进行。变化是**立竿见影**。
*   他展示了框架、系统 UI 和一个单独的应用程序覆盖。他展示了导航栏、通知、设置和计算器应用的主题化。
*   他的手机是**未根**的，通过使用[根检查器](https://forum.xda-developers.com/showthread.php?t=927629)应用显示。

我希望这个演示有助于展示你的 Android Oreo 设备的主题化是多么的简单和无缝。然而，很多用户在昨天读了我的文章后，对 Android 8.0 的无根底层主题的某些部分感到困惑。虽然下面的所有问题都在那篇文章中得到了回答，但我意识到它包含了很多关于 Android 8.0 上完全主题支持的技术信息，以及它是如何工作的，所以这些要点可能被忽略了。因此，让我们澄清一些常见的误解。

* * *

## 常见问题

### 底层和安卓奥利奥

*   这只是一个第三方 app/框架/修改/黑掉，这个和谷歌或者安卓奥利奥官方无关！
    *   虽然谷歌在 Android 8.0 上确实没有提供主题管理应用，但这**并不意味着**这是一个“黑客”或“mod”。这里没有修改任何东西，也没有涉及到让它工作的黑客。Android 8.0 **原生支持 OMS 主题**，这也是 Substratum 所基于的。Substratum 正在使用谷歌官方的内置命令来改变主题，这些命令通过官方提供的 API 来改变主题。谷歌官方 Android 版本中唯一缺少的是一个主题管理器应用，这也是 Substratum 将要提供的。
*   那么为什么谷歌不提供一个主题管理器呢？
    *   我们不能说谷歌的动机。很明显，OMS 正处于它应该可以用于主题的阶段，但也许谷歌对 OMS 有另一个想法，因为它不仅仅可以用于主题。正如一个[承诺](https://android.googlesource.com/platform/frameworks/base/+/ea2f3be7aae9435ce21743c959b62731c87a36b8)所证明的，也许谷歌正在引入 OMS 支持，作为一种让原始设备制造商更容易支持多种类似设备的方式。
*   这会影响我的设备性能吗？会不会乱成一团？
    *   如果有*任何*性能影响，那将是非常**最小的**。索尼移动工程师已经对 OMS 进行了测试和改进，谷歌也对其进行了测试。Substratum 正在使用的主题框架不是业余爱好者开发人员拼凑的 API，而是来自索尼和谷歌的专业 Android 工程师的作品。
*   这会破坏 SafetyNet/Android Pay 吗？
    *   **否**。OMS/底层不修改任何文件。
*   这安全吗？
*   哪些手机会得到安卓奥利奥？
    *   不要问我们！大多数公司(除了 HTC 和 T2 和一加)还没有宣布他们将为哪些设备提供 Android 8.0 支持。不过，和往常一样，许多设备可能会接收 Android Oreo 的非官方端口(如[小米 Mi 3 和 Mi 4](https://www.xda-developers.com/android-oreo-xiaomi-mi-3-mi-4/) )，所以请继续关注我们的 XDA 实验室应用论坛！

### 设备支持

*   原始设备制造商能够屏蔽这项功能吗？
    *   是的。如果制造商选择的话，OMS 支持可能不会出现在你的设备上，但是你会惊讶于什么样的设备支持某种形式的 OMS。然而，如果 OMS 在其他设备上的实现与 AOSP 有很大不同，那么 Substratum 就有可能只在那些设备上有问题。不幸的是，这就是在没有这些制造商通常不提供的源代码的情况下盲目工作的后果！
*   这能在一加或摩托罗拉手机等非谷歌设备上运行吗？
    *   特别是一加和摩托罗拉的手机，如果或当这些设备获得 Android 8.0 更新时，应该可以使用这一功能。这并不是一种保证，而是一种观察，基于这样一个事实，即这些制造商往往不会偏离 AOSP 太远。
*   这将适用于哪些设备？
    *   任何当前的 Android Oreo/8.0 设备，如谷歌 Nexus 5X、谷歌 Nexus 6P、谷歌 Pixel、谷歌 Pixel XL 和谷歌 Pixel C。也可能是任何未来的 Android 8.0 设备，如[谷歌 Pixel 2、谷歌 Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-launch-snapdragon-836/) 、OnePlus 3、OnePlus 3T、OnePlus 5 和许多摩托罗拉设备。

*   为什么我需要桌面工具？
    *   通常，要在 Android 8.0 上运行更改主题所需的命令，你需要在一个 ADB shell 中。这意味着你要么需要一直插在电脑上(这很麻烦)。然而，Substratum 团队已经想出了一个窍门，使 Substratum 应用程序能够运行这些相同的命令**，而无需将**连接到您的计算机来使用 ADB。桌面工具是实现这个技巧的工具，它授予底层类似于 ADB shell 的特权。
*   你说的“特权提升”是什么意思
    *   Android 有一个适当的许可系统，防止应用程序使用可能对隐私或安全有潜在危险的服务和方法。然而，人们可以通过 Android Debug Bridge (ADB)做很多事情，这是一个旨在供开发人员调试和测试他们的应用程序或系统的各个方面的工具。Substratum 本质上运行在与 ADB 相同的特权级别，比 root 低一级，允许它运行某些命令，否则它不能这样做。
*   它运行的是什么命令？
    *   这些命令在这里列出[。](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r1/services/core/java/com/android/server/om/OverlayManagerShellCommand.java#72)
*   准入门槛太高！这对我来说太难了！
    *   如前所述，桌面工具将是一个**一键式工具**。只需在您的手机上下载 Substratum 应用程序，在您的 PC/笔记本电脑上下载该工具，运行该工具，您就可以开始了！
*   我必须通过亚行安装应用程序吗？我如何在我的设备上得到底层？
    *   谷歌 Play 商店上将会有无根的底层**。它的配套桌面工具可以在线下载，可能在我们的论坛上。不过，这并不难找到，这款应用会指引你找到它。**
*   我需要学习如何使用亚行吗？
    *   **否**。桌面工具将为您处理一切。尽管如此，我还是强烈建议你学习亚行，因为通过我们的教程，你可以用它做很多很酷的事情。
*   每次重新启动时，我必须重新启用我的主题吗？
*   每次开机时，我必须插上手机并运行桌面工具吗？
    *   除非你需要改变一个主题！**您已经启用的主题将在重新启动后保持启用状态**，但是如果您想要添加、删除或启用/禁用主题，您必须重新运行桌面工具。
*   为什么以及何时我必须在重启后运行桌面工具？
    *   当你重新启动时，Substratum 用来提升特权的进程被终止。因此，如果您决定在将来修改主题，您将需要再次运行该工具。大多数人选择一两个主题并坚持下去，所以这对大多数用户来说不应该是一个令人头痛的原因。
*   这在 Mac/Linux 上行得通吗？

### 主题

*   我能用这个得到一个黑暗的主题吗？
*   主题会因此免费吗？
    *   那要看主题了。Substratum 只是一个框架，它本身不提供任何主题。在 Play Store 上搜索[“sub tum ”,你会看到免费和付费主题的健康组合。](https://play.google.com/store/apps/collection/search_results_cluster_apps?clp=ggEMCgpzdWJzdHJhdHVt:S:ANO1ljKAR64)
*   我可以使用游戏商店中的任何主题吗？
    *   只要上面说和 Substratum 兼容，那就可以。
*   我找到的主题说需要 root 权限。但这不是无根吗？
    *   主题开发者只需要更新他们的游戏商店描述。
*   我可以改变字体或表情符号吗？
    *   是也不是。事实上，你不能在整个系统的基础上改变字体/表情符号，但你可以在每个应用程序的基础上这样做。例如，这里有一个 [Whatsapp 表情符号转换器](https://play.google.com/store/apps/details?id=com.thepsycraft.emojisub)应该可以工作。
*   为什么我不能更改字体、表情符号或其他一些东西？
    *   虽然你可以对任何系统和第三方应用程序进行主题化，但是并不是所有有根底层用户可以做的事情都适用于无根版本。例如，用 Substratum 更改字体需要实际修改位于系统分区中的字体文件，这需要 root 访问权限。
*   我真的需要有主题的基础吗？
    *   从技术上来说，不会，因为对 OMS 的支持是内置在 Android Oreo 中的，Substratum 使用的命令可以被任何拥有 ADB 的人使用，但如果没有它，这个过程会困难得多。
*   在没有底层的情况下，如何手动安装主题？
    *   您将需要覆盖 APK 文件，一个工作 ADB 设置，并熟悉命令行。你需要的命令在这里列出[。请注意，Play Store 中可用的主题并不是您需要的实际覆盖 apk。谷歌不允许 Play Store 上的应用包含其他应用。相反，Substratum 在设备本身上编译覆盖 APK 文件，然后使用前面列出的覆盖命令安装它们。](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r1/services/core/java/com/android/server/om/OverlayManagerShellCommand.java#72)

### 定价/发布信息

*   这要花多少钱？
*   为什么我要为底层付费？
    *   为了支持团队的开发工作，他们花费了无数的时间将这个令人敬畏的主题管理器带给你。
*   如果我是根用户或者使用自定义的 ROM，我需要为底层付费吗？
    *   没有。根用户/自定义 ROM 用户的底层将保持免费，一如既往。
*   什么时候发布？

还有其他问题吗？请在下面留下你的评论，我或者希望底层开发者可以回答！