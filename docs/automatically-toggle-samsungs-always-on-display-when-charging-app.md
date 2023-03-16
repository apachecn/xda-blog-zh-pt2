# 充电时自动切换三星的始终显示[App]

> 原文：<https://www.xda-developers.com/automatically-toggle-samsungs-always-on-display-when-charging-app/>

三星因其软件的性能优化受到了很多批评(尽管这些批评有多少是合理的和/或准确的是另一个时间的争论)，但很难否认他们的软件带来了多少附加值。我可以继续讲述你在 Samsung Experience(以前称为 TouchWiz)上可以找到的所有功能，但今天我将专注于如何让一个功能稍微好一点:始终显示。具体来说，如何在充电时**自动启用 Always on Display，而在不充电时**禁用。

对于那些不了解情况的人来说，三星的永远显示(AOD)功能是一种特殊的屏幕模式，在 Android 超时时显示。在这种模式下，你可以快速看到当前的日期、时间、消息、日历事件，以及更多的[可定制功能](https://play.google.com/store/apps/details?id=com.samsung.android.app.aodservice)。AOD 是三星 Galaxy S7 和 S8 系列智能手机的专属，是一种无需触摸手机就能快速浏览重要信息的有用方式。

AOD 可以根据设置中的时间表自动切换，但除此之外，没有多少其他上下文可以用来控制 AOD 何时激活。幸运的是，借助 Tasker 的强大功能，我们可以设置 AOD 开启/关闭时想要触发的任何上下文。我做了一个**简单的应用程序，你可以在你的三星 Galaxy S7、S7 Edge、S8 或 S8+上安装并忘记它，当只给**充电时，它会打开 AOD，但我也会告诉你如何设置你想要的任何其他上下文。

[**从 XDA 实验室**下载 AOD 充电 App](https://labs.xda-developers.com/store/app/tasker.xda.aodcontrol)

**注:以上 app 是用 Tasker 配合 Tasker App Factory 制作的。它没有用户界面。请在安装后隐藏应用程序抽屉中的应用程序图标。你可以通过下面的步骤看到这个应用程序是如何制作的。**

* * *

## 教程-在自定义上下文中触发 AOD 模式

### 要求

虽然我在这里使用 Tasker，但你可以自由使用你选择的任何其他自动化应用程序。Tasker 是目前最流行的，也是大多数人最熟悉的，所以我用的就是它。

### 选项 1 -连接到特定 WiFi 网络时切换 AOD 模式

以下是如何设置该脚本的分步说明。我将重点介绍当您连接/断开您的家庭/工作 WiFi 网络时启用/禁用 AOD 模式，但您可以设置任何其他您想要的触发器。

1.  打开 Tasker，点击右下角的+按钮，创建一个新的配置文件。
2.  点击“状态”以添加状态上下文。
3.  选择“网络”，然后选择“WiFi 已连接”
4.  在 SSID 下，点击放大镜以显示保存的 SSID 列表。在此选择您想要的 WiFi 网络。
5.  按下返回键，Tasker 将要求您附加一个现有的任务或创建一个新的任务。选择“新任务”不用费心去命名了。
6.  进入任务编辑屏幕后，点击底部中间的+图标添加操作。
7.  选择“代码”，然后选择“Java 函数”
8.  点击咖啡图标并选择上下文。
9.  点击 Function 附近的放大镜，搜索 getContentResolver()。
10.  一个新的“返回”字段应该显示在顶部。在此输入“cr”。按 back 返回任务编辑屏幕。
11.  添加另一个 Java 函数动作(步骤 6-7)。这一次，对于类别或对象字段，点击放大镜并查找 Settings$System。对于功能字段，点击放大镜并选择输入。现在将出现一组参数。对于参数(ContentResolver ),点击咖啡杯并选择“cr”对象。对于参数(字符串),输入 aod_mode。对于 Param (int ),输入 1。
12.  按 back 返回任务编辑屏幕。现在长按我们做的两个动作，点击剪贴板按钮来复制它们。按 back 退出 Tasker 的主屏幕。
13.  在 Tasker 的主屏幕上，长按我们刚刚创建的任务，点击“添加退出任务”不要为任务命名。
14.  当您在新任务的编辑屏幕中时，长按屏幕中间的任意位置，直到粘贴操作出现。点击以粘贴我们之前复制的两个操作。
15.  点击此处的操作#2 并向下滚动。将 Param (int)下的 1 更改为 0。点击返回按钮，直到你回到 Tasker 的主屏幕，你就完成了！

### 选项 2 -当设备面朝上放在桌子上时触发 AOD 模式

以下是如何设置该脚本的分步说明。我将重点介绍当您的设备正面朝上时启用/禁用 AOD 模式。

1.  打开 Tasker，点击右下角的+按钮，创建一个新的配置文件。
2.  点击“状态”以添加状态上下文。
3.  选择“传感器”，然后选择“方向”
4.  在“是”下面，确保写着“面朝上”
5.  按下返回键，Tasker 将要求您附加一个现有的任务或创建一个新的任务。选择“新任务”不用费心去命名了。
6.  进入任务编辑屏幕后，点击底部中间的+图标添加操作。
7.  选择“代码”，然后选择“Java 函数”
8.  点击咖啡图标并选择上下文。
9.  点击 Function 附近的放大镜，搜索 getContentResolver()。
10.  一个新的“返回”字段应该显示在顶部。在此输入“cr”。按 back 返回任务编辑屏幕。
11.  添加另一个 Java 函数动作(步骤 6-7)。这一次，对于类别或对象字段，点击放大镜并查找 Settings$System。对于功能字段，点击放大镜并选择输入。现在将出现一组参数。对于参数(ContentResolver ),点击咖啡杯并选择“cr”对象。对于参数(字符串),输入 aod_mode。对于 Param (int ),输入 1。
12.  按 back 返回任务编辑屏幕。现在长按我们做的两个动作，点击剪贴板按钮来复制它们。按 back 退出 Tasker 的主屏幕。
13.  在 Tasker 的主屏幕上，长按我们刚刚创建的任务，点击“添加退出任务”不要为任务命名。
14.  当您在新任务的编辑屏幕中时，长按屏幕中间的任意位置，直到粘贴操作出现。点击以粘贴我们之前复制的两个操作。点击此处的操作#2 并向下滚动。将 Param (int)下的 1 更改为 0。点击返回按钮，直到你回到 Tasker 的主屏幕，你就完成了！

*注意:图片格式的其余步骤可以按照与选项#1 中的前一组截图完全相同的方式进行。从第二行截图开始，继续往下看。*

* * *

### 结论

正如你所看到的，你可以启用或禁用始终显示模式，基本上任何情况下，你想感谢 Tasker。我做的这个简单的应用程序旨在涵盖 AOD 最常要求的功能版本，但如果你想在 AOD 之外有所不同，那么做出这些改变的权力就在你手中。