# Android Q AMA 总结:谷歌在 Reddit 上对 Android 10 的评价

> 原文：<https://www.xda-developers.com/android-q-ama-summary/>

去年，谷歌的 Android 团队在 Reddit 的/r/Android dev subredit 上举办了一个“问我任何问题”(AMA)，回答关于 Android P 开发者预览版的问题。今年，负责 Android Q 测试版的工程团队在 Reddit 上回答了问题。[AMA](https://www.xda-developers.com/android-q-engineering-team-reddit-ama/)于太平洋时间 8 月 1 日中午 12:00 开始，大约一个半小时后结束。33 名谷歌工程师参与了 AMA，在 AMA 持续的短暂时间内回答了大量问题。这是我们对所学新知识的总结。

## AMA:我们从谷歌学到的一切

### 来自 Android Q beta 团队的参与者

*   **亚当·科恩:**安卓启动器/系统用户界面上的 TLM
*   **Adam Powell:** TLM 论 UI 工具包/框架；视图、生命周期、片段、支持库
*   **Alan viverette****:**tlm，Jetpack / AndroidX
*   **Allen Huang:** 对 UI、启动器、通知、搜索集成等进行 PM！
*   **Andrew Sappirstein:**Android 上的 TLM 设置
*   Brahim Elbouchikhi:Android 机器学习和相机(NN API、ML 套件、CameraX、相机平台)项目经理
*   **Chad Brubaker** :软件工程师，Android 平台安全
*   李思欣·德席尔瓦:隐私保护
*   **切特·哈斯** **:** Android 首席倡导者，开发者关系
*   **Diana Wong:** PM，应用兼容性，非 SDK API 使用，艺术，NDK
*   **Dianne hack born****:**Android 框架团队经理(资源、窗口管理器、活动管理器、多用户、打印、可访问性等。)
*   **钟奕基:**UX 导演
*   **Ian Lake:** 软件工程师，Jetpack(片段、导航、架构组件)
*   **Iliyan Malchev:** 项目主线首席软件工程师
*   Jacob Lehrbaum:Android 开发者关系总监
*   杰克·沃顿:软件工程师，Jetpack
*   **贾马尔·伊森** **:** 下午，安卓工作室
*   杰夫·贝利(Jeff Bailey):TLM，安卓开源项目(AOSP)
*   Jeff Sharkey :软件工程师，Android 框架
*   杰弗里·梵高:安卓工作室，编译器
*   **Jen Chai:** PM、位置和上下文、验证、自动填充、非 SDK API 使用、艺术
*   **Karen Ng:**Android 开发工具、Android Studio、Android Tookit 和 Jetpack 的项目经理小组
*   **Paul bank head:**Google Play 产品管理总监
*   **Rohan Shah:**Android 系统 UI 产品经理
*   **罗曼盖伊****:**Android Toolkit/Jetpack 团队经理
*   **Sagar kam Dar:**Android 产品管理总监
*   **Sat K:**Android 连接工程总监
*   **Selim Cinek** :软件工程师，Android 系统 UI
*   **斯蒂芬妮·萨阿德·卡斯伯特森** **:** 安卓产品管理高级总监
*   Sumir Kataria: 软件工程师，Jetpack(工作经理)
*   **特拉维斯·麦考伊:**下午，安卓平台
*   **Trystan Upstill:** 杰出工程师，Android 系统 UI &智能负责人
*   **葡萄酒模式:**下午，Android 相机

### 当用户在最近刷走应用程序时，原始设备制造商不再能杀死它们

如果你曾经使用过中国品牌的智能手机，那么你可能会遇到恼人的“电池优化”功能，这些功能会在后台杀死所有你最喜欢的应用程序。这种行为不仅让那些出于任何原因希望某些应用程序继续在后台运行的用户感到恼火，也让那些不得不忍受用户差评的开发者感到恼火，因为他们不明白这不是应用程序的错。虽然谷歌*仍然*没有完全解决这个问题(他们声称这种行为可能已经违反了 Android 兼容性定义文件的要求)，但该公司[正在采取行动](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evq703f/)反对一些原始设备制造商采用的一种“节省电池”行为改变。

> #### “为了帮助解决这种情况，我们在 Android Q 中添加了一个 CTS 测试，以确保应用程序在从最近的应用程序中删除时不会被杀死。”

### Android R 可能会给截图带来比我们预期更多的变化

谷歌计划在 Android R 中添加[滚动屏幕截图，但与此同时，](https://www.xda-developers.com/adding-scrolling-screenshot-support-android-infeasible/) [Android 团队正在](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evq9y8h/)“密切关注【他们】如何改善 R 的整个屏幕-[X]体验。”因此，我们可能会在下一个主要 Android 版本中看到屏幕截图(和截屏)行为的其他改进。

### 澄清 Android Q 的新桌面模式

Android Q 的第一个公开测试版为 AOSP 和 Pixel 启动器带来了一个隐藏的桌面模式界面。尽管谷歌[在一次谷歌 I/O 会议上简要提到了功能](https://www.xda-developers.com/google-more-information-desktop-mode-android-q/)，但我们从未直接从谷歌那里听说新功能如何融入 Android 生态系统。谷歌[现在澄清](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evqa3xs/):

> #### “在 Q AOSP‘桌面模式’是一个面向应用程序开发人员的开发人员选项。它允许他们在多显示器和自由窗口模式环境中测试他们的应用程序。以前，没有方便的方法来测试应用程序在辅助显示器上的行为，以及在普通 Android 上自由调整窗口的大小。这个特性本身并没有产品化，目前也不适合普通用户。尽管如此，对于原始设备制造商来说，创新和做出伟大的产品是 Android 平台的基线。”

因此，我们可以期待看到原始设备制造商建立在 Android Q 的原生桌面模式上。例如，[一加 7 Pro 支持通过 HDMI](https://www.xda-developers.com/oneplus-7-pro-usb-pd-hdmi-variable-refresh-rate/) 显示输出，因此基于 Android Q 的 [OxygenOS 10 未来有可能拥有自己的桌面模式界面。我们也希望谷歌为即将到来的](https://www.xda-developers.com/oxygenos-10-android-q/) [Pixel 4](https://www.xda-developers.com/google-pixel-4-leaks-rumors/) 开发该功能。

### 基于时间的黑暗模式

Android Q 终于带来了一个被广泛要求的功能:[全系统黑暗模式](https://www.xda-developers.com/android-q-dark-mode-overview/)。目前，黑暗模式既可以在设置中手动启用，也可以通过快速设置磁贴启用，或者它可以在启用节电模式时自动激活。在 Android Q 之前，有一个基于时间启用黑暗模式[的选项，但该选项已被否决。根据克里斯·贝恩斯的说法:](https://www.xda-developers.com/android-q-toggle-dark-theme/)

> #### 在 AppCompat v1.1.0 中不推荐(而不是删除)此功能有几个原因:它要求应用程序请求位置权限才能准确，即使位置有效，日出/日落时间的计算也可能会出错

当被问及这些 bug 时，Banes 先生说“计算日出/日落是出了名的困难，尤其是在靠近南北极的地方。”用户提出，自 Android 7.1 牛轧糖以来，夜灯可以根据日落/日出时间表自动切换。Banes 先生接着说，由于 Night Light 使用了来自 ICU4J 的 CalendarAstronomer，它使用了“一大块我们不希望 AppCompat 依赖的代码。”然而，团队[声明](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evqamdp/)这个特性是“他们将会研究的东西”

### Android Q 发布设备强制支持 Camera2 API/Camera HAL3

谷歌推出了 Camera2 API，以更好地定义应用程序如何与连接到智能手机的各个相机进行交互。虽然谷歌[鼓励](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evq9pz2/)智能手机供应商“向开发者公开他们所有的物理摄像头”，但许多供应商选择不这样做，尽管“API 本身目前并不阻止他们。”这意味着许多第三方相机应用程序无法使用现代智能手机上的二级或三级相机模块。然而，随着 Android Q 改进了 [LOGICAL_MULTI_CAMERA](https://developer.android.com/reference/android/hardware/camera2/CameraMetadata.html#REQUEST_AVAILABLE_CAPABILITIES_LOGICAL_MULTI_CAMERA) ，这是一个 API，它让开发人员可以更好地访问设备上的所有相机，并让 OEM 厂商可以控制功耗和管理多个相机状态。

此外，谷歌表示，他们已经为所有使用 Android Q 的设备添加了原生支持 Camera2 API/Camera HAL3 的要求。[根据 Vinit Modi](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evqdw9j/) :

> #### “从 Android P 开始，配备 1GB 或更多 RAM 的新设备需要原生使用 HALv3/camera2。从 Android Q 开始，所有新设备都需要原生支持 HALv3/camera2。不幸的是，从 HALv1 到 HALv3 的无线升级相当复杂，可能会产生意想不到的后果，因此我们不得不将范围限制在新设备上。”

有趣的是，莫迪关于普通 RAM Android P 发布设备的声明[与谷歌早些时候告诉我们的](https://www.xda-developers.com/android-pie-camera-hal3/)以及在线图像测试套件页面上发布的内容相矛盾。

### 使用 Jetpack 编写动态应用程序主题

索尼的 OMS 主题框架在几个版本之前就被添加到了 AOSP，但是它仅仅是为原始设备制造商准备的。我们已经知道[谷歌反对](https://www.xda-developers.com/rootless-custom-themes-android-p/)用户使用运行时资源覆盖来应用主题，但是对于开发者来说，该公司[希望](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evq7vm9/)它的 [Jetpack Compose UI](https://www.xda-developers.com/android-jetpack-camerax-biometrics/) 框架将带来“有趣的动态主题化方法”

### vulkan-Skia 呈现 UI 的后端

去年，[我们在谷歌工程师中发现了一场讨论](https://www.xda-developers.com/google-android-q-vulkan-graphics-render-ui/),讨论他们计划让 Android 框架使用 Vulkan graphics API 进行 UI 渲染。虽然现在有可能启用 Vulkan 硬件加速后端而不会让你的手机崩溃，但我们还没有听到谷歌关于他们计划何时推出这些变化的任何具体计划。这个 AMA 没有回答这个问题，但至少我们确认它仍在工作中。[据罗曼·盖伊](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evqbg5o/):

> #### “该团队一直在为 Skia 开发 Vulkan 后端，这是 Android 使用的 2D 渲染器，但目前默认情况下没有启用。UI 和画布仍然通过 OpenGL ES。”

### 让 Android Q 的手势栏更加动态

XDA 的一些人仍然认为安卓的新手势一团糟，但我个人认为它们很好。不过，如果你尝试一下 Android Q 中的新手势，你会发现手势栏不会随着你的手指移动。它还会停留在不需要它的屏幕上，比如主屏幕或最近的应用概述。艾伦·黄[说](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/ev23jzc/)他们“完全同意有机会”让“航线不那么静态”他进一步说“这是我们正在努力的——但是也要保持平衡，这样它就不会令人分心地出现/消失。”

### 存储访问框架的改进

Android Q 的许多变化极大地提高了平台的安全性和隐私性。其中一个被称为“作用域存储”的变化，以一种合理的方式限制了应用程序对外部存储上的文件的访问；例如，音乐应用不需要查看你的图库。运行在 Android Q 上的文件管理应用程序必须使用一个叫做存储访问框架的 API 来继续正常工作，但是[一些开发者认为这个 API 不如以前可用的 API](https://www.xda-developers.com/android-q-storage-access-framework-scoped-storage/)。来自谷歌[的 Jeff Sharkey 说](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evq8qxb/)团队已经解决了一些开发者的抱怨:

> #### “我们在最新的 Android Q 测试版中进行了一些 SAF 性能改进；你能根据最新的测试版检查你的基准吗？还应确保在运行任何批量操作时使用 ContentProviderClient。

### 与 Android Oreo 相比，Project Treble 提高了 Android Pie 的采用率

我们已经看到了 Project Treble，一个主要的 Android 框架的底层重构，是如何改进新的 Android 操作系统版本的采用的。谷歌归功于去年加入 [Android P beta](https://www.xda-developers.com/android-p-beta-program-is-now-available/) 和今年加入 [Android Q beta](https://www.xda-developers.com/android-q-beta-3-released/) 的智能手机厂商的三倍。首席项目 Treble 和[主线](https://www.xda-developers.com/android-q-project-mainline-security/)工程师[Ili Yan mal chev](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evqeobj/)表示，2018 年底，Android Pie 的采用率是 Android Oreo 的“3 倍”。

在同一篇评论中，Dick Dougherty 调侃道，Android 版本分布图中有更多有用的指标。这张图表最近一次更新是在 5 月份，但是它的数据对记者来说比应用开发者更有用。

### 屏幕录制仍然是 WIP

早期的 Android Q betas 版为基本的屏幕录制器添加了一个功能标志，但该平台本身已经通过允许应用程序从其他应用程序捕获音频而大大改善了屏幕录制的实用性。斯蒂芬妮·萨阿德·卡斯伯特森说，团队正在考虑“我们如何才能在屏幕录制需求方面做得更好。”其他智能手机品牌如[【一加】](https://www.xda-developers.com/download-oneplus-screen-recorder-android-q/)、华硕、华为和三星都有强大的屏幕记录器，可以记录内部音频，因此谷歌将在这方面迎头赶上。

### 黑暗主题所有的事情！

如果你错过了，谷歌正在给他们的大多数应用程序添加黑暗模式。斯蒂芬妮·萨阿德·卡斯伯特森(Stephanie Saad Cuthbertson [表示](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evqdjj3/)预计所有“主要应用程序”都将支持“官方(Android Q)发布”的黑暗主题即使是谷歌 Chrome，目前在启用全系统黑暗主题时强制页面重新加载，也将更新为主题改变时不再刷新。

### 是的，第三方启动器将(最终)支持手势

当你使用第三方启动器时，Android 的手势有点儿[失灵。这是因为最近的应用程序 UI 包含在股票启动器应用程序中，谷歌还没有找到一种方法来实现我们在股票像素启动器中使用手势时看到的无缝过渡。亚当·科恩](https://www.xda-developers.com/android-q-beta-5-third-party-launcher-gesture-navigation/)[证实](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evqy129/?context=3)谷歌计划“在发布后尽快”解决这些问题他进一步表示，这种不兼容性“将在 Q 更新后得到解决，并在 Q 发布的新设备中进行反向移植。”

### 动态/逻辑分区不是用来杀死定制的 rom 的

为了支持 Android Q 中的动态系统更新，谷歌 Pixel 3 和 Pixel 3 XL 等设备使用了逻辑分区。这些分区可以动态调整大小。这一变化已经证明[在获得根访问工作](https://www.xda-developers.com/magisk-google-pixel-3-pixel-3a-android-q/)方面具有挑战性，一些开发者担心定制 rom 成为目标。Iliyan Malchev 向我们保证，其目的并不是要限制定制的 rom。作为[，他解释道](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evtzmle/):

> #### “动态分区并不意味着限制你可以用定制的 rom 做什么。它们只是解决固定分区大小和缺乏在 OTA 上重新分区设备的安全方法的问题。在动态分区出现之前，如果 OEM 在调整系统分区等方面出现错误，那么他们将受到该选择的限制，使得在某个时间点之后几乎不可能升级设备。一些原始设备制造商在实践中确实在 OTA 上对他们的设备进行了重新分区，但这是 a)在 Android 中不被官方支持，以及 b)改变分区表被认为是相当冒险的。动态分区旨在通过在物理分区表和操作系统之间引入一个间接层来缓解这个问题。这反过来允许我们在 OTA 上安全地调整分区大小。至于定制的 rom，你不应该像今天这样被你所能做的所束缚。支持定制 rom 是并将继续是每个 OEM 决定启用的功能。”

### 项目主线-艺术模块和支架长度

Mainline 是 Google 的一项新举措，旨在标准化某些库和包，以便它们可以独立于平台更新而更新。有些人想知道为什么 Android 运行时(ART)还不是一个主线模块，但我在 Google I/O 上被告知，模块化 ART 所涉及的复杂性阻止了他们将其作为初始 APEX 包之一。正如 Iliyan Malchev 和 Diana Wong 解释的那样:

> #### “对运行时进行更新(尤其是性能& GC 修复和核心库)绝对是我们在主线环境中探索的事情。我们可以看到很多好处，能够使这些更新在所有设备和主线的多个版本之间保持一致。这也是一个巨大的技术挑战，因为我们认为如何为开发者做得最好，可能需要多年的努力。这不是 Mainline 目前能做的事情，但肯定是我们正在考虑的事情。”

如果你追随 AOSP 的精神，你会发现谷歌一直在努力打造运行时顶点。目前，他们似乎正在[将 Bionic 和 ART/libcore](https://android-review.googlesource.com/c/platform/art/+/1012047) 拆分成独立的 APEX 模块。

关于项目主线的好处，一位用户询问主线更新的长度。作为回应，Iliyan Malchev [说](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evtzmle/)“这是一个政策问题，我们仍在评估，但我们希望尽可能长时间地更新设备上的主线模块。”XDA 知名开发人员 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 询问是否会提供预建主线模块，以便定制 ROM 开发人员可以合并更新，对此，杰夫·贝利[重申](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evtyrvi/)“从 AOSP 分离出来的模块将拥有与每个模块版本相匹配的源代码版本。”我们已经可以在 AOSP 看到新的 APEX 模块的进展，例如用于[神经网络 API](https://android-review.googlesource.com/c/platform/system/core/+/1014637) 的模块。

### 相机符合 ml 套件

在今年的 I/O 大会上，谷歌推出了 [CameraX Jetpack 库](https://www.xda-developers.com/android-jetpack-camerax-biometrics/)。这个库旨在使开发人员更容易支持 Android 的 Camera2 API，同时保持与 Android Lollipop 的兼容性。Vinit Modi [调侃道](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evtyjrr/)该公司正致力于将 CameraX 与 [ML Kit](https://www.xda-developers.com/google-ml-kit-machine-learning/) ，谷歌的机器学习 Firebase SDK 整合，这样开发者就可以将图像帧输入 ML Kit 进行分析。

### CameraX 供应商扩展和发布日期

一个相机应用程序的开发者感叹道，第三方相机应用程序无法使用谷歌像素的夜视等先进的相机功能。这应该可以通过 CameraX 供应商扩展来解决，对此 Google 的 Jeff Sharkey】说“所有的像素设备都针对 CameraX 内核进行了优化。”他开玩笑说，“扩展方面将在新的和即将到来的设备上得到支持。”此外，谷歌正在“与几家制造商合作，以便能够将他们的设备功能带给开发者和用户。”虽然没有得到直接证实，但我们可能会看到像[谷歌像素 4](https://www.xda-developers.com/google-pixel-4-leaks-rumors/) 上的[夜视](https://www.xda-developers.com/google-pixel-night-sight-google-camera-review/)这样的功能可以用于使用 CameraX 库的第三方相机应用程序。

夏基先生表示，谷歌的目标是在今年年底推出测试版。

### Android Q 中的内存管理改进

Pixel 3 因发布后出现[众多问题而遭到痛斥，但谷歌通过众多](https://www.xda-developers.com/google-pixel-3-pixel-3-xl-issues-problems-help-list/)[发布后更新](https://www.xda-developers.com/google-pixel-performance-digital-wellbeing/)做了大量工作来解决这些问题。内存管理一直是 Pixel 3 最薄弱的方面之一，但在 Android Q 版本中情况应该会有所改善。根据 Selim Cinek 的说法:

> #### “例如，在 SystemUI 中，我们在 Q 中进行了各种大的重构工作，以减少通知和其他表面的 RAM 使用量。”

### 我们最终会得到无线 ADB 吗？

如果你想无线调试你的手机，你必须根你的设备。Android 工作室团队的 Jamal Eason】说他们目前正在解决这个功能的可行性。

### 谷歌还在平板电脑上测试吗？

XDA 知名开发者 Luk1337 询问谷歌是否仍在平板电脑上测试 AOSP·UX。考虑到[缺乏好的安卓平板电脑](https://www.xda-developers.com/samsung-galaxy-tab-s6-spen-announced/)和当前版本中存在的[漏洞](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evu1o49/)，这是一个合理的问题。Allen Huang [说](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/evtzbj5/)谷歌仍然“每年测试和修复”，该公司正与合作伙伴密切合作，“以确保良好的 Android 平板电脑体验。”

* * *

Reddit 上有很多完整的帖子。我在这里介绍的内容总结了我们了解到的所有新信息，但是一些谷歌员工(尤其是 Dianne Hackborn)对削减 X 特性或不实现 Y 权限进行了深入的分析。如果你想更好地理解 Android 团队的决策，我建议你阅读 AMA 的全文。

[**/r/Android dev**上阅读完整 AMA](https://www.reddit.com/r/androiddev/comments/ci4tdq/were_on_the_engineering_team_for_android_q_ask_us/?sort=qa)