# 谷歌助手现在支持第三方应用的快捷方式

> 原文：<https://www.xda-developers.com/google-assistant-now-supports-shortcuts-for-third-party-apps-and-new-features-on-smart-displays/>

在周四的助理开发者日，谷歌推出了令人兴奋的谷歌助理新功能，这是该公司的虚拟助理服务。新功能之一是与 Android 上的第三方应用程序进行更深入的集成，允许用户打开和搜索应用程序，并完成更复杂的任务，包括播放音乐、开始跑步或在社交媒体上发布消息。

这项新功能目前已经可以在所有支持助手的 Android 手机上使用，它可以与 Google Play 上的 30 多个顶级应用程序配合使用，更多的应用程序支持将很快推出。根据 [*Droid-Life*](https://www.droid-life.com/2020/10/08/google-assistant-adds-app-shortcuts-to-do-simple-tasks-by-voice/) 显示，目前支持快捷方式的应用列表包括:花旗、Dunkin、Paypal、Wayfair、Wish、优步、Yahoo！Mail、Nike Adapt、Nike Run Club、Spotify、Postmates、Grubhub、MyFitnessPal、Mint、Discord、沃尔玛、Etsy、Snapchat、Twitter、YouTube、谷歌地图、Instagram、Twitch 和百思买。

作为更深层次整合的一部分，谷歌助手还获得了对第三方应用快捷方式的支持。“因此，你可以创建一个快捷方式，而不是说‘嘿，谷歌，用 Nike Adapt 系紧我的鞋’，而是说‘嘿，谷歌，系紧鞋带。“如果这不是对未来的一瞥，我不知道什么是。

开发者可以通过[应用动作](https://developers.google.com/assistant/app/overview)将内置集成添加到他们的应用中，允许用户在应用中搜索，也可以在这些应用中打开特定页面。“从今天开始，你可以使用 GET_THING 意图在应用内搜索，使用 OPEN_APP_FEATURE 意图在应用中打开特定页面，”谷歌在博客文章中宣布[。开发者将拥有工具来实现一个](https://developers.googleblog.com/2020/10/google-assistant-developer-day-new.html)[内置意图](https://developers.google.com/assistant/app/intents)或者一个[自定义意图](https://developers.google.com/assistant/app/custom-intents)；您可以通过在 Actions.xml 文件中声明对这些常见意图中的一个或多个[的支持来立即开始。为了更深入的集成，你可以创建一个特定于垂直领域的内置意图(BII)，让谷歌助手处理自然语言理解(NLU)。谷歌表示，现在 10 个垂直领域有超过 60 个意向，包括“社交、游戏、本地旅游、生产力、购物和通信等新类别”。](https://developers.google.com/assistant/app/reference/built-in-intents/common)

为了提高可发现性和易用性，谷歌设计了一些建议和快捷方式，帮助用户了解支持应用程序操作的 Android 应用程序。要查看可用的快捷方式，用户只需说，“嘿，谷歌，快捷方式，”即可在设置中设置和浏览建议的快捷方式。用户需要在使用谷歌助手之前添加快捷方式。谷歌将主动提供快捷方式建议，作为助手搜索结果中的一个芯片，或者用户可以逐个应用程序地启用快捷方式。

## 智能显示器上谷歌助手的改进

谷歌还通过引入改进的语音和可信的支付语音来改善智能显示器上的助手。谷歌称有两种新的声音听起来更自然。开发者可以通过改变动作控制台中的模型来使用新的声音。你可以听听其中一个声音[就在这里](https://drive.google.com/file/d/1cakhPrtlbJ_hwhmZZHriT1k7Q4v5UOTP/view)。

至于可信的付款声音，听起来就是这样。谷歌将允许用户直接从他们的智能显示屏上购买东西，因为谷歌知道你的声音，只有授权用户才能发起支付。你只需要问一下就可以付款，很快谷歌将引入显示的 CVC 条目，以增加一层安全性。

此外，谷歌还将交互式画布扩展到教育和讲故事垂直领域的动作，引入动作测试 API 作为测试关键用户旅程的编程方式，在动作控制台中提供新的 [DialogFlow 迁移工具](https://developers.google.com/assistant/conversational/dialogflow-to-builder)，以自动将项目迁移到新平台，并为游戏开发者推出新的[资源中心](https://developers.google.com/assistant/games)。要了解更多关于谷歌智能显示助手的其他变化，请访问[谷歌开发者博客文章](https://developers.googleblog.com/2020/10/google-assistant-developer-day-new.html)。