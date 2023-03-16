# 高通骁龙 845 源现已在 CAF 上提供

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-845-sources-caf/>

高通最新的高端片上系统——高通骁龙 845，于去年年底在骁龙科技峰会上发布。凭借一个 [Adreno 630 GPU](https://www.xda-developers.com/qualcomm-snapdragon-845-adreno-630-gpu/) ，4 个效率核心和 4 个性能核心，它是一个性能怪兽，是迄今为止为 Android 手机提供的最佳产品。今年几乎所有的主要旗舰产品，如小米 Mix 2S，三星 Galaxy S9，LG G7 ThinQ 和 OnePlus 6 都采用了它，这对用户来说太好了。传统上，高通在 Code Aurora Forums (CAF)上发布了许多特定于平台的代码，帮助开发人员开始构建基于 AOSP 的定制 rom。然而，该公司推迟发布骁龙 845 的来源。当我们就此事联系高通时，我们被告知[他们将在 6 周后](https://www.xda-developers.com/qualcomm-snapdragon-845-kernel-source-code/)被释放。6 周的窗口已经过去，高通骁龙 845 平台的源代码现在可以在 CAF 上获得。

简单地说，CAF 的存在是采用高通芯片的 Android 智能手机如此受 XDA 开发社区欢迎的原因之一。虽然 GPLv2 许可证要求供应商发布他们的内核源代码，但这并不总是足以创建基于 AOSP 的定制 rom。SoC 厂商不需要发布特定于芯片组的代码，但高通经常为 Hal、框架分支等提供其芯片组特定代码的公共部分，这对开发人员来说是一大优势。开发人员无需了解新的芯片组功能如何工作，就可以构建该平台。如果无法访问这些代码，为设备构建基于 AOSP 的定制 ROM 就会变得困难得多。

这正是问题所在，因为骁龙 845 的原始资料花了几个月才发布。这比通常需要的时间长得多，这导致一些开发人员担心高通正在变得像其他 SoC 供应商一样，如联发科和海思。幸运的是，该公司现在已经发布了代码，开发者可以开始为他们的设备构建代码了。

[**高通骁龙 845 来源于代码极光论坛**](https://source.codeaurora.org/quic/la/platform/manifest/commit/?h=LA.UM.6.3.r4-04300-sdm845.0)

但是我们为什么要等这么久呢？嗯，以前的代码下降经常破坏即将到来的芯片组发布。这是一个公平的借口，鉴于高通骁龙 710 被泄露[提前](https://www.xda-developers.com/qualcomm-snapdragon-670-kernel-source/)感谢 CAF 来源。既然[高通骁龙 632、439 和 429 平台](https://www.xda-developers.com/qualcomm-snapdragon-632-439-429-mobile-platforms/)已经过时，骁龙 845 来源也适当删除了任何提及未发布芯片组的内容，该公司可以放心地公开发布了。