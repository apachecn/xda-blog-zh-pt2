# Google 相册会暂时禁用某些消息应用程序的备份

> 原文：<https://www.xda-developers.com/google-photos-temporarily-disables-back-up-facebook-whatsapp/>

上周，我们发现谷歌正准备禁用许多社交媒体/消息应用程序的 Google 相册备份。该应用的字符串明确提到了新冠肺炎疫情的原因，称“为了节省互联网资源，备份&同步已被关闭”，用于消息应用。今天，这一改变正式生效。

之前发现的消息现在已经正式发布在谷歌照片社区论坛上。谷歌照片应用程序也会向用户显示通知。这意味着默认情况下，受影响服务中的照片和视频将不再备份。用户必须手动进入应用程序，选择要备份的文件夹。

谷歌的声明只是特别提到“像 WhatsApp、Messages 和 Kik 这样的消息应用”是会受到这一变化影响的应用。然而，在最新的谷歌照片 APK 的拆解中，我们发现了所有包含的应用程序。名称与以下正则表达式匹配的文件夹将不会被备份:

```
 .*(Facebook|Helo|Instagram|LINE|Messages|Messenger|Snapchat|Twitter|Viber|WhatsApp).* 
```

这意味着来自脸书、Helo、Instagram、LINE、Messages、Messenger、Snapchat、Twitter、Viber 和 WhatsApp 的图片将不会被备份。这些文件夹中以前的备份将不受影响。如上所述，你仍然可以进入应用程序中的设置，手动启用备份。如果您有旧的或[新的照片 UI](https://www.xda-developers.com/google-photos-new-logo-redesign/) 进行更改，请前往“设置”>“备份和同步”>“备份设备文件夹”。

我们已经看到谷歌[在疫情期间做出类似的改变](https://www.xda-developers.com/youtube-android-restricts-maximum-video-streaming-quality-480p-standard-definition-india-covid19/)来节省带宽，所以类似这样的事情并不罕见，尽管考虑到疫情接管我们的生活已经有多久了，这有点晚了。

* * *

**来源:[谷歌](https://support.google.com/photos/thread/56206903?hl=en) | Via: [安卓警察](https://www.androidpolice.com/2020/06/29/google-photos-will-no-longer-back-up-images-from-whatsapp-messages-and-kik-by-default/)**