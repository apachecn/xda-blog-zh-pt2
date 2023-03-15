# 牛轧糖和 abforce 子模块的公开框架已说明

> 原文：<https://www.xda-developers.com/xposed-nougat-abforce-explained/>

Xposed 框架过去是——现在仍然是——定制 Android 设备的主要方式，兼容几乎所有设备，让您可以轻松安装模块来调整几乎任何细节。

想要获得定制 ROM 提供的所有功能，而无需闪存？[gravity box](https://forum.xda-developers.com/xposed/modules/app-gravitybox-v6-0-0-tweak-box-android-t3251148)或者[XTouchwiz](https://forum.xda-developers.com/xposed/modules/app-xtouchwiz-customize-stock-samsung-t3296878)都会这么做。想要在每个应用程序的基础上调整某些设置，如更改特定应用程序的 DPI？ [App 设置](https://forum.xda-developers.com/xposed/modules/mod-app-settings-v1-9-2014-05-14-t2437377) 有你涵盖。希望应用程序的开发者想到添加一个特定的功能，像谷歌让你 [个性化 Hangouts](https://forum.xda-developers.com/xposed/modules/xhangouts-mms-fixes-google-hangouts-t2888102) 或者脸书让你 [下载你喜欢的 Instagram 帖子](https://forum.xda-developers.com/xposed/modules/mod-xinsta-download-images-videos-t3077110) ？您不需要这样做，因为 Xposed 让开发人员能够修改他们想要的任何东西，无论是需要定制 ROM 的系统级特性，还是针对特定应用程序的调整。

对于开发者来说，Xposed 框架有一个很大的优势，那就是易于开发(相比之下，必须为 ROM 调整编译 AOSP，或者必须编辑 Smali 代码)。它还为用户带来了巨大的优势:**方便，因为它不再强迫他们找到并闪存提供他们正在寻找的每一个功能的 ROM(相反，他们可以混合和匹配独立的模块)，以达到他们的稳定性和性能的目标平衡。它还使 **调整应用程序** 变得更加容易，因为不需要处理不同的签名，这将要求用户卸载原始版本或在应用程序检查其签名时跳过某些环节(例如，修改后的 YouTube 客户端处理的事情)。**

 **唯一的问题？由于其性质和 Xposed 的开发者(我们自己的资深公认开发者， [rovo89](https://forum.xda-developers.com/member.php?u=4419114) )所拥有的空闲时间量，它往往落后于 Android 版本。 [大概用了四个月的时间才更新到支持棒棒糖](https://www.xda-developers.com/xposed-framework-for-android-lollipop-is-here/) ，大概用了一年的时间才来到牛轧糖。如果你想一想 *有多少 Android 用户实际上在使用牛轧糖* (大约 13.5%[)这并没有看起来那么糟糕，尽管请记住 Android 爱好者、Xposed 的目标受众也更有可能在使用牛轧糖)。然而，不能同时使用您最喜欢的 Xposed 模块和最新最棒的 Android 版本仍然是非常令人讨厌的。](https://developer.android.com/about/dashboards/index.html)

有了 Xposed 框架的源代码(至少对于稳定的已发布版本来说)，开发者 [abforce](https://github.com/abforce) 决定亲自动手，看看他能否将 rovo89 的一些修改移植到 Nougat 上。abforce 选择了一种不同的、更简单的方法，从本质上修改了 Xposed 的一部分，它实际上在安装后就变得很神奇，并且使得在编译你自己的 ROM 时包含它成为可能(在那之后，[其他的解决方法浮出水面](https://www.xda-developers.com/flashable-xposed-framework-android-nougat/))。这种方法可以说是非常不同的**，因为它忽略了 Xposed 的核心优势之一，即每个人都可以轻松使用。**然而，所有的进步都是受欢迎的，多头处理一项任务可能是有利的，并提供新的见解。在我们看来，主要问题是围绕这一发展的错误信息(由一些其他“开发者”和一些博客传播)，以及社区的一些反应。希望这篇文章能让整个画面更清晰。

* * *

# Xposed 是如何工作的？

首先，为了理解官方 Xposed 框架以及 abforce 版本的工作，我们需要看看这个框架是如何工作的。虽然框架本身只是项目**的一部分** *，但我们通常指的是框架和安装程序，因为没有通用安装程序，框架失去了许多优势，这也需要大量的工作。*

Xposed 的强大来自一个简单的概念:任何方法都可以被“挂钩”(方法是组成任何程序的小部分)，让 Xposed 模块的代码在它之前、之后或代替它执行。让我们举一个简单的例子:假设 Instagram 在你点击菜单按钮时使用了一个名为“showMenuOptions”的方法，该方法处理向你显示“报告”和“分享”按钮。例如，通过创建一个 Xposed 模块，您可以修改该方法，添加一个额外的按钮来下载图像，而不是共享图像。修改的范围可以从简单的调整(例如 [播放商店变更日志](https://forum.xda-developers.com/xposed/modules/mod-play-store-changelog-changelog-t2922667) )到大的检修(例如 [重力盒](https://forum.xda-developers.com/xposed/modules/app-gravitybox-v6-0-0-tweak-box-android-t3251148) ，其目的是提供定制 rom 将具有的所有特征)！

这让 Xposed 变得强大，但这只是等式的一部分。其他部分是多功能性——或者实际上能够在几乎任何设备上使用 Xposed(支持 Android 版本)，以及易用性。用户所要做的就是抓取安装程序，它会发挥它的魔力，动态地修补他们的系统来集成 Xposed。要应用一个模块，你只需要安装它，启用它，并重新启动。不需要大惊小怪，不需要刷新自定义 ROM(特别是当自定义 ROM 并不总是可行的选择)，不需要卸载 APK 来安装另一个不同的签名签名。所有你需要的是根(你绝对可以有一个自定义的 ROM，这在很多时候是有意义的；但是虽然 Xposed 可以提供定制 ROM 所能提供的大部分功能，但它还不止于此)。

尽管如此，在这种简单的背后还有很多工作要做

1.  **对于模块开发者来说，提供的 API 必须是稳定的，保证能够工作。**x posed 框架不能随机失效某些 ROM 和/或 hook 组合(例外情况除外)。换句话说，如果用户遇到问题，这个问题应该是用户的错误(没有正确安装/启用某些东西)或者是模块开发人员的错误(模块中有错误)。但几乎可以肯定的是，框架本身正在按预期工作，而不是会让用户沮丧和开发人员困惑的错误来源。
2.  对于用户来说，该框架必须易于安装在他们的设备和 ROM 上，无论他们是运行最新版本 TouchWiz 的三星还是安装了 LineageOS 的 Nexus。Xposed 安装程序在幕后处理所有这些。为了在各种设备和 ROM 组合上测试安装程序和框架，必须做大量的工作。发现错误，通常是由于 OEM 的不同实现，必须修复以确保所有用户的可靠性。
3.  Android 的重大修订有时会带来重大变化，这需要重新思考框架架构的某些部分，以适应这些变化。 有时，新版本也会带来额外的机会，需要一些额外的时间来开发更好的产品。例如，当 ART 第一次被引入时，让 Xposed 禁用了某些优化，以便挂钩可以正确工作。以牛轧糖为例， [实时(JIT)编译器](https://developer.android.com/about/versions/nougat/android-7.0.html#jit_aot) 给 [保留那些优化](https://github.com/rovo89/Xposed/issues/230#issuecomment-316623920) 带来了机会。

上面的许多工作都涉及到了次要的细节，框架的大部分功能都符合预期，但是不一致和次要的问题会让用户觉得这是一场赌博，也是模块开发人员的支持和开发噩梦。 **然而，发布的产品旨在让所有人都可以使用，没有任何意外。** 当然，也有一些例外，因为一些原始设备制造商的变化需要更多的努力来适应，但这些都是次要的，绝大多数用户(和开发者)都享受到了稳定可靠的体验。任何遇到的异常都用 [明确的免责声明](https://forum.xda-developers.com/showthread.php?t=3034811) 记录下来，这样就不会有人感到惊讶了。

综上所述，rovo89 对 Xposed 的愿景是成为一个稳定的解决方案，为用户和开发者提供可靠且易于使用的合同。尽管你可能不同意他的观点，但他的理念简单易懂:产品应该在准备好可以使用的时候发布，因为之前发布会带来更多的麻烦而不是好处。

* * *

## abforce 的牛轧糖展示艺术子模块

我们不愿意称 abforce 的工作为“港口”或“非官方的曝光”,因为这是不准确和误导的。正如我们所见，Xposed 有两个主要组件:

1.  Xposed 框架本身的核心，它处理挂钩方法的魔力。
2.  Xposed installer，确保该框架易于在所有设备上正确安装。

abforce 所做的是在 Nougat 的第一部分(仅 Xposed 框架)上移植 rovo89 的 Marshmallow 代码，这种方式要求在编译自定义 ROM 时烘焙更改。除此之外，框架的许多次要(但重要)部分没有完全适应牛轧糖。就这一点而言，行为可能是不一致的，虽然它大多是有效的(尽管 [而不是](https://forum.xda-developers.com/showpost.php?p=73293259&postcount=1849) [对于](https://forum.xda-developers.com/showpost.php?p=73293330&postcount=1850) [每个人](https://forum.xda-developers.com/showpost.php?p=73289505&postcount=1828) )，但这并不可靠。对于模块开发者和用户来说，依赖于不完整和不一致的实现只会 [为所有相关方提供不好的体验](https://forum.xda-developers.com/showpost.php?p=73097833&postcount=9061)[一些模块根本无法工作或者导致设备无法启动](https://github.com/abforce/xposed_art_n/issues/1#issue-243599788) 。虽然许多用户可能不介意拥有 [而不是一无所有](https://forum.xda-developers.com/xposed/unofficial-list-modules-nougat-xposed-t3639615) ，但是开发者的观点仍然是完全可以理解的(特别是如果你记住免责声明不能阻止虚假的支持问题和抱怨)。

(除了以上两点，我们还将期待最终的官方 Xposed 框架的进一步变化，以利用 Nougat 中引入的变化。)

**应该注意的是，当大多数人满足于简单地谈论** 时，abforce 做得非常出色，但他的工作远非完全的体验，也没有开发者或博客声称不是这样(abforce 肯定不是；再说一次，我们对所有真正投入工作和精力的开发者充满敬意。事实上，正如我们稍后将提到的，社区的一些反应(无论是用户还是“开发者”)是这个开发链中唯一令人不快的部分。

* * *

# 社会反应

让我们开门见山，直奔主题:任何社区都有不好的元素和方面。对于像 Android 爱好者这样庞大的社区来说，不良分子可能看起来像是很大一部分，但他们只是很小的一部分(相当大，但相对而言仍然很小)。没有糖衣，虽然，很多社区对牛轧糖的开发的反应是非常幼稚的，不体贴的或不负责任的。

第一个主要问题是许多人对“Xposed 之死”表现出的居高临下的态度，因为牛轧糖发布的时间太长了。尽管 rovo89 的 [更新了](https://www.xda-developers.com/rovo89-updates-on-current-status-of-xposed-for-android-nougat/) [和](https://www.xda-developers.com/rovo89-updates-on-the-situation-regarding-xposed-for-nougat/) [保证了](https://www.xda-developers.com/xposed-android-nougat-support/) ，尽管在 ART 的最初版本推出时 Lollipop 发生了几乎完全相同的情况。停止使用 Xposed 是好的，但这不是侮辱任何人的能力或攻击其他人有不同的哲学或不能确保你的闪存需求立即得到满足。对于一个完全自由的项目来说更是如此，开发者已经表达了他的开发方法和背后的原因。

社区反应的另一个问题是对 abforce 工作性质的误解，许多人称赞它是新的 Xposed 或宣传它是牛轧糖的港口。这方面的一个主要问题是“开发人员”急于提供 flash 版本，而没有理解(或关心)缺点，因为在一些线程中根本没有提供免责声明，有些人甚至认为应该归功于 abforce，而不是 rovo 89(x posed 的绝大多数工作背后的人)和其他贡献者。

作为最后一点，我们觉得应该再次提出 rovo89 的开发理念。许多直言不讳的用户声称让最新的变化开源将是有益的。虽然这在理论上听起来不错，但在实践中它的 [并不容易](https://en.wikipedia.org/wiki/The_Mythical_Man-Month) 尤其是如果我们考虑 rovo89 的解释:

*[...]我认为仅仅推出当前状态对项目没有帮助。我们可能会看到“一些”由编译代码的人很快发布，看到它似乎工作良好，并将其作为“他们的端口”发布，尽管他们不会意识到这些问题和要做的事情。所以说我自私吧，但我不会希望看到这样一个半成品的发布。* [*【出处】*](https://github.com/rovo89/Xposed/issues/225#issuecomment-314017010)

这实际上被证明是对当前形势的一个相当好的预测，几个“开发者”应用了 abforce 的变化，并提供了一个 flash ZIP，只有最少或没有警告，不完整的学分，同时要求捐款。

* * *

我们希望这些解释消除了你的一些疑虑，并解决了你可能有的误解。Xposed 是一个令人惊叹的项目，已经吸引了我们的大量爱好者和 flashaholic 社区，Xposed for Nougat 应该是另一个充满机会的巨大里程碑。随着像 GravityBox 这样的模块已经提供牛轧糖支持，rovo89 的完成项目将返回到一系列选项。

* * *

***你对自己的牛轧糖 ROM 曝光感到兴奋吗？请在评论中告诉我们！*****