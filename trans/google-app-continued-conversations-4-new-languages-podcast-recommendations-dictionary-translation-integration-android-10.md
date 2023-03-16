# 谷歌应用程序为 Android 10 准备了 4 种新的辅助语言、播客推荐和词典/翻译集成

> 原文：<https://www.xda-developers.com/google-app-continued-conversations-4-new-languages-podcast-recommendations-dictionary-translation-integration-android-10/>

在 IFA 2019 和最近[谷歌像素 4 泄露](https://www.xda-developers.com/tag/google-pixel4/)的疯狂中，谷歌应用的两个新测试版开始推出:版本 10.53.3 和 10.57.4。前者带来了一些变化，暗示着未来与 Android 10 的有趣集成，而后者则暗示着谷歌助手中持续对话的新语言和谷歌播客中更好的播客发现。这是我们的发现。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

## 谷歌助手继续对话的可能新语言

在谷歌 I/O 2018 上，谷歌[宣布了](https://www.xda-developers.com/google-assistant-continued-conversations-multiple-searches-pretty-please/)一个新的谷歌助手持续对话功能。这项功能让你可以跟踪谷歌助手的回复，而不必再次说“好，谷歌”或“嘿，谷歌”。尽管该功能已经从智能手机扩展到了[智能扬声器](https://www.xda-developers.com/continued-conversations-google-home-more-countries/)和[智能显示器](https://www.xda-developers.com/continued-conversations-smart-displays/)，但它[仍然只在你的助手语言设置为英语时才有效](https://support.google.com/googlenest/answer/7685981?hl=en)。过去的谷歌应用版本暗示了即将到来的对德语的支持，有一个字符串说谷歌目前正在对德语(DE)区域进行内部测试。现在，同样的字符串已经被更新，以反映谷歌正在为 4 种新语言提供持续对话支持:西班牙语、法语、意大利语和日语。

旧字符串:

```
 <string name="assistant_settings_summer_time_mode_availability_clarification_override">"Continued Conversation is currently available for English. If you use devices not shown here, the person with the primary account on those devices may turn Continued Conversation on or off in their Assistant settings.
We are also currently dogfooding the following locales: German (DE)."</string> 
```

新字符串:

```
 <string name="assistant_settings_summer_time_mode_availability_clarification_override">"Continued Conversation is currently available for English. If you use devices not shown here, the person with the primary account on those devices may turn Continued Conversation on or off in their Assistant settings.
We are also currently dogfooding the following locales:German, Spanish, French, Italian and Japanese."</string> 
```

## 谷歌播客推荐

近年来，播客的选择激增。也有很多好的电视节目、电影、电子游戏和其他形式的娱乐活动在争夺你的时间。如果你想找到你肯定会喜欢的新播客，那么谷歌播客新的个性化推荐功能可能会有所帮助。根据你拥有谷歌账户的时间和你注册了多少服务，谷歌可能有大量关于你偏好的信息。谷歌播客已经分析了一个节目的播客听众也在听什么，以便为类似的节目提供推荐，但这将进一步根据你的口味定制推荐。

```
 <string name="recommendations_promo_card_auto_awesome">Auto awesome</string>
<string name="recommendations_promo_card_browse_podcasts">Browse podcasts</string>
<string name="recommendations_promo_card_episode_subtitle">View personalized recommendations based on what you like to listen to</string>
<string name="recommendations_promo_card_episode_title">Looking for a great episode?</string>
<string name="recommendations_promo_card_no_thanks">No thanks</string>
<string name="recommendations_promo_card_show_subtitle">View personalized recommendations and discover great shows to subscribe to</string>
<string name="recommendations_promo_card_show_title">Looking for new podcasts?</string> 
```

## Android 10 的词典和翻译上下文菜单集成

在 Google App 10.53.3 中，我发现了两个活动的新清单声明:。SearchActivityFromDefine 和。SearchActivityFromTranslate，都是 minSdkVersion 设置为 29，SDK 版本的 [Android 10](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/) 。意图过滤器引用了两个新的活动动作:[Android . intent . action . translate](https://android.googlesource.com/platform/frameworks/base/+/android10-release/core/java/android/content/Intent.java#3862)和[Android . intent . action . define](https://android.googlesource.com/platform/frameworks/base/+/android10-release/core/java/android/content/Intent.java#3871)。这些意图的目的是允许一个应用程序接受从另一个应用程序翻译或定义的文本。虽然这在 Android 中已经可以使用 intent action Android . intent . action . send with intent EXTRA _ TEXT，但谷歌在 Android 10 中明确地为这两个特定的用例添加了 intent action，因此更多的应用程序可以充当默认的“[翻译器](https://android.googlesource.com/platform/frameworks/base/+/4bad09cd1d97e687c91c991396259070a6b62918)或“[字典](https://android.googlesource.com/platform/frameworks/base/+/e1f3ac064c2df9f70a9ac356314275273ef2ff97)”

通过检查反编译的代码，我们发现了 Google App 计划如何处理这两个新意图。一旦接收到意图，谷歌应用程序将解析来自 intent extra[Android . view . TEXT CLASSIFIER . extra . from _ TEXT _ CLASSIFIER](https://developer.android.com/reference/android/view/textclassifier/TextClassifier#EXTRA_FROM_TEXT_CLASSIFIER)的文本，该文本通常来自长按上下文菜单发送的意图，以决定是否需要翻译或定义所选文本。因此，你将能够在 Android 10 的任何应用程序中长按文本，并选择谷歌助手来处理定义单词或翻译文本块。你甚至不需要安装谷歌翻译(虽然它仍然绝对值得)或第三方词典应用程序。

我们设法让谷歌应用程序为 Android . intent . action . translate 设置了默认处理程序，但该功能目前似乎无法工作，因为选择该选项只会打开常规的谷歌助手操作。

一旦这些功能上线，我们会通知大家。你可以从 APKMirror 下载最新版本的谷歌应用测试版，或者在 Google Play 上注册测试版。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*