# Android 11 AMA:没有滚动截图，更快的应用程序启动，等等

> 原文：<https://www.xda-developers.com/android-11-ama-summary/>

昨天，谷歌发布了 [Android 11 Beta 2](https://www.xda-developers.com/android-11-platform-stability-beta-2-available-google-pixel-2-3-3a-4-xl/) ，为开发者带来了最终确定的 SDK、NDK、面向应用的表面、平台行为以及对非 SDK 接口的限制。今天，谷歌在 Reddit 的/r/AndroidDev 社区[上回答了与 Android 11 相关的问题，这是继上周](https://www.xda-developers.com/google-android-11-developers-reddit-ama/)回答问题之后。这里总结了我们从谷歌 AMA 学到的一切(问我任何问题)。

当操作系统[于 9 月 8 日](https://www.xda-developers.com/stable-android-11-update-september-8th/)退出测试时，Android 11 最受期待的功能之一将无法使用:滚动屏幕截图。最初[计划在 Android 11](https://www.xda-developers.com/adding-scrolling-screenshot-support-android-infeasible/) 中推出，谷歌现在已经确认该功能“没有通过 r”。Android 11 开发者预览版 1 和所有后续的 DP 和 Beta 版本都有一个占位符按钮，用于拍摄滚动屏幕截图，可以通过隐藏的开发者命令手动显示[，但点击该按钮只会显示一条 toast 消息，说明该功能“尚未实现”](https://www.xda-developers.com/android-11-scrolling-screenshot-feature/)

 <picture>![Android 11 scrolling screenshot](img/79dc71f3cbf3ebfb8ccde11f1bbefecb.png)</picture> 

Android 11's unimplemented scrolling screenshot button.

我们希望这个特性能够进入测试版，甚至是稳定版，但是看起来这是不可能的。

可以理解，这个消息会让一些用户感到不安。毕竟，许多原始设备制造商已经在他们自己的软件中拥有这项功能多年了，那么谷歌为什么花了这么长时间才将其添加到 Pixel 手机中？正如谷歌系统 UI 团队的丹·桑德勒(Dan Sandler)所解释的那样，问题在于谷歌想把事情做对。一些滚动屏幕截图实现只是简单地模拟一个滚动，然后随着屏幕的移动将多个屏幕截图拼接在一起。如果你曾经在 Android 上处理过 UI 自动化，你会知道这并不总是有效的，因为正如桑德勒先生提到的，应用程序可以使用“一个 bog 标准的 RecyclerView 或实现他们自己的 OpenGL 加速滚动引擎。”由于谷歌计划不仅为 Pixel 智能手机，而且为作为 AOSP 一部分的整个 Android 生态系统实现这一功能，他们需要确保它能在所有应用上运行，而不仅仅是“特定设备上的一两个精选应用”

因为团队必须“集中[他们的]有限资源”，特别是由于新冠肺炎带来的挑战，团队决定在未来的 Android 版本中暂时搁置滚动截图。

## 新 CDD 要求告知用户背景限制

众所周知，许多 Android OEMs 厂商，尤其是中国的 OEM 厂商，对后台运行的应用程序有着严格的限制。一些开发者对他们的应用程序在后台被扼杀感到非常沮丧，他们联合起来创建了一个名为“[不要扼杀我的应用程序](https://www.xda-developers.com/phone-software-killing-apps-background/)”的网站，根据原始设备制造商处理后台应用程序的糟糕程度对他们进行排名。这些开发者[最近甚至做了一个基准](https://www.xda-developers.com/dontkillmyapp-benchmark-test-background-app-killing/)，这样用户就可以测试他们的设备在后台杀死应用程序的力度。很多 OEM 厂商爱杀后台 app 进程的原因很复杂，但我觉得最好用 Redditor/u/[possibly questioned](https://www.reddit.com/r/Android/comments/hnsduz/phone_makers_are_breaking_your_favorite_apps_with/fxe2838/)的这个评论来解释。该评论概述了 Android 应用程序开发在中国的复杂状况，中国科技公司如何参与进一步复杂化的事情，以及缺乏谷歌服务如何加剧了目前的混乱。

无论如何，许多应用程序开发人员对 Android 平台行为的这些调整感到沮丧，这是可以理解的，这导致开发人员将一条评论[推至 Reddit AMA 的顶部，询问谷歌他们正在做什么](https://www.reddit.com/r/androiddev/comments/hk3hrq/were_on_the_android_engineering_team_ask_us/fwqqjnx/)。以下是谷歌的回应:

从这个回答中我们可以学到一些东西。首先，谷歌希望原始设备制造商在他们应用的后台应用限制方面对用户更加透明。我查看了(未发布的)Android 11 兼容性定义文档(CDD ),发现第 3.5 节“API 行为兼容性”中增加了以下内容:

> #### 如果设备实现实施专有机制来限制应用，并且该机制比 AOSP 上的“稀有”待机桶更具限制性，则它们:
> 
> #### [C-1-5]必须告知用户应用程序限制是否自动应用于某个应用程序。(新)不得在实施此类限制前 24 小时之前提供此类信息。
> 
> #### (注)强制停止被认为比“罕见”更加严格，必须符合 3.5.1 中的所有要求，包括新的 3.5.1/C-1-5

基本上，谷歌并没有阻止原始设备制造商实现他们自己的限制性应用程序扼杀功能。他们只要求原始设备制造商告知用户他们的应用程序限制是否被自动应用。OEM 可以显示一个对话框，告诉用户他们将停止消耗电池的后台应用程序在后台运行，用户可能会同意，但没有意识到他们真正想在后台运行的应用程序也受到了影响！谷歌让开发者承担责任，处理他们的应用程序在后台被意外终止的情况。事实上，Reddit 的评论继续强调了新的“[应用程序进程退出原因](https://developer.android.com/preview/features#app-process-exit-reasons)”API，它可以告诉开发者他们的应用程序是被用户、操作系统杀死的，还是只是崩溃了。

另一方面，谷歌终于解决了原始设备制造商允许某些特权应用程序绕过其后台应用程序限制的不公平做法。开发者 Timothy Asiimwe 的这篇中型文章详细介绍了 WhatsApp、脸书等应用程序，其他应用程序自动免除了一些 OEM 软件的苛刻背景限制。谷歌表示，他们“要求设备制造商不要为热门应用创建允许列表。”我们不知道这将如何实施，但很高兴知道原始设备制造商最终将被迫平等对待第三方开发者——无论他们的应用程序有多大或多小。

最后，谷歌还提到了 Android 11 如何“增加了额外的措施来防止行为不端的应用程序的滥用行为”，从而降低了 OEM 厂商积极杀死后台进程的吸引力。然而，该公司没有详细说明这些“额外措施”意味着什么。

## 改进的设备到设备备份

上个月，我们发现了 Android 11 文档的一个变化，即[暗示支持更好的本地数据备份](https://www.xda-developers.com/android-11-force-app-local-backup-restore-handicap-cloud-backup/)。在 Android 11 中，当用户启动应用程序文件的“设备到设备”迁移时，系统将忽略任何以 API 级别 30 为目标的应用程序的 allowBackup 清单属性。谷歌的埃利奥特·斯托克表示，这项功能旨在让“手机制造商更容易构建设备到设备的迁移工具”，如“三星优秀的智能开关产品”，以帮助“从用户的角度来看，确保应用程序更可靠地在设备之间转移。”遗憾的是，这并不适用于基于云的备份，因为谷歌希望“让软件开发者能够控制他们的应用数据会发生什么。”因此，Android 11 仍将尊重任何基于云的备份和恢复的 allowBackup 属性，例如通过 Google Play 服务内置的 Google Drive 备份。最后，谷歌承认每个应用程序 25MB 的备份上限对一些开发者来说可能不够，所以他们正在寻找解决这个问题的方法。不过，本地备份到个人电脑并不在考虑之列，谷歌重申了他们的计划，即在未来的 Android 版本中，[将逐步淘汰 adb 备份。](https://www.xda-developers.com/adb-backup-and-restore-depreciated/)

鼓励开发人员实现无摩擦的数据迁移方法。[新的 Block Store 库](https://www.xda-developers.com/google-new-block-store-library-easier-sign-in-apps-new-devices-migration/)是谷歌身份服务库的一部分，旨在使新设备上登录从云恢复的应用程序变得更容易，但这取决于开发人员是否想要实现这个库。

## 借助 I/O 预读流程(IORap)加快应用启动速度

谷歌一直在尝试提高 Android 性能的方法。他们在 Android 10 中添加的一个鲜为人知的功能叫做非专业化应用进程池(USAP)。该功能消除了应用启动过程中的分叉 Zygote，在 Pixel 2 设备上节省了大约 5 毫秒的平均应用启动速度。该功能目前在 AOSP 被默认禁用，谷歌解释说其增加的内存使用仍需测试。然而，更有趣的是，Android 11 将有一个新功能，称为 I/O 预读进程( [IORap](https://android-review.googlesource.com/q/%2522iorap%2522) )。[根据谷歌](https://www.reddit.com/r/androiddev/comments/hk3hrq/were_on_the_android_engineering_team_ask_us/fxgccq2/)的说法，这一功能将导致“冷创业公司的速度提高 5%以上，英雄案例的速度提高 20%。”这个特性“将在启动过程中预取应用程序工件(如代码和资源)”，以提高应用程序的启动速度。

谷歌还“对用于优化引导类路径和系统映像的配置文件进行了改进”，这将提高应用程序的性能，并降低与系统工件相关的内存和存储成本。这些变化将主要有利于内存容量更高的设备，尽管谷歌没有说我们将在哪里看到最大的好处。

## Android 11 的作用域存储发生变化——为什么访问/下载受到限制？

针对 Android 11 并使用 ACTION_OPEN_DOCUMENT_TREE 意图请求访问外部存储上特定目录的应用程序将不再能够要求用户访问外部存储的根目录(/data/media/{user})、下载目录(/data/media{user}/Download)或外部存储(/Android/data 或/Android/obb)上任何应用程序特定的数据目录。为什么对下载目录的访问受到限制？根据谷歌 Roxanna Aliabadi 的说法，这是因为下载文件夹“最有可能包含私人信息”例如，下载纳税申报表或银行对账单的用户不必担心应用程序滥用他们对目录的连续读取权限的可能性。谷歌说文档选择器将会有“更新的文本”...以表明 Android 限制了某些文件夹的选择。”这将有望减少困惑，为什么他们不能授予应用程序访问某些目录了。

有关即将到来的范围存储和播放策略更改的更多信息，[请参考本文](https://www.xda-developers.com/google-play-july-2020-policy-update-introduces-extended-timeline-compliance-detailed-violation-emails-other-changes-developer-console/)。

## 杂项主题

*   **谷歌对生根/改造的立场**
    *   谷歌 AOSP 团队的杰夫·贝利重申了公司支持选择的立场。谷歌将“继续确保设备像素线的修改/根化是可能的”，但也将“支持原始设备制造商不允许他们的设备被根化的选择。”此外，谷歌给软件开发者提供了“不允许他们的软件在根设备上运行”的选择，参考安全网证明 API 的[软件篡改检测的最新变化。](https://www.xda-developers.com/safetynet-hardware-attestation-hide-root-magisk/)
*   **“打开并设置为默认”是怎么回事？**
*   **使用 Vulkan Graphics API 渲染 UI？**
*   **许多设备上缺少 CallScreeningService**
    *   Android 应用程序可以实现 [CallScreeningService API](https://developer.android.com/reference/android/telecom/CallScreeningService) 来拦截新的呼入和呼出电话，允许它们识别呼叫者并接受或拒绝呼叫。据开发者/u/ [_zeromod_](https://www.reddit.com/r/androiddev/comments/hk3hrq/were_on_the_android_engineering_team_ask_us/fwrj2ug/) 称，虽然这是一个官方记录的 API，但显然有许多 OEM 厂商没有正确实现它。谷歌[证实](https://www.reddit.com/r/androiddev/comments/hk3hrq/were_on_the_android_engineering_team_ask_us/fxgbz5k/)该 API 通过了兼容性测试套件(CTS)的验证，这是一个自动化测试套件，所有设备都必须通过才能被视为与 Android 兼容。不管出于什么原因，这个 API 在华为、Vivo、小米或三星等 OEM 厂商的设备上调用时会返回 null，所以很可能这些 OEM 厂商的软件中存在漏洞。
*   **没有音频插件框架计划**
    *   一名开发者问谷歌他们是否计划实现一个类似苹果 Audio Units 的音频插件框架，但是[的答案](https://www.reddit.com/r/androiddev/comments/hk3hrq/were_on_the_android_engineering_team_ask_us/fxgq5sx/?context=3)是这不太可能在不久的将来发生。

你可以在这里阅读 Android 工程团队的所有答案。团队在一些评论中谈到了 Java、Kotlin、Android 构建系统、CameraX API 和其他主题。也有一些关于 Wear OS、Android TV 和 Android Auto 的评论，但谷歌主要重申了他们在这些平台上的现有工作，并告诉开发者在 8 月 10 日开始的“ [Android Beyond Phones](https://developer.android.com/11weeksofandroid) ”周期间关注更多信息。