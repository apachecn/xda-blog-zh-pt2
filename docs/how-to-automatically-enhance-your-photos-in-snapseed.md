# 如何在 Snapseed 中自动增强照片

> 原文：<https://www.xda-developers.com/how-to-automatically-enhance-your-photos-in-snapseed/>

我不擅长照片编辑(和一般的摄影)，我不羞于承认这一点。我没有像我的一些同事那样费心去学习如何使用[手动相机控制](https://www.xda-developers.com/using-manual-camera-controls-improving-the-quality-and-versatility-of-your-photography/)或[编辑原始图像](https://www.xda-developers.com/a-guide-to-editing-raw-photography/)。像大多数人一样，我使用相机的默认功能，所有选项都设置为自动，让软件决定最佳的白平衡、对焦、亮度等。应设置为。

有时，如果我最初的照片没有像我希望的那样出来，我会通过 [Snapseed 的](https://play.google.com/store/apps/details?id=com.niksoftware.snapseed&hl=en)自动调谐功能运行它。但如果我想对大量照片(比如说，> 50 张)执行这个操作，这将很快变成一个麻烦，因为我必须在 Snapseed 中手动打开、调整、然后保存每张照片。鉴于我在 Android 自动化方面的背景，我对自己说:为什么不把这个过程自动化呢？于是我照做了。认识一下**自动快照种子任务脚本**。

* * *

## 使用 Tasker 的自动快照种子自动增强您的照片

这个项目显然需要 Snapseed，因为这是我们用来微调照片的应用程序。Tasker 是必需的，因为我们将使用这个自动化应用程序与两个插件进行交互:AutoInput 和 AutoShare。AutoShare 是在 Android 的共享菜单中创建新项目所必需的，这样你就可以快速增强照片，并共享那些将在 Snapseed 中打开的照片。AutoInput 然后自动进行必要的点击，以自动增强照片。

一旦你安装了这些应用程序，我们必须设置一些东西。首先，您需要授予 AutoInput 启动其辅助功能服务的能力，一旦您打开它，该应用程序就会提醒您这样做。接下来，我们需要创建一个新的 AutoShare 命令，这样当我们打开图像共享对话框时，我们将有一个菜单选项来选择 AutoShare。打开 AutoShare，向下滚动到“AutoShare 设置”,确保选中“AutoShare 命令”。然后，向上选择“管理命令”点击+图标添加一个新命令，并将其命名为“自动快照种子”选择您想要的任何图标，但是我建议使用 Snapseed 图标来清楚地说明这是做什么的。

现在我们准备开始在 Tasker 中制作我们的脚本。打开 Tasker，按右下角的+创建一个新的配置文件。将其命名为“Auto-Snapseed ”,并选择**事件**上下文。进入插件- >自动共享- >自动共享命令。按铅笔图标打开配置，然后选择您之前创建的“Auto-Snapseed”命令。

退出概要文件配置，Tasker 将要求您创建一个新任务。您可以选择命名任务，但这不是必需的。点击复选标记打开任务编辑屏幕。我将一步一步地指导你需要做什么，但是对于那些已经熟悉 Tasker 的人来说，你可以展开下面的开关来查看脚本的描述。

### 自动快照种子任务描述

```

Profile: Auto-Snapseed (208)
Event: AutoShare [ Configuration:Command: Auto-Snapseed
Sender: all
Subject: all
Text: all
File: all ]
Enter: Auto-Snapseed (207)
A1: For [ Variable:%image Items:%asfile() ]
A2: AutoShare [ Configuration:Package: com.niksoftware.snapseed
Class: com.google.android.apps.snapseed.EditActivity
App: AutoShare
Action: Share
MimeType: image/jpeg
File: %image Timeout (Seconds):10 ]
A3: AutoInput Action [ Configuration:Type: Text
Value: Add filter
Action : Click Timeout (Seconds):20 ]
A4: Wait [ MS:0 Seconds:1 Minutes:0 Hours:0 Days:0 ]
A5: AutoInput Action [ Configuration:Type: Text
Value: Tune Image
Action : Click Timeout (Seconds):20 ]
A6: Wait [ MS:0 Seconds:1 Minutes:0 Hours:0 Days:0 ]
A7: AutoInput Action [ Configuration:Type: Text
Value: Auto Adjust
Action : Click Timeout (Seconds):20 ]
A8: Wait [ MS:0 Seconds:1 Minutes:0 Hours:0 Days:0 ]
A9: AutoInput Action [ Configuration:Type: Text
Value: Apply
Action : Click Timeout (Seconds):20 ]
A10: Wait [ MS:0 Seconds:1 Minutes:0 Hours:0 Days:0 ]
A11: AutoInput Action [ Configuration:Type: Text
Value: DONE
Action : Click Timeout (Seconds):20 ]
A12: Wait [ MS:0 Seconds:3 Minutes:0 Hours:0 Days:0 ]
A13: End For 
```

1.  **任务- >为。**变量:**%图像**。项目: **%asfile()** 。这将使变量%image 在您通过共享对话框共享的图像中循环。
2.  **插件- >自动共享- >自动共享。**包: **com.niksoftware.snapseed** 。class:**com . Google . Android . apps . snapseed . edit activity**。App: **自动分享**。动作:**分享**。MimeType: **image/jpeg** 。文件:**%图像**。此操作会将%image 引用的共享图像逐个发送到 Snapseed 进行编辑。
3.  **插件**->-**自动输入**->-**动作。**按“简易设置”,然后打开您的图库应用程序，选择任何要分享到 Snapseed 的图片。拉下通知阴影，展开自动输入通知，并按下“添加”按钮。现在按下浮动铅笔图标按钮，允许 AutoInput 记录/捕获此输入。AutoShare 将自动打开“最近使用的应用程序”菜单，并要求您返回 Tasker。这样做，当您返回时，应该会看到一个弹出窗口，询问您选择什么值。选择"**添加过滤器"**文本类型并选择**点击**动作。
4.  **任务**->-**等待**。等待 1 秒钟。
5.  **插件- >自动输入- >动作。**再次按“简易设置”并返回 Snapseed。这一次，在开始自动输入的记录之前，按下浮动铅笔图标。您应该会看到 Snapseed 提供的所有图像增强选项。现在拉下通知并按“添加”选择“调整图像”选项，让 AutoInput 记录它。返回 Tasker，选择**【调谐图像】**文本类型，选择**点击**动作。
6.  任务- >等待。等待 1 秒钟。
7.  **插件- >自动输入- >动作。**希望你现在已经明白了。我们正在逐步推进手动图像调整过程，并让 AutoInput 记录我们的操作，以便我们可以自动播放它们。回到 Snapseed，这次按下“调整图像”选项，调出亮度/饱和度等。选项。下拉自动输入通知，选择“添加”按钮，现在按下 Snapseed 中的“**自动**(魔杖)”按钮来记录该动作。返回 Tasker，选择**“自动调整**”文本类型，选择**点击**动作。
8.  任务- >等待。等待 1 秒钟。
9.  **插件- >** **自动输入- >动作。**打开 Snapseed，拉下通知遮光板，然后按“添加”现在图像已经自动调整，选择右下角的勾号图标让 AutoInput 记录下来。返回 Tasker，选择**“应用”**文本类型，选择**点击**动作。
10.  任务- >等待。等待 1 秒钟。
11.  **插件- >自动输入- >动作。**最后一次打开 Snapseed，开始自动输入记录，然后按左上角的“完成”按钮记录该输入。返回 Tasker，选择**【完成】**文本类型，选择**点击**动作。
12.  任务- >等待。等待 3 秒钟。我们需要这个 3 秒钟的计时器来确保 Snapseed 有足够的时间来保存照片，然后再继续下一张照片。
13.  **任务- >结束。**结束 for 循环！

就是这样！这里的麻烦是设置 for 循环，这需要您手动记录应用 Snapseed 的自动图像调整功能所涉及的步骤。但是一旦你做了一次，你就再也不用手动做了！额外的好处是，你现在可以通过共享菜单向 Snapseed 发送 2、3 甚至几十张照片，它会自动增强每一张照片！你所要做的就是坐以待毙。您编辑过的照片将位于内部存储器的 **Snapseed 文件夹**中。

* * *

## 下载并导入

一如既往，我们提供 Tasker 脚本，以便您可以快速下载和导入它。从下面下载. prf.xml 文件，并将其保存在内部存储的任何位置。打开 Tasker，在首选项中禁用初学者模式。然后，返回主菜单，长按顶部的个人资料选项卡。您应该会看到一个导入概要文件的选项。选择它并找到您下载的 XML 文件。

[**下载自动快照脚本**](https://www.androidfilehost.com/?fid=457095661767148532)

一旦您导入了它，请确保您仍然返回并如前所述设置自动输入和自动共享。否则，AutoShare 将不会显示在您的共享菜单中，AutoInput 将无法在您的手机上发送输入点击！

让我知道你是否喜欢这个项目，以及你希望在下面的未来教程中看到什么样的自动化！