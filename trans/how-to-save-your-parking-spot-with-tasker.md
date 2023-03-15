# 如何用 Tasker 节省你的停车位

> 原文：<https://www.xda-developers.com/how-to-save-your-parking-spot-with-tasker/>

如果你已经注册并经常使用 Google Now，你可能会看到“我在哪里停车”的卡片。每当谷歌认为你已经停止驾驶并离开车辆时，就会显示这张附加卡。

我不经常开车，而是到处骑自行车，每次谷歌给我这张卡，我都觉得很荣幸。这证明谷歌还不知道我们的一切，但如果你足够快，这张卡可以用来再次找到你的自行车(除非它被偷了)。

随着我即将到来的中国之旅，我意识到谷歌服务不会在我的日常生活中帮助我。中国屏蔽谷歌。当然，这也意味着不再有 Google Now 了。如果你足够幸运去 Google 不能去的地方旅行，或者你不是 Google Now 的粉丝，你可能会有兴趣复制下面的简介。如果没有，您可以滚动到底部下载并导入项目文件。

这个项目最初是由米沙·拉赫曼创建的，但通过讨论、实验和合作，后来我自己扩展了这个项目。

* * *

## 伙计，我的车呢？拯救我的停车位

这个配置文件相当简单。在我的设置中，我已经使用桌面小工具保存了我的停车位。然而，如果你更喜欢使用语音激活或通知按钮，我已经为这些情况提供了以下说明。在任何情况下，当配置文件被激活时，位置被存储在一个变量中，并在需要时被调用。

值得指出的是，Android 在管理您的位置访问方面做得相当不错，以确保最小的电池消耗，但如果您喜欢禁用您的位置服务，您必须启用位置服务，以便 Tasker 可以获得位置修复。您启用的定位服务越多，修复速度就越快。

默认情况下，Android 将在“高性能”模式下使用 GPS、移动数据和 WiFi 来检查您的位置。如果您总是让定位服务开着，请继续下一部分。否则，您可以使用 Tasker 中的 below *run shell* 操作来切换位置(需要 root)。

```
settings put secure location_providers_allowed=gps,network,wifi
```

或者，您可以使用安全设置插件来切换这些设置([这里的](http://www.notenoughtech.com/tasker/secure-settings-nougat/)是如何在 Android Nougat 上进行安全设置)。最后，对于那些没有 root 权限的人，如果你[授予自动工具](https://joaoapps.com/AutoApps/Help/Info/com.joaomgcd.autotools/com.joaomgcd.autotools.activity.ActivityConfigsettings.html)SECURE _ SETTINGS 权限，你就可以使用那个插件切换位置。

## 保存位置

### 保存位置

```
LocCar 中止现有任务A1:变量 Clear [ Name:%LastLocation 模式匹配:Off ]A2:通知取消[标题:位置问题警告不存在:关闭]A3:获取位置[源:任何超时(秒):20 立即继续任务:关保持跟踪:关出错后继续任务:开]A4:变量集[Name:% last location To:% LOC Recurse Variables:Off Do Maths:Off Append:Off]A5:通知[标题:位置保存文本:点击导航图标:hd_location_place 编号:0 永久:关闭优先级:5 ]如果[ %LastLocation Set ]A6:设置小部件图标[Name:loc car Icon:content://com . Android . external stage . documents/document/primary % 3a material-Icons-010317-032209% 2 fres % 2 fdrawable-xxxhdpi % 2 fic _ car . png]If[% last location Set]A7: Notify [ Title:位置问题 Text:很抱歉无法设置位置。图标:hd_aaa_ext_car 编号:0 永久:关闭优先级:5 动作:(1) ]如果[ %LastLocation！设置]A8:设置 Widget Icon[Name:loc car Icon:content://com . Android . external storage . documents/document/primary % 3a material-Icons-010317-032710% 2 fres % 2 fdrawable-xxxhdpi % 2 fic _ car . png]If[% last location！设置]
```

### 获取位置(A1-A4)

在定位之前，我想做几件事。因为大多数时候 **%LOC** (Tasker 的全局位置变量)已经被赋予了一个值(最后一次定位)，所以我只想使用通过概要文件请求的位置坐标。我将使用全局变量 **%LastLocation** 来存储这些坐标。如果任务由于错误或超时而再次运行，我需要用通知取消操作清除现有的警告通知。

### 通知(A5、A7)

“获取位置”操作有两种结果。我们将以一组新的坐标结束，否则操作将无法获取坐标。如果找到了修复方法，将会显示一个通知。请注意此通知的名称。稍后我们将使用这个名称来触发返回位置配置文件。如果没有进行位置定位，或者坐标与获取位置操作之前的坐标相同，我们希望显示一条警告，并提供再次运行相同任务的选项(操作执行任务分配为按钮)。

### 按钮(A6、A8)

我早些时候提到，将有一个按钮，它会改变颜色，以显示我们的停车配置文件的状态。颜色代码是:

*   白色(就绪)
*   红色(失败)
*   绿色(武装)

你所需要的是一个 Tasker 小工具(不是快捷方式)放在你的主屏幕上，用于保存位置的任务。确保为此任务分配一个图标，以便能够从小部件屏幕添加任务快捷方式。我用这个代替快捷方式，因为我让 Tasker 根据当前状态改变图标的颜色。

我最喜欢的获取图标的方式之一是材料设计图标收集，因为你可以找到适合你的图标，并快速提供它的颜色选择。

我已经标记了这些行动，以显示哪一个与失败/成功结果相对应。IF 条件**% lastlocation**=**置位/未置位**决定了结果。

## 返回位置

### 返回位置

```
 ReturnLocation A1:发送意图[Action:Android . Intent . Action . view Cat:None Mime Type:Data:Google . navigation:q = % last location & mode = w Extra:Extra:Extra:Package:com . Google . Android . apps . maps Class:Target:Activity]A2:设置小工具图标[Name:loc car Icon:content://com . Android . external stage . documents/document/primary % 3a material-Icons-010317-032200% 2 fres % 2 fdrawable-xxxh dpi % 2 fic _ car . png]A3:等待[毫秒:0 秒:3 分钟:0 小时:0 天:0 ]A4:变量清除[名称:%LastLocation 模式匹配:关]
```

任务很简单。我们将运行一个包含位置链接的谷歌地图意向:

```
Action: android.intent.action.VIEW

数据:Google . navigation:q = % last location & mode = w

package:com . Google . Android . apps . maps

目标:活动
```

我们的 location 全局变量将提供必要的坐标。一旦完成，我们只需要清理变量(请添加一个等待动作)并将小部件图标的颜色改为白色。

### 配置文件:返回位置

### 返回位置配置文件

```
Profile: Return To Location事件:通知单击[所有者应用:*标题:位置已保存]输入:返回位置
```

现在我们已经设置了汽车的位置，我们将创建一个配置文件，当我们稍后手动请求汽车的位置时会触发该配置文件。要从我们之前创建的通知中触发此任务，请创建一个事件**通知，单击**并添加之前创建的通知的名称(保存的位置)

现在，您已经准备好了一个完整的配置文件。

### 使用语音命令

### 自动语音描述文件

```
Profile: Save Location事件:自动语音识别[配置:简单命令:保存我的位置，保存这个位置，保存我的停车位，保存这个停车位，记住我的停车位，记住我的位置，标记这个位置，标记这个停车位，标记这个停车位回应:好的，我会帮你保留停车位]输入:LocCar
```

如果您希望添加一个语音触发器来保存您的停车位位置，请使用**自动语音识别**事件创建一个配置文件。在输入中填入您可能会使用的语音命令，用逗号分隔。如果你想听到回应-包括一个在回应菜单中。一旦完成，将它与之前创建的 **LocCar** 任务链接起来。

如果您希望使用自动语音命令来查找您保存的位置。创建一个新的自动语音识别事件，并将其链接到 **ReturnLocation** 任务。

* * *

## 结论

很容易假设每个人都可以访问相同的资源，但事实并非如此。如果你发现自己需要一个简单的方法来节省你的停车位，而不依赖于谷歌服务，或者你只是喜欢完全避免谷歌服务，这个项目是给你的。

这个项目还可以修改，用于其他用途，不像 Google Now 的停车卡，所以看看你能不能想出更好的东西。您还可以尝试自动通知，使通知更漂亮或更具互动性。我让整个项目接近普通的 Tasker 体验(除了使用 AutoVoice)。

[**在这里下载项目！**](https://www.androidfilehost.com/?fid=745425885120698997)

为了导入 Tasker 项目文件，请下载上述文件并将其保存在内部存储器中的任何位置。打开 Tasker 并检查以确保“初学者模式”在首选项菜单中被禁用。然后，长按左下角的“主页”图标，点击“导入”。找到您之前保存的 prj.xml 文件，并选择它进行导入。现在，您将在底部一行看到一个新的选项卡，包含我们在本文中引用的所有概要文件和任务。

我们希望你喜欢我们的这个小发明，如果你认为我们可以做任何改进，请告诉我们！