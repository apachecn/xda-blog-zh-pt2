# Google Play 服务 20.12.14 提示让父母为孩子创建第二锁屏

> 原文：<https://www.xda-developers.com/google-play-services-20-12-14-parents-create-secondary-lockscreen-for-kids/>

# Google Play 服务 20.12.14 提示让父母为孩子创建第二锁屏

APK 拆除了 Google Play 服务，这表明父母很快就能为他们的孩子创建第二锁屏。

距离谷歌发布 Android 11 的第一个开发者预览版已经过去一个多月了。不用说，目前发布的两个版本都比 Android 10 有很多变化，包括新的一次性权限使用、通知历史等。虽然我们已经在[开发者预览版 1](https://www.xda-developers.com/android-11-developer-preview-changes/) 和更新的[开发者预览版 2](https://www.xda-developers.com/android-11-developer-preview-2-changes/) 中涵盖了大多数面向用户和幕后的变化，但仍有许多新的 API 我们一直在关注。其中之一是[DevicePolicyKeyguardService](https://developer.android.com/reference/android/app/admin/DevicePolicyKeyguardService.html)API，它旨在为 SystemUI 提供辅助锁屏。由于设备管理要求，我们最初认为这只是为了企业使用，但我们发现了作为 Family Link 的新家长控制工具的另一个潜在用途。

我们在 Google Play 服务 20.12.14 的清单文件中挖掘出的一个新服务表明，我们可能很快就会看到这个 API 的第一方集成。这项服务的名字“com . Google . Android . GMS . kids . secondarylockscreenservice”让我们相信 [Family Link](https://www.xda-developers.com/digital-wellbeing-integration-family-link-parental-controls/) 将会利用它。我们可以做出一个有根据的猜测，谷歌将让父母为他们的孩子设置一个辅助锁屏，然后显示不同于主锁屏的信息。API 文档提到实现必须由设备管理应用程序提供，Google Play 服务满足了这一点。服务中的 boolean“platform leastr”暗示该功能将仅适用于运行 Android 11 及以上版本的设备。

```
 <service android:enabled="@bool/platformIsAtLeastR" android:exported="@bool/platformIsAtLeastR" android:name="com.google.android.gms.kids.SecondaryLockscreenService" android:permission="android.permission.BIND_DEVICE_ADMIN" android:process="com.google.android.gms.ui" chimera:autoEnabled="false">
    <intent-filter>
        <action android:name="android.app.action.BIND_SECONDARY_LOCKSCREEN_SERVICE"/>
    </intent-filter>
</service> 
```

请记住，即使该服务出现在 Google Play 服务清单中，我们也没有找到任何与该功能相关的字符串或资产。同样，Family Link 的最新版本也没有关于该功能的任何细节。这可能意味着该功能处于早期开发阶段，所以我们必须等待它变得更加充实。不过，我认为在 Android 11 稳定版发布后，我们会很快看到更多细节。