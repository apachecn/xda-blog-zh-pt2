# Android Q 可能会让你在谷歌 Pixel 2 和 Pixel 3 上重新映射 Active Edge

> 原文：<https://www.xda-developers.com/android-q-google-pixel-2-pixel-3-remap-active-edge/>

谷歌 Pixel 2 和 Pixel 3 的最佳功能之一是 Active Edge。Active Edge 允许您挤压像素的侧面来启动助手或静音警报、计时器、通知和来电。与 [HTC 的 Edge Sense](https://www.xda-developers.com/new-edge-sense-beta-u11-customization/) 不同，Active Edge 最有可能是基于的[，Active Edge 仅限于推出谷歌助手服务。只要你愿意](https://www.xda-developers.com/google-completes-acquisition-htc-engineers-google-pixel-2/)[安装一个第三方应用](https://www.xda-developers.com/remap-active-edge-squeeze-google-pixel-2/)或者 [root 你的手机](https://www.xda-developers.com/customize-google-pixel-2-active-edge-sense-plus/)，有很多方法可以重新映射 Active Edge 来做你想做的任何事情。然而，随着 [Android Q beta](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/) 的发布，可以重新映射挤压功能，以启动 Pixel 2、Pixel 2 XL、Pixel 3 或 Pixel 3 XL 上的任何默认助手。

[**像素 2 论坛**](https://forum.xda-developers.com/pixel-2) [**像素 2 XL 论坛**](https://forum.xda-developers.com/pixel-2-xl)

[**像素 3 论坛**](https://forum.xda-developers.com/pixel-3) [**像素 3 XL 论坛**](https://forum.xda-developers.com/pixel-3-xl)

在深入研究 Android Q 的第一个测试版时，我发现了谷歌添加的一个隐藏属性，允许用户挤压手机时启动第三方助手。使用 Android 调试桥(ADB ),可以启用这个设置，否则无法访问。关于如何在任何 Windows、Linux 或 macOS 电脑上设置 ADB 的说明可以在[这里](https://www.xda-developers.com/install-adb-windows-macos-linux/)找到。设置好 ADB 后，只需输入以下命令，Active Edge 就可以启动您选择的任何助手——Cortana、Alexa 等。—只要在“设置”中设置为默认助手即可。

```
 adb shell settings put secure assist_gesture_any_assistant 1 
```

*在 Android Q 中更改默认的助手应用程序。截图是在一个谷歌 Pixel 3 XL 上拍摄的。*

更好的是，你可以设置 Active Edge 来启动任何你想要的应用程序。例如，如果您将 Tasker 设为默认助手，您可以挤压像素来切换手电筒。

我们不能保证这一功能会进入最终的 Android Q 版本，但我们希望谷歌[效仿三星](https://www.xda-developers.com/remap-bixby-button-google-assistant/)。