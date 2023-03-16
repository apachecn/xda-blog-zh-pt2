# 首先看看谷歌 Pixel 4 的 Android 10 实时字幕功能

> 原文：<https://www.xda-developers.com/android-10-live-caption-google-pixel-4/>

除了新一代谷歌助手，谷歌在今年的 I/O 上展示的 Android 10 最酷的新功能之一是实时字幕。这是谷歌推动 Android 对听力障碍等残疾用户更容易使用的一部分，它所做的是将设备上播放的音频转录成字幕，浮在屏幕上。它可以离线使用，也可以和大多数在手机上播放音频的应用程序一起使用，包括视频和播客。谷歌在 I/O 上播放的一个预先录制的视频中演示了这项功能，但他们不会像 Live Transcribe 一样立即提供这项功能，而是将它推广到“今年晚些时候选择运行 Android Q 的手机”由于我们从 Pixel 4 XL 获得了一个未发布的 APK，我们设法在该功能正式发布之前获得了直播字幕。这是我们第一次看到这个新特性。

多亏了 [*Nextrift*](https://nextrift.com/) ，我们从 Pixel 4 中获得了大量的 APK，包括[动作感应 APK](https://www.xda-developers.com/google-pixel-4-motion-sense-list-countries-supported-apps/) 和[新的实时壁纸](https://www.xda-developers.com/download-google-pixel-4-live-wallpapers-port/)。他们还发给我们一个未发布版本的“设备个性化服务”这个应用程序负责在最近的应用程序概述和 Pixel Launcher 应用程序抽屉中显示应用程序快捷方式，它也允许 Pixel 所有者在最近的应用程序概述中选择文本和图像。该应用的 1.6.255525616 版本在技术上比公开发布的版本更老 APKMirror 上的最新版本是 2 . 0 . 268948072——但它从未公开发布。在我的 Pixel 2 XL 上安装了这个 APK，并进行了一些其他调整，我能够在 Android 10 的设置中显示实时字幕。

正如你在下面左边的第一张截图中看到的，直播字幕的主设置页面有 3 个选项。第一个选择是改变语言，尽管目前仅限于英语，因为这是发布时唯一支持的语言。遗憾的是，没有任何迹象表明将来还会支持哪些语言。接下来，我们可以看到一个切换来掩盖亵渎。这将在标题中用星号替换脏话。最后，在音量面板中有一个显示实时字幕切换的选项。除了这三个开关，底部还有一个简短的视频演示和解释其工作原理的文本。

当该功能首次检测到正在播放音频时，您会看到一个对话框出现。你可以通过向下滑动通知面板，展开“实时字幕”通知，然后点击“停止”按钮来停止字幕。你也可以像使用画中画窗口或[气泡](https://www.xda-developers.com/android-q-system-alert-window-deprecate-bubbles/)一样，向下拖动标题以消除它。

默认情况下，在纵向模式下，字幕显示在屏幕中间，在横向模式下，字幕显示在屏幕底部稍上方。您可以轻按并上下拖动标题来重新定位它，或者双击标题来展开它。

我在 YouTube、Google Podcasts、Google Photos、Amazon Prime Video 和网飞测试了这一功能，它在所有这些应用程序中都有效。它的准确性足以让我在不提高音量的情况下理解所说的内容，但在正式发布之前，我不想全面回顾或测试该功能。

实时字幕在电话、语音或视频通话中不起作用，因为此功能使用的 API 存在限制。同样的 API 允许在 Android 10 中录制[内部音频，尽管由于设备个性化服务是一个系统应用，它](https://www.xda-developers.com/android-10-record-internal-game-audio/)[比屏幕录制应用有更少的限制](https://www.xda-developers.com/android-q-record-audio-monitor-device-temperature/)。

这是一段展示我的 Pixel 2 XL 功能的屏幕录像。正如你所看到的，它基本上捕捉到了 TK 在他的[一加 7T](https://www.xda-developers.com/tag/oneplus7t) 拆箱视频中所说的话，尽管这里那里有一些错误。

谷歌表示，由于内存和空间的限制，直播字幕将适用于“精选的高端设备”。该公司计划在我们接近稳定的 Android 10 发布时发布一系列支持该功能的设备，但显然这从未发生。我打赌谷歌将在 Pixel 4 上推出该功能，但奇怪的是，在没有设备具备该功能的情况下，他们一直在 Android 10 的官方网页上宣传该功能。一旦该功能面向用户推出，我们会通知您。