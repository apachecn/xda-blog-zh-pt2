# 零起点开源项目(GZOSP):一个用于定制 ROM 开发的 Android Oreo 基础

> 原文：<https://www.xda-developers.com/ground-zero-open-source-project-gzosp-android-oreo/>

Ground Zero roms，ROM 开发团队为我们带来了流行的定制 ROMs Tesla、Tipsy 和 Validus，提供了一个中央 Android Oreo 存储库，无需从头开始(意味着直接从 AOSP)就可以构建定制 ROM。地面零开源项目(GZOSP)的想法是给定制 ROM 构建者一个更好的起点，既有必要的 AOSP 代码，又有 CAF (Code Aurora Forum，高通自己的存储库，对带有骁龙 SOC 的非 Nexus 设备很有用)代码来构建各种设备。

它不应该与流行的 rom[Tesla、Tipsy 和 Validus](https://forum.xda-developers.com/ground-zero-roms/ground-zero-roms-feature-development) 混淆，因为**它不包含任何使这些 rom 独特的特征**。因此，当你从这个库中构建时，团队要求你**不要**将你的 rom 标记为非官方的 Tesla、Tipsy 或 Validus 版本，直到他们发布第一个面向公众的官方版本。

该存储库包括以下内容:

*   所有定制 rom 的基本功能(如高级重启菜单、夜间模式和快速设置亮度滑块控制)
*   谷歌直到下个月的安全补丁或者下一次 Android 维护更新才会推出的错误修复
*   谷歌默认停用的 AOSP 功能，如系统用户界面调谐器
*   在这里或者在知识库的主页[这里](https://github.com/GZOSP)列出了其他 Android 奥利奥特有的添加内容

如前所述，GZOSP 并没有*而不是*包括我们从广受欢迎的 Zero ROMs Tesla、Tipsy 和 Validus 中期待的定制功能集。例如，你不会看到任何内置的黑暗系统主题，狼窝自定义设置部分，或 Validus 壁纸。原因很简单:该团队的目标是**为任何和所有开发者提供一个构建他们自己的定制 ROM**的基础，而不局限于该项目最著名的三个零基础 ROM 品牌。

如果你直接从 GZOSP 库构建，你会得到一个标准的 Android 8.0 Oreo 构建，增加了前面列出的内容，但是没有任何现有定制 rom 的特性。这是从 LineageOS 15.0 作为基础或者从 Slim 或 Paranoid Android 构建的替代方案，在这些 Android 中，默认情况下包含了它们所有的自定义功能。与此同时，你有任何你需要的 CAF 代码来运行这里列出的非 Nexus 设备(更多将及时添加)，你不会被谷歌在 AOSP 合并所限制。

当然，也有其他尝试来建立一个为定制 rom 开发设计的中央存储库，但在 GZOSP 的情况下，团队向我们保证他们会保持更新，因为这是他们创建 Validus 存储库的起点(在进一步通知之前，Validus 将是唯一为 Android Oreo 开发的零基础 ROM)。如果你对 GZOSP 有任何进一步的疑问，你可以在团队的 [Google+社区](https://plus.google.com/communities/109330559573276360638/stream/c5536b6b-7875-4e93-ae0f-8c0e19ea7d72)或 [XDA 论坛](https://forum.xda-developers.com/ground-zero-roms/ground-zero-roms-feature-development/gzosp-aio-thread-t3679343)上发表。

*感谢 GZOSP 团队就他们的新项目向我们伸出援手。如果你是一名开发者，并且想分享你或其他成员正在做的一个有趣的项目，请通过我们的联系方式联系我们[。](https://www.xda-developers.com/suggest-content/)*