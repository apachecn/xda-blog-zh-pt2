# Fitbit 正准备将谷歌助手支持带到健身手表上

> 原文：<https://www.xda-developers.com/fitbit-google-assistant-support/>

去年年底，谷歌宣布了以 21 亿美元收购 Fitbit 的计划。这笔交易仍在等待批准，我们已经有一段时间没有听到任何消息了。我们仍然不知道这两家公司计划做什么，但看起来 Fitbit 可能正在努力为其设备提供谷歌助手支持。

目前，Fitbit 在 Versa 2 健身手表上支持亚马逊 Alexa。该设备没有大声朗读答案的扬声器，也没有热门词汇检测功能。与成熟的智能手表相比，这种集成还很初级，但总比没有好。据报道，Fitbit 曾就将 Assistant 引入 Versa 2 一事与谷歌接洽，但该公司不太愿意促成此事。在 Fitbit Android 应用程序最近的更新中发现的字符串似乎表明事情已经发生了变化。

谷歌的人在 APK 发现了一些关于“助手”的内容。这些字符串可以很容易地引用 Amazon Alexa，但是一些 XML 文件明确地命名为“google_assistant”字符串和 XML 文件列出了诸如激活助手、错误消息、开机等基本信息。支持的基础似乎已经就绪。

```
 <string name=”ga_activate_assistant”>Activate Assistant</string>
<string name=”ga_activate_assistant_general_error”>Unable to process request to activate Assistant</string>
<string name=”ga_deactivation_error”>Error deactivating Assistant</string> 
```

*   RES/layout/a _ Google _ assistant _ on _ boarding . XML
*   RES/layout/f _ Google _ assistant _ landing . XML
*   RES/layout/f _ Google _ assistant _ teaser . XML

进一步挖掘 Fitbit 应用程序，其中提到一次只能使用一个助手，并且可以随时切换提供商。用户可能会在亚马逊 Alexa 和谷歌助手之间进行选择，但他们也可以随心所欲地切换。对于可能投资于这两种生态系统的用户来说，这是一个很好的选择。

如前所述，目前 Fitbit Versa 2 支持 Alexa，这使得它很可能成为谷歌助手支持的候选对象。Fitbit 也完全有可能把它留到新品发布会上。对于谷歌生态系统中的任何 Fitbit 粉丝来说，这无疑是一个令人兴奋的发展。

* * *

**来源:[9 to 5 Google](https://9to5google.com/2020/06/11/google-assistant-fitbit-support/)**