# Tasker Beta 可让您导出到 URL 并监控更改设置

> 原文：<https://www.xda-developers.com/tasker-export-url-monitor-settings/>

在[收购了名为 Tasker 的流行自动化应用](https://www.xda-developers.com/tasker-autoapps-interview-joao-dias/)后，开发者 joo Dias 一直在努力改进该应用。他的第一个测试版增加了[安全设置权限](https://www.xda-developers.com/tasker-beta-secure-settings-permission-lock-screen-screenshot-action-android-p/)，因此用户可以在他们的设备上自动进行任何设置。他的第一个公开版本对此进行了扩展，将它变成了应用程序中的一个动作，他还通过[添加运行时权限和对 Magisk root 的支持](https://www.xda-developers.com/tasker-v5-2-immersive-mode-runtime-permissions/)对应用程序进行了现代化。现在，该应用程序的最新测试版增加了两个令人兴奋的新功能:将任务/配置文件/项目导出到 URL 以便于共享的能力，以及监控设置更改的新事件和状态上下文。

### 导出到 URL

我们是 XDA 自动化的超级粉丝。作为 Tasker 多年的忠实用户，我见证了这款应用在用户界面和功能上的诸多变化。但是 Tasker 还没有发展的一个领域是它的备份和共享功能。乱七八糟。导出和导入您的工作一直是一件痛苦的事情，因为您需要将您的任务/档案/项目导出为 XML 文件，像 Google Drive 帐户一样共享该文件，让某人下载该 XML 文件，然后指示他们打开 Tasker 并手动导入它。有了新的导出到 URL 功能，许多工作都被删除了，因为您只需要共享一个 URL 供其他人导入您的工作。用户只需从他们的设备上点击链接，它就会被导入！

这是开发者展示这一特性的视频:

### 监视器设置

这是我亲自要求开发者添加的一个特性，我真的很高兴看到它最终被包含进来:监控设置的能力。安全，设置。全局和设置。用于更改的系统表！在 XDA 上，我们过去发布过许多利用这些隐藏设置表的教程。一些例子包括:[在 Android Oreo 上启用“自动打开 WiFi”功能](https://www.xda-developers.com/turn-on-wifi-automatically-nexus5x-nexus6p/)，[自定义电池节电触发百分比](https://www.xda-developers.com/change-battery-saver-trigger-percent-start-when-screen-off/)，[减少超过最低值的长按延迟](https://www.xda-developers.com/how-to-reduce-the-long-press-delay-beyond-its-lowest-setting/)，[启用全系统沉浸式模式](https://www.xda-developers.com/how-to-enable-system-wide-immersive-mode-without-root/)，[禁用高音量警告](https://www.xda-developers.com/how-to-automatically-disable-the-high-volume-warning-without-root/)，[在 Android Oreo 上自定义电池节电](https://www.xda-developers.com/customize-battery-saver-mode-android-8-0/)，以及[在 Android 8.1 Oreo 上取消圆角和状态栏填充](https://www.xda-developers.com/google-pixel-2-rounded-screen-corners/)。

如果你曾经在你的设备上看到一个设置，并希望你能在它上面添加一些额外的动作，这个新功能就是为你准备的！例如，我已经弄清楚如何在 Android P 开发者预览版 4 中**每当夜灯打开**时自动启用黑暗主题。俏皮！([你可以在这里查看如何操作](https://www.xda-developers.com/enable-android-p-dark-theme-night-light/)。)

设置它非常简单。您所要做的就是创建一个新的概要文件，或者在现有的概要文件上添加一个额外的上下文，并选择一个新的“自定义设置”选项。您可以将其视为系统事件或系统状态。状态假设您知道要寻找什么值，因此不会在任务中给出变量输出，而事件会将结果存储在%evtprm 数组中(最重要的信息存储在%evtprm3 中。)

一旦选择了事件或状态上下文，就需要指定要监视的设置是安全设置、全局设置还是系统设置。然后，将设置的名称放入 name 部分，如果希望概要文件在某个值上触发，还可以选择放入值。例如，我输入“night_display_activated”并将值设置为“1 ”,这样每当夜灯启用时，我的配置文件就会触发。

如何找到设备上可用的设置？它高度依赖于设备/OEM，所以没有主列表。但是，查找设置的最佳方法是将您的设备连接到 PC，并运行以下 ADB 命令:

```
 adb shell settings list system
adb shell settings list global
adb shell settings list secure 
```

由您来决定每个值的含义。不过，简单的谷歌搜索通常会帮你找到答案！

或者，Tasker 有一个内置的设置列表，您可以查看。它不会像 ADB 命令那样列出每个设置，但是它应该包含大多数设置。您可以通过在状态/事件设置期间按下放大镜，然后点击“选择设置”来访问它

## 下载 Tasker Beta 5.2.bf6

如果你想下载这个版本的 Tasker，你首先需要在这里注册测试程序。然后，从 Play Store 购买应用程序，并确保您下载的是版本 5.2.bf6，因为这是最新的测试版！

## Tasker Beta 5.2.bf6 变更日志

这是完整的变更日志，供感兴趣的人参考。

增加

*   **导出为 URL** :彻底改变共享 Tasker 数据的方式。Tasker/配置文件/项目可以导出为 URL，要导入它们，用户只需点击安装了 Tasker 的 URL
*   **自定义设置状态/事件**:监控 Android 的设置，这样你就可以对它们的变化做出反应。例如，当夜灯开启时，调低音量
*   新的州和事件的徽章
*   使用 **wifi 系绳**保持 Wifi 开启的选项
*   将自动找到更多自定义设置

变化

*   如果 Tasker 拥有写入安全设置权限，SMS 应用程序操作现在将在没有提示的情况下设置它
*   更新的支持电子邮件地址

错误修复

*   修复了**数组集**未清除先前存在的同名数组的问题
*   在状态附近的 **Wifi 连接**和 **Wifi 时请求位置许可**
*   修复了从名称以“Tasker”开头的文件夹打开文件的问题
*   修正了从外部 Tasker 运行时生物特征对话框不显示的问题
*   修复了运行**创建目录**操作时的错误消息
*   修正了不能一次删除多个配置文件的问题
*   修正了安卓系统的无线网络共享问题
*   当 Tasker 在其主屏幕上时，如果其他应用程序打开，请不要退出 Tasker