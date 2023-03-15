# 如何在没有 Root 的三星 Galaxy 手机上增加 Edge 屏幕尺寸

> 原文：<https://www.xda-developers.com/increase-edge-screen-size-samsung-galaxy/>

虽然三星 Galaxy S6 Edge、S7 Edge、S8、S8+和 Note 8 上的 Edge Screen 功能提供了一种访问您最喜爱的应用程序、任务等的有用方式，但激活它可能是一种痛苦，尤其是因为较新的手机如此之高！大小(和识别区域)可以在设置中调整，但是，您可以设置的最大大小对一些用户来说不够。如果你觉得手机上的边缘手柄太小，你可以很容易地将其更改为自定义值，而不需要 root 或太多的努力，这要归功于最初由 XDA 资深会员 [Pedroc1999](https://forum.xda-developers.com/member.php?u=4967998) 制作的教程[。](https://forum.xda-developers.com/galaxy-s8+/how-to/adb-fullscreen-edge-handle-t3682114)

它最初是在三星 Galaxy S8+上测试的，然而，我们也确认了它在新的[三星 Galaxy Note 8](https://www.xda-developers.com/galaxy-note-8-835-rear-cameras-spen/) 上也可以工作。它也可以在定制的基于 TouchWiz 的 rom 上运行，并启用 [edge 特性](https://www.xda-developers.com/how-to-add-an-edge-panel-with-contacts-tasks-and-apps-on-the-galaxy-note-5/)。

* * *

## 增加三星手机的边缘屏幕手柄尺寸(ADB)

对于本教程，一如既往，你需要在你的手机和电脑上正确设置 Android 调试桥。幸运的是，我们[之前已经做过一个关于如何建立 ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的教程。请务必在继续之前查看，因为它包括在 Windows、Linux 和 macOS 计算机上进行设置的完整说明。

 `一旦你在电脑上设置了 ADB，你就需要打开一个命令提示符/终端，输入以下命令:

```
 adb shell 
```

最后，要根据您的喜好更改边缘屏幕句柄大小，请使用以下命令:

```
 settings put global edge_handle_size_percent insertvaluehere 
```

您可以在其中为自定义值更改“insertvaluehere”。在这种情况下，我们希望句柄填满屏幕的整个边缘，所以我们将其更改为“100.00”。

`settings put global edge_handle_size_percent 100.00`

手柄尺寸仍然是默认的，所以为了使这个设置保持不变，只需进入边缘屏幕手柄设置。你会发现 edge 屏幕手柄尺寸现在变成了全尺寸。你可以走了！

### 增加三星手机的边缘屏幕手柄尺寸(终端+根)

如果你手边没有电脑，或者你只是不想设置 ADB 或使用电脑，你可以直接从实际的手机上完成——前提是你的手机是[根](https://www.xda-developers.com/samsung-galaxy-note-8-root-samfail/)的。你将需要事先下载一个类似 Termux 的终端 app，并赋予其 root 权限，所以在开始之前一定要从 Play Store 下载。

然后，启动您选择的终端应用程序，并使用以下命令授予它 root 权限:

```
 su 
```

由于您已经在 Android shell 中，您可以简单地使用以下命令来更改句柄大小:

```
 settings put global edge_handle_size_percent insertvaluehere 
```

同样，将“insertvaluehere”更改为您选择的值。转到手柄设置，找到并设置您的自定义尺寸。

* * *

## 说明

你实际上可以在设置中调整屏幕手柄的大小，用滑块变小/中/大，然而，有些人发现即使在最大的设置下它也真的很小，这可能很烦人，因为最新的三星旗舰手机有多高。挖掘背景。全局数据库您将能够找到“edge_handle_size_percent”设置，可以使用设备的外壳界面轻松调整该设置。

虽然本教程最初是在三星 Galaxy S8+上测试的，但正如我们在文章开头所说，我们也已经确认本教程适用于三星 Galaxy Note 8，并且它可能也适用于 Galaxy S7 edge 和 S6 edge，因为它们都有边缘屏幕，因此也有边缘功能。这在没有这种边缘屏幕功能的平板屏幕三星手机上不起作用。然而，如果你正在运行一个定制的 ROM，可以在你的平板三星手机上启用 edge 功能，你可能也能利用这个调整。`