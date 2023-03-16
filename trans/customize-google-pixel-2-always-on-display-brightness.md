# 如何自定义谷歌像素 2 始终显示的亮度没有根

> 原文：<https://www.xda-developers.com/customize-google-pixel-2-always-on-display-brightness/>

谷歌最新的旗舰智能手机 [Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/tag/google-pixel-2/) ，是第一款提供[永远显示功能](https://www.xda-developers.com/google-pixel-2-xl-announced-price/)的谷歌智能手机。其他智能手机，如大多数[三星 Galaxy 旗舰机](https://www.xda-developers.com/tweak-always-on-display-samsung-galaxy-s8-substratum/)已经有一段时间拥有这样的功能，但随着像素旗舰机引入该功能，该功能的源代码也随之而来，这使得它可以在旧的 Nexus 和第一代像素手机上工作。始终显示当前显示时间、日期、闹钟、通知图标，以及通过[正在播放的](https://www.xda-developers.com/google-pixel-2-now-playing-feature-ported/)正在播放的背景歌曲(尽管[可以定制](https://www.xda-developers.com/ambient-lock-screen-music-pixel-2/))。今天，我们将向您展示如何定制 Pixel 2 始终显示的另一个方面:亮度。

当你把设备放在桌子旁边时，AOD 功能会很有用，但这实际上取决于你的照明情况。在许多情况下，AOD 可能看起来太暗，实际上不可读。在谷歌上快速搜索“[Pixel 2 Always on Display brightness](https://www.google.com/search?q=pixel+2+always+on+display+brightness)”，你会看到大量关于它有多暗的抱怨。

这里的问题是，AOD 的亮度与[自适应亮度](https://www.xda-developers.com/underburn-change-brightness-level-screen-content/)有关，这是谷歌的自动亮度功能，我相信大多数人都启用了它。根据环境光的多少，AOD 的亮度值可以从最小的 2 到最大的 28。这超出了 255，255 是设置中显示器亮度的最大整数值。本质上，AOD 可以通过自适应亮度获得的最亮亮度大约是最大显示亮度的 11%——在许多情况下这是非常可怜的。谢天谢地，这是可以调整的，最好的部分是它不需要你 [root 你的手机](https://www.xda-developers.com/how-to-unlock-bootloader-and-root-the-google-pixel-2-and-pixel-2-xl/)。

* * *

## 自定义谷歌像素 2 始终显示的亮度

我们现在要做的是改变一个隐藏的设置，这个设置只能从 Android 8.1 Oreo T1 开始使用。这不是问题，因为每个 Pixel 2 用户都应该已经运行了最新版本，但无论如何都值得一提。隐藏设置只能通过 Android 调试桥(ADB)访问，这意味着你需要将手机连接到 PC。如果你手边有一台电脑，那么你可以按照以下步骤操作:

1.  按照本[先前教程](https://www.xda-developers.com/install-adb-windows-macos-linux/)中的描述设置 ADB。
2.  打开命令提示符或终端，按以下格式输入命令:`adb shell settings put global always_on_display_constants "screen_brightness_array=-1:0:1:2:3"`
3.  将上述命令中的“0:1:2:3”替换为从 0 到 255 的任何一组 4 个数字(例如“2:25:100:250”)。将“-1”保留在原位。

现在，您的始终显示亮度可以调整到比以往任何时候都高！如果你想知道数组中的每个数字代表什么，你输入的第一个数字代表“夜晚”条件(非常非常低的环境光)，第二个代表“低”光条件，第三个代表“高”光条件，最后一个代表“太阳”(非常非常高的环境光)。

上面显示了 AOD 亮度数组中的默认值。如果您想恢复您在此所做的更改，可以参考该文档。

### 额外收获:其他总是显示调整

除了亮度调整之外，还有一些与始终显示的像素 2 相关的其他设置，您可以修改。列表如下:

*   `dimming_scrim_array`:将环境亮度类型映射到调光稀松布的整数数组。这实际上是用一个覆盖层“掩盖”了 AOD，使它变得更加模糊(不知道为什么要这样)。
*   `prox_screen_off_delay`:从覆盖接近传感器到关闭屏幕的延迟时间(毫秒)。
*   `prox_cooldown_trigger`:触发冷却定时器的阈值时间(以毫秒为单位)，该定时器将关闭近程传感器一段时间。
*   `prox_cooldown_period`:如果`prox_cooldown_trigger`被触发，关闭接近传感器的时间(毫秒)。

下面是一个如何使用这些值来调整 AOD 的例子。比方说，我想让它在手机的接近传感器被覆盖后 5 秒钟关闭屏幕，此时总是显示。我将输入以下命令:

```
 adb shell settings put global always_on_display_constants "prox_screen_off_delay=50000" 
```

您可以尝试使用这些设置来自定义 AOD 的行为，尽管不幸的是，这些都是您可以在没有 root 访问权限的情况下修改的。