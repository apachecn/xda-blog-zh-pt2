# 用 Tasker 和 AutoTools 复制 Google Dialer 的浮动气泡功能

> 原文：<https://www.xda-developers.com/replicate-google-dialer-floating-bubble-feature/>

之前，我们已经分享了如何通过修改 Android 设备上的文件来[启用谷歌手机应用程序的新浮动拨号气泡](https://www.xda-developers.com/enable-google-dialer-floating-bubble/)。从那以后，我们最喜欢的 Tasker 插件开发者，[joo Dias](https://plus.google.com/+Jo%C3%A3oDias)，想出了一个自己的解决方案，用他的 AutoTools 应用程序来重现同样的浮动泡泡。他的视频很酷，但附带的[帖子](http://forum.joaoapps.com/index.php?resources/create-google-dialer%E2%80%99s-floating-bubble-feature-with-a-web-screen.294/)在其描述中略有欠缺，所以我想我应该创建一个单独的教程，并通过在拨号器浮动气泡中的切换添加视觉反馈来改进 joo 的设计。

像往常一样，我们将首先跟随一个教程，然后在最后你可以找到关于导入项目的下载链接和说明。

* * *

## 复制谷歌拨号器的浮动气泡

[app box Google play com . joaomgcd . autotools]

AutoTools 插件带有一个新的网页预设:浮动栏。使用这个预设，我们可以在任何手机上重新创建谷歌拨号器浮动气泡。如果你熟悉 Tasker，你会发现它很容易重新创建，但如果你不熟悉 Tasker 和 AutoTools，那么请继续阅读，我们会告诉你如何做。

我所做的更改包括删除音量和麦克风图标的路径，并替换为变量。我对这些选项的命令做了同样的操作。这样，当按钮被按下时，我们可以创建一个可视的切换。它特别有助于静音选项，所以你可以看到麦克风是否启用。

### 呼入

当电话被接听时，该情景模式会被激活。将显示 AutoTool WebScreen:浮动栏预设。

### TASKER 配置文件-通话进行中

```
Profile: Call In Progress 事件:电话摘机输入:通话进行中A1: Flash [ Text:Calling...龙:关]A2:变量集[ Name:%callMute To:mute递归变量:Off 做数学:Off 追加:Off ]A3:变量集[名称:%callSpeaker To:speaker递归变量:Off 做数学:Off 追加:Off ]A4:变量集[名称:%mutePathTo:/pathto/micoff.png递归变量:Off 做数学:Off 追加:Off ]A5:变量集[名称:%volPathTo:/pathto/voloff.png递归变量:Off 做数学:Off 追加:Off ]A6: AutoTools 网页屏幕[配置:屏幕预设:浮动栏显示模式:覆盖关闭覆盖 ID:调用 uiSource: /pathto/page.html烤面包持续时间:5000背景色:# 00 咖啡蜂宽度:75身高:75重力:左侧偏移 X: 50Y 偏移:-100动画:放大覆盖 Id:调用 ui显示持续时间:500隐藏持续时间:250拖动:可拖动到任何地方拖动运动:所有方向抛弃:没有抛弃的抛弃更新:真的图标:%volPath，%mutePath，/pathto/endcall.png，命令:%callSpeaker，%callMute，结束命令前缀:phonecall可见项目:3第一项:3、4、2、5物品填充物:24动画时间:400折叠时画圈:真自定义展开图标:/pathto/call.png贴齐项目:true浮动条颜色:#1565C0扩展器颜色:黑色扩展器背景颜色:#0D47A1 超时(秒):30 ]
```

我使用变量 **%mutePath** 和 **%volPath** ，而不是麦克风和音量的预定义路径以及它们各自的命令。这些将随后根据发出的命令而改变。

**%callMute** 和 **%callSpeaker** 持有分配给现有按钮的实际命令。当按下按钮时，命令会改变，拨号器浮动气泡会显示正确的图标。

创建(或者修改这个气泡，如果你使用了 Joao 的教程)有点痛苦，但是好消息是我们可以稍后复制并粘贴这个动作。确保分配 WebScreen ID，因为我们稍后将需要它来取消气泡。

### 通话结束

它由命令触发: **phonecall=:=end** 并运行任务 Call Ended。在关闭显示模式下使用 AutoTools WebScreen。使用与来电配置文件中相同的 WebScreen ID。

### TASKER 个人资料-通话结束

```
Profile: Call Ended 事件:电话空闲输入:通话结束A1: Flash [ Text:通话结束....龙:关]A2:自动工具网页屏幕[配置:显示模式:关闭关闭覆盖 ID:调用 ui烤面包持续时间:5000身高:400重力:中心动画:从顶部滑入显示持续时间:500隐藏持续时间:250 超时(秒):30 ]
```

### 命令

此配置文件控制拨号器浮动气泡发送的所有操作。每个触发器都以前缀 **phonecall=:=** 开始，并根据截取的输入触发其中一个切换/动作。

### TASKER 配置文件-调用命令

```
Profile: Call Commands 事件:AutoApps 命令[配置:命令筛选器:phonecall=:=变量名:命令]回车:调用命令A1:如果[ %command ~ *speaker ]A2:变量集[名称:%callSpeaker To:unspeaker递归变量:Off 做数学:Off 追加:Off ]If [ %command ~ speaker ]A3:变量集[名称:%volPath To:/pathto/volon.png递归变量:Off 做数学:Off 追加:Off ]If [ %command ~ speaker ]A4:变量集[ Name:%callSpeaker To:speaker递归变量:Off 做数学:Off 追加:Off ]如果[%命令~取消标记]A5:变量集[名称:%volPath To:/pathto/voloff.png递归变量:Off 做数学:Off 追加:Off ]如果[%命令~取消标记]A6:自动工具网页屏幕[浮动条-与通话进行中相同]A7:免提电话[设置:切换]A8: Else If [ %command ~ *mute ]A9:变量集[ Name:%callMute To:mute递归变量:Off 做数学:Off 追加:Off ]如果[%命令~取消静音]A10:变量集[名称:%mutePath To:/pathto/micoff.png递归变量:Off 做数学:Off 追加:Off ]如果[%命令~取消静音]A11:变量集[名称:%callMute To:unmute递归变量:Off 做数学:Off 追加:Off ]如果[%命令~静音]A12:变量集[名称:%mutePath To:/pathto/micon.png递归变量:Off 做数学:Off 追加:Off ]如果[%命令~静音]A13:自动工具网页屏幕[浮动条-与通话进行中相同]A14:麦克风静音[设置:切换]A15: Else If [ %command ~ end ]A16:结束通话A17:结束 If
```

我知道这个描述一开始看起来令人生畏，但这是重复两次的同一套动作。当静音或扬声器被按下时，我们必须创建一个替代的网页屏幕，向用户显示相反的图标和命令。

#### A1，A8

如果命令= speaker/mute，将会出现一系列动作。我稍微修改了一下命令，以便更容易处理所有的动作。我们通过这些动作捕捉静音/取消静音和扬声器/非扬声器命令。这就是我在 IF 条件中使用*通配符的原因。

#### A2、A4 和 A9、A11

根据发出的命令(静音/取消静音|扬声器/取消扬声器),我设置了一个正确的命令，该命令将在我下次按下开关时分配。例如，如果我按下静音按钮(command=:=mute)，我希望更新网页屏幕，并确保下次按下此按钮时通话将被取消静音(command=:=unmute)。扬声器动作也是如此。

#### A3，A5 和 A10，A12

以类似的方式，我想确保一旦发出按钮，到相应图标的路径就会改变。如果我按下静音图标，我希望取消静音图标被替换，因此必须更新路径。

#### A15

如果命令显示 end—结束通话。

#### A7，A14

只需使用操作静音和扬声器来切换设置。

* * *

## 结论和下载

现在你知道如何用 Tasker 和 AutoTools 来做这件事了。新的拨号器浮动气泡项目为您提供了一个很好的，可视化的反馈，使您在打电话时与您的电话互动更容易一点。请随意进一步修改这个 Tasker 项目。

[**下载 Tasker 拨号器浮动按钮项目**](https://www.androidfilehost.com/?fid=817906626617941690)

下载上面的 ZIP 文件，并将内容解压缩到您的 Android 设备的内部存储中。**将文件夹 callui 解压到 Tasker/icons 目录**。打开 Tasker，在首选项中禁用“初学者模式”。然后，回到 Tasker 的主页，长按左下角的 home 图标。您将看到一个“导入”项目的选项。点击该选项，然后找到您之前提取的. prj.xml 文件。导入后，您将会在 Tasker 的默认主页图标旁边的底部看到一个新标签。它包含这个助手项目的概要文件和任务。

跟随 [XDA 开发者教程](https://www.xda-developers.com/category/tutorials/)获取更多这样的帖子。此外，查看我们的 [Tasker Tips & Tricks](https://forum.xda-developers.com/u/tasker-tips-tricks) 论坛，了解我们社区中自动化爱好者的最新创造。