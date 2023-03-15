# 使用 Yeelight 智能 RGB LED 灯泡和 Tasker 轻轻唤醒

> 原文：<https://www.xda-developers.com/wake-up-gently-with-tasker-and-yeelight/>

在北半球，这里变得越来越暗，特别是在英国，自然光在下午 6 点后就消失了。由于这些条件不会很快得到改善(至少要到春天)，让我们使用 Tasker 和 Yeelight 智能 RGB LED 灯泡按需模拟日落和日出。

Yeelight 应用已更新。引入了新的 Tasker 选项，包括亮度、颜色和温度变量。不幸的是，更新打破了预定义的场景，使我的其他教程无关紧要。我已经联系了 Yeelight 的员工并传递了我的反馈。我希望我们能在下一次更新中看到功能的恢复！

听起来是个好计划！如果你想了解更多关于 Yeelight 智能 RGB 灯泡的信息，请查看本文。简而言之，这款 WiFi 灯集成了 Tasker，因此无需黑客攻击。它也支持亚马逊 Alexa 和谷歌助手！我将向您展示如何在手机上下颠倒时触发人工日落，以及如何创建一个警报来逐渐打开您房间的灯。

* * *

## Tasker 和 Yeelight 日落和日出行为

[app box Google play com . yee light . cherry]

[app box Google play com . joaomgcd . autotools]

[app box Google play com . ter delle . twilight]

为了省事，我用了暮光之城的 Tasker 插件，它能告诉 Tasker 现在是白天还是晚上。我有一个日夜触发器，它将变量**%我要用这些来控制 Tasker 和 Yeelight 触发器。**

### TASKER 个人资料黄昏日出/日落

```
Profile: Sunlight Day 状态:暮光[配置:在设备位置从日出到日落。]回车:阳光运算符+A1:变量集[名称:%日光至:天递归变量:Off 做数学:Off 追加:Off ]简介:阳光之夜状态:暮光[配置:在设备位置从日落到日出。]输入:阳光操作员-A1:变量集[ Name:%Sunlight To:night递归变量:Off 做数学:Off 追加:Off ]
```

### 日落

由于 Yeelight 应用程序带有非常简洁的预设，我们可以用它来创建日落行为。预设持续 15 分钟，从暖橙色/红色到暗淡的颜色，最后完全熄灭。

### TASKER 个人资料-日落

```
Profile: Sunset 状态:方向[是:面朝下]状态:Wifi 已连接[ SSID:FASTBERRY MAC:* IP:*活动:是]状态:变量值[%日光~夜晚]进入:日落A1: Yeelight 设备[配置:设备:灯，动作:场景，参数:70 超时(秒):0 ]
```

如果你想延长/缩短人造日落，你可以使用应用程序创建一对夫妇的颜色预设，并在 Tasker 混合使用等待和亮度动作的组合。

在我的场景中，我使用了 WiFi 信息和**%阳光**的值来防止 Yeelight 智能灯泡意外切换日落模式。随意分配另一个触发器或语音命令。

### 日出

日出行为最好与设定的闹铃相结合。在我的场景中，我在闹钟响前 5 分钟开灯。一开始光线很暗，然后在接下来的 15 分钟内改变颜色和亮度，直到达到最大亮度。

#### Tasker 和 Yeelight 报警器

我使用自动工具来获得正确的时间选择器对话框。如果你想制造一个场景，请随意。你也可以把它和语音命令联系起来。无论什么适合你，只要你得到 15:43 格式的时间就很棒。

### TASKER 任务-警报

```
Alarm A1:自动工具对话框[配置:对话框类型:日期和时间选择时间:真时间选择器标题:设置闹钟格式:小时:分钟日期格式分隔符:，超时(秒):60 ]A2:变量集[Name:% sun rise 1 To:% at datetime seconds-300递归变量:Off 做数学:On 追加:Off ]A3:变量集[Name:% sun rise 2 To:% at datetime seconds-300递归变量:Off 做数学:On 追加:Off ]A4:变量 Split[Name:% at datetime 1 Splitter::Delete Base:Off]A5:设置闹钟[小时:%在日期时间 11 分钟:%在日期时间 12标签:带灯声音:振动:默认确认:关闭]
```

##### A2、A3

通过自动工具设置的时间以秒为单位，我们可以直接使用它来指定 **%Sunrise1** 和 **%Sunrise2** 的值(我们需要它来创建时间上下文并绕过任何[时间问题](http://www.notenoughtech.com/tasker/time-event-conditions-in-tasker/))。

##### A5 号

但是，要设置闹钟，我们需要单独提供给我们的小时和分钟。我们可以用“:”拆分现有变量 **%atdatetime1** ，如 **A4** 所示。完成后，我们得到了小时的 **%atdatetime11** 和分钟的**%**

#### 日出轮廓

是时候(没有双关的意思)设置环境和触发 Yeelight 了。动作很简单，选择 Yeelight 动作，场景设置为日出。根据上下文，使用时间，并分配 **%Sunrise1** 和 **%Sunrise2。**

### TASKER 个人资料-日出

```
Profile: Sunrise 时间:从% 1 日出到% 2 日出状态:变量值[%日光~夜晚]进入:日出A1: Yeelight 设备[配置:设备:灯，动作:场景，参数:68 超时(秒):0 ]
```

## 结论和下载

如你所见，Tasker 和 Yeelight 几乎是天作之合。当你入睡时，灯光看起来很棒，希望它能减轻早起的压力。我已经向 Yeelight 团队传达了关于支持 Tasker 变量的反馈。如果亮度、颜色和场景都可以用变量来表示就好了。

[**下载 Tasker Yeelight 轻轻唤醒项目**](https://www.androidfilehost.com/?fid=745849072291683200)

下载上面的 ZIP 文件，并将内容解压缩到您的 Android 设备的内部存储中。打开 Tasker，在首选项中禁用“初学者模式”。然后，回到 Tasker 的主页，长按左下角的 home 图标。您将看到一个“导入”项目的选项。点击该选项，然后找到您之前提取的. prj.xml 文件。导入后，您将会在 Tasker 的默认主页图标旁边的底部看到一个新标签。它包含这个助手项目的概要文件和任务。

跟随 [XDA 开发者教程](https://www.xda-developers.com/category/tutorials/)获取更多这样的帖子。此外，查看我们的 [Tasker Tips & Tricks](https://forum.xda-developers.com/u/tasker-tips-tricks) 论坛，了解我们社区中自动化爱好者的最新创造。