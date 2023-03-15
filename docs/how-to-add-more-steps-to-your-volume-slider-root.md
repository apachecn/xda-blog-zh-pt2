# 如何添加更多的步骤到您的音量滑块[根]

> 原文：<https://www.xda-developers.com/how-to-add-more-steps-to-your-volume-slider-root/>

在我寻求发现有趣的调整以与 XDA 开发者社区分享的过程中，我经常在许多不同的论坛上遇到一个请求:

> #### "如何向音量滑块添加更多的步骤？"-没有特别的人

在寻找可靠地增加更多卷粒度的方法时，我发现谷歌 Play 商店上的大多数应用程序根本不适用于大多数现代设备。我发现的另一个解决方案涉及使用 Xposed 模块 [VolumeSteps+](https://forum.xda-developers.com/xposed/modules/mod-volumesteps-t2884962) ，不幸的是，这意味着该方法仅限于支持 Xposed 框架的根设备(也就是说，没有 Android 牛轧糖支持)。最后，你们很多人都知道的最后一种方法是闪存定制 ROM，但对于我们这些在这方面没有太多选择的人(华为 Mate 9 目前缺乏开发热情)或希望保留股票根版本的人来说，这种选择很难接受。

幸运的是，有一种简单的方法可以为你的通话或媒体量增加更多步骤，这种方法**不需要 Xposed 框架**和**也可以在 Android 6.0+** 上工作。最重要的是，如果你愿意，你可以留在你的股票根设置！你所需要做的就是利用一个简单的、完全未公开的 **build.prop 调整。**

*注:我测试的设备是两台运行 Android 6.0 棉花糖和 7.1 牛轧糖的谷歌 Nexus 6 手机。我没有办法在每一个设备上用每一个软件版本测试这个调整。这一调整来自于对 AOSP 的观察，但没有测试其他设备或查看它们的源代码，我不能确切地说它将在哪些设备上工作。*

* * *

## 通过构建进行精确的音量控制。适当调整

Android 的开源文档展示了该软件的音频服务是如何在 AudioService.java 实现的。在代码中，有一个特定的部分定义了如何在引导时初始化卷级别。

```

        int maxVolume = SystemProperties.getInt("<strong>ro.config.vc_call_vol_steps</strong>",
                MAX_STREAM_VOLUME[AudioSystem.STREAM_VOICE_CALL]);
        if (maxVolume != MAX_STREAM_VOLUME[AudioSystem.STREAM_VOICE_CALL]) {
            MAX_STREAM_VOLUME[AudioSystem.STREAM_VOICE_CALL] = maxVolume;
            AudioSystem.DEFAULT_STREAM_VOLUME[AudioSystem.STREAM_VOICE_CALL] = (maxVolume * 3) / 4;
        }
        maxVolume = SystemProperties.getInt("<strong>ro.config.media_vol_steps</strong>",
                MAX_STREAM_VOLUME[AudioSystem.STREAM_MUSIC]);
        if (maxVolume != MAX_STREAM_VOLUME[AudioSystem.STREAM_MUSIC]) {
            MAX_STREAM_VOLUME[AudioSystem.STREAM_MUSIC] = maxVolume;
            AudioSystem.DEFAULT_STREAM_VOLUME[AudioSystem.STREAM_MUSIC] = (maxVolume * 3) / 4;
        }

```

我在上面加粗的两个术语看起来与/system 中的 build.prop 文件中的行非常相似，不是吗？这是因为它们是，尽管默认情况下，您不会在 build.prop 文件中看到这些属性。幸运的是，如果您自己定义这些属性，您可以**手动设置音量步长的数量**。

如果您熟悉如何编辑和添加代码行到 build.prop 中，那么就开始动手吧！如果没有，这里有一个简单的方法让你开始。

在谷歌 Play 商店上下载 JRummy 的 [BuildProp 编辑器](https://play.google.com/store/apps/details?id=com.jrummy.apps.build.prop.editor)并打开。点击右上角的“铅笔”图标，调出手动编辑模式。一直滚动到底部，添加上面提到的 build.prop 行中的任何一行，并将其设置为您想要的体积步长数。例如，在末尾输入这两个命令将分别使通话音量步长和媒体音量步长加倍。

`ro.config.vc_call_vol_steps=14`

ro.config.media_vol_steps=30

一旦你输入了这些命令，重启你的手机。如果成功的话，您现在应该拥有与 build.prop 中指定的一样多的体积步长。

享受这个漂亮的调整！如果它适用于你的设备和内部版本，请在下面的评论中告诉我们。