# Google App v7.3 准备添加一个通知监听器服务来拦截通知

> 原文：<https://www.xda-developers.com/google-app-v7-3-prepares-to-add-a-notification-listener-service-to-intercept-notifications/>

谷歌应用 v7.3.16 测试版正在 Play Store 上向用户推出，虽然我们传统的 APK 拆卸并没有透露太多我们认为有趣的信息，但有一个功能我认为值得分享。Android Manifest 文件中的新字符串实现了一个[通知监听器服务](https://developer.android.com/reference/android/service/notification/NotificationListenerService.html),它暗示了谷歌应用程序可以拦截你的通知的可能性。具体出于什么目的，目前只能推测。

虽然 APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都有可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## 谷歌应用 7.3 版 APK 拆卸

现在我知道你们中的一些人可能会想:“谷歌应用程序不是已经支持通知了吗？”是的，但这不是我们在这里谈论的。Google App 支持的通知是针对 Google Now 发送给你的各种提醒和更新。通知监听器服务允许谷歌应用程序拦截由其他应用程序发布的通知。

Android 清单文件中包含了新的通知监听器服务。老实说，除了它确实存在这一事实之外，这里没什么可说的。

```
 <service android:enabled="false" android:exported="true" android:name="com.google.android.apps.gsa.notificationlistener.GsaNotificationListenerService" android:permission="android.permission.BIND_NOTIFICATION_LISTENER_SERVICE" android:process=":interactor">
<intent-filter>
<action android:name="android.service.notification.NotificationListenerService"/>
</intent-filter>
</service> 
```

Google 应用程序使用相应的显式广播接收器来对发布/移除通知做出反应。

```
 <receiver android:name="com.google.android.apps.gsa.staticplugins.ipa.notifications.IpaBroadcastReceiver" android:process=":interactor">
<intent-filter>
<action android:name="com.google.android.apps.gsa.notificationlistener.NOTIFICATION_LISTENER_SERVICE_CONNECTED"/>
</intent-filter>
</receiver> 
```

在一个新的 smali 文件(位于 com/Google/Android/apps/GSA/notification listener 中的 d.smali)中，有更多关于这一点的证据:

```
 invoke-virtual {p0}, Landroid/content/Context;->getContentResolver()Landroid/content/ContentResolver;

move-result-object v1

const-string v2, "enabled_notification_listeners"

invoke-static {v1, v2}, Landroid/provider/Settings$Secure;->getString(Landroid/content/ContentResolver;Ljava/lang/String;)Ljava/lang/String;

move-result-object v1 
```

对字符串“enabled_notification_listeners”的引用是指设置。同名的安全首选项，包含以冒号分隔的已启用通知监听程序服务列表。

此时，通知侦听器服务不能在实时构建中启用，所以我们不能确切地确认它将用于什么。然而，如果我们稍微推测一下，我们认为这可能是指我们上个月发现的[“Bisto”设备类型](https://www.xda-developers.com/google-app-7-0-4-prepares-for-multi-user-hotword-detection-rating-services-and-references-a-device-called-bisto/)。当时，谷歌应用程序被拆除，显示 Bisto 将是一种耳机，你可以通过它收听通知。但监听你手机所有通知的唯一方法是，如果该应用程序启用了通知监听服务，那么这是我们最有可能的解释。

* * *

如果我在实时构建中或者通过 APK 的拆除发现了什么有趣的东西，我会继续挖掘并更新这篇文章。如果你正在寻找谷歌应用程序的最新版本，你现在就可以在 [APKMirror](https://www.apkmirror.com/apk/google-inc/google-search/google-search-7-3-16-release/) 下载。关注我们的 [APK 拆卸标签](https://www.xda-developers.com/tag/apk-teardown/)获取更多类似的文章！