# 谷歌像素 2 有 25 个媒体音量步骤，更精细的音量控制

> 原文：<https://www.xda-developers.com/google-pixel-2-25-media-volume-steps/>

# 谷歌像素 2 有 25 个媒体音量步骤，更精细的音量控制

新的谷歌 Pixel 2 和谷歌 Pixel 2 XL 具有 25 个媒体音量步长，允许更精细的音量控制，这样你就不会在晚上伤害你的耳朵。

小小的软件调整有时会对用户体验产生巨大的影响。多年来，Android 手机的一个痛点是缺乏粒度音量控制。默认情况下，媒体音量有 15 档，通知音量有 7 档，通话语音音量有 6 档。虽然音量级数很少，可以很快从最小音量调到最大音量，但这也意味着很难在每种情况下都找到最佳音量。幸运的是，谷歌似乎终于通过其最新的[谷歌像素 2 和谷歌像素 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 纠正了这个问题，因为这两款智能手机**现在具有 25 个媒体音量级**。

这种变化如此微妙，以至于我们在威瑞森商店测试这款设备时，一开始没有注意到。据我们所知，似乎没有人真正注意到这种变化。当我们查看 Pixel 2 的 build.prop 文件时，我们发现它有 25 个媒体音量级。在里面，我们发现了下面一行字:

```
 ro.config.media_vol_steps=25 
```

这一行是介质卷步数的系统属性值。就像我们在之前的教程中描述的一样，任何根用户都可以手动更改它。对于任何设备不是 rooted 的人来说，有一个名为[精确音量](https://forum.xda-developers.com/android/apps-games/app-precise-volume-override-androids-t3573562)的应用程序可以给你多达 100 个音量步长，尽管它没有集成股票音量滑块。

看到这条线后，我们在威瑞森商店重新检查了 Pixel 2 和 Pixel 2 XL，并确认音量滑块中确实有 25 级。无论如何，这都不是一个巨大的变化，但是到时候你一定会喜欢的。这是我在 [OnePlus 5](https://www.xda-developers.com/oneplus-5-media-volume-steps/) 中喜欢的一个变化(尽管即使是 OnePlus 5 的 30 步对我来说也不够，所以我现在坚持使用[重力盒模块](https://www.xda-developers.com/gravitybox-xposed-module-nougat/)为[曝光框架](https://www.xda-developers.com/official-xposed-framework-android-nougat/)进行 50 步的体积步)。现在你可以在晚上听一小段视频剪辑，而不会吹破你的耳膜或吵醒你的伴侣。