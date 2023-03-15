# 音频焦点修复口袋妖怪 Go(和其他应用程序)没有根

> 原文：<https://www.xda-developers.com/pokemon-go-audio-focus/>

尽管人气下降,《口袋妖怪 Go 》( Pokemon Go )( T1)仍有大量 T2 粉丝(T3)每天玩这款游戏。虽然游戏的大部分问题都与作弊有关，但是还有其他更小的问题困扰着现有用户。其中一个问题与 Android 中的音频焦点有关。喜欢在玩 Pokemon Go 时听音乐或播客的用户发现，当他们启动游戏时，音频播放会立即停止。这需要用户手动重启他们最喜欢的媒体应用程序的播放，如 Google Play Music、Spotify 或 PocketCasts。今天，我将向你展示如何阻止 Pokemon Go(或任何其他应用程序)窃取永久音频焦点- **无根**。

当 Pokemon Go 启动时，它会向系统请求音频焦点，这意味着相同音量流上的任何现有媒体播放都将被[回避](https://en.wikipedia.org/wiki/Ducking)。这里的问题是，Android 的音频焦点依赖于应用程序之间的荣誉系统。Android 并不挑选哪些应用程序应该优先获得焦点，相反，它依赖于应用程序根据需要请求和释放焦点。因此，因为 Pokemon Go 在启动时会请求音频焦点，所以其他应用程序无法阻止它接管媒体卷。

一些应用程序，如 Poweramp 或 T2 Podcast Addict 有实验性的设置来保持音频焦点，以防止其他应用程序窃取它，但显然许多媒体应用程序没有这样做。一些用户想出了他们自己的方法，通过使用 Tasker 配置文件来保持音频焦点，如果没有更好的方法，我可能会尝试这样做——但谢天谢地有。它涉及到使用一个隐藏的 ADB 命令来访问 Android 权限管理系统 appops 的命令行界面。只需一个简单的命令，你就可以阻止口袋妖怪 Go(或任何其他应用程序)再次获得音频焦点！

我们在这里使用的方法是针对没有运行任何定制 ROM 的普通用户。定制 ROM 用户，比如 LineageOS 上的用户，可以访问一个更强大的权限控制方法，让他们绕过对这个命令的需求。

* * *

## 停止口袋妖怪 Go 采取音频焦点-教程

1.  为你的[设备](https://developer.android.com/studio/run/oem-usb.html)下载然后安装 USB 驱动程序——很可能只有在 Windows 上才有必要。
2.  为您的操作系统下载 [ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/),并将文件解压到您电脑上的任意文件夹。
3.  在您的手机上，打开设置，然后找到“关于手机”选项。
4.  向下滚动找到“Build Number”值，点击 7 次，启用开发者模式。
5.  回到主菜单中的设置，进入开发者选项。
6.  在这里启用 USB 调试模式，如下图所示。
7.  将手机插入电脑，将手机的 USB 模式从“仅充电”模式改为“文件传输(MTP)”模式。
8.  回到 PC，导航到您提取 ADB 二进制文件的位置。
9.  在这个 ADB 目录中打开一个命令提示符。在 Windows 上，最简单的方法是按 Shift+右键。在上下文菜单中，选择“在此打开命令窗口”选项。Mac 或 Linux 用户，打开终端。
10.  输入以下命令:`adb devices`
11.  这将启动 ADB 守护程序。如果这是您第一次运行 ADB，您将看到一个提示，要求您授权连接。允许它。
12.  从步骤 10 重新运行命令，您将在输出中看到设备的序列号。如果是，继续下一步。如果没有，请重新安装您的驱动程序。
13.  (*可选*):如果你想限制 Pokemon Go 之外的某个应用有音频聚焦，那么安装[应用检查器](https://play.google.com/store/apps/details?id=com.ubqsoft.sec01)应用，找到该应用名称下列出的包。
14.  发送以下命令:`adb shell`
15.  然后执行这个命令:`cmd appops set <package> TAKE_AUDIO_FOCUS ignore`。例如，对于 Pokemon Go，命令将是:`cmd appops set com.nianticlabs.pokemongo TAKE_AUDIO_FOCUS ignore`<picture>![](img/a3dde588135f8a2af8ad1b925f9cadc1.png)</picture>

    例如:用于 Pokemon Go 的命令

    更新:如果以上命令对您不起作用，请尝试从命令中排除“cmd”。我一直听说，如果你运行的是 Android 6.0 棉花糖或更早的版本，这可能是需要的。

16.  只要你没有在窗口中得到一个错误消息，它应该已经工作了。恭喜你！现在 Pokemon Go 不会阻止 Google Play 音乐、Spotify、PocketCasts 或任何其他应用程序在它上面播放！

* * *

## 说明

正如开头提到的，我们使用命令行与 appops 接口，appops 是 Android 面向用户的处理应用权限的系统。默认情况下，用户可以通过设置 UI 切换的权限很少。某些自定义 rom(如带有隐私保护的 LineageOS)暴露了更多您可以限制的权限，但对于非 ROMs 用户，处理这些权限的唯一方法是通过命令行。

不管怎样，我们限制的特定权限是`android.permission.TAKE_AUDIO_FOCUS`，任何在`AndroidManifest.xml`文件中请求它的应用程序在安装时都会自动被授予。多亏了上面的 appops 命令，我们可以从 Pokemon Go 中取消这一权限，这意味着它不能再请求音频焦点，从而不能再阻止你手机上的其他音乐或播客应用程序播放。

虽然上面的教程是针对 Pokemon Go 用户的，但从技术上来说，你可以对任何其他 app 做同样的事情。只需在第 15 步中用你想要的任何其他应用程序修改包的名称。只是要小心，不要随意限制这种权限，因为谷歌有意隐藏这种权限，以免用户把事情搞砸。

在我们的[教程类别](https://www.xda-developers.com/category/tutorials/)中查看其他类似的优秀教程。通过 XDA 实验室应用程序了解最新消息。