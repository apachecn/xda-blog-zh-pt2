# 以下是如何立即试用 Android 消息的方法[Root]

> 原文：<https://www.xda-developers.com/try-android-messges-for-web-now/>

# 以下是如何立即试用 Android 消息的方法[Root]

期待已久的 Android 消息网络客户端即将推出。它适用于谷歌浏览器、火狐浏览器等等。下面是现在尝试的方法。

期待已久的 Android 客户端消息今天开始发布。它可以让你通过谷歌 Chrome、Mozilla Firefox、Opera、苹果 Safari 和微软 Edge 等网络浏览器从电脑上发送短信。它完全免费使用，支持表情符号，发送图像，同步信息，并通知你新的信息。web 客户端有一个漂亮的 Google Material 设计主题，甚至还有一个黑暗的主题。我们已经发布了一个关于[如何启用 Android Messages】的教程，这样你就可以从你的笔记本电脑或台式机上发送短信，但是如果你还没有收到该功能，并且渴望尝试一下，我们已经为你准备好了。以下是如何在任何基于](https://www.xda-developers.com/send-text-messages-pc-android-messages-for-web/) [**的**](https://www.xda-developers.com/root/) 安卓设备上强制启用该功能。

*截图鸣谢:XDA 认可开发商[quinny 899](https://forum.xda-developers.com/member.php?u=3563640)*

## 如何为 web 强制启用 Android 消息

*这些步骤的信用属于 XDA 认可的开发商[Quinn 899](https://forum.xda-developers.com/member.php?u=3563640)。*

1.  下载最新的 Android Messages 应用程序(版本 3.3.043。)如果你没有在谷歌 Play 商店上看到它，请从[这里](https://www.apkmirror.com/apk/google-inc/messenger-google-inc/messenger-google-inc-3-3-043-release/android-messages-3-3-043-xylophone_rc22_xxhdpi-arm64-v8a-phone-android-apk-download/)抓取它。
2.  从谷歌 Play 商店下载偏好设置管理器。
3.  打开首选项管理器，并在请求时授予其 root 访问权限。
4.  如果 Android Messages 像 Google Pixel 或 Android One 设备一样被预装为系统应用程序，请按右上角的三点菜单，然后选择“显示系统应用程序”
5.  查找“消息”
6.  左右滑动，直到找到“PhenotypePrefs.xml”
7.  搜索“多”
8.  将下面截图中以红色突出显示的两个首选项从“假”更改为“真”
9.  再次搜索“覆盖”并更改出现的两个首选项。
10.  **强制关闭**安卓消息。**暂时不要打开应用！**
11.  在 ADB shell 中，输入以下命令:
    1.  `adb shell`
    2.  `su`
    3.  `am start -n com.google.android.apps.messaging/com.google.android.apps.messaging.ui.ditto.DittoActivity`
12.  或者，如果您安装了类似于 [Material Terminal](https://play.google.com/store/apps/details?id=yarolegovich.materialterminal) 的终端模拟器应用程序，那么您可以输入以下命令:
    1.  `su`
    2.  `am start -n com.google.android.apps.messaging/com.google.android.apps.messaging.ui.ditto.DittoActivity`
13.  现在您可以[按照这些步骤](https://www.xda-developers.com/send-text-messages-pc-android-messages-for-web/)完成设置。

我已经通过我的谷歌 Pixel 2 XL 在 Android P 上运行了大约一个小时的 Android Messages for web client。Quinny899 报告连接在他身上关闭，所以你的里程可能会有变化。这种方法是在 web 客户端尝试所有功能的快速方法。我确信这个特性很快会广泛推广，所以我不会依赖这种方法来访问未来的 web 客户端。