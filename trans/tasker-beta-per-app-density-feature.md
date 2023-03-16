# Tasker 测试版增加了流行的偏执 Android 每应用程序密度功能

> 原文：<https://www.xda-developers.com/tasker-beta-per-app-density-feature/>

# Tasker 测试版增加了流行的偏执 Android 每应用程序密度功能

Tasker Beta 增加了显示尺寸动作特性。它使用户能够基于每个应用程序修改显示密度(DPI)。

显示密度以每英寸点数(DPI)来衡量。它确定给定设备显示器上 UI 元素的大小。更高的显示密度意味着用户可以一次看到更多的界面元素。另一方面，较低的显示密度意味着较少的 UI 元素将在显示器上可见，并且元素将更大。Tasker [Beta](https://www.xda-developers.com/tasker-export-url-monitor-settings/) 现在增加了一个**显示尺寸**选项来动态改变显示尺寸。

概括地说，Android 7.0 Nougat 引入了一个显示尺寸调整工具，使用户能够改变显示密度(例如，从“大”到“小”)，而不必使用 ADB。然而，Android 中的显示尺寸调整工具是全球通用的。如果用户设置更高的显示密度，那么他们将在每个应用程序和系统 UI 中看到更多的用户界面元素(如显示器上更多的文本行)。他们不能在每个应用程序的基础上动态调整显示密度。

在过去，偏执的 Android (PA)有一个流行的功能，允许用户在每个应用程序的基础上设置 DPI。例如，他们可以为系统设置较高的 DPI，但为谷歌 Play 商店或谷歌 Chrome 等应用程序设置较低的 DPI。新的偏执型 Android 版本中没有该功能。Joao Apps 现在已经将该功能添加到 Tasker Beta 5.3b 中。

该功能的工作方式很简单:用户可以选择**动作类别>显示动作>显示大小**，然后编辑显示密度，从**最小**到**最大。**

最新 Tasker 测试版中的其他新功能包括切换 NFC 开关、隐藏状态栏图标和强制显示旋转。

Tasker 5.3b 的完整变更日志如下所示:

### 变更日志

新操作:

*   **显示尺寸动作**:动态改变你的显示尺寸。
*   **NFC 动作**:开启或关闭 NFC
*   **状态栏图标**:隐藏状态栏上的图标。
*   **强制旋转**:强制旋转显示器。

其他添加、更改或错误修复:

*   当从 URL 导入数据时，在导入之前，增加了显示导入内容描述的选项。
*   向清单添加了 android.permission.DUMP 权限
*   当 Tasker 崩溃时，会生成一个通知，这样用户可以直接向开发人员报告崩溃
*   如果设备是根设备**,结束调用**将与根设备一起执行，因此它始终工作
*   如果需要，写入文件操作会创建缺失的目录
*   修复了由于载体阻塞导致 wifi 连接失败时的崩溃问题
*   修正了一些对话框在 Android 后退按钮被按下时接受积极动作的问题

* * *

[**来源:若昂应用**](https://groups.google.com/forum/#!topic/tasker/F5PJ3G_1XYw)