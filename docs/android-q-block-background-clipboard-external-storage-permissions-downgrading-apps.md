# Android Q 将通过新功能更好地保护您的隐私

> 原文：<https://www.xda-developers.com/android-q-block-background-clipboard-external-storage-permissions-downgrading-apps/>

Android 的每个新版本都有新的功能，这意味着 Android 需要新的权限来访问这些功能。我在 Android Q 的框架中发现了许多新的权限(我不会在本文中全部介绍，因为其中许多并不有趣)。我发现的一些权限没有任何描述，但是它们的名称是不言自明的。让我们深入讨论 Android Q 中新的幕后隐私增强功能，以及我发现的其他一些有趣的功能。

*特别感谢 PNF 软件公司为我们提供了使用 [JEB 反编译器](https://www.pnfsoftware.com/?aid=xdadev)的许可。JEB Decompiler 是一款针对 Android 应用的专业级逆向工程工具。*

### 阻止后台剪贴板访问

你知道吗[Android 中的每个应用程序都可以读取你的剪贴板](https://www.xda-developers.com/stop-apps-reading-android-clipboard/)，而且你不需要授予他们运行时权限来这样做。许多人可能会复制敏感信息，如用户名、密码、地址等。所以任何应用程序都很容易在后台抓取这些数据。这就是为什么像 [KeePass](https://www.xda-developers.com/host-your-own-cross-platform-password-manager-with-keepass/) 这样的许多密码管理应用程序都有自己的键盘，你可以用来绕过 Android 剪贴板管理器。在你复制和粘贴任何东西后，密码管理器应用程序通常会为你清除剪贴板。Android 应用程序需要读取剪贴板的原因是，如果没有它，它们不能从剪贴板接受任何文本，这意味着你不能粘贴你复制的任何文本。谢天谢地，Android Q 正在寻求改变这种状况。

添加了一个名为“`READ_CLIPBOARD_IN_BACKGROUND`”的新权限，听起来就像它所说的那样:限制哪些应用程序可以在后台读取剪贴板。此权限的保护级别为“签名”，这意味着只有 OEM 签名的应用程序才能被授予此权限。

```
 <permission android:name="android.permission.READ_CLIPBOARD_IN_BACKGROUND" android:protectionLevel="signature"/> 
```

### 支持降级应用？

你有没有在 Google Play 上为一个应用安装了更新，然后马上后悔的经历？有时，开发人员会推出一个他们没有预料到的更新，但是一旦更新被推出并安装，做任何事情都为时已晚。开发人员必须快速发布热修复程序，用户要么需要停止使用该应用程序，直到发布更新，要么卸载该应用程序并下载旧版本。除非你有一个装有类似 [TitaniumBackup](https://www.xda-developers.com/titanium-backup-v8-1-0-adds-support-for-oreo/) 的应用程序的根设备，否则没有办法降级应用程序，因为 Android 的软件包管理器会阻止你安装旧版本的应用程序。这样做有一个很好的理由，因为如果应用程序的数据没有被清除，安装旧版本的应用程序可能会导致损坏，或者如果旧版本容易出现安全漏洞，可能会使用户面临危险。

虽然我们不确定谷歌是否会允许用户将应用回滚到旧版本，但我们确实在 Android Q 中发现了几个权限和命令，表明这是可能的。首先，新增的“`PACKAGE_ROLLBACK_AGENT`”和“`MANAGE_ROLLBACKS`”权限，提示预装市场 app 可以代理管理应用版本回滚。前者的权限是“签名”，而后者是“签名”之上的“安装程序”，因此这意味着只有平台签名的应用程序才能安装应用程序(通常只有包管理器、谷歌 Play 商店或其他第三方应用程序商店，取决于设备)才能使用这些权限。增加了两个新的受保护的广播意图:“`PACKAGE_ENABLE_ROLLBACK`”和“`PACKAGE_ROLLBACK EXECUTED`”这些广播不能由第三方应用程序发送，可能旨在让受影响的应用程序知道它何时被降级(很像应用程序在更新时被告知的方式，让它们有机会在下次启动时显示一些消息。)最后，一个新的标志被添加到了“`pm install`”shell 命令中。这个名为“`--enable-rollback`”的标志可以让你将应用程序回滚到早期版本。不过，我不能让它工作。

```
 <protected-broadcast android:name="android.intent.action.PACKAGE_ENABLE_ROLLBACK"/>
<protected-broadcast android:name="android.intent.action.PACKAGE_ROLLBACK_EXECUTED"/>
<permission android:name="android.permission.PACKAGE_ROLLBACK_AGENT" android:protectionLevel="signature"/>
<permission android:name="android.permission.MANAGE_ROLLBACKS" android:protectionLevel="installer|signature"/> 
```

### 保护外部存储上的文件

Android 中的数据存储包括“内部存储”(/数据排除/数据/媒体)和“外部存储”(/数据/媒体和任何安装的 SD 卡或 USB 驱动器)。apk 及其最敏感的数据存储在内部存储器中，而任何共享媒体如文档、图像、视频等。存储在外部存储器中。默认情况下，应用程序只能读写外部存储中的单个目录:/data/media/[user]/Android/data/[package _ name]。(要了解更多关于这种行为的信息，我推荐你阅读我在 Android Oreo 上发表的关于 sdcardfs 的[文章。)一旦用户授予应用程序外部存储权限组(`READ_EXTERNAL_STORAGE`或`WRITE_EXTERNAL_STORAGE`)下的任何权限，应用程序就可以读取或写入外部存储中的任何文件。这是有问题的，因为当你只是想让一个应用程序读取或写入某些文件时，你就授予了它获取大量关于你的数据的能力。为了解决这个问题，谷歌似乎要在 Android Q 中引入几个新的外部存储相关权限。这些权限将限制以下功能:](https://www.xda-developers.com/diving-into-sdcardfs-how-googles-fuse-replacement-will-reduce-io-overhead/)

*   从媒体中读取位置的能力。(可能默认阻止对图像元数据的访问。)
*   能够访问音乐文件。
*   访问照片的能力。
*   能够访问视频。

对于在 Android Q 更新之前已经拥有`READ_EXTERNAL_STORAGE`或`WRITE_EXTERNAL_STORAGE`权限的应用程序，他们将获得新的*读取*权限，而不是新的*写入*权限。例如，一个已经被用户授予了`READ_EXTERNAL_STORAGE`权限的应用将被自动授予`READ_MEDIA_IMAGES`权限，而不是`WRITE_MEDIA_IMAGES`权限。

### 来自 Android Q 框架的相关字符串-res

```
 <string name="permgroupdesc_aural">access your music</string>
<string name="permgrouplab_visual">Photos &amp; Videos</string>
<string name="permgrouprequest_aural">Allow &lt;b>%1$s&lt;/b> to access your music?</string>
<string name="permgroupdesc_visual">access your photos &amp; videos</string>
<string name="permgrouplab_activityRecognition">Activity recognition</string>
<string name="permgrouplab_aural">Music</string>
<string name="permdesc_videoRead">Allows the app to read your video collection.</string>
<string name="permdesc_videoWrite">Allows the app to modify your video collection.</string>
<string name="permdesc_imagesRead">Allows the app to read your photo collection.</string>
<string name="permdesc_imagesWrite">Allows the app to modify your photo collection.</string>
<string name="permdesc_audioRead">Allows the app to read your music collection.</string>
<string name="permdesc_audioWrite">Allows the app to modify your music collection.</string>
<string name="permlab_audioRead">read your music collection</string>
<string name="permlab_audioWrite">modify your music collection</string>
<string name="permdesc_mediaLocation">Allows the app to read locations from your media collection.</string>

the ability to <em>read</em> new typed permissions in the Q release; they
won't gain the ability to <em>write</em> that content. -->

<split-permission name="android.permission.READ_EXTERNAL_STORAGE"
targetSdk="10000">
<new-permission name="android.permission.READ_MEDIA_AUDIO" />
<new-permission name="android.permission.READ_MEDIA_VIDEO" />
<new-permission name="android.permission.READ_MEDIA_IMAGES" />
</split-permission>

<split-permission name="android.permission.WRITE_EXTERNAL_STORAGE"
targetSdk="10000">
<new-permission name="android.permission.READ_MEDIA_AUDIO" />
<new-permission name="android.permission.READ_MEDIA_VIDEO" />
<new-permission name="android.permission.READ_MEDIA_IMAGES" />
</split-permission> 
```

### 后台位置访问的回归

Android Oreo 和 Android 9 Pie 在保护用户隐私方面向前迈出了一大步，但一些用户认为谷歌走得太远了。可以被认为是特征回归的一个这样的区域是在[背景位置访问](https://www.xda-developers.com/android-oreo-background-location-whitelist/)中。Android Oreo 和更高版本中的位置访问如果没有完全关闭后台运行的应用程序，也会受到严重限制，因此如果应用程序想要持续轮询设备的位置，它们需要处于前台或运行前台服务。这阻止了应用程序在后台监视你的位置，但也阻止了用户在后台使用应用程序绘制自己的位置。这是我们在另一篇文章中提到的问题，看起来谷歌正在 Android Q 中添加一个新的权限，以解决这些开发者和用户的担忧。

在 Android Q 中，增加了一个新的权限，允许应用程序后台访问设备的位置。对用户的权限描述警告说，“应用程序将始终可以访问该位置，即使你不使用该应用程序。”该权限可以被授予“除了近似或精确位置”权限之外的权限，因此应用程序“可以在后台运行时访问该位置”相比之下，粗略定位权限只能根据手机信号塔或 Wi-Fi 网络等网络来源来获取您的位置，但前提是应用程序位于前台。

### 来自 Android Q 框架的相关字符串-res

```
 <string name="permgroupbackgroundrequest_location">Always allow &lt;b>%1$s&lt;/b> to access this device’s location?</string>
<string name="permgroupbackgroundrequestdetail_location">The app will always have access to the location, even when you’re not using the app.</string>
<string name="permdesc_accessBackgroundLocation">If this is granted additionally to the approximate or precise location access the app can access the location while running in the background.</string>
<string name="permdesc_accessCoarseLocation">This app can get your location based on network sources such as cell towers and Wi-Fi networks, but only when the app is in the foreground. These location services must be turned on and available on your phone for the app to be able to use them.</string>
<split-permission name="android.permission.ACCESS_FINE_LOCATION"
targetSdk="10000">
<new-permission name="android.permission.ACCESS_BACKGROUND_LOCATION" />
</split-permission>

<split-permission name="android.permission.ACCESS_COARSE_LOCATION"
targetSdk="10000">
<new-permission name="android.permission.ACCESS_BACKGROUND_LOCATION" />
</split-permission> 
```

### 身体活动识别

Android Q 增加了一个新的权限，允许应用程序“识别你的身体活动”这在技术上并不新鲜，因为它已经是 Google Play 服务的一部分，但这可能意味着 Google 将把许可从 Play 服务中分离出来。鉴于 Google Play 服务在提供 Android 核心功能方面的不可或缺性，很高兴看到它的一些权力回归 AOSP。

```
 <string name="permgroupdesc_activityRecognition">recognize activity</string>
<string name="permgrouprequest_activityRecognition">Allow &lt;b>%1$s&lt;/b> to recognize your physical activity?</string>
<string name="permdesc_activityRecognition">This app can recognize your physical activity.</string> 
```

* * *

要了解更多 Android Q 新闻，请查看我们的[标签](https://www.xda-developers.com/tag/android-q/)，其中包含按日期排序的最新新闻。我们最近发表了一篇文章，其中有很多证据指向谷歌正在研究在 Android Q 中支持类似 Face ID 的面部认证硬件的[。我们也有一个泄露的 Android Q 版本](https://www.xda-developers.com/android-q-face-id-rumor/)(甚至还有一个视频)的[早期实践，你应该在这里检查一下。我们将发布更多我们从这个早期 Android Q 版本中获得的发现，敬请关注。](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)