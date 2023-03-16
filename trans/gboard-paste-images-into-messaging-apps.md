# Gboard 准备让你将复制的图片粘贴到多个社交和信息应用中

> 原文：<https://www.xda-developers.com/gboard-paste-images-into-messaging-apps/>

许多操作系统的一个基本特性是复制和粘贴图像的能力。这是我们在使用 PC 时想当然的事情，但在移动设备上就没这么简单了。几天前，[我们发现了一个 Chromium commit](https://www.xda-developers.com/google-chrome-copy-images-directly-android-clipboard/) ,它提到了添加对将图像复制到 Android 剪贴板的支持。从那以后，提交已经被合并，并且特性标志是可用的。现在，谷歌正准备更新 Gboard，以增加对该功能的支持。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

正如你在上面看到的，一旦启用了 Chrome 标志，图像的上下文菜单现在包括了“复制图像”但一旦图像被复制到剪贴板，我们发现目前无法将其粘贴到 Telegram 或 Twitter 等应用程序中。在 Android 10 中，只有默认键盘和当前前台应用程序[可以读取剪贴板](https://www.xda-developers.com/android-q-blocks-background-clipboard-access/)，所以一旦你从你复制图像的应用程序中切换出来，就由它们来处理图像。我们发现 Google 正在准备让 Gboard 在 9.0.2 版本中能够处理从剪贴板插入图像。

```
 <string name="clipboard_notice_banner_description">A promo to let users know that current application does not support pasting images.</string>
<string name="image_info_clip_description">Image from Gboard Clipboard</string>
<string name="image_share_intent_whitelist">com.android.mms, com.whatsapp, com.facebook.orca, com.viber.voip, jp.naver.line.android, com.android.messaging, ru.ok.android, com.tencent.mm, com.facebook.mlite, com.snapchat.android, com.motorola.messaging, com.google.android.apps.messaging, com.vkontakte.android, com.skype.raider, com.imo.android.imoim, com.samsung.android.messaging, com.zing.zalo, com.google.android.apps.docs, com.twitter.android, com.badoo.mobile, com.google.android.talk, app.buzz.share, com.random.chat.app</string> 
```

上面的字符串是 Gboard 最新版本 9.0.2 新增的。第一个字符串是 toast 通知，告诉用户当前应用程序不支持粘贴图像。第三个字符串向我们展示了如果该功能启动，可以支持粘贴图像的应用程序列表。这些应用程序包括:

*   AOSP 消息
*   WhatsApp
*   脸谱网
*   Viber
*   线条
*   好
*   微信
*   Messenger Lite
*   Snapchat
*   摩托罗拉消息
*   谷歌消息
*   维生素 k
*   网络电话
*   国际海事组织；依我之见
*   三星信息
*   萨梵
*   谷歌文档
*   推特
*   巴杜
*   聚会场所
*   直升机

我们能够在 Chrome 中启用功能标志并复制图像，但无法将其粘贴到 Twitter 中，因此该功能目前似乎没有在 Gboard 中上线。这是许多人可能甚至没有意识到他们的手机缺少的一个功能，但当你意识到这一点时，它就很有意义了。我们希望很快看到它。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*