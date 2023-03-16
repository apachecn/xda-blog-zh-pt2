# Google Play 服务将很快帮助您在 Android 中设置 RCS/聊天应用程序

> 原文：<https://www.xda-developers.com/google-play-services-20-15-13-rcs-chat-android-messages/>

美国的信息传递与世界其他地方有很大不同。虽然像 [WhatsApp](https://forum.xda-developers.com/t/whatsapp) 和 [Telegram](https://www.xda-developers.com/announcing-the-official-xda-developers-telegram-group/) 这样的应用程序已经成为许多国家的主要通信平台，但美国的 Android 用户仍然非常依赖短信来发送信息，特别是因为他们使用 iPhones 的同行已经与苹果的 iMessage 挂钩。这启发了 Google 去开发一个平行的，导致该公司帮助推动 RCS 消息。丰富的通信服务[，谷歌简单地称之为“聊天”](https://www.xda-developers.com/google-allo-paused-chat-rcs-apple-imessage/)，支持多媒体功能和阅读回执，不像短信。虽然 RCS 和 Chat 仅限于少数第一方消息应用，包括谷歌的 Messages 应用，但仍有许多用户可能不知道它的存在。

谷歌将很快在设置中添加一个新页面，显示所有支持 RCS 和/或聊天消息的已安装应用程序的列表。通过分析最新 APK 包中的资源，我们在最新的 Google Play 服务测试版中发现了对这一即将推出的功能的引用。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

我们在 Google Play 服务 v20.15.13 中发现的新字符串表明，Google Play 服务中的新设置页面将显示手机上支持 RCS 的应用程序列表。该页面还将指导用户如何在这些应用程序中设置和使用 RCS 消息。然而，更新并没有增加任何新的选项来打开或关闭每个应用程序的 RCS，因为该功能可能仅限于单个应用程序。鉴于您一次只能使用一个消息应用程序发送和接收短信，RCS 功能将只能通过默认的短信应用程序使用。

Google Play 服务 v20.15.13 中的以下字符串暗示了即将推出的功能可能如何工作:

```
 <string name="c11n_chat_features_activity_label">Chat features</string>
<string name="c11n_chat_features_learn_more">Learn more about Chat features</string>
<string name="c11n_chat_features_privacy">Privacy Policy</string>
<string name="c11n_chat_features_terms_of_service">Terms of Service</string>
<string name="c11n_chat_features_text">"Chat features lets you send upgraded, high-quality images and videos over Wi-Fi and mobile data using Rich Communication Services (RCS).&lt;br/>&lt;br/>When you turn on Chat features from Google, you agree to the %1$s. Google will occasionally verify your number with your carrier (SMS charges may apply). Google's %2$s describes how data is handled. %3$s."</string>
<string name="c11n_connected_apps">Connected apps</string> 
```

我们还发现了以下字符串，该字符串引用了如何在 Samsung Messages 应用程序中启用 RCS 消息传递的教程:

```
 <string name="c11n_samsung_steps">To turn Chat features on/off&lt;br/>1\. Open %1$s&lt;br/> 2\. Go to More options &lt;b>⋮&lt;/b> and tap &lt;b>Settings&lt;/b>&lt;br/> 3\. Tap &lt;b>Chat Settings&lt;/b> and turn Rich Communication settings on/off</string> 
```

RCS 在三星的 Messages 应用程序中已经可用了一段时间，但对于那些不知道它存在的人，该页面将告诉他们如何启用它。谷歌的信息应用程序也是如此。下面的截图显示了即将到来的设置页面，展示了如何在 Google Pixel 设备上的 Messages 应用程序中启用聊天。

当该功能开始推出时，我们会及时通知您。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*