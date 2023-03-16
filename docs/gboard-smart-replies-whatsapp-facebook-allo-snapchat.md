# Gboard 正在测试 WhatsApp、脸书、Allo、Snapchat 等应用的智能回复

> 原文：<https://www.xda-developers.com/gboard-smart-replies-whatsapp-facebook-allo-snapchat/>

自从安卓版 Swype 停产以来，谷歌用于 Nexus 和 Pixel 智能手机的股票键盘应用 Gboard 一直是我的首选键盘。Android 设备的流行键盘应用程序最近获得了创建 gif 的[功能](https://www.xda-developers.com/gboard-gif-creation/)，但最近一次添加了我称之为“智能”的功能的更新是在二月份，添加了[电子邮件地址自动完成功能](https://www.xda-developers.com/gboard-beta-email-address-autocompletion-chinese-korean-languages/)。现在，随着 Gboard 测试对 WhatsApp、Facebook Messenger、Google Allo、Snapchat 等即时通讯应用的智能回复，一月份拆机时暗示的功能[似乎即将完成。](https://www.androidpolice.com/2018/01/18/gboard-v6-9-prepares-smart-replies-messenger-notifications-deeper-bitmoji-integration-apk-teardown/)

该功能目前正在开发中，是由 XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 发现的( [Mighty Quinn Apps](http://quinny898.co.uk) 的 Kieron Quinn)。设置这个功能需要首先打开一个有快速回复框的通知，然后在 Gboard 的自动完成栏中点击建议来启用这个功能。然后，Gboard 将请求您授予它通知访问权限。

一旦获得授权，您将开始从以下应用程序接收邮件的智能回复:

*   Android 消息
*   脸书信使
*   Facebook Messenger Lite
*   谷歌喂
*   谷歌视频
*   Snapchat
*   WhatsApp
*   微信

我们在 Hangouts 上测试了这一功能，尽管它也适用于其他提到的应用程序，如 Facebook Messenger、WhatsApp、Allo 和 Snapchat。我们通过拆卸最新版本的谷歌键盘应用程序获得了受支持应用程序的列表。在这个 [URL](https://www.gstatic.com/android/keyboard/modelpack/notificationsmartreply/superpacks_manifest.json) 处，我们可以看到谷歌仍在调整用于智能回复的 TensorFlow 机器学习模型。模型最近一次更新是在 2018 年 5 月 14 日。

就我个人而言，我更喜欢在 Gboard 中使用智能回复，而不是使用'[回复](https://www.xda-developers.com/reply-google-smart-replies-twitter-hangouts-android-messages-facebook-messenger/)'应用程序。当然，回复应用程序支持更多的应用程序，但由于它涉及到替换原始消息应用程序的实际通知，所以有一些烦恼，比如在桌面客户端上取消通知(比如说 [Android Messages for Web](https://www.xda-developers.com/send-text-messages-pc-android-messages-for-web/) )不会清除 Android 上的通知。另一方面，回复应用程序将适用于 Facebook Messenger、Allo、Snapchat 或 WhatsApp 等应用程序，而不管你的键盘应用程序如何。

智能回复功能最近已经进入了一系列谷歌应用和服务。非 Project Fi Android Messages 用户[刚刚开始获得它](https://www.xda-developers.com/smart-reply-android-messages-non-project-fi/)和[主要桌面 Gmail 重新设计](https://www.xda-developers.com/gmail-web-redesign-rollout/)也带来了这样的功能。我们将密切关注智能回复功能何时在 Android 上推出，特别是如果它[成功转移到 Chromebooks](https://www.xda-developers.com/chrome-os-android-keyboards-gboard/) 。

如果你想知道，第一组截图中丢失的后退按钮来自我运行的一个[特殊 ADB 命令](https://twitter.com/MishaalRahman/status/1012766142841188352)以使后退按钮不可见。第二组截图中的导航栏不见了，因为我在 XDA 导航手势应用中启用了新的一加风格手势。最后，快速设置面板是主题化的，这要归功于 Substratum [对 Android P 设备的支持。](https://www.xda-developers.com/custom-themes-android-p-root-substratum/)