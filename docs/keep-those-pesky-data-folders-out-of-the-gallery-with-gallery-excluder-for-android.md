# 使用 Android 图库排除程序将那些讨厌的数据文件夹从图库中清除出去

> 原文：<https://www.xda-developers.com/keep-those-pesky-data-folders-out-of-the-gallery-with-gallery-excluder-for-android/>

在 Android 设备上打开您的图库应用程序。去吧；我谅你也不敢。注意到里面有一堆你不想出现的东西吗？如果你有一点 Android 的敏锐度，你会意识到放置一个简单的*。违规目录中的 nomedia* 文件会将其排除在 Android 的媒体处理程序(如图库和音乐播放器)之外。然而，不幸的是，手动创建或复制文件有点麻烦。

为了让事情变得简单，XDA 论坛成员 [knox420](http://forum.xda-developers.com/member.php?u=2608226) 创建了一个奇妙的小工具来放置(和移除)这些前面提到的*。nomedia* 文件相当容易。

> **原因如下:**
> 
> 许多应用程序在 sd 卡上创建文件夹，然后把它们放在那里。通常，他们也会放置图片。现在，Android 会不时检查 sd 卡中的新媒体，这些文件夹将被添加到媒体数据库中，并显示在股票图库应用程序中。
> 
> **方法如下:**
> 
> Gallery Excluder 分别列出了“/SD card”/“mnt/SD card”的所有直接子文件夹，并在列表中显示它们。如果项目/文件夹被选中，则会出现一个。放在那个文件夹里。如果文件夹未被选中。“nomedia”已删除。
> 
> 由于更新图库需要一段时间，您可以通过选项菜单强制手动更新。

你还在等什么？请务必访问[应用程序线程](http://forum.xda-developers.com/showthread.php?t=1063358)，亲自体验一下！