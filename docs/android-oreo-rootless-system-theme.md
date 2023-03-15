# 独家:Android Oreo 将在 1 周内获得无根、全系统主题支持

> 原文：<https://www.xda-developers.com/android-oreo-rootless-system-theme/>

更新 09/13/17:Andromeda add-on for Substratum 允许在非 root Android Oreo 设备上定制主题，现已发布。[详见本文](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)。原文会留在下面。

随着谷歌 Android 操作系统的每一个新版本的发布，大多数用户不再有理由让他们的设备扎根于 T2。然而，在仍然选择根设备的剩余用户中，最常引用的原因之一是启用系统范围的主题支持。通常，这是通过底层[主题框架](https://www.xda-developers.com/layers-manager-is-being-deprecated-in-favor-of-substratum/)来管理的，自从[CyanogenMod 主题引擎](https://www.xda-developers.com/exclusive-dead-cyanogenmod-theme-engine-cmte-not-coming-back-lineageos-replacement/)不幸消亡之后。随着时间的推移，底层背后的[团队努力工作，通过在 ROM 级别](https://www.xda-developers.com/an-interview-with-the-team-behind-the-substratum-theme-engine/)加入底层支持[来包含对更多设备的支持，因此它可以在没有根访问的情况下运行。现在，该团队已经超越了我们任何人的想象，为任何 Android Oreo 设备带来了完全系统范围的主题支持。](https://www.xda-developers.com/substratum-to-work-on-custom-roms-without-root-soon/)

*截图显示 [Sai 的安卓奥利奥黑色主题](https://play.google.com/store/apps/details?id=baka.sai.o)运行在安卓奥利奥 8.0.0 的未 root 谷歌 Pixel 上*

为了让你知道这是多么不可思议的一个发展，考虑下面这些没有根的**现在将是可能的:**

*   Android 框架和 Android 系统 UI 以及任何其他系统应用的主题化。(你们中的许多人将会爱上*，终于有了一个黑暗主题！)*
**   任何第三方应用程序的主题化*   第三方应用程序的自定义字体*   许多其他修改，如状态栏中心时钟模式*

 *不胜枚举！Substratum 有一个[广泛的可用主题列表](https://play.google.com/store/search?q=substratum&c=apps)，支持框架*(所有这些都在即将发布的 Android 8.0 Substratum 新版本中得到支持)*， [Google+](https://plus.google.com/communities/102261717366580091389) 上的活跃社区和我们自己的[论坛](https://forum.xda-developers.com/apps/substratum)，鉴于这种发展，这种支持必将增长！

* * *

## Android Oreo 和覆盖管理器服务

 <picture>![Substratum Theme Support](img/0b533a03d30e8a548746403516305239.png)</picture> 

A sample of some Substratum Themes.

自从谷歌在 Android 6.0 棉花糖、[中加入了对索尼运行时资源覆盖](https://www.xda-developers.com/a-brief-history-of-theming-from-oem-themes-to-rro-layers/) (RRO)主题引擎的原生支持以来，我们一直在等待谷歌提供一个内置接口和公共 API，开发者可以使用它们来主题化系统框架应用程序和第三方应用程序。唉，自从索尼的 RRO 被加入 Android 开源项目(AOSP)以来，Android Nougat 的发布并没有带来什么新的东西。

但是多亏了索尼移动工程师们的勤奋工作，RRO 主题引擎最终演变成了覆盖管理服务(OMS ),这也是 Substratum 所基于的。索尼是开源主题解决方案的先驱，但自从他们的 OMS 主题引擎在最终的 Android 7.1 发布时被 AOSP 接受以来，非索尼设备的用户利用主题引擎的唯一方式就是通过定制的 ROM。

这在 Android 8.0 中有所改变。当 Substratum 最初为[首批 Android O 开发者预览版](https://www.xda-developers.com/latest-substratum-update-adds-full-android-o-theming-dynamic-refresh-mode-and-more/)发布时，Substratum 的开发者意识到[对索尼](https://android.googlesource.com/platform/packages/apps/Settings/+/android-8.0.0_r4/src/com/android/settings/display/ThemePreferenceController.java) [OMS](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/om/OverlayManagerService.java) 的全面支持已经可用。这意味着用户可以安装一个现有的底层支持的主题，它将在 Android Oreo 设备上完全运行，而不需要任何 ROM 补丁。不过只有一个问题:启用已安装底层主题的过程需要 root 访问权限，*或者他们认为是*。

* * *

## Android Oreo 的无根、全系统底层主题支持

虽然开发人员悄悄地把他们的工作放在为 Android Oreo 用户提供一个完全无根的主题解决方案的问题上，但我们独立地挖掘了每个 Android O 开发人员预览版，并找到了主题引擎发挥作用的证据，尽管[我们误认为它](https://www.xda-developers.com/google-preparing-enable-custom-themes-built-on-sony-rro-framework/)是基于旧的 RRO 而不是索尼的新 OMS。谷歌甚至在 Reddit 上以开发者为中心的 AMA 上取笑社区对主题的支持，声称在完整的主题化解决方案可以内置到 Android 中之前，还有一些障碍需要克服。

我们对这个答案并不满意，我们想看看 Google 在为 Android Oreo 获得主题支持方面走了多远。为了做到这一点，我在最终版本发布后深入研究了 Android 8.0 的源代码，并发现了亚行 shell 命令的[存在，这些命令可以启用或禁用覆盖](https://www.xda-developers.com/android-oreo-command-line-themes/)，XDA 作家亚当·康威昨天对此进行了报道。

 <picture>![Substratum Theme Support Android Oreo CMD Overlay](img/c2a0d194e7d62fac19e414862aba3d9f.png)</picture> 

Disabling the default overlay

最初，我对这个发现没有太大的印象，因为据我当时所知，它在功能上是无用的，因为我和我的同事认为安装一个主题仍然需要 root 访问权限，因为主题文件需要移动到用户空间无法访问的文件夹中(在/system/vendor/overlay 中，这就是 RRO 的功能)。Substratum 的主要开发者之一 Nicholas Chum 自己在我们的帖子中评论说，他知道这些命令的存在已经有一段时间了，[已经在 Android O 版本中使用它了](https://github.com/substratum/substratum/blob/release/app/src/main/java/projekt/substratum/common/platform/ThemeManager.java#L61-L64)。

然而，有一个人在我们昨天发表文章后看到了机会。XDA 自己的[杰夫·科克兰](https://www.xda-developers.com/interview-with-xda-labs-and-feed-developer-jeff-corcoran-app-rom-development-the-future-of-xda-apps-and-more/)，我们内部 [XDA 实验室应用](https://www.xda-developers.com/xda-labs/)的开发人员，意识到有一个潜在的变通办法可以让安卓奥利奥的原生命令行界面在没有 root 的情况下为 OMS 工作。它涉及一种被流行的无根备份解决方案 [Helium](https://www.xda-developers.com/must-have-app-review-helium-backup-without-root/) 使用的方法，以及最近被称为 [Brevent](https://www.xda-developers.com/brevent-is-an-open-source-alternative-to-greenify-works-without-root/) 的开源 Greenify 替代方案使用的方法。

### 通过脚本提升权限

通常，谷歌添加到 Oreo 版本中的“ [cmd overlay](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/om/OverlayManagerShellCommand.java#72) ”命令只能通过具有 root 权限的设备运行，或者通过与调用 Android 调试桥(ADB)外壳的计算机相连的设备运行。几年来，一些聪明的开发人员，如氦和 Brevent 开发人员，想出了如何从本质上提升手机上运行的应用程序的权限，以匹配 ADB shell 的权限。这样，应用程序就可以发送由于受限权限而通常不能发送的命令。在底层的情况下，这意味着**应用程序可以安装，然后启用或禁用底层主题没有根**。

这一认识是昨天晚上才发现的重大突破。在几个小时的过程中，Nicholas(在 Jeff 的帮助下)能够为 Android Oreo 设备创建一个快速的无根底层主题管理器的 alpha 版本。它确实有效——但是有一些注意事项。

### 无根底层支撑的注意事项

授予 Substratum ADB shell 提升权限所需的过程将需要使用一个非常简单和轻量级的桌面应用程序(如果您知道自己在做什么，也可以只使用一个 ADB shell 命令)。一旦被授予，底层将发挥你所期望的功能，它能够处理管理你所有已安装的底层主题。**你安装的任何主题都将保持安装状态**，直到你再次选择通过底层卸载。

然而，Substratum 被授予的特权是暂时的，因为当用户执行完全重启时，它们**会丢失(尽管幸运的是系统 UI 的软重启不会丢失特权)。这意味着，如果你重启了手机，并希望使用 Substratum 来添加、删除或修改主题，你将不得不再次运行桌面程序。我想再次重申，**你安装的任何主题将保持安装，即使你重新启动**，这意味着如果你想只是偶尔改变一些主题，这应该是最适合你的。**你也应该能够从设置菜单**中切换主题，因为[开发者预览版在显示设置下的“主题”选项](https://www.xda-developers.com/android-o-adds-inverted-light-theme-to-display-options/)可以识别已安装的主题，并允许你在它们之间切换**

最后，我需要提到的最后一件事是，一旦你想起来似乎是显而易见的，但在你听到消息时的兴奋中，你可能已经忘记了。*您的设备仍未启动*。这意味着你不能接触或修改任何绝对需要 root 权限才能编辑的文件，即使你安装的 Substratum 主题承诺要改变一些东西。抱歉，但不幸的是，这意味着你不能应用一个系统范围的字体变化到[带回斑点表情符号，](https://www.xda-developers.com/android-o-redesigns-the-emojis-get-them-now-on-any-rooted-android-5-0-device/)虽然如开始提到的，它*是*底层主题可能改变个别应用程序的字体。

### 底层的必要性

现在让我们来解决一个重要的细节问题。这是什么时候？正如标题所提到的，谷歌 Nexus 5X、谷歌 Nexus 6P、谷歌 Pixel 和谷歌 Pixel XL 等 Android 8.0 设备的无根底层的首次公开可用性应该是在 1 周内**。这**无论如何都不能保证**，因为在开发过程中事情可能会发生变化，这可能需要额外的时间投入，但由于 OMS 已经在 AOSP 得到完全支持，所有的底层团队现在正在工作的是底层应用程序和非根设备之间的接口。**

接下来:它会是免费的吗？**号【Android Oreo 设备的底层将是一个**付费应用**。我不能告诉你要花多少钱，因为尼古拉斯还没有决定价格，但请放心，考虑到你将收到的东西的价值，这个价格是公平的。到目前为止，很多设备都可以免费使用 Substratum，所以可以考虑通过首先支持 Substratum 团队来支持这种开发。你可以等待谷歌最终发布你一直想要的黑暗主题(哈，不错的主题)，或者你可以投入几个便士来支持许多人认为理所当然的独立开发。**

还不相信它的价值？你可以*尝试*在你自己的非 root 8.0 设备上安装底层主题。事实上，这正是我们在上面所做的。当然，为了做到这一点，我们得到了尼古拉斯的一些帮助。如果你想从谷歌 Play 商店安装一个现有的底层主题，以下是一般步骤:

1.  下载并安装 APK 文件到您的设备上。
2.  提取内容，并将每个叠加图编译成一个单独的 APK 文件，用于每个要进行主题化的应用程序
3.  安装您在步骤#2 中手动编译的每个单独的覆盖 APK 文件
4.  对于您安装的每个覆盖 APK，运行以下命令来启用它:`cmd overlay enable <package>`
5.  如果您想更改覆盖的优先级，请使用:`cmd overlay set-priority <package> PARENT|lowest|highest`
6.  用`cmd overlay list`列出所有已安装的覆盖图
7.  使用`cmd overlay disable <package>`移除任何不想要的覆盖

如果你真的想使用命令行来管理主题，请自便！就我个人而言，我无法通过第二步。Substratum 并没有使用一些你自己想不出的隐藏方法，但是它让你更容易管理。当有可能手动做一些事情，但应用程序可以更容易地为我做，我倾向于让应用程序做它的工作。但这取决于你。

就我个人而言，我真的非常非常期待看到这一天的到来。对于任何还不支持内置主题管理系统的设备(如摩托罗拉或一加设备)，你现在有另一个理由期待 Android 8.0 的更新。对于那些有幸品尝过这种甜奥利奥的人来说，一周后你会有所期待。

* * *

三星用户，你知道你的设备[已经支持底层主题](https://www.xda-developers.com/sungstratum-samsung-substratum-touchwiz/)而不需要 root 吗？

你是一个有兴趣了解更多底层知识的开发人员吗？点击这里查看尼古拉斯的[精彩幻灯片演示](https://docs.google.com/presentation/d/1OMVCt1nbndrXFeLtC56xXH19Frax7Psw1xVhgkgGg7k/edit?usp=sharing)！*