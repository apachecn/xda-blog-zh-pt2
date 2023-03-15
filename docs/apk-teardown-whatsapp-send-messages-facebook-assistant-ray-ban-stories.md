# WhatsApp 可能很快会让你通过脸书助手发送关于雷朋故事的信息

> 原文：<https://www.xda-developers.com/apk-teardown-whatsapp-send-messages-facebook-assistant-ray-ban-stories/>

WhatsApp 是目前最受欢迎的即时通讯应用。尽管它很受欢迎，但在引入新功能方面却进展缓慢。例如，[社区功能早在 2021 年 10 月就被我们首次发现](https://www.xda-developers.com/whatsapp-new-community-feature-apk-teardown/)，直到昨天[才正式宣布](https://www.xda-developers.com/whatsapp-making-group-chats-better/)。WhatsApp 的一个痛点仍然是它与语音助手的不集成——你不能要求谷歌助手在 WhatsApp 上给某人发送消息。Meta 可能正在努力让这一切发生，但不是用谷歌助手，而是用脸书助手和它的[雷朋故事智能眼镜](https://www.xda-developers.com/facebook-ray-ban-stories/)。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

最新的 WhatsApp 测试版 2.22.9.13 包括一些字符串和资产，表明这家 Meta 拥有的即时通讯应用程序可能正在努力让用户通过其 Ray-Ban Stories 智能眼镜上的脸书助手发送消息。

```
 <string name="instrumentation_auth_complete_bullet_one">Tell Assistant who you want to contact. Be sure to say “on WhatsApp” after their name so Assistant knows to open a WhatsApp message secured with end-to-end encryption.</string>
<string name="instrumentation_auth_complete_bullet_three">"Wait to say your message after Assistant asks you, so you know you're speaking into WhatsApp."</string>
<string name="instrumentation_auth_complete_bullet_two">For example, “Hey Facebook, message Anna on WhatsApp.”</string>
<string name="instrumentation_auth_complete_button">Connect with Ray-Ban Stories</string>
<string name="instrumentation_auth_complete_link">&lt;a href=\"%1$s\">Learn how your voice information is kept private on Ray-Ban Stories.&lt;/a></string>
<string name="instrumentation_auth_complete_title">Send a WhatsApp Message With Assistant</string>
<string name="instrumentation_auth_perm_button">Next</string>
<string name="instrumentation_auth_perm_paragraph_one">When you use WhatsApp with Ray-Ban Stories, the contents of your personal messages and calls are always secured with end-to-end encryption. Not even WhatsApp can read or listen to them.</string>
<string name="instrumentation_auth_perm_paragraph_two">&lt;a href=\"%1$s\">Learn more about your privacy on WhatsApp.&lt;/a></string>
<string name="instrumentation_auth_perm_title">Use WhatsApp with Ray-Ban Stories</string>
<string name="instrumentation_auth_title">Link with WhatsApp</string> 
```

一些字符串只是提到了“助手”，但在你抱有希望之前，这些字符串的上下文表明它可能是指脸书助手而不是谷歌助手。雷朋故事智能眼镜包括脸书助手作为语音助手的选择，让用户通过语音命令在智能眼镜上拍摄照片和视频。上面的字符串变得不言自明。智能眼镜用户将能够把他们的智能眼镜与手机上的 WhatsApp 连接起来，然后说出类似“嘿，脸书，在 WhatsApp 上给安娜发消息”的命令，就可以继续发送消息，而无需从口袋中拿出手机。

除了字符串之外，APK 还包含以下两种图形资源(和一些其他较小的图标):

第一个图形巩固了我们从弦乐中学到的东西。第二个图形用于突出显示端到端加密，当通过脸书助手使用基于语音的命令时，该加密可能仍然有效。

目前还不清楚该功能何时推出。但它应该只会让一小部分用户受益——那些拥有雷朋 Stories 智能眼镜、也使用 WhatsApp、希望利用语音命令在该平台上发送信息的用户。目前，没有迹象表明语音命令支持会扩展到其他虚拟助手，也没有迹象表明它会扩展到智能眼镜用例之外。所以保持你的期望。

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*