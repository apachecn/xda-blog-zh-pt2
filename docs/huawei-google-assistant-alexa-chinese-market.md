# 独家:这是华为针对中国市场对 Google Assistant 和 Alexa 的回答

> 原文：<https://www.xda-developers.com/huawei-google-assistant-alexa-chinese-market/>

虚拟助手的世界由两个名字主宰:亚马逊和谷歌。根据 [*Strategy Analytics* 的数据，2017 年第三季度，亚马逊 Echo 和谷歌 Home 设备以惊人的 92%的市场份额占据主导地位。](https://www.xda-developers.com/google-home-amazon-echo-smart-speaker-market-share/)这一领域的其他著名竞争对手包括拥有 [Bixby 助手](https://www.xda-developers.com/google-home-amazon-echo-smart-speaker-market-share/)的三星和拥有 Siri 的苹果，但与亚马逊和谷歌相比，它们的市场渗透率相形见绌。即使是像华为这样的电信巨头也很难在这一领域竞争，特别是华为，它已经放弃了专注于中国市场。

事实上，在去年的消费电子展上，华为技术公司消费者业务集团首席执行官 Richard Yu 告诉[*【The Verge】*](https://www.theverge.com/2017/2/16/14634290/huawei-china-voice-assistant)该公司没有在国际市场寻求虚拟助理的计划。

> #### “今天，亚马逊和谷歌比我们强大；Alexa 和谷歌助手更好。我们怎么竞争？”-华为消费者业务集团首席执行官理查德·于接受《The Verge》采访

在另一份报告中，不愿透露姓名的消息人士向彭博 透露，华为正在开发自己的智能手机语音助手——但只针对中国市场。该报告当时没有提供多少细节，但提到语音助手将被设计成与苹果的 Siri、谷歌助手和亚马逊 Alexa 竞争。

自本文发布以来，我们没有听到有关华为助手的进一步细节，但是， *XDA 开发者*已经从基于 Android 8.1 Oreo 的中国华为 Mate 10 EMUI 8.1 版本的固件文件中获得了华为 HiAssistant 和 HiAI 应用程序的访问权限。

*以下信息基于 [@FunkyHuawei](https://twitter.com/FunkyHuawei) 获得的固件文件，他是 [FunkyHuawei.club](https://funkyhuawei.club/) 服务的幕后人，该服务允许用户付费[更新](https://funkyhuawei.club/models)、[解锁](https://www.reddit.com/r/FunkyHuawei/comments/7d5wsi/introducing_funkyhuawei_unbrick_flash_tool/)或[更名](https://www.reddit.com/r/FunkyHuawei/comments/7a5sab/introducing_funkyhuawei_rebrand_tool_rebrand_any/)华为和 Honor 手机。他只向 XDA 开发者提供对这些固件文件的访问。*

* * *

## HiAssistant——华为对苹果 Siri、亚马逊 Alexa 和谷歌助手的回应

对于在中国地区销售的智能手机，华为预装了一款名为“HiVoice”的应用。该应用程序提供了对智能手机的非常基本的控制，例如询问它在哪里和打电话，所以它不像其他虚拟助手那样复杂。然而，这种情况正在发生变化，因为华为在海思麒麟 970 上的神经处理单元(NPU)的工作最终将获得回报。该公司长期以来一直在吹捧 SoC 的人工智能能力，但除了 EMUI 相机应用程序中的一些[基本场景识别](https://www.xda-developers.com/huawei-mate-10-makeup-object-recognition-camera/)，我们还没有看到他们的工作成果。

在华为 Mate 10 Pro 的最新中文版本中，由 [HiAI 移动计算平台](http://developer.huawei.com/consumer/en/resources/index.php?title=HiAI_Mobile_Computing_Platform_Overview)支持的华为 HiAssistant 应用程序向我们暗示了即将到来的虚拟助手的全部功能。基于我们所看到的，似乎该平台将提供的功能不仅可以与谷歌助手和亚马逊 Alexa 竞争，还可以与[谷歌镜头](https://www.xda-developers.com/google-lens-arcore-augmented-reality/)和三星 Bixby 竞争。

 <picture>![HiAssistant Huawei](img/1686d71a7476cb8262d64d972c0054d5.png)</picture> 

HiAssistant's Logo

HiAssistant 的一个主要焦点是其自然语言理解(NLU)能力。NLU 指的是机器能够解释人类输入的非结构化句子的方式。尽管一个人可以有效地与另一个人交流，尽管发音错误、口头语和其他言语怪癖，但机器通常需要结构化的输入，以便理解命令的意图。

创建一个有效的 NLU 系统将解决语音助手最大的挫折之一，因为它将允许用户在不学习精确短语的情况下与助手说话，以达到预期的结果。虽然我们不能说华为的实现有多有效(我们没有在实时设备上运行 HiAssistant，也不会说它支持的中文之一)，但代码中到处都提到了 NLU，所以我们认为这是该技术的一个主要焦点。

### 辅助可用性

首先明确的是，HiAssistant 将**仅面向中国**用户，并且仅在运行 **EMUI 8.1** 的**麒麟 970** 的华为设备上使用。我们已经检查了用于[华为 P20](https://www.xda-developers.com/exclusive-huawei-p20-will-launch-with-android-8-1-oreo-and-emui-8-1/) 和 [P20 Plus](https://www.xda-developers.com/huawei-p20-plus-4000-mah-battery-always-on-display/) 的 EMUI 8.1 国际版的固件文件，但找不到这些应用程序。此外，在 EMUI 8.0 上检查中国华为 Mate 10 的固件时，HiAssistant 同样不可用。最后，HiAI 服务仅限于麒麟 970(因为它接入了它的 NPU)，因此不会在其他麒麟设备上可用。

### 辅助设备控制

华为 EMUI (Emotion UI)的最新版本目前为其少数设备提供 8.0 版本。8.1 版本将很快推出，很可能是随着即将发布的华为 P20 系列的发布，它将增加 EMUI 中已经存在的大量功能。像三星 Bixby 一样，HiAssistant 将允许用户通过语音控制设备上的几乎所有设置。

可以控制的设备设置列表太大，我无法一一列出，所以我将发布 HiAssistant 应用程序中引用可用设置进行控制的所有常量的截图。一般来说，你不仅要控制所有基本的硬件功能(蓝牙、NFC、Wi-Fi)，还要控制所有的软件功能(自动旋转、夜间模式、音量、显示屏色温、手套模式、位置设置、热点/移动数据等)。)

有趣的是，还有几个字符串暗示 HiAssistant 能够控制 QQ、微信等热门中文应用。我们发现了更多暗示 HiAssistant 应用程序能够发送的其他意图的字符串，包括与电话呼叫、地图/导航、信息、音乐/视频播放、页面导航等相关的字符串。

### 辅助搜索和集成

在上面显示的意图中，我们可以看到 HiAssistant 提供了搜索食物、表情、公共汽车、音乐、飞机票、导航路线、出租车、火车票、视频以及通过微博的能力。该助手还将提供搜索特定类别项目的能力，包括音乐专辑、动漫、书籍、电影、电视节目等。

不涉及太多细节，这些分析器如何在 NLU 处理后通过一系列复杂的正则表达式(regex)工作。例如，下面是动画分析器方法的一段代码。

华为的助手中提到了几个集成，但最大的一个集成似乎是直接从应用程序向中国几家主要银行付款的能力。

### 海康威视

最后，华为将提供一系列让我们想起谷歌镜头的功能。称为 HiVision，它将能够识别物体的类别，如食物、护照、人、配件、动物、器具、工具、玩具、车辆等。HiAI 移动计算平台将允许第三方应用程序使用其场景识别来识别海滩、自行车、汽车、猫、狗、烟花、鲜花等。最后，HiVision 还可以读取条形码、文本等，非常像谷歌镜头。

## 结论

从这些功能来看(同样，我们无法正确测试)，很明显华为的目标是成为谷歌助手、亚马逊 Alexa 和苹果 Siri 的适当竞争对手——至少在中国是如此。HiAssistant 不仅能提供对智能手机的完全控制，还能与众多流行的中国服务整合，以简化中国公民的生活。

尚不清楚华为在这里的努力是否会以任何方式转化为潜在的国际发布，因为华为似乎满足于在国际市场上与亚马逊和谷歌合作。如果我会说普通话，我会很乐意测试华为的 HiAssistant 和 HiVoice out，但遗憾的是，在 EMUI 8.1 正式发布、中国用户有机会测试之前，我们不会知道虚拟助手的效果如何。