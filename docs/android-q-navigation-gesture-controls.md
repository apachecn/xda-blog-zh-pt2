# Android Q:放弃后退按钮，实现完整的导航手势控制

> 原文：<https://www.xda-developers.com/android-q-navigation-gesture-controls/>

我在 1 月中旬获得的 Android Q 的泄露版本透露了下一个 Android 版本的许多重大变化。[全系统黑暗模式](https://www.xda-developers.com/android-q-dark-mode-overview/)、[隐私和权限改进](https://www.xda-developers.com/android-q-privacy-permission-controls/)和[新桌面模式](https://www.xda-developers.com/android-q-desktop-mode/)是亮点，但后来我发现谷歌正在原型制作[改进的导航手势控件](https://www.xda-developers.com/android-q-gestures-back-button/)，取消了后退按钮。面向所有三代 Pixel 智能手机的新 [Android Q beta](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/) 仍然具有谷歌对手势导航的实验性改变，由于一些隐藏的设置，你现在就可以启用它们。

如果你想看看 Android Q 的新手势与 Android Pie 的手势相比如何，这里有一个我上个月做的视频。然而，请注意，我后来发现 Android Q 的手势有更多的功能，包括它们是(部分)可定制的！

谷歌很可能不会让你在[最终 Android Q 版本](https://www.xda-developers.com/android-q-beta-release-schedule/)中实际自定义导航手势。我发现的只是他们的原型功能，他们可能用它来测试不同的手势控制设置，看看哪个是最好的。不过，既然这个功能已经存在，我们不妨利用它来改进 Android Pie 的手势。

**要求:**

*   运行 Android Q 测试版的 Google Pixel、Google Pixel XL、Google Pixel 2、Google Pixel 2 XL、Google Pixel 3 或 Google Pixel 3 XL
*   在您的电脑上设置 Android 调试桥(ADB)。我们在这里有一个关于如何建立亚洲开发银行的教程。

## 如何在 Android Q 中去掉全导航手势的后退键

*特别感谢 XDA 公认的开发者[扎卡里 1](https://forum.xda-developers.com/member.php?u=7055541) 和[乔奥姆克德](https://forum.xda-developers.com/member.php?u=4805489)(Tasker 开发者)，感谢他们协助破译这是如何工作的！*

在我向您展示任何命令之前，让我解释一下这是如何工作的。有一个隐藏的设置。名为“quick step controller _ gesture _ match _ map”的全局首选项，采用 6 位或 6 位以上的整数值。偏好设置接受 1-7 之间的数字(忽略 0、1 和 8)，您输入数字的顺序决定了药丸推送手势将采取的操作。

以下是可能的操作:

1.  快速步骤(进入最近的应用概述)
2.  QuickScrub(在按住药丸的同时左右移动手指，在最近的应用程序之间循环)
3.  后退(回去)
4.  快速切换(快速切换到上一个应用程序)
5.  空(什么都不做)
6.  助手(启动默认的助手应用程序)
7.  通知面板(下拉通知面板)

以下是手势映射的顺序:

1.  向上滑动
2.  向下滑动
3.  向左滑动
4.  向右滑动
5.  未知的
6.  未知的

我还没搞清楚第 5 和第 6 个手势是什么。无论我怎么尝试，我都无法改变单击 home 键和长按 home 键的动作。如果我发现如何重新映射这些动作，我会更新这篇文章。

因此，这里有一些 ADB 命令的例子，你可以发送来更好地改变 Android Q 的手势。(对于以下 ADB 命令，如果您在 Windows 上使用 PowerShell，请在命令前加上一个“. \”(无引号)。如果您使用的是 macOS 或 Linux，请在命令前加一个“.”。/(无引号)。)

### 示例 1:新的后退手势、向下滑动通知、旧的快速切换动画

这是我现在首选的设置，因为在最近的应用程序之间切换的新过渡动画，如前面的视频所示，有点问题。这个 ADB 命令将使你可以向左滑动药丸返回(使后退按钮多余)，向下滑动下拉通知面板(超级有用！)，最后保留 Android Pie 最近应用滚动。

1.  在存储 ADB 二进制文件的目录中打开命令提示符或终端窗口。
2.  将你的 Pixel 手机接入你的电脑。
3.  要去掉后退按钮，输入这个命令:

    ```
     adb shell settings put global quickstepcontroller_hideback 1 
    ```

4.  运行以下命令来更改手势药丸行为:

    ```
     adb shell settings put global quickstepcontroller_gesture_match_map 173255 
    ```

### 示例 2:新的后退手势、向下滑动通知、新的快速切换动画

如果你想尝试 Android Q 的最后一个应用程序动作的新过渡动画，你可以用 1 替换第四个位置的 2。请注意，过渡看起来有点古怪，因为它仍然是一个正在进行中的工作，并且你不能在主屏幕上向右滑动药丸。我想至少看起来不错。

1.  遵循上一节中的步骤 1-3。
2.  运行该命令:

    ```
     adb shell settings put global quickstepcontroller_gesture_match_map 173155 
    ```

### 救命啊！我的电话一直死机！我想要回以前的手势！

还记得我说过偏好取 6 位数或更多的值吗？嗯，我是认真的。如果你输入 5 位数或更少的整数，这个方法就不能处理它，SystemUI 就会反复崩溃。幸运的是，这很容易解决。您可以重新输入上述命令之一，这次使用一个 6 位数的值，或者您可以通过发出以下命令来重置手势:

```
 adb shell settings put global quickstepcontroller_hideback 0
adb shell settings delete global quickstepcontroller_gesture_match_map 
```

* * *

尽情体验 Android Q 中的新手势吧！这篇文章只给你一小部分谷歌正在幕后做的工作，以改善 q 中的手势控制。至少还有 6 个其他隐藏的设置。我在这里没有分享的全球价值观以及其他无法通过亚行实现的实验。我会在谷歌 Pixel 3 XL 上继续摆弄 Android Q beta，看看还有什么可以分享的。更多 Android Q 提示和技巧:

如果你觉得这篇文章很有用，并决定在社交媒体上分享，请联系我们！我们将很快为您提供更多教程。更多安卓 Q 新闻，关注我们的标签。

[**安卓 Q 新闻**](https://www.xda-developers.com/tag/android-q/)