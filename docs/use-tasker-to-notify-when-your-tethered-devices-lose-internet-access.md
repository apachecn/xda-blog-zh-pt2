# 使用 Tasker 通知您的连接设备何时无法访问互联网

> 原文：<https://www.xda-developers.com/use-tasker-to-notify-when-your-tethered-devices-lose-internet-access/>

从上一篇文章中，你知道我花了相当多的时间在火车上。这是写一两篇文章的绝佳时机，只要我能上网查找事实和想法。在火车上共享可能会很棘手，因为我的路线上分散着一些无信号的区域。我发现当我在隧道里时，很容易判断出我即将离线，但当火车穿过北约克郡的开阔草地时，这种情况就不那么明显了。Android 的内置共享解决方案没有任何方法让你知道你将无法在接下来的 5 分钟内加载该网站。

这就是为什么，作为一个 Tasker 爱好者，我想如何使用流行的 Android automation 应用程序来解决我的问题。我已经解决了我的问题，用 Tasker 建立了一个网络共享“无网络”警告。该项目的目的是让你知道什么时候你的手机不再在蜂窝网络范围内。这将通过 3 种方式完成:

*   使用 LED 通知灯(最适合您联系朋友的时候)
*   使用智能手机图标(需要智能手表)
*   使用加入推送(最适合个人设备-可以用自动远程替换)

你可以在通知方面更有创意，但是，我将只使用离散选项，因为共享最有可能在公共场所使用。没人喜欢讨厌的通知，对吧？请记住，通知将使用互联网连接在连接的设备上显示。当网络不存在时，您可以使用 **AutoRemote** (通过蓝牙)发出警告。这将要求相关设备通过蓝牙进行配对。

* * *

## 使用 Tasker 启用网络共享“无网络”警告

与其检查是否启用了共享，不如用**自动通知**替换状态栏中的磁贴，并设置一个切换行为。如果你没有使用 Android 7.0，你可以使用快捷方式或小工具来代替。

如果您从未启用过带有**自动通知**的磁贴，您会发现这有点尴尬。您需要创建一个设置任务，该任务会将模板图块转换为我们选择的图块。在图块区域放置一个空图块，即**自动通知 02** (点击编辑编辑可见图块)。

### 创建共享单幅图块

### 系绳瓷砖

```
Tile SetupA1:自动通知图块[配置:图块:2命令:hotspottoggle标签:热点icon:Android . resource://net . dinglisch . Android . task erm/HD _ AAA _ ext _ signal状态:1要求解锁:假隐藏通知:真实超时(秒):60 ]A2:变量集[Name:% hotspot Variable To:0 Recurse Variables:Off Do Maths:Off Append:Off]A3:变量集[Name:% hotspot dialog To:0 Recurse Variables:Off Do Maths:Off Append:Off]
```

您只需要运行一次来设置图块和变量。该区块将使用命令 **hotspottoggle** 来改变网络共享的状态，并将其设置为非活动状态。一旦按下，它还会折叠状态栏。您可以用自己选择的标签和图标来装饰磁贴。

将创建另外两个变量，并将其设置为 0。 **%HotspotVariable** 将显示系绳的状态(0 =否，1 =是)，而 **%HotspotDialog** 将显示一个对话框，询问我们想要通知什么设备(0 =不显示，1 =显示对话框)。

### 拴系开关

### 拴系开关

```
Hotspot Toggle A1:变量 Add [名称:%HotspotDialog 值:1 回绕:2 ]A2:自动通知图块[配置:图块:2命令:hotspottoggle标签:热点icon:Android . resource://net . dinglisch . Android . task erm/HD _ AAA _ ext _ signal国家:999要求解锁:假隐藏通知:真实超时(秒):60 ]A3: WiFi 系绳[设置:切换]A4:执行任务[名称:热点对话优先级:%优先级参数 1 (%par1):参数 2 (%par2):返回值变量:Stop:Off ] If [ %HotspotDialog ~ 1 ]A5:等待[毫秒:0 秒:5 分钟:0 小时:0 天:0 ]A6:变量添加[名称:% hotspot 变量值:1 回绕:2 ]A7:变量 Clear [ Name:%HotspotDevice 模式匹配:Off ] If [ %HotspotVariable ~ 0 ]
```

我想只在启用网络共享时显示一个对话框。该对话框将显示我拥有的一些设备，并允许我设置通知目标。在每种情况下，我都会设置我的共享手机，让它在每次接收效果不好的时候快速闪烁。

当按下磁贴时，它会将状态更改为活动。 **%HotspotDialog** 变为 1，触发 **HotspotDialog** 任务。当我们选择我们的设备时，通过将变量 **%HotspotVariable** 设置为 1 来装备热点配置文件。当我再次按下一个图块以结束共享时， **HotspotDialog** 返回到 0，不再提示显示对话框，并且 **%HotspotVariable** 被设置为中间值 0。

### A1、A6

动作**变量 Add +1** 将把我们的起始变量的值从 0 改变为 1，并使其围绕 2。这意味着这些变量将总是取值 1 或 0。动作的放置也是相关的，因为 **%HotspotDialog** 将控制对话框何时显示。我们正在运行相同的任务来禁用和启用网络共享，但是我们不希望每次切换时都出现对话框。

### A7

在此过程中，如果执行该任务是为了禁用 tether(**% Hotspot variable**= 0)，我们希望清除存储热点对话任务所通知的设备名称的变量。

### A5 号

添加**等待**动作是为了防止切换热点设置时可能出现的差范围信息立即显示。

### A3 号

只需**切换 WiFi 系绳**动作。这一步并不复杂。

### A4 号

显示一个单独的任务，显示**自动工具对话框**和我所做选择的动作。这将在我们的对话框控制变量 **%HotspotDialog = 1** 时运行。

### 主动脉第二声

当按下 toggle 时，我们希望确保 tile 将状态切换为活动/非活动，并保留相同的命令: **hotspottoggle** 。最后，确保它会折叠状态栏。

## 热点对话框

### 热点对话框

```
Hotspot Dialog A1:自动工具对话框[配置:对话框类型:列表标题:启用不良网络通知？icon:/storage/emulated/0/Tasker/Material Icons/IC _ wifi . png列表类型:1文本:平板电脑、手机、电脑、手表、笔记本电脑文本大小:20图片:/storage/emulated/0/Tasker/Material Icons/IC _ table t-1 . png、/storage/emulated/0/Tasker/Material Icons/IC _ cell phone _ Android-1 . png、/storage/emulated/0/Tasker/Material Icons/IC _ desktop _ MAC-1 . png、/storage/emulated/0/Tasker/Material Icons/IC _ watch-1 . png、/storage/emulated/0/Tasker/Material Icons/IC _ laptop-1 . png图像宽度:50暗淡背景:真列数:3上边距:16下边距:16底部按钮上边距:16底部按钮下边距:16选择时关闭:真分隔符:，命令变量:atcommand可取消:真打开屏幕:真实超时(秒):60 ]A2:变量集[Name:% hotspot device To:% at text Recurse Variables:Off Do Maths:Off Append:Off]
```

**自动工具对话框**用于显示可用的器件。选择设备后，对话框将关闭，并将 **%HotspotDevice** 的值设置为该设备的名称。每次停止共享时，该变量都会被清除。

### 接收不良/无数据

### 接收不良/没有数据配置文件

我已经创建了 2 个配置文件，将检查信号强度和互联网连接。每一个都由变量 **%HotspotVariable** 控制，并且仅在启用共享时才处于活动状态。激活和停用时，两个配置文件将触发相同的任务。一个包含状态上下文-信号强度-另一个包含移动网络。理想情况下，发出通知时，连接仍然存在。这就是我将信号强度设置为 1 的原因。

### 信号差

### 信号差

```
Profile: Poor Reception (91)状态:变量值[ %HotspotVariable ~ 1 ]状态:信号强度[从:0 到:1 ]输入:PoorSignal (89)A1:自动通知[配置:使用 HTML: false标题:接收效果不佳icon:Android . resource://net . dinglisch . Android . task erm/HL _ device _ access _ network _ cell状态栏图标:设备访问网络单元状态栏文本大小:16身份证号:55优先级:-1持久:真Is 组汇总:假LED 颜色:红色LED 亮起:300LED 熄灭:30p跳过图片缓存:假更新通知:假仅在电话上:真实超时(秒):20 ]A2:加入发送推送[配置:设备:Chrome@Laptop正文:极差标题:接收效果不佳icon:/storage/emulated/0/Tasker/Material Icons/IC _ wifi . png 超时(秒):60 ] If [ %HotspotDevice ~ Laptop ]A3:加入发送推送【配置:设备:Chrome@Home正文:极差标题:警告icon:/storage/emulated/0/Tasker/Material Icons/IC _ wifi . png 超时(秒):60 ]A4:加入发送推送[配置:设备:平板电脑正文:极差icon:/storage/emulated/0/Tasker/Material Icons/IC _ wifi . png 超时(秒):60 ] If [ %HotspotDevice ~ Tablet ]A5: AutoWear App [配置:立即执行:真触发事件:真触觉反馈:真名称:App自动磨损元素:显示自动磨损元素 Id: poorrange打开屏幕:真超时(秒):60 ]如果[ %HotspotDevice ~ Watch ]退出:取消(90)A1:自动通知取消[配置:Id: 55全部取消:假超时(秒):0 ]A2: AutoWear 应用[配置:立即执行:真触发事件:真触觉反馈:真名称:App自动磨损元素:隐藏自动磨损元素 Id: poorrange打开屏幕:真超时(秒):60 ]如果[ %HotspotDevice ~ Watch ]配置文件:无数据(92)状态:变量值[ %HotspotVariable ~ 1 ]状态:移动网络[ 2G:开启 3G:关闭 3G - HSPA:关闭 4G:关闭]输入:PoorSignal (89)A1:自动通知[配置:使用 HTML: false标题:接收效果不佳icon:Android . resource://net . dinglisch . Android . task erm/HL _ device _ access _ network _ cell状态栏图标:设备访问网络单元状态栏文本大小:16身份证号:55优先级:-1持久:真Is 组汇总:假LED 颜色:红色LED 亮起:300LED 熄灭:30p跳过图片缓存:假更新通知:假仅在电话上:真实超时(秒):20 ]A2:加入发送推送[配置:设备:Chrome@Laptop正文:极差标题:接收效果不佳icon:/storage/emulated/0/Tasker/Material Icons/IC _ wifi . png 超时(秒):60 ] If [ %HotspotDevice ~ Laptop ]A3:加入发送推送【配置:设备:Chrome@Home正文:极差标题:警告icon:/storage/emulated/0/Tasker/Material Icons/IC _ wifi . png 超时(秒):60 ]A4:加入发送推送[配置:设备:平板电脑正文:极差icon:/storage/emulated/0/Tasker/Material Icons/IC _ wifi . png 超时(秒):60 ] If [ %HotspotDevice ~ Tablet ]A5: AutoWear App [配置:立即执行:真触发事件:真触觉反馈:真名称:App自动磨损元素:显示自动磨损元素 Id: poorrange打开屏幕:真超时(秒):60 ]如果[ %HotspotDevice ~ Watch ]退出:取消A1:自动通知取消[配置:Id: 55全部取消:假超时(秒):0 ]A2: AutoWear 应用[配置:立即执行:真触发事件:真触觉反馈:真名称:App自动磨损元素:隐藏自动磨损元素 Id: poorrange打开屏幕:真超时(秒):60 ]如果[ %HotspotDevice ~ Watch ]
```

在手机上创建**自动通知**通知，但只是让 LED 闪烁。根据您的个人喜好选择通知的其他值，并以您喜欢的颜色设置快速 LED 闪烁(我的是 300 毫秒开/关)。这个想法是在屏幕唤醒时显示离散的信息，而不是完全侵入式的警告。该通知被保存为永久通知，其 **ID 为 55** 。

接下来是为你拥有的每台设备提供的**加入推送**。为每个设备选择一个 **Join push** ，使用 IF 条件匹配 **%HotspotDevice** 变量的值。

配置**加入推送**动作来发送您选择的通知。由于这些通知将在目标设备上被消除，因此不需要其他操作。

## 智能手表

### 智能手表档案

```
Profile: Remove Watch Icon 事件:AutoWear 命令[配置:命令筛选器:closepoorrange不区分大小写:false确切:正确正则表达式:假变量数组:false ]输入:关闭佩戴图标(55)A1: AutoWear 应用[配置:立即执行:真触发事件:真触觉反馈:真名称:App自动磨损元素:隐藏自动磨损元素 Id: poorrange打开屏幕:真实超时(秒):60 ]
```

你会注意到我已经改变了智能手表的通知方式。以上都不会出现在我的手表上。我想在我的手表上展示的唯一东西是一个小图标，它可以根据要求被取消。

使用 **AutoWear 管理浮动图标** *(你必须进入 AutoWear 应用程序)创建一个图标，并在你的手表上测试大小和位置。该图标将在任何屏幕上绘制，所以确保它包含一个点击关闭它的命令。我使用了 **closepoorrange** 并将图标命名为 **poorrange** 。我的图标的大小是 30x30 像素，它被放置在 65%的权利和 20%的顶部。

一旦你对大小和位置满意了——使用**自动穿戴应用**动作来显示图标和 IF 条件，以将其链接到 **%HotspotDevice** 变量。

## 取消

### 取消

```
Cancel (90)A1:自动通知取消[配置:Id: 55全部取消:假超时(秒):0 ]A2: AutoWear 应用[配置:立即执行:真触发事件:真触觉反馈:真名称:App自动磨损元素:隐藏自动磨损元素 Id: poorrange打开屏幕:真超时(秒):60 ]如果[ %HotspotDevice ~ Watch ]
```

为了结束 LED 闪烁并从手表中移除浮动图标，我将使用一个简单的**自动通知取消**操作，使用我的通知 ID(**55**)来执行隐藏浮动图标的**自动佩戴应用**操作。

智能手表有一个额外的配置文件，如果按下图标，将会删除浮动图标。为此，我使用了 **AutoWear 命令**event’**closepoorrange**，然后我运行了一个单独的任务，它包含了与 **Cancel** 任务几乎相同的动作。

* * *

我们希望你喜欢我们的这个小发明，如果你认为我们可以做任何改进，请告诉我们！一如既往，您可以通过点击下面的链接下载该项目。

[**在此下载网络共享“无网络”警告项目文件！**](https://www.androidfilehost.com/?fid=745425885120700969)

为了导入带有 Tasker 项目文件的网络共享“无网络”警告，请下载上述文件并将其保存在您的内部存储中的任何位置。打开 Tasker 并检查以确保“初学者模式”在首选项菜单中被禁用。然后，长按左下角的“主页”图标，点击“导入”。找到您之前保存的 prj.xml 文件，并选择它进行导入。现在，您将在底部一行看到一个新的选项卡，包含我们在本文中引用的所有概要文件和任务。