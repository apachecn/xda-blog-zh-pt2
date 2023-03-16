# 这可能是用于定制 Android 10 的谷歌像素主题应用程序

> 原文：<https://www.xda-developers.com/google-pixel-themes-customize-android-10/>

本周，我们已经被大量关于谷歌 Pixel 4 的泄露所淹没，但大多数泄露都与其硬件有关。我们刚刚了解了它的[8 倍变焦能力、6GB 内存](https://www.xda-developers.com/google-pixel-4-xl-8x-zoom-6gb-ram-white-color/)和 [90Hz 显示屏](https://www.xda-developers.com/google-pixel-4-90hz-display-android-10-source-code/)，但我们也开始了解它的软件。早在 Android Q 测试版期间，我们发现了一个名为“[像素主题](https://www.xda-developers.com/android-q-pixel-themes-google-pixel/)的隐藏应用，它暗示可以在谷歌像素智能手机上定制字体、图标形状和强调颜色。后来，我们开始在设置应用中看到一个建议，告诉用户“[自定义[他们的]像素](https://www.xda-developers.com/android-q-pixel-customization/)。”点击这个建议只是打开了现有的谷歌壁纸应用程序，没有任何额外的定制选项。现在，我们获得了 Android 10 的主题选择器应用程序的截图，该应用程序将有可能在谷歌 Pixel 智能手机上被称为“Pixel Themes”。

XDA 公认的贡献者 [MSF Jarvis](https://forum.xda-developers.com/member.php?u=6552280) 告诉我们，随着 [Android 10 源代码](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/)的发布，一个名为“ThemePicker”的新应用[被上传到了 AOSP](https://android.googlesource.com/platform/packages/apps/ThemePicker/) 。安装后，应用程序会在应用程序抽屉或 Pixel 启动器的长按上下文菜单中显示为“Styles & wallpapers”。这个应用程序的字符串告诉我们，这个应用程序将允许用户定制锁定屏幕/环境显示时钟面，像素启动器网格大小，锁定屏幕和主屏幕壁纸，以及“风格”(包括强调颜色，图标形状和字体)。)您还可以从可用的选项中进行混合和匹配，以创建自己的风格，甚至可以命名。我们之前对 Android 10 [的分析显示](https://www.xda-developers.com/android-q-lock-screen-clock-customization/)钟面包括一个模拟时钟和一个气泡伸展时钟(type/text 钟面在开发过程中不幸被移除了。)最后，我发现了定制图标包的代码，尽管我不能 100%确定这是否不同于定制图标形状。

经过几个小时的修补，我们只能部分启动并运行 ThemePicker 应用程序。对我们来说幸运的是，XDA 发现开发者 luca020400 发现了一个链接到(可能不是故意的)公开的谷歌相册的提交，该相册揭示了 Android 10 的主题管理器应用程序的用户界面。左边的图片(下图)显示了 Pixel Launcher 中的“Wallpapers”上下文菜单项被替换为“Styles & wallpapers”，而右边的图片(下图)显示了我们可以找到的该应用程序的最新 UI。使用我们对 Android Q beta 2 的 Pixel Themes 应用程序的分析，我们认为 3 个非默认预装主题将对 Android 10 UI 应用以下更改:

*   蜡笔:紫色强调色，杨梅字体，圆形/泪珠图标
*   拼贴:绿色强调色，Arvo 和 Lato 字体，填充图标
*   灰:黑色强调色，Rubik 字体，圆形/松鼠图标

我们之前提取了这个预览中显示的壁纸，所以任何人都可以[在这里](https://www.androidfilehost.com/?fid=1395089523397932414)下载它们。

旧的提交还包含了 ThemePicker 应用预览的链接，但这些截图仍然显示了我们之前发现的“安东尼”、“约翰娜”和“小早川怜子”的代号。(我们现在知道，“安东尼”是“灰”的主题，“约翰娜”是“拼贴”的主题，“蜡笔”是“小早川怜子”的主题。)这些图片确实显示了定制强调色、字体和壁纸的预览屏幕，所以我们觉得它们值得放在这里。

尽管提交中共享的图像没有展示 Pixel Launcher 网格定制或锁屏/环境显示时钟定制，但 XDA 认可的开发人员 luca020400 设法部分激活了这两个功能，尽管他只能在 AOSP/linegeos 17 Android 10 上工作，而不是 Pixel 软件。他给我们发来了左边的截图(下图)，显示你可以选择 3x3、4x4 或 5x5 的主屏幕布局。他在右边(下图)发送的截图展示了时钟类型，尽管他[手动添加了](https://twitter.com/MishaalRahman/status/1169263040820391936)类型/文本时钟，因为谷歌将其从 AOSP 移除。

在引擎盖下，该功能使用了当前 Android 10 版本中的现有覆盖。ThemePicker 应用程序使用 OverlayManagerService APIs，从 8.0 Oreo 开始集成到 Android 中，在不实际修改应用程序的情况下修改应用程序的资源。这些覆盖图可以通过开发者选项或 adb 手动切换，但谷歌正在努力通过一个面向用户的应用程序来展示对它们的控制。Pixel Themes 应用程序可能会在下个月与谷歌 Pixel 4 一起推出，我认为用户界面看起来非常接近我们在开源版本中看到的。如果我们了解更多关于 Android 10 UI 定制或谷歌 Pixel 4 的信息，我们会让你知道。

[**谷歌 Pixel 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**谷歌 Pixel 4 XL 论坛**](https://forum.xda-developers.com/pixel-4-xl)

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*