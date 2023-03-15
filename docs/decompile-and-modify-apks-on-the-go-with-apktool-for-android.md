# 使用 APKTool for Android 随时随地反编译和修改 apk[XDA 聚焦]

> 原文：<https://www.xda-developers.com/decompile-and-modify-apks-on-the-go-with-apktool-for-android/>

APKTool 是 XDA 资深会员 [ibotpeaches](https://forum.xda-developers.com/member.php?u=3924617) 开发的一款功能强大的软件。该工具允许你[逆向工程 APK 文件](https://ibotpeaches.github.io/Apktool/)，允许你解码资源文件，这样你可以修改它们，然后重新编译应用程序。

很难确定这个工具对 Android 社区有多重要，但是它的一些更受欢迎的用例列表应该会让你很好地理解为什么这个工具和它的开发者受到如此高的重视。APKTool 用于将应用程序[移植到以前不支持的设备](https://www.xda-developers.com/google-camera-v4-2-from-the-pixel-system-dump-is-now-available-for-all-nougat-devices/)，[主题化一些你最喜欢的应用程序](https://forum.xda-developers.com/showthread.php?t=2283828)，查看 APK 文件的字符串以了解[在未来的更新中可能会有什么](https://www.xda-developers.com/tag/apk-teardown/)，并为应用程序提供[翻译。另一方面，它也可以被恶意地用于隐藏和分发恶意软件，或者反过来用于 Kali Linux 中的 Android 应用渗透测试。](https://forum.xda-developers.com/android/apps-games/app-fleksy-language-packs-t3548347)

APKTool 自最初发布以来就可以在 Linux/GNU 发行版和微软 Windows 操作系统上使用，但是 Android 对该工具的支持已经消失了很长时间。对 Android 设备的有限支持持续了几个月，但对工具的[官方 Android 版本的更新在 2013 年停止，使得它无法对任何现代 APK 文件进行逆向工程。然而，一个名为](https://code.google.com/archive/p/apktool/downloads) [Andro Black](https://www.androidfilehost.com/?w=profile&uid=24562946973631820) 的开发者已经独立发布了用于 Android 的 APKTool 的[更新版本，因此你可以在任何基于**的 Android 设备**上随时反编译和修改 APK 文件。](https://www.androidfilehost.com/?w=files&flid=149532)

XDA-开发者不允许使用 APKTool 进行任何形式的应用盗版。使用 APKTool 的原因有很多，但出于盗版目的修改应用程序不应该是其中之一。

* * *

该应用程序本身有点粗糙，因为它包含一些拼写错误和一个相当错误的主题切换器，但老实说，我不太在乎，因为 Android 上没有其他工具可以完成这一功能。APKTool for Android 做的正是它的老大哥 PC 版本所做的——逆向工程 APK 文件。你可以直接在手机上反编译和重新编译应用程序，如果你想快速修改 APK 的资源而不需要在你的桌面前，这是很有用的。这对于那些经常编辑 APK 文件并把它发送到他们的设备上进行实时测试的人来说尤其有用。但是要注意，APKTool 应用程序不能用于实际编辑反编译的文件，因为你需要在你的设备上安装一个文本编辑器。

设置菜单允许你改变应用程序的主题，如前所述，但更重要的是你可以选择 AAPT 和 APKtool 版本，你想使用反编译 APK 文件。在设置中还有一个“root”的复选标记，没有这个复选标记你就不能正确编译应用程序(默认情况下它是不被选中的。)

要使用应用程序，您有两个菜单，一个显示在短按上，另一个显示在长按上。如下所示的点击菜单显示了你可以用来处理 APK 文件的功能，主要的有*反编译所有*和*符号*。这里还有许多其他的函数，但是如果您以前有使用 APKTool 的经验，这些函数对您来说应该不会陌生。

反编译一个 APK 后，你可以浏览它的内容，只需点击带有 APK 名字的文件夹来显示它的内容。点击一个文件将加载默认的 Android 行为，并询问你想用哪个应用程序打开该文件，此时如果你试图修改一个资源，你将使用你选择的文本或图像编辑器。

一旦您完成了对 APK 的修改，您也可以从 APKTool 应用程序内部安装您修改过的版本。长按菜单允许您删除/重命名文件和文件夹，但它也是上下文感知的，所以当您长按一个文件夹时，您将获得选项来编译所有的资源和 smalis 到一个 APK 文件再次。

我发现该工具对于快速更改现有应用程序非常有用，因为我能够反编译现有应用程序，更改 strings.xml 文件，并重新编译应用程序以查看更改。不过，该工具执行这些操作的速度取决于您的设备。在我的谷歌 Nexus 6P 上，反编译一个 APK 文件需要大约 2 分钟，而重新编译一个 APK 文件需要大约 2 分钟，所以我个人不希望经常在手机上使用 APKTool。

在你的手机上处理 APK 文件并不是最直接的过程，但是 APKTool 工具使它可行。我不建议开发人员在他们的 Android 手机上专门修改 apk，因为它既慢又更难管理，但如果你拥有一台 Android 平板电脑，并且正在寻找一种更方便的方式来进行频繁的小修改并在实际设备上进行测试，那么 APKTool for Android 是你的最佳选择。

* * *

## 资源

[**在你的根安卓设备上安装 apk tool**](https://www.androidfilehost.com/?w=files&flid=149532)

[**在你的 Linux/Windows 设备上安装 apk tool**](https://ibotpeaches.github.io/Apktool/install)

[**顺着 XDA 的思路**](https://forum.xda-developers.com/showthread.php?t=1755243)

[**贡献给 APKTool 项目**](https://ibotpeaches.github.io/Apktool/contribute/)

[**在官方 Gitter 频道讨论 apk tool**](https://gitter.im/iBotPeaches/Apktool)

[**在官方 IRC 频道**](https://webchat.freenode.net/?channels=apktool) 讨论 APKTool