# jOnePlus 工具让你定制 OxygenOS 并解锁隐藏功能[XDA 聚焦]

> 原文：<https://www.xda-developers.com/customize-oxygenos-unlock-hidden-features-joneplus-tools/>

随着最近发布的 Android Oreo 和 Oxygen OS 的公开测试版，用户现在有足够的时间来玩它，并发现他们喜欢和不喜欢的东西。如果你想发现更多隐藏的功能或进一步定制 OxygenOS，我们找到了一款可以做到这一点的应用。该应用名为 **JOnePlus Tools** ，让你**定制 OxygenOS 4+并解锁 OnePlus 3、OnePlus 3T 和 OnePlus 5** 上的隐藏功能。该应用程序有一些有用的功能，其中一些需要 root 用户，一些不需要。

如果你有根权限，那太好了！你不需要做任何额外的事情来设置 jone plus Tools——只要在你第一次启动它的时候授予它超级用户权限。如果您没有 root 访问权限，那么某些功能将仅限于您使用，您必须通过 ADB 手动授予应用程序 WRITE_SECURE_SETTINGS 权限。我们有一个关于[建立 ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的教程，您可以参考。一旦你设置好 ADB，你所要做的就是输入下面的命令让应用程序开始工作:

```
 adb shell pm grant net.jroot3d.joneplustools android.permission.WRITE_SECURE_SETTINGS 
```

现在您可以使用 jOnePlus 工具并解锁 OxygenOS 的隐藏功能！这里列出了可用的特性，其中一些我们在以前的文章中已经介绍过了(但是在这里更容易访问，因为它被打包在一个应用程序中。)我们将通过在末尾添加(root)来标记需要 ROOT 的特性。

您可以从谷歌 Play 商店免费下载 jOnePlus 工具。如果你喜欢开发商的作品，可以考虑捐赠给他们。

如果您有兴趣了解 jOnePlus 工具中的一些特性是如何工作的，这里是它发送的 shell 命令的分类。

这是最初拉下通知阴影后可以访问的切换次数。您可以看到的默认数量是 6，但是您可以简单地运行以下命令来编辑您的快速设置单幅图块数量。

```
 adb shell settings put secure sysui_qqs_count N 
```

其中 N 是您想要的快速图块的数量。

### 自定义快速设置磁贴强调颜色

有些人会说，在 Oxygen 操作系统的模式下，强调颜色的选择非常有限，但谢天谢地，用户可以通过使用一个简单的 adb 命令轻松地解决这个问题！

```
 adb shell settings put system oem_black_mode_accent_color  
```

其中“黑色模式”是指显示设置中的 OxygenOS 深色主题，“白色模式”是指 OxygenOS 浅色主题。要获得您想要的颜色，请用您想要的颜色的十六进制数替换 x。可以用[这个网站](http://htmlcolorcodes.com/)算一下！一旦你做了更改，去显示设置并重新选择你当前的主题，以使更改生效。

### 单色模式

单色模式可通过 adb 启用。我们不确定它为什么有用，但是你可以。

```
 adb shell settings put secure accessibility_display_daltonizer_enabled 1 
```

### 自动电话录音

另一个有点有用的功能，你可以通过亚行是自动电话录音！所有录音都以 aac 格式存储在/storage/emulated/0/Record/phone Record 中。

```
 adb shell settings put global op_voice_recording_supported_by_mcc 1 
```

### 更改虚拟屏幕分辨率

这实际上并没有改变你设备的显示分辨率，但是它确实让安卓*认为你在不同的分辨率下运行。这可能是有用的，因为它允许你欺骗游戏降低或增加图形，因为他们认为你正在运行的分辨率不是你的设备。*

`wm size WxH`

其中 W 是水平分辨率，H 是垂直分辨率。例如，将分辨率更改为在 4K 运行需要输入 2160x3840。

* * *

所以现在你已经知道了你的一加设备是多么的可定制，要么去看看应用程序，要么去看看上面的文章或 adb 命令！你可以做很多事情和改变，所以我们建议如果你使用的是 Oxygen OS 4 或者更高版本的话，把它们都尝试一下！