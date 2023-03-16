# 谷歌 Pixel 4 的隐藏高亮度模式修复了糟糕的亮度

> 原文：<https://www.xda-developers.com/google-pixel-4-high-brightness-mode-fix/>

与 2017 年和 2018 年的像素一样，2019 年的 Pixel 4 和 Pixel 4 XL 也有不同的显示器制造商、显示器分辨率和显示器尺寸。虽然两款 Pixel 智能手机的显示屏质量都很高，但它们的最大亮度水平仍有很多不足之处。在我们的初步测试中，Pixel 4 和 Pixel 4 XL 在 100%屏幕亮度下达到了约 450 尼特的最大亮度。这远远低于其他竞争对手的旗舰智能手机显示屏。幸运的是，有一种方法可以使用隐藏的高亮度模式来提高最大亮度，但您需要 root 权限才能启用它。

如果你在阳光直射下使用过 Pixel 4，你可能很难看到屏幕，因为显示屏不够亮。Pixel 智能手机在户外时一直存在显示屏模糊的问题，因此这对谷歌来说并不是一个新问题。然而现在，价格便宜几百美元的智能手机有更亮的显示屏，所以谷歌没有理由在竞争中失利。

 <picture>![](img/85de2324a8f4a48c4b8b7297b0d40a82.png)</picture> 

Display Brightness Reference Chart. Credits: Dylan Raga/XDA.

然而，使用隐藏的高亮度模式，你可以将谷歌 Pixel 4 显示屏的峰值亮度从大约 450 尼特提高到大约 610 尼特。这是显示器亮度的一个重大提升，根据我的经验，实际上使谷歌 Pixel 4 在户外可读。不管是什么原因，谷歌决定在正常使用中不使用高亮度模式。你不能在“设置”中的任何地方手动触发它，也不能在室外启用自适应亮度时触发它。Pixel 4 唯一一次可以达到约 610 尼特是在播放 HDR 视频时。我们不知道谷歌为什么不使用这种隐藏显示模式来提高阳光清晰度，自从我们审查了 [Pixel 3](https://www.xda-developers.com/google-pixel-3-display-analysis-a-real-tangible-improvement-yet-still-behind-the-curve/) 和 [Pixel 3 XL](https://www.xda-developers.com/google-pixel-3-xl-display-review-what-google-needs-to-improve-for-the-pixel-4/) 显示屏以来，我们一直在问自己这个问题。

**[谷歌 Pixel 4 论坛](https://forum.xda-developers.com/pixel-4)**| |**|[谷歌 Pixel 4 XL 论坛](https://forum.xda-developers.com/pixel-4-xl)**

## 如何启用高亮度模式

*注意:在启用高亮度模式后，我们建议通过进入设置>应用&通知>所有应用>设备健康服务>存储&缓存>清除存储来重置自适应亮度。自适应亮度利用机器学习来学习你的亮度变化习惯，加上高亮度模式，你的亮度变化习惯大概会有所调整。*

### 用手

无论如何，我们很高兴谷歌在内核中保留了高亮度模式，因为很容易手动将其切换为 root 访问。在[启动你的谷歌 Pixel 4 或 Pixel 4 XL](https://www.xda-developers.com/google-pixel-4-root-magisk/) 后，你所要做的就是输入以下 shell 命令:

```
 su
echo on >> /sys/class/backlight/panel0-backlight/hbm_mode 
```

如果你想知道打开这个是否安全，你可能不必担心。在我们的测试中，看起来只有当屏幕处于最大 UI 亮度水平时，高亮度模式才会真正启动。你唯一需要担心的是对电池寿命的影响。由于显示屏已经是智能手机电池消耗的最大因素，而且显示屏在更高的亮度下运行需要更多的电力，因此高亮度模式激活的时间越长，Pixel 4 的电池寿命就会越长。

不幸的是，因为每当你关闭屏幕时，HBM 看起来就会自动关闭，所以你需要使用像 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) 这样的应用程序来自动切换它。你甚至可以设置它，使它只在环境或 UI 亮度水平高于某一点时打开。

### 自动地

如果你不想学习如何使用 Tasker 或者不想输入 shell 命令，你可以下载最新版本的(付费)FK 内核管理器应用程序。他的应用程序有一个点击开关来启用 HBM，一个每当达到用户定义的环境照明阈值时就启用 HBM 的开关，以及基于每个应用程序启用 HBM 的能力。

要在 FK 内核管理器中启用 HBM，请确保您的版本是 4.7。前往“设置”>“显示控制”并选择“高亮度模式”你可以通过上面的主开关启用 HBM，但如果你想让 HBM 根据环境照明自动打开，那么就切换“自动高亮度模式”设置。如果你想在每个应用程序的基础上启用 HBM，请前往设置>每个应用程序的配置文件，并设置您想要的配置文件。

* * *

*更新 1:添加了一句关于 Pixel 4 在播放 HDR 视频时可以达到 610 尼特的句子，并澄清了 HBM 似乎会在屏幕关闭时重置，因此您需要使用自动化应用程序在需要时打开它。*

更新 2:提到了 FK 内核管理器，这是在 Pixel 3/Pixel 4 上切换 HBM 的一种更简单的方法。我还重新整理了文章的部分内容。