# 谷歌手机 47 准备添加“翻转到静音”和单向视频

> 原文：<https://www.xda-developers.com/google-phone-flip-to-silence-answer-1-way-video/>

谷歌今天在测试频道推出了 47.0 版本的谷歌手机应用程序，对 APK 的新资源进行了简单的回顾，揭示了 Pixel 拨号器应用程序的一些新功能。这些功能尚未在公开测试版中上线，但它们可能会在下一个 Pixel 功能发布时上线。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**用单向视频回答**

一个字符串表明，谷歌手机应用程序将让用户以单向视频的形式接听来电。这可能意味着您可以看到其他来电者的视频，但他们看不到您的视频源。

```
 <string name="call_incoming_chip_answer_video_as_one_way_video">Answer as 1-way video</string> 
```

**翻转到静音**

另一组字符串描述了一个新的“翻转到静音”功能。这项功能可以让用户将手机面朝下放在平面上，使来电铃声静音。

```
 <string name="flip_to_shush_title">Flip To Shhh</string>
<string name="flip_to_silence_key">flip_to_silence_key</string>
<string name="flip_to_silence_summary">To silence an incoming call, place your phone face down on a flat surface</string>
<string name="flip_to_silence_title">Flip To Silence</string> 
```

检查谷歌手机应用程序的反编译代码，我们发现该应用程序在启用到该设置的链接之前会查询[Digital wellness 的“Flip to Shhh”](https://www.xda-developers.com/digital-wellbeing-flip-to-silence-google-pixel-2/)的存在，否则，将显示新的“Flip to Silence”切换。这是因为尽管 Flip to Shhh 的功能描述称，它只在你翻转手机时打开勿扰模式，但这个动作实际上已经让来电铃声静音了，至少在我的 Pixel 4 上是这样的。因此，如果“翻转到 Shhh”可用，那么“翻转到静音”将不需要向用户显示。但是，如果“翻转到嘘”不可用，那么“翻转到静音”将需要显示。目前，Flip to Shhh 在 Pixel 2 、Pixel 3、Pixel 3a 和 Pixel 4 上可以使用[，而谷歌手机应用不仅可以在 Pixel 设备上使用，也可以在 Android One 设备上使用。然而，我们不知道谷歌是否计划为非像素设备启用“翻转静音”。](https://www.xda-developers.com/digital-wellbeing-flip-to-shhh-pixel-2/)

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*