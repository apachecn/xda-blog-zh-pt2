# 如何将安卓奥利奥后台位置节流的应用列入白名单

> 原文：<https://www.xda-developers.com/android-oreo-background-location-whitelist/>

谷歌最新的美味佳肴——安卓 8.0 奥利奥有很多让人喜欢的地方。从[会加快更新速度的重大低级改动](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/)到[小的生活质量改动](https://www.xda-developers.com/bluetooth-in-band-ringtone-android-o/)到[全定制主题支持](https://www.xda-developers.com/android-oreo-rootless-system-theme/)，在[最新更新里有东西让大家](https://www.xda-developers.com/list-android-oreo-unofficial-ports/)欣赏。但是 Android Oreo 最大的变化之一，[后台应用限制](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)，已经让一些用户有点头疼。不，这并不是令人讨厌的“应用程序正在后台运行”通知，我们已经[展示了如何隐藏](https://www.xda-developers.com/hide-app-running-background-notification-android-oreo/)。相反，事实是这些新的后台位置限制已经**破坏了某些用户的某些应用**，特别是那些**依赖于不断获取你的位置更新的应用**。

平心而论，这不一定是安卓奥利奥本身的问题。最新的操作系统更新旨在控制一些表现不佳的应用程序，这些应用程序经常在后台运行，耗尽你的电池或内存。这取决于应用程序开发人员自己[确保他们的应用程序使用前台服务](https://developer.android.com/about/versions/oreo/background-location-limits.html)，这样他们的应用程序就可以不受任何限制地继续轮询位置。对于一个普通用户来说，要想让他们喜欢的需要持续 GPS 定位的应用程序保持运行，最好的办法就是**联系开发者**，友好地要求他们遵守 Android Oreo 的新要求。

但是，有时您可能希望继续使用一个已经过时或被放弃的应用程序，这样就没有更新的希望了。我们不会评判。在这种情况下，显然联系开发商对你没有任何好处。但值得庆幸的是，有一种方法可以绕过 Android Oreo 的新后台位置节流——它**不需要 root 或修改任何 apk**。

* * *

## Android Oreo 后台位置调节的白名单应用

前几天，一位用户告诉我,[的 GolfPad 应用程序](https://play.google.com/store/apps/details?id=com.contorra.golfpad)在之前的 Android 版本上无法正常工作，之后这个问题[在 Reddit 的一个帖子](https://www.reddit.com/r/Android/comments/6yjawo/oems_are_required_to_implement_android_oreos/dmnuwre/)上引起了我的注意。经过一番挖掘，我发现了一个**隐藏的开发者 ADB 命令**，它可以用来将任何你想要的应用列入白名单，不受 Android 8.0 中引入的严格的后台位置限制。这是如何做到的:

1.  将 ADB 安装到您的电脑上。
2.  获取要加入白名单的应用程序的包名。为此，我们建议使用[包名查看器](https://play.google.com/store/apps/details?id=com.csdroid.pkg)。
3.  打开命令提示符或终端，输入以下命令:`adb shell`
4.  现在，输入这个 ADB 命令:`settings put global location_background_throttle_package_whitelist "package1,package2,package3"`
5.  在上面的引号之间，您输入一个逗号分隔的包名称列表，用于您想要加入白名单的每个应用程序。在前面提到的 GolfPad 应用程序中，命令是这样的:`settings put global location_background_throttle_package_whitelist "com.contorra.golfpad"`

搞定了。如果你正确输入命令，你不会看到错误或任何东西。现在你喜欢的 app 可以在安卓 8.0 奥利奥继续无限制使用 GPS 定位了！

### 结论

如前所述，我们在这里所做的只是简单地使用 ADB 命令，这是开发人员用来测试他们的应用程序的。相反，我们用它来挑选我们希望在后台使用 GPS 的应用程序。这不是我们第一次将开发者命令用于意想不到的目的，也绝对不会是最后一次！

如果你遇到了这样一个你认为会影响到许多其他人的问题，请随时通过我的作者页面上列出的我的[电子邮件或者通过](https://www.xda-developers.com/author/mishaalrahman/) [Reddit](https://www.reddit.com/user/MishaalRahman/) 上的私人消息联系我。我不回应技术支持问题，但如果你发现一些值得研究的东西，我一定会回应！如果你觉得这类教程很有趣，那么我推荐你关注我们的[教程 RSS feed](https://www.xda-developers.com/category/tutorials/feed/) 或者下载 XDA 实验室的应用程序。