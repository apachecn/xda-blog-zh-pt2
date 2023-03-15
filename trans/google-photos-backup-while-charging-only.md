# 如何在充电时恢复 Google 相册备份选项

> 原文：<https://www.xda-developers.com/google-photos-backup-while-charging-only/>

谷歌照片是谷歌雄心勃勃的免费照片备份解决方案。这是最好的谷歌服务之一，自从谷歌输入输出以来，它已经变得越来越好了。但并不是每一个功能变化都受到了欢迎。早在 6 月下旬，谷歌[突然取消了](https://forum.xda-developers.com/u11/help/google-photos-backup-charging-missing-t3621948)设备充电时才备份照片的功能。据谷歌产品帮助论坛的一位顶级贡献者称，这一[变化是有意的](https://productforums.google.com/forum/#!topic/photos/0ZoOGGRXel4;context-place=forum/photos)，尽管谷歌仍然没有提供他们为什么删除的原因。更奇怪的是，谷歌照片充电时备份选项的取消并不普遍——一些用户报告说仍然有，而许多人没有。

也许谷歌正在过渡到一种基于 JobScheduler 的新算法，他们认为这不会对电池产生重大影响。不管是什么原因，这种转变没有得到很好的处理。当设备连接到 WiFi 时，让谷歌照片自动开始备份照片是一个很大的痛苦，因为它削弱了我缓慢的家庭互联网(我在我的城市没有太多的选择)。尽管如此，我还是想出了一个办法，让你在充电功能时**手动恢复 Google 相册备份，但这需要一点努力(和 root 访问)。**

*左:充电时无备份，仅选项。右图:仅充电时备份选项。*

下面的教程**需要您设备上的 root 访问权限**,因为您将修改位于/data 目录中的文件，这在非 root 设备上是不可访问的。这意味着您的设备的引导加载程序可能是解锁的，并且您已经通过 SuperSU 或 Magisk 安装了超级用户二进制文件。

* * *

## 充电时带回 Google 相册备份

我可以确认以下调整是可行的，因为我已经在运行 Android 7.1.1 Nougat 的 OnePlus 5 和 Android O Developer Preview 4 的 Google Pixel 上测试了 Google Photos 版本 3.3.0.165520514。

如前所述，您需要安装一个能够浏览/data 分区中的目录的文件浏览器应用程序。这意味着应用程序应该是根启用的。虽然我个人更喜欢 Solid Explorer，但如果你还没有你喜欢的文件浏览器，我建议你从我们的应用和游戏论坛下载免费的 MiXplorer 应用。

[appbox xda com.mixplorer]

安装文件管理器应用程序后，打开它，然后导航到以下目录:

`/data/data/com.google.android.apps.photos/shared_prefs`

现在打开以下首选项文本文件:

```
 photos.backup.backup_prefs.xml 
```

找到靠近顶部的下面一行，将值“false”改为“ **true**

`<boolean name="backup_prefs_backup_only_when_charging" value="false" />`

*偏好更改为仅充电时启用 Google 相册备份*

更改布尔值后，关闭首选项文件。进入设置->应用程序，找到并强制关闭 Google 相册。现在重新打开谷歌照片，你应该能够启用备份，而只收取谷歌照片选项！

关注[教程类别](https://www.xda-developers.com/category/tutorials/)获取更多类似的帖子。下载 XDA 实验室应用程序，了解门户网站和论坛的最新消息！