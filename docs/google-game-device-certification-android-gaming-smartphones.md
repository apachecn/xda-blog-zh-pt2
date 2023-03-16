# 独家报道:谷歌开始对游戏手机进行游戏设备认证

> 原文：<https://www.xda-developers.com/google-game-device-certification-android-gaming-smartphones/>

随着最近像《使命召唤手机版》这样的手机游戏的成功，很容易理解为什么 AAA 游戏发行商、[谷歌/苹果](https://www.xda-developers.com/google-play-pass-monthly-subscription-store-apps-games/)和智能手机原始设备制造商如此努力地推动手机游戏。在智能手机领域，我们已经看到像[华硕](https://www.xda-developers.com/asus-rog-phone-ii-specs-features-pricing-availability/)、[黑鲨](https://www.xda-developers.com/black-shark-2-pro-snapdragon-855-plus-12gb-ram-china/)、[雷蛇](https://forum.xda-developers.com/razer-phone-2)、[努比亚](https://www.xda-developers.com/nubia-red-magic-3-review/)等品牌推出以游戏为中心的旗舰产品。在芯片组厂商[高通](https://www.xda-developers.com/qualcomm-snapdragon-665-snapdragon-730g/)和[联发科](https://www.xda-developers.com/mediatek-helio-g90-series-hyperengine-game-technology-launched/)的支持下，随着游戏智能手机转向中端市场，竞争只会更加激烈。为了确保未来的游戏智能手机足够强大，并且对 Android 游戏开发者来说行为足够可预测，谷歌正在制定一项游戏设备认证计划。

我们第一次从一个可靠的来源得知谷歌的意图是在 7 月，但当时我们没有任何具体的细节或证据可以分享。现在，3 个月后，我们获得了 Google 对 OEM/ODM 的 GMS 要求的最新版本。本文档列举了智能手机 OEM/ODM 必须满足的技术要求，以便根据谷歌与 OEM/ODM 之间的商业协议，被允许预装 GMS 或谷歌移动服务。该文档类似于 Android 兼容性定义文档( [CDD](https://source.android.com/compatibility/cdd) )，但是尽管该文档在线发布，但该文档并未公开。

我们获得了该文件 7.0 版本的副本，最后一次更新是在 9 月 3 日，也就是谷歌向公众发布 Android 10 的同一天。该文件的第 13 节详细说明了设备必须满足的附加 Android“平台要求”，以便获得使用 GMS 的批准。第 13.14 小节涵盖了新的“游戏设备认证”技术要求。如果 OEM/ODM 想要声明设备已经获得游戏设备认证，则必须满足这些要求。

总之，这些要求确保认证游戏设备的行为可预测，“因此游戏开发人员不会面临意外的节流、CPU 内核丢失或其他奇怪的系统行为。”该文档详细解释了 OEM/ODM 如何构建具有可预测行为的游戏设备。对于高性能和可预测的 GPU 行为，谷歌表示，认证设备必须“提供现代、最新的高性能 GPU 和显示 API，并实现合理的帧内省。”具体来说，认证的游戏设备必须支持 Vulkan Graphics API 的[1.1 版本，通过](https://www.xda-developers.com/khronos-group-vulkan-1-1-specs/) [Khronos](https://www.khronos.org/conformance/adopters) 提供的最新 OpenGL ES/Vulkan 图形一致性测试，并满足与[编舞](https://developer.android.com/reference/android/view/Choreographer)和 [SurfaceFlinger](https://source.android.com/devices/graphics/surfaceflinger-windowmanager) 相关的其他要求。最后，为了合理的内存行为，谷歌希望 OEM/ODM 确保游戏设备允许应用程序在被系统杀死之前分配至少 2.3GB 的内存。

由于我们没有 GMS 需求文档的旧版本，我们不能 100%确定游戏设备认证计划实际上有多新。然而，我们在 LinkedIn 上发现了一份工作申请，要求招聘一名“Android 游戏设备认证”的开发者关系项目经理。由于列表已经关闭，我们看不到它是什么时候发布的，尽管 6 月 28 日发布了另一个求职网站对[页面的重新整合。我们不知道这个重新托管的页面是什么时候删除了原来的页面，但是，我们注意到](https://in.jobappmatch.org/developer-relations-program-manager--android-game-device-certification-a381389621)[彼得·卡德威尔](https://www.linkedin.com/in/peter-cardwell-8a36894/)，一位前微软员工，似乎在五月份已经接受了这份工作，所以这个程序肯定是新的。

工作清单证实了这一新项目的全貌。谷歌正在建立一个团队，与原始设备制造商和 SoC 制造商合作，就我上面列出的即将到来的要求对他们进行教育。如前所述，该团队的任务是创建测试套件和工作负载，以证明符合新计划。

谷歌尚未公开宣布这一新的游戏设备认证计划，目前市场上没有获得游戏认证的设备。谷歌表示，选择加入该计划的设备必须声明支持 com . Google . Android . feature . gamecert _ PREVIEW 功能标志。我在黑鲨 2 (Android 9 Pie)、华硕 ROG 手机 II (Android 9 Pie)、一加 7 Pro (Android 10)和谷歌 Pixel 2 XL (Android 10)上检查了这个功能标志，所有人都报告说它不存在。我怀疑谷歌不会对这个程序保密，他们会公布一个兼容设备的列表，比如 Android Enterprise 推荐的兼容设备，所以你不需要自己检查这个标志。

在这篇文章发表的前几天，我联系了谷歌，要求他们确认我们收到的文件的合法性。虽然我还没有收到回复，但我们已经从文件中证实了足够的细节，让我相当确定这是真的。这份文件大约有 57 页长，我们有更多的东西可以分享。