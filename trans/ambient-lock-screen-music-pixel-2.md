# 环境锁屏音乐是一个根应用程序，可以在 Pixel 2 的环境显示器上显示任何音乐

> 原文：<https://www.xda-developers.com/ambient-lock-screen-music-pixel-2/>

谷歌最新的 [Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 旗舰有一个令人敬畏的新功能，叫做“正在播放”。使用软件、硬件和机器学习的结合，Pixel 2 使用离线数据库[识别后台播放的数万首歌曲](https://www.xda-developers.com/how-google-pixel-2-now-playing-works/)。然后，它会将这些歌曲显示在手机的锁定屏幕上，一直显示，或者作为一个持续的通知。这个功能听起来有点噱头，但是在我自己使用后，我发现它真的很好用。话虽如此，这种功能并不是每个人都喜欢的，所以 XDA 认可的贡献者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 开发了一款名为 **Ambient Lock Screen Music** 的应用程序，它允许你**在你的设备上显示任何当前播放歌曲**的名称和艺术家，而现在播放的文本通常会出现在那里。

正如你在上面的视频中看到的，开发人员启用了应用程序，然后开始播放 Google Play Music 中的一首歌曲。当它们显示锁定屏幕时，您可以在底部看到当前播放的歌曲，而通常您会看到“正在播放”功能在识别歌曲时插入文本。

应用程序**仅在 Pixel 2/2 XL** 上工作，因为它发送一个意图，其对应的意图接收器仅在 Pixel 2 上的 SystemUIGoogle 应用程序中可用。此外，应用程序**需要 root 访问权限**才能运行。你可以通过下面的链接从 XDA 实验室下载应用程序。

[appbox xda com . Kieron Quinn . app . ambientlsmusic]

它不仅免费(T1)，而且完全不含广告(T3)。它支持显示几乎任何音乐应用程序的歌曲名称/艺术家，如 Google Play Music、Spotify、YouTube Red 等。您还可以将应用程序列入黑名单，禁止其在环境显示器上显示文本。最后，该应用程序甚至允许您双击环境显示屏上显示的文本来启动音乐应用程序。

我们应该注意，这并不一定会取代现在播放的功能，尽管它可能会与之冲突。如果与此同时启用了 Now Playing，并且您正在听音乐，而 Now Playing 正在主动检测一首歌曲，则无论哪个向 SystemUI 发送意图，最新的将显示在环境显示屏上。无论如何，现在播放仍然会显示一个通知，无论它检测到什么歌曲，所以如果你使用环境锁定屏幕音乐，你不会错过这个功能。

* * *

## 环境锁定屏幕音乐如何工作

### 意图

如前所述，该应用程序通过向 SystemUIGoogle 应用程序发送意图来工作。在 Quinny899 的应用中，这是负责发送意图的代码:

```
 Intent intent = new Intent("com.google.android.ambientindication.action.AMBIENT_INDICATION_SHOW").putExtra("com.google.android.ambientindication.extra.VERSION", 1).putExtra("com.google.android.ambientindication.extra.TEXT", broadcastString).putExtra("com.google.android.ambientindication.extra.TTL_MILLIS", time);
if(clickIntent != null)intent.putExtra("com.google.android.ambientindication.extra.OPEN_INTENT", clickIntent);
else if(packageName != null) intent.putExtra("com.google.android.ambientindication.extra.OPEN_INTENT", PendingIntent.getActivity(context, 1, context.getPackageManager().getLaunchIntentForPackage(packageName), 0));
intent.setPackage(pName);
context.sendBroadcast(intent, "com.google.android.ambientindication.permission.AMBIENT_INDICATION"); 
```

让我们分解一下。这个意图中的动作是“`com.google.android.ambientindication.action.AMBIENT_INDICATION_SHOW`”，它有几个可以随它一起发送的意图附加项。

第一个额外的是“`com.google.android.ambientindication.extra.VERSION`”，它目前只取整数值 1。下一个额外的是“`com.google.android.ambientindication.extra.TEXT`”，我们在这里设置想要在环境显示锁定屏幕上显示的字符串。第三个额外的是“`com.google.android.ambientindication.extra.OPEN_INTENT`”，它接受双击文本打开的 PendingIntent。Quinny899 设置 PendingIntent 以打开任何正在播放音乐的应用程序或`android.intent.action.MUSIC_PLAYER`的拾音器。

最后，为了发送这个意图，调用应用程序必须拥有权限“`com.google.android.ambientindication.permission.AMBIENT_INDICATION`”此权限被定义为 signature|privileged，这就是为什么此应用程序需要 root 访问权限。

如果您想自己测试，可以打开一个根终端或 ADB shell 会话，并输入以下命令:

```
 am broadcast -a com.google.android.ambientindication.action.AMBIENT_INDICATION_SHOW --ei com.google.android.ambientindication.extra.VERSION 1 --es com.google.android.ambientindication.extra.TEXT "hello world" 
```

这将在环境显示器上显示文本“hello world”。但是，它不允许您双击，因为该命令不设置 PendingIntent。

### 显示歌曲

该应用程序有两种方法来捕捉正在播放的歌曲。第一种是通过 MediaController，它需要将应用程序绑定为通知侦听器(尽管这实际上并不意味着应用程序正在拦截通知以读取当前播放的歌曲)。第二种是通过广播接收器，它不需要通知监听器(因此消耗更少的内存)，但兼容性较差，因为一些音乐应用程序不发送该应用程序设置的广播意图。

### 其他应用

使用同样的意图，您可以设置一个应用程序或 Tasker，将您想要的任何文本发送到环境显示。这打开了新的定制选项，完全取决于你想看到什么。例如，你可以用天气来代替音乐。