# 谷歌可能会删除 Android P 中未记录/隐藏的 API

> 原文：<https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/>

**2018 年 2 月 28 日**更新:谷歌今天发布了一篇博客文章，证实了这些变化。更多详情在文末。

当一些 Android 爱好者在猜测下一个版本的 Android 将以什么甜点命名时，一些有趣的发展正在幕后进行。我们已经在 Android P 中发现了[几个值得注意的](https://www.xda-developers.com/tag/android-p/)即将推出的功能，但 Android 开源项目(AOSP)中一个更近的发现被证明要有趣得多。根据这些最近的提交，应用程序可能被限制访问 Android SDK 中未记录的 API(例如由 javadoc 的属性@hide 标记的 API)。

* * *

## 为什么这很重要

Android 软件开发工具包(SDK)为开发人员提供了测试和构建新的 Android 应用程序所需的 API 库和工具。随着 Android 的每一个新版本，开发人员都可以通过 Android SDK 获得大量新的 API。应用程序可用的 API 取决于开发人员设置的编译器版本。这就是为什么谷歌的[新 Play Store 需求](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)如此重要——它将迫使应用程序更新并迁移到使用更新的 API。

Google 为每个类和每个 API 级别中可用的所有方法托管了[文档页面](https://developer.android.com/reference/classes.html)。这些是官方 Android SDK 中提供的一组有文档记录的 API。你可以使用 Android 应用程序轻松浏览课程列表，例如 Android 工程师[杰克·沃顿](https://twitter.com/JakeWharton)最近发布的 Android SDK 搜索应用程序。

然而，并不是每个 Android 版本中可用的所有 API 都被 Google 记录在案，或者在官方 Android SDK 中可用。通常有一些有用的 API 是[未记录的](https://forum.xda-developers.com/showthread.php?t=1711653)，但是仍然非常有用。不建议开发人员使用未记录的或隐藏的 API 来构建他们的应用程序，但许多人这样做是因为如果他们想提供某个特定的功能，他们没有其他选择。使用隐藏或未记录的 API 的开发人员也可以使自己处于竞争优势，因为他们可以提供他们的竞争对手——坚持 Android SDK 提供的 API——无法提供的功能。

虽然我无法提供使用未记录 API 的应用程序列表(开发人员可能不会分享他们使用的应用程序，因为这会让他们的竞争对手占上风)，但这个列表可能相当大。因此，我认为禁止访问隐藏的 API 意义重大。Commonsware 的创始人马克·墨菲对此表示赞同:

> #### 我同意这样的评估:如果真的实现了，大规模禁止访问带@hide 注释的项目将是一件大事。希望很少有应用程序将这些项目作为关键功能的一部分来访问。然而，我怀疑许多名牌应用有时会直接或通过图书馆使用它们。

* * *

## Android P 到底是怎么回事？

这些即将到来的变化首先被 XDA 资深公认开发者 [rovo89](https://forum.xda-developers.com/member.php?u=4419114) 注意到， [Xposed 框架](https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/)的开发者。他向我指出了两个提交，其中一个是[，它的](https://android-review.googlesource.com/#/c/platform/art/+/580003/)已经被[合并了](https://android-review.googlesource.com/#/c/platform/art/+/565782/)，引入了一个新的构建工具‘hiddenapi’如果 DEX 文件中所有类成员的签名出现在输入灰名单或黑名单中，该工具将修改它们的访问标志，如果是这样，被标记的方法将被视为访问受限的内部 API。另一个提交描述了 API 黑名单是如何工作的；它阻止对由前述‘hiddenapi’标记的[引导类](https://forum.xda-developers.com/wiki/BOOTCLASSPATH)方法和字段的访问，开发者可以通过静态链接、反射和 JNI 来访问这些方法和字段。

根据 rovo89 的说法，Android P 的这两个变化的最终结果如下:

> #### 如果这些提交被合并，这将意味着应用程序不能再使用/访问隐藏的 API，即在 AOSP 用@hide 注释的类、方法和字段，因此不是官方 SDK 的一部分。这对于 Xposed 模块来说不是问题，因为我可以很容易地恢复这些提交或者允许模块也访问这些 API。但是有许多应用程序利用了隐藏的 API，这些应用程序将来会失败。

事实上，进一步的提交表明这可能是谷歌的计划。该[提交](https://android-review.googlesource.com/#/c/platform/external/doclava/+/586606/)声明如下:

虽然这个特定的提交没有被合并，因为它被放弃以支持 3 个更小的提交，但提交消息描述了这些更改的目的。另一组[提交](https://android-review.googlesource.com/#/q/topic:hiddenapi-doclava+(status:open+OR+status:merged))表明谷歌将向寻求使用非公共 API 的开发者建议替代方案:

然而，对于某些隐藏的 API，通常没有替代方法。我们在 XDA 可以从经验上说，不幸的是，这种变化可能意味着一些创新应用的终结，或者它可能需要一些大牌应用来减少它们的功能。这一即将到来的变化似乎与最近[打击无障碍服务](https://www.xda-developers.com/google-threatening-removal-accessibility-services-play-store/)的精神相似(谢天谢地[在谷歌评估创新用途时暂停了](https://www.xda-developers.com/google-pauses-accessibility-services-takedown/))。虽然大多数应用程序利用未记录的 API 是出于善意，但可能有一些应用程序出于恶意滥用了它们。

正因为如此，谷歌可能会锁定对 Android P 中所有隐藏 API 的访问，以保护用户免受少数人的滥用。很难说这会对用户产生多大的影响，但是如果你是一个正在考虑浏览 AOSP 来寻找一个隐藏 API 的创新用法的开发者，那么你可能要重新考虑了。

* * *

## 更新:谷歌证实

在今天(2 月 28 日)发表的一篇博客文章中，谷歌证实了这些变化。谷歌表示，由于用户面临崩溃风险，随后迫使开发者推出紧急修复程序，该公司已逐渐转向劝阻开发者访问非 SDK 接口。从 Android P 开始，限制将扩展到 SDK 的 Java 语言接口。

该公司声明“一些非 SDK 方法和领域将受到限制”，尽管他们没有详细说明哪些将受到限制。最初，限制将集中在很少使用的接口上，在一段时间内，公司将允许开发人员继续使用非 SDK 方法和领域，在这些领域中，过渡到 SDK 方法在技术上具有挑战性。然而，最终限制将会扩大，因此使用非 SDK 方法的应用程序开发者应该尽快过渡，为 Android P 做准备。至于没有 SDK 替代方法的方法，谷歌要求开发者在他们的 [bug 追踪器](https://issuetracker.google.com/issues/new?component=328403&template=1027267)上发布更多信息。

下一个开发者预览版，表面上很快就会到来，将允许开发者在最终发布之前根据黑名单或灰名单测试现有的应用。