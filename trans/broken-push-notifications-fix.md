# 自定义 rom 上 Android 设备的坏推通知修复

> 原文：<https://www.xda-developers.com/broken-push-notifications-fix/>

在 XDA 开发者中，我们都是定制 rom、主题和其他各种修改的超级粉丝。我们中的一些人经常在不同的定制 rom 之间切换，因此使用 app 备份解决方案，如 [oandbackup](https://f-droid.org/packages/dk.jens.backup/) 或流行的 Titanium Backup。许多用户报告了在干净的闪存或 ROM 切换后推送通知中断的问题，WhatsApp 是最大的违规者之一。其他应用程序，如 Tumblr，也成为不显示任何推送通知的受害者。这是为什么？你如何解决这个问题？

* * *

## 问题是

安装了 Google Play 服务的 Android 设备注册了 Firebase Cloud Messaging (FCM)服务，以前称为 Google Cloud Messaging (GCM)。这是为你计算一个唯一的设备令牌，然后当你安装一个支持 FCM 的应用程序(如 WhatsApp)时，它会向 FCM 推送服务注册，这样它就可以向你发送推送通知。当您的设备处于休眠模式时，只要有高优先级的 FCM 通知推送到您的设备，您的设备就会被唤醒。例如，高优先级的 FCM 通知包括 WhatsApp 和其他即时消息应用程序。然而，如果你在设备上安装新的 ROM 时擦除系统，你的手机将注册一个新的**FCM 令牌，并且你用数据恢复的任何应用将无法再推送 FCM 通知，因为它们仍在使用旧令牌。**

但是如果你的手机没有安装 Google Play 服务呢？您如何接收通知？嗯，支持 FCM 的应用通常会有自己的推送通知服务作为后备。例如，Facebook Messenger 使用一项名为 FBNS 的服务，当谷歌 Play 服务未被检测到时，它会默认使用这项服务。这可以在隐藏在 Facebook Messenger 内部的“推送通知”部分旁边的截图中看到。我相信一些应用程序会检测到 FCM 何时不起作用，并在 FCM 中断时回退到自己的服务，但显然不是每个应用程序都这样做。

* * *

## 解决中断的推送通知

避免遇到问题的最简单方法是**正常安装应用程序**，而不是在干净的闪存或 ROM 切换后通过 Titanium Backup(或您选择的其他备份服务)进行恢复。对于一些应用程序来说，这可能很困难，但 WhatsApp 等许多应用程序允许你在应用程序中备份聊天记录。Tumblr 等其他应用程序的所有数据都在云中，因此没有理由恢复这些数据。如果您在推送通知方面遇到问题，并且使用了备份服务来恢复您的应用程序，请尝试通过 Play Store 重新安装它们。我个人遇到的任何推送通知问题都已经通过正常方式(通过 Play Store 或直接通过 APK)重新安装该应用程序得到了修复，所以请尝试一下，我希望它可以修复您的推送通知故障！

* * *

**建议阅读:**[Gmail 自动静音烦人的工作邮件](https://www.xda-developers.com/silence-annoying-work-emails-automatically-with-quiet-for-gmail/)