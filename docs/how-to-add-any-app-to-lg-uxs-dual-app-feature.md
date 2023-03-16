# 如何将任何应用添加到 LG UX 的双应用功能中

> 原文：<https://www.xda-developers.com/how-to-add-any-app-to-lg-uxs-dual-app-feature/>

# 如何将任何应用添加到 LG UX 的双应用功能中

XDA 初级成员 zenith22 找到了一种方法，可以在运行 LG UX 皮肤的 LG 手机上的双应用空间内添加任何应用。继续阅读，了解更多信息！

LG UX 定制 Android 界面可能不是最受欢迎的 OEM 软件，但它确实包含一些有用的功能，如最新版本的桌面模式。LG 还提供了运行同一应用程序的不同实例的功能，这就是我们所知的应用程序克隆的概念。这个被称为“双应用”的特别功能可以在>设置下找到。默认情况下，韩国 OEM 只允许少数消息平台和社交媒体应用被克隆为双应用，但人们可以很容易地绕过这一允许列表。

事实证明，LG 的 Dual 应用程序在很大程度上类似于一加在 OxygenOS 中实现的[“并行应用程序”。在这两种情况下，都会创建一个隐藏的用户配置文件，以便安装应用程序的克隆实例，并将关联的应用程序数据与主用户配置文件分开。但是，LG UX 和 OxygenOS 的二级用户配置文件的配置文件 ID 是不同的。当一加将用户“999”用于并行应用程序时，LG UX 公司为此生成了 ID 为“98”的新用户配置文件。XDA 初级成员](https://www.xda-developers.com/add-any-app-oxygenos-parallel-apps-space-oneplus-phones/) [zenith22](https://forum.xda-developers.com/member.php?u=9943867) 已经[通过执行`adb shell pm list users`发现了](https://forum.xda-developers.com/lg-v60-thinq/how-to/lg-v60-install-app-dual-app-parallel-app-t4112393)这个重要的细节，同时修补了双应用程序部分。

现在我们有了用户配置文件 ID，在 LG 的双应用程序容器中安装您选择的任何应用程序都是轻而易举的事情。所需的步骤如下:

1.  [设置 ADB shell 访问](https://www.xda-developers.com/install-adb-windows-macos-linux/)。您可能需要将 LG 手机上的 USB 模式更改为“MIDI ”,以正确初始化 USB 调试。
2.  从可信来源下载所需应用程序的 APK 文件，将其克隆到您的电脑上。
3.  运行以下 ADB 命令:

    ```
     adb install  
    ```

4.  这将把应用安装到用户简档 98，即双应用的简档。
5.  为了让事情变得更简单，你可以尝试将[Aurora Store](https://forum.xda-developers.com/android/apps-games/galaxy-playstore-alternative-t3739733)安装到隐藏的“双应用”用户配置文件中。Aurora Store 是谷歌 Play 商店的一个非官方客户端，它允许你直接在双应用程序容器中安装应用程序。

* * *

**您在 LG 智能手机上使用 Dual App 的频率如何？请在下面的评论中告诉我们！**