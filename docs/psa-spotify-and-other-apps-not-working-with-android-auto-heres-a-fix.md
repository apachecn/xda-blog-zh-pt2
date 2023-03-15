# PSA: Spotify(以及其他应用)无法与 Android Auto 兼容？这里有一个解决办法。

> 原文：<https://www.xda-developers.com/psa-spotify-and-other-apps-not-working-with-android-auto-heres-a-fix/>

对于那些有幸拥有一辆内置 Android Auto integration 的汽车的人来说，你们中的一些人可能在试图让 Spotify 等某些音乐应用程序工作时遇到了一个相当恼人的问题。它[只是](https://community.spotify.com/t5/forums/v3_1/forumtopicpage/board-id/spotifyandroid/thread-id/53870/page/1) [拒绝](https://forum.xda-developers.com/galaxy-s8/help/s8-android-auto-spotify-t3593577)到[在仪表盘上显示](https://forums.androidcentral.com/android-auto/634420-i-have-car-android-auto-but-i-cannot-find-spotify-only-has-google-play-music.html)。为什么会发生这种情况，对此能做些什么？我们有答案。

* * *

### 为什么会这样？

你可以把这归咎于 Android Auto 应用程序。使用[getInstallerPackageName()](https://forums.androidcentral.com/android-auto/634420-i-have-car-android-auto-but-i-cannot-find-spotify-only-has-google-play-music.html)方法，Android Auto 应用程序在允许应用程序显示在 Android Auto 仪表板中之前，会检查应用程序的安装源。不幸的是，这意味着如果你从谷歌 Play 商店以外的地方(比如通过 XDA 实验室或 APKMirror)下载 Spotify 应用程序，那么 Android Auto 集成将停止工作(尽管你仍然可以通过蓝牙收听 Spotify，但这样做违背了 Android Auto 的整个目的)。

*左:从 Play Store 安装的 Spotify。*

*右图:XDA 实验室安装的 Spotify。*

*注:上面截图显示的安装细节是在 Android 7.0 牛轧糖中添加的。*

* * *

### 对此能做些什么呢？

幸运的是，通过使用 ADB 命令，我们仍然可以侧加载 Spotify 应用程序(或任何其他应用程序),同时告诉系统将其视为从谷歌 Play 商店安装的。

ADB 是 Android Debug Bridge 的缩写，是一个为开发人员设计的工具，用于与他们的智能手机进行交互，以便调试设备。然而，它有许多有用的特性，我们也可以利用。以下是如何设置和使用 ADB:

1.  从本文中的[链接下载适用于您特定操作系统的 ADB 二进制文件。](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)
2.  将 zip 文件解压缩到一个可以快速访问的文件夹中。
3.  在您的手机上，进入设置并点击关于手机。找到内部版本号，点击 7 次以启用开发者选项。
4.  现在进入开发者选项，找到 USB 调试。启用它。
5.  将手机插入电脑，从“仅充电”模式切换到“文件传输(MTP)”模式。
6.  在您的计算机上，浏览到您解压缩 ADB 二进制文件的目录。
7.  从 XDA 实验室或你选择的任何地方下载最新的 Spotify APK 文件(或任何其他不适合你的应用程序)，并将该文件另存为“spotify.apk”(或其他容易记住的名称，取决于应用程序)。还记得你把 APK 的文件保存在哪里吗？
8.  接下来，在您的计算机上打开该目录下的命令提示符。对于 Windows 用户，只需按住 shift 然后右键单击，您将看到一个“在此打开命令提示符”选项。
9.  一旦进入命令提示符/终端，输入以下命令:`adb devices`
10.  您将看到系统正在启动 ADB 守护程序。如果这是您第一次运行 ADB，您将在手机上看到一个提示，要求您授权与计算机的连接。批准吧。
11.  现在，如果您重新运行 adb 设备命令，终端将打印您的设备的序列号。如果是这样，那么你已经准备好继续前进了。
12.  输入以下命令:`adb shell`
13.  最后，输入这个最后的命令来安装包:`pm install -i "com.android.vending" -r /sdcard/path/to/spotify.apk`

-i 命令指定安装源，而-r 命令指定不应覆盖以前安装的数据。命令的“路径/到”部分应该替换为您保存 spotify APK 的实际位置。例如，如果它位于下载文件夹中，那么/sdcard/Download/spotify.apk 将是您要输入的内容。最后，如果你在使用另一个应用程序时遇到问题，只需将“spotify.apk”替换为你试图下载的 apk 文件的名称。

一旦输入命令，如果成功安装了应用程序，它将返回“成功”。如果你运行的是 Android Nougat 及以上版本，那么你只需打开应用程序的设置页面，看看它是否正确指定了安装源。如果没有，那么您可以简单地运行这个命令来检查安装源:

`pm list packages -i`

在输出的某个地方，您会发现“`com.spotify.music`”包和它旁边的安装源包。如果它显示“`com.android.vending`”，那么你就设置好了。

*上图:从 Play Store 安装的 Spotify。*

*底部:从系统包管理器安装的 Spotify。*

希望这可以解决你在让 Spotify 或其他应用程序被 Android Auto 识别时可能遇到的任何问题。我不知道为什么 Android Auto 要求应用程序只能从谷歌 Play 商店安装，但这一行为让很多用户感到困惑。