# 任务栏 4.0 为 Android Pie 设备带回了自由形式窗口支持

> 原文：<https://www.xda-developers.com/taskbar-freeform-window-android-pie/>

对 Android 多窗口的支持最初是由三星普及的，但该功能慢慢进入了 Android。Android 6.0 Marshmallow 引入了分屏多窗口支持，而 Android 7.0 Nougat 悄悄添加了自由形式窗口支持，尽管解锁自由形式窗口支持需要 ADB 命令或启用开发者选项。不幸的是，随着第一个 Android P 开发者预览版的发布，似乎自由形式窗口支持被移除了，因为用于支持它的传统方法不再有效。令人欣慰的是，现在有一个变通办法可以在 [Android Pie 设备](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/)上恢复自由形式窗口支持，而且不需要 root！

XDA 资深会员[farmerbb](https://forum.xda-developers.com/member.php?u=4289533),[任务栏](https://forum.xda-developers.com/android/apps-games/app-taskbar-freeform-window-enabler-t3517608)的开发者，在 Android 9 Pie 的[源代码发布](https://www.xda-developers.com/android-pie-source-code-aosp/)后，发现了启动自由形式窗口的新方法。我在 Twitter[上联系了这位开发者，听听他对 Android Pie 中应用窗口的改变的看法，以下是他的回答:](https://twitter.com/farmerbb1/status/1029153593264230400)

> #### Android Pie 似乎已经抛弃了窗口“堆栈”的概念，取而代之的是一种叫做[窗口配置](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/app/WindowConfiguration.java)的东西...每个应用程序窗口都可以分配一个特定的窗口模式。自由形式窗口只是列出的各种窗口模式中的一种。当开始一个活动时，你可以通过调用[这个方法](https://android.googlesource.com/platform/frameworks/base/+/android-9.0.0_r3/core/java/android/app/ActivityOptions.java#1199)(使用反射)来设置它使用任何你想要的窗口模式。

因此，为什么早期版本的任务栏不再能启动自由形式的窗口是因为 Android 改变了应用程序窗口模式的确定方式。有了现在可用的源代码，farmerbb 就能够找出如何使用新方法启动自由形式的窗口。他解释道:

> #### 您可以:
> 
> *   #### 使用通过反射调用的 setLaunchWindowingMode 方法启动一个提供 ActivityOptions 包的活动(需要 27 或更早版本的 targetSdk，否则您会遇到非 Sdk 接口限制[这里是](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/)。
>     
>     
> *   #### 或者，使用提供的- windowingMode 参数通过 adb 运行 am start-activity 命令，例如:ADB shell am start-activity-windowing mode 5 com.farmerbb.taskbar/.MainActivity

(如果你有兴趣了解 Android 9 Pie 之前自由形式窗口支持是如何工作的，可以看看 [farmerbb 在 XDA](https://www.xda-developers.com/android-nougats-freeform-window-mode-what-it-is-and-how-developers-can-utilize-it/) 上的精彩客座博文。)

farmerbb 选择了第一种方式，因此，目前来看，该应用程序的 targetSdkVersion 是 27，而不是 28。一旦他被迫将 targetSdkVersion 提高到 28，他将不得不使用我推荐的变通方法(如果到那时这仍然有效的话)。)不过，当我们到达那一点时，我们会过桥的。

## 在 Android Pie 上带回自由形式的窗口

如果你对在 Android 9 Pie 设备上获得自由形式的窗口感兴趣，那么你所要做的就是从谷歌 Play 商店安装最新版本的任务栏应用程序。最新版本 4.0 已经推出。只需安装应用程序，并按照安装说明在应用程序中启用自由模式。如果你过去使用过这个应用程序来启动自由形式的窗口，你会注意到之前的实现和它现在在 Android Pie 中的工作方式有一个直接的区别。我会让法默伯解释:

> #### 这一变化的副作用是，现在自由形式的窗口可以浮动在全屏窗口的顶部，而不是局限于自己的堆栈！很酷的改变，虽然你不能像 PIP 窗口一样把它们固定在窗口的顶层。

顺便说一下，这看起来是这样的:

不要用这个来强迫 YouTube 进入伪 PiP 模式。它不起作用。你只需要[等待 YouTube PiP 在你的地区推出](https://www.xda-developers.com/youtube-picture-in-picture-rolling-out-us-non-red-premium-users/)或者升级到 [YouTube Premium](https://www.xda-developers.com/revamped-youtube-music-soon-youtube-premium-later/) 。无论如何，如果你想将这个功能用于其他目的，这里有下载该应用程序的链接。