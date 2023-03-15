# XDA 聚焦:用 Chromium 自动更新程序生活在前沿

> 原文：<https://www.xda-developers.com/xda-spotlight-living-on-the-bleeding-edge-with-chromium-auto-updater/>

回到 2015 年 10 月，开发人员开始编译针对骁龙设备优化的 Chromium 的第[个版本。通常被称为“CAF Chromium”构建(以源代码起源的代码 Aurora Forums 命名)，这些铬的开源衍生物迅速开始在网络上扩散。很快，就有几十个基于 CAF Chromium 的构建版本出现在各种来源上(包括我们自己的 XDA 实验室应用市场上的一些)。](https://www.xda-developers.com/chromium-optimized-for-snapdragon-devices/)

这个项目的每一个变化，都是由个人开发者根据自己的喜好挑选功能，为用户提供了很多。夜间模式，内置广告拦截，省电模式，以及更多的功能可以在这些版本中找到。一些变体甚至支持同步你的谷歌账户，但这通常是罕见的(并且很可能在不久的将来[变得不可能](https://forum.xda-developers.com/showpost.php?p=70497242&postcount=544))。总的来说，许多用户可能分辨不出每个 CAF Chromium 变体之间的区别——尤其是在性能方面。尽管基准测试[声称差异显著](https://www.youtube.com/watch?v=uQaAfzYIPag&feature=youtu.be)，大多数用户可能会坚定地告诉你“他们的”是最快的。

还有信任的问题。虽然最初的 CAF Chromium 是开源的，但是这些变体中的许多都不是。用户可能没有理由不信任一些更受欢迎的变体的维护者，但是过去一些 CAF 变体曾出现过 T2 问题。此外，在[海豚浏览器事件](https://forum.xda-developers.com/showthread.php?t=1319529)之后，人们继续对浏览器可能收集的数据保持警惕。

但是更实际地说，CAF Chromium 变体的最大问题是保持与 Chromium 最新版本的同步。谷歌定期更新其浏览器以修复安全问题，但一个开发人员定期维护自己的分支可能很耗时。另一方面，开发团队可以更容易地为浏览器提供频繁的更新。幸运的是，开源的 Chromium 正是如此。

* * *

## 生活在铬污染的边缘

为了了解 Chrome 比 Chrome 频道领先多少，让我们看看每个浏览器目前的版本。

*   Android 版 chromium:**v 58 . 0 . 2990 . 0**
*   Chrome 金丝雀: **v57.0.2987.4**
*   Chrome 开发: **v57.0.2984.3**
*   chrome Beta:**v 56 . 0 . 2924 . 68**
*   铬稳定: **v55.0.2883.91**

如你所见，Chromium 甚至比谷歌 Chrome 最具实验性的分支 Canary 还要领先。这并不意味着铬本身不适合日常使用——远非如此。Chromium for Android 直接从源代码运行 Chromium 的最新版本，这意味着它可能会在任何单独的版本中出现错误，也可能不会。那些有运行定制的每夜 ROM 构建经验的人可能知道我在说什么。但是那些喜欢只使用最新稳定版本的人可能会对安装如此实验性的东西保持警惕。

就特性而言，Chromium 并没有提供我在本文开头提到的大多数闭源 CAF Chromium 衍生物的所有功能。没有内置广告拦截，没有夜间模式，也没有省电模式。这只是直接从源代码构建的纯 Chromium，具有开源项目中目前正在开发的任何实验特性。如果你是那种喜欢在 chrome://flags 中挖掘和玩新功能的人，或者你只是喜欢运行最新的实验版本来体验 Chromium 团队所做的所有改进，那么这款浏览器就是为你准备的。

如果你不是那种每天都想运行脚本从源代码中为 Android 构建 Chromium 的人(我们大多数人可能都不是)，幸运的是，确实有一些源代码可以让你轻松下载最新版本。一个名为 **Chromium Auto Updater** 的开源应用程序就是这样一种容易保持最新的方法，但还有其他应用程序(以及我将提供的一个简单的 Tasker 项目，它具有相同的功能)。

* * *

## 与铬保持同步

每天晚上，Chromium build bot 将 Chromium 与任何提交的代码变更一起编译成所谓的**快照**版本。这些快照构建的二进制文件可以在谷歌的存储服务器上[找到。在通过一系列](https://storage.googleapis.com/chromium-browser-snapshots/index.html)[自动化测试](https://www.chromium.org/developers/testing)后，这些快照可能最终成为 Chromium 的稳定版本。目前，Chromium 团队没有为 Android 提供任何稳定的 Chromium 版本。你只能下载 Chromium 的快照版本，但是这样做对于普通用户来说并不容易——考虑到它的实验状态，这是意料之中的。

弗朗索瓦·博福特(Franç ois Beaufort)创建了一个[网页](https://download-chromium.appspot.com/?platform=Android)(现在由 Chromium 团队维护)，让你只需点击一下鼠标，就可以快速下载任何操作系统的最新 Chromium 版本，然而，这需要你手动访问页面以保持更新。[另一个网页](https://chromium.woolyss.com/#android)提供了一个 RSS 源和一个 API(以及一船与项目相关的信息),让你可以自动下载最新版本——前提是你知道如何正确解析这类数据。如果我们想自动下载最新版本，我们可以使用前面提到的[开源](https://github.com/adolfintel/chromiumUpdater)应用 Chromium Auto Updater。

这个应用程序的工作方式非常简单。它会定期轮询 Chromium snapshot build 页面寻找新版本，如果找到新版本，它会通知您有新版本可供下载。如果您在您的设备上有 root 访问权限，您可以在后台自动更新最新的构建版本(出于好奇，应用程序使用*包管理器* shell 命令来安装更新)。否则，单击通知将通过标准包管理器界面打开更新应用程序的意图。

尽管 Chromium Auto Updater [并不是同类应用中唯一的一个](https://github.com/andDevW/getChromium)，但我更喜欢它而不是其他两个。对于初学者来说，getChromium 没有为 root 用户自动安装最新版本的选项，而且它目前也不能安装在 Nougat 设备上。你能在 Play Store 里找到的另一个 Chromium updater 应用似乎也不是开源的(或者至少，我找不到它的源代码)。因此，我坚持使用 Chromium 自动更新程序来更新 Chromium 的最新版本。

最后，作为一种 DIY 选择(因为我喜欢 Tasker)，我创建了自己的自动更新 Chromium 项目。我将在下面分享组成该项目的两个概要文件的描述，以及您可以下载和导入的项目文件。我认为复制这些开源应用程序会是一个有趣的项目，如果你渴望提高你的任务技能，我建议你尝试重新创建我下面的项目。根据描述，这应该相当简单！

### 更新铬

```

Profile: Update Chromium (141)
 Day: Sun, Tue, Thu or Sat
 Time: 11:59PM
Enter: Update Chromium (133)
 A1: HTTP Get [ Server:Port:https:
 A2: If [ %HTTPD neq %Version ]
 A3: Variable Set [ Name:%Version To:%HTTPD Recurse Variables:Off Do Maths:Off Append:Off ] 
 A4: Notify [ Title:Downloading Chromium... Text:Fetching latest version from Google. Icon:hd_av_download Number:0 Permanent:Off Priority:3 ] 
 A5: HTTP Get [ Server:Port:https:
 A6: Notify Cancel [ Title:Downloading Chromium... Warn Not Exist:Off ] 
 A7: UnZip [ File:Tasker/chrome-android.zip Delete Zip:On ] 
 A8: Notify [ Title:Chromium Update Available! Text:Tap to install. Icon:hd_location_web_site Number:0 Permanent:Off Priority:5 ] 
 A9: End If 

```

### 安装铬合金

```

Profile: Install Chromium (142)
 Event: Notification Click [ Owner Application:* Title:Chromium Update Available! ]
Enter: Anon (143)
 A1: Open File [ File:Tasker/chrome-android/apks/ChromePublic.apk Mime Type: ] 

```

您可以通过以下按钮从 AndroidFileHost 下载项目文件:

[**下载 Chromium 更新器 Tasker 项目！**](https://www.androidfilehost.com/?fid=385035244224414667)

为了导入它，首先将文件保存到您的内部存储器。打开 Tasker，并在首选项中禁用“初学者模式”。然后，返回主屏幕，长按左下角的“主页”图标。您将看到一个弹出窗口，显示“导入”选择该选项，然后浏览到保存. prj.xml 文件的位置，并单击将其导入。瞧啊。现在你应该看到“Chromium”项目是 Tasker 底部的另一个标签。您可以并且应该定制自动更新程序检查新 Chromium 版本的时间，以满足您的偏好。享受这个项目！