# 如何将 YouTube 应用程序中的任何视频/播放列表发送到您的 Google Home

> 原文：<https://www.xda-developers.com/how-to-cast-any-video-from-the-youtube-app-to-your-google-home/>

与任何谷歌新产品打交道时，最令人沮丧的地方之一是缺乏人们会认为是显而易见的功能。

那些已经购买了 Google Home 的人可能会很兴奋，因为这款设备可以充当 Google Cast 接收器，使你能够在智能手机上选择你最喜欢的歌曲，并开始在 Google Home 上播放。但是有一个应用程序已经失去了对谷歌主页的支持，这就是 Android 应用程序的官方 YouTube。

似乎没有任何技术障碍阻止 Google Home 播放 YouTube 视频的音频——毕竟，这个完全相同的功能**存在于桌面 YouTube 页面上。**但是，当你试图在智能手机上浏览同一视频时，你会注意到在谷歌主页上播放的选项明显不见了。

虽然我们只能猜测为什么 Android 应用程序中缺少这一看似显而易见的功能(也许是为了推动用户使用 YouTube 音乐——碰巧的是，它允许你转换到 Google Home ),但我们不能肯定为什么它不在那里。YouTube 上有很多内容，只听音频更好，但 YouTube 音乐上没有这些内容，所以我们想找到一种方法来解决这个问题。

虽然从技术上来说，可以通过进入 Google Home 应用程序并选择边栏中的“播放屏幕/音频”选项来播放智能手机上生成的任何和所有音频，但我个人不喜欢这个选项，因为它要求你每次想播放视频时都要手动启用这个选项，还要求你的手机继续播放视频，这使你无法使用其他应用程序。因此，我想到了一个更干净的解决方案，它利用了 Google Home 的原生 Google Cast 功能，但不需要你的手机被扣为人质。

* * *

## 将任何视频从 YouTube 应用程序上传到 Google Home

这个把戏背后的想法很简单。我们将把 YouTube 视频或播放列表 URL 发送到 Google Home，这样它就可以独立处理播放。为此，我们将利用两个不同的 Tasker 插件:AutoShare 和 AutoCast。AutoShare 将允许我们从 **Android 的内置共享菜单**中**共享 YouTube 视频/播放列表的 URL，而 AutoCast 将通过 Google Cast 协议**将该链接发送到 Google Home，这样它就可以开始播放了。在谷歌最终更新 YouTube 应用程序以支持向谷歌主页发布内容之前，这是最干净、最简单的选择。这是怎么做的。

我们需要做的第一件事是设置 AutoShare 和 AutoCast。打开自动共享，确保“自动共享设置”下面的**自动共享命令**被**选中**然后，点击**管理命令**。现在，您应该进入命令创建屏幕。在顶部，点击 **+** 图标创建一个新命令。把它命名为 **Cast to Home。** AutoShare 会要求你给命令一个图标。使用一个“内置”图标或者选择任何你喜欢的图标——这真的没关系。

一旦你做到了这一点，下一步我们将继续设置自动成本。打开 AutoCast 应用程序，点击**管理演职人员设备。**点击顶部的 **+** 图标，等待 AutoCast 检测到你的 Google Home。将您喜欢的 Google Home 设备添加到列表中。如果您的 Google Home 设备没有出现，请仔细检查您使用的是 AutoCast 的测试版，因为稳定的 Play Store 版本还不支持 Google Home！

现在，我们将通过 Tasker 连接这两个插件。这里是任务的描述，供那些对 Tasker 比较了解的人参考。如果您不熟悉 Tasker，请继续阅读分步说明。

```
 Profile: Home - Play Youtube Audio (156)
Event: AutoShare [ Configuration:Command: Cast to Home
Sender: all
Subject: all
Text: all
Image: all ]
Enter: Anon (157)
A1: AutoCast Best Guess [ Configuration:Cast Device: Bedroom Home
Value to Cast: %astext Timeout (Seconds):0 ] 
```

打开 Tasker，点击右下角的 **+** 图标，创建一个新的**档案**。点击**事件**->-**插件- >自动共享**，然后在弹出时再次点击自动共享。点击铅笔图标，调出自动共享配置。在**命令过滤器**下，选择 **Cast to Home** ，这是我们之前创建的命令。按下**复选标记**图标，然后点击左上方的返回箭头退出配置文件配置。

接下来，将要求您命名一项任务。你可以选择命名，也可以不命名，都无所谓。点击复选标记进入任务创建屏幕。在屏幕底部中间，再次点击 **+** 图标，为该任务创建一个新动作。点击**插件- >自动预测- >自动预测最佳猜测。**点击铅笔图标打开 AutoCast 的配置屏幕。在 **Cast Device** 下选择你的 Google Home 设备。对于要转换为的**值，请键入 **%astext。**该变量将包含我们将从 YouTube 共享到 Google Home 的 URL。点击顶部的复选标记以完成编辑此操作，并返回到 Tasker 的主屏幕。**

你完了！就像我说的，这是一个相当简单的解决方案，因为它只需要在 Tasker 中运行一个动作。但是，您实际上是如何让它运行的呢？只需找到任何 YouTube 视频或播放列表 URL(无论是在网络上还是从 YouTube 应用程序中共享)，在 Android 的共享菜单中选择 **AutoShare 命令**，然后最后选择 **Cast to Home** ，让 AutoCast 在您的 Google Home 上开始播放。

您的 Google Home 设备应该会很快开始播放。播放列表将自动逐个循环播放每个视频。如果你想停止播放，你可以通过点击智能手机上的自动播放通知或使用常用的 Google Home 命令来强制停止播放。我更喜欢“嘿，谷歌，闭嘴。”而是每个人自己的。

* * *

## 在 Tasker 中导入配置文件

和往常一样，我们提供了一个链接，可以让那些只想导入并开始使用的人下载这个概要文件。为了导入此配置文件，首先从下面的链接下载. prf.xml 文件。将其保存在内部存储器的任何位置。打开 Tasker，在首选项中禁用初学者模式。然后，回到主屏幕，长按“个人资料”轻触顶部。一个弹出窗口应该显示一个“导入”配置文件的选项。点击它，浏览到保存 XML 文件的位置，并选择要导入的文件。请注意，导入此配置文件仍需要您设置 AutoShare 和 AutoCast，并且您还需要编辑“AutoCast Best Guess”操作下的“Cast Device ”,以便它将指向您的特定 Google Home。

[**从 AndroidFileHost 下载“Cast to Google Home”配置文件！**](https://www.androidfilehost.com/?fid=745425885120708473)

* * *

如果这对你有用，请在下面的评论中告诉我们！