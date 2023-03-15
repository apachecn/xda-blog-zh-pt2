# 这就是谷歌 Pixel 2 的“现在播放”功能的工作原理

> 原文：<https://www.xda-developers.com/how-google-pixel-2-now-playing-works/>

本月早些时候，谷歌正式推出了 Pixel 2 和 Pixel 2 XL T1，这两款手机配备了一项名为“正在播放”的新功能。该功能会在后台监听音乐，如果它识别出其中一首歌曲，就会在锁定屏幕上显示歌曲名称和艺术家。当该功能最初宣布时，没有太多关于它的公开信息。不过，今天我们有了更多关于谷歌 Pixel 2 和 Pixel 2 XL 智能手机独有的 Now Playing 功能如何工作的细节。

我们[最初认为现在播放功能利用了一种叫做“ambient sense”](https://www.xda-developers.com/google-pixel-2-now-playing-ambientsense-battery-drain/)的技术来检测并通知用户当前正在播放的歌曲。这种怀疑源于威瑞森谷歌 Pixel 2 机型上预装的 Pixel Ambient Services 应用程序的包名。由于预装在/system/priv-app 中的 APK 的名字叫做“AmbientSense ”,并且关于该技术的细节似乎也匹配，我们觉得这是一个公平的假设。然而，谷歌伸出手告诉我们，现在播放功能不是基于该技术。

我们跟进了谷歌给我们的声明，以了解更多关于 Now Playing 的细节。一位谷歌发言人后来联系了我们，提供了关于该功能的更多细节，称离线歌曲识别数据库包含一个数十首歌曲的列表，虽然他们没有给出确切的数字，但承诺它是高端的。这意味着我们从威瑞森 Pixel 2 型号中提取的[数据库并不代表现在播放功能可以识别的所有歌曲。](https://www.xda-developers.com/google-pixel-2-now-playing-song-list/)

我们进一步从我们的联系人那里了解到,“正在播放”功能只有在听到音乐时才会被激活。如果 Pixel 2 检测到正在播放的音乐(使用软件、硬件和机器学习的组合)，它将在手机上的数据库中查找音频指纹，然后向您显示歌曲名称或艺术家。顺便说一句，这个数据库是**每周**更新的音乐，并且是基于来自 Google Play 音乐目录的**最受欢迎的歌曲。它还根据市场进行了本地化，因此，该数据库不会针对用户的 Google Play 音乐帐户进行个性化设置。**

[*VentureBeat*](https://venturebeat.com/2017/10/19/how-googles-pixel-2-now-playing-song-identification-works/) 独立联系谷歌，以了解一些关于正在播放功能的更多细节。音频采样每 60 秒进行一次**，以试图节省电池寿命**(而不是一直运行)，因此有时您会在屏幕上看到最后播放的歌曲。他们还了解到，数据库更新仅通过 WiFi 进行，并且仅替换您的区域特定数据库的过时部分。