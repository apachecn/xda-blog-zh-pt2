# Android 11 暗示多设备媒体和有线耳机音频切换

> 原文：<https://www.xda-developers.com/android-11-multi-device-media-output-wired-headset-audio-switching/>

随着 Galaxy S8 的发布，三星推出了[双音频](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=Android+11+DP2+hints+at+supporting+multi-device+media+output+and+switching+audio+to%2Ffrom+wired+headsets&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fandroid-11-multi-device-media-output-wired-headset-audio-switching%2F&u1=UUxdaUeUpU27685&url=https%3A%2F%2Fwww.samsung.com%2Fau%2Fsupport%2Fmobile-devices%2Fsetup-dual-audio%2F&ourl=https%3A%2F%2Fwww.samsung.com%2Fau%2Fsupport%2Fmobile-devices%2Fwhat-is-the-dual-audio-feature%2F)功能，允许用户将蓝牙音频传输到两个相连的蓝牙设备。自 Galaxy S8 以来，每款旗舰 Galaxy S、Galaxy Note 和 Galaxy Tab 设备都支持双音频，但绝大多数 Android 设备都没有将音频传输到多个蓝牙设备的能力，只有少数来自摩托罗拉、HMD Global 和 TCL 的手机使用了 [Tempow 的](https://tempow.com/)技术。一个[常见的误解](https://www.youtube.com/watch?v=T-CPobBQi6E)是这项功能是由蓝牙 5.0 实现的，但如今许多 Android 设备都支持蓝牙 5.0，不能向多个设备传输媒体。Android 9 Pie 增加了同时连接最多 5 个蓝牙设备的支持，现在看来 Android 11 可能会增加选择多个设备向其播放流媒体的支持。更重要的是，谷歌似乎还增加了改变媒体输出到当前连接的有线音频设备或从当前连接的有线音频设备改变媒体输出的能力。

*在 Android 11 中，你目前可以在 2 个或更多连接的蓝牙设备之间切换媒体输出，但你不能选择多个设备同时进行流媒体播放。*

在最新的预览版中查看设置 Google 时，我们发现了以标题“media_output_group”开头的新字符串，这似乎表明您可以选择多个音频设备进行输出。有一个字符串提到了“casting”，你可能一开始会联想到 Google Cast 协议，但是我们不相信这个特性与 Google Cast 有关。这是因为现有的“media_output”字符串与从一个连接的蓝牙设备到另一个设备改变媒体输出的能力有关；该功能已经可以在由 Slice 提供的音量面板 UI 中或通过设置>声音来访问，如上面的截图所示。第二，Google Cast 是由 Google Play 服务控制的，而不是由 SettingsGoogle 控制的，我就是在这个应用程序中发现这些字符串的。第三，“cast”也可以泛指将音频流式传输到连接的蓝牙设备，尤其是蓝牙扬声器。

```
 <string name="media_output_group">Group</string>
<string name="media_output_group_panel_multiple_devices_summary">%1$d devices selected</string>
<string name="media_output_group_panel_single_device_summary">1 device selected</string>
<string name="media_output_group_panel_title">Add outputs</string>
<string name="media_output_panel_stop_casting_button">Stop casting</string> 
```

我们还发现了一个名为“media _ transfer _ wired _ device _ name”的新字符串，它建议您可以选择一个当前连接的有线耳机(通过 USB Type-C 端口或 3.5 毫米耳机插孔)来输出媒体。目前还不清楚这一新传输目标的增加是否允许用户在连接有线耳机的情况下通过设备的扬声器播放音频，就像一些原始设备制造商允许你做的那样，或者这一功能是否只是让你在连接蓝牙音频设备的情况下与有线耳机交换媒体输出。

```
 <string name="media_transfer_wired_device_name">Wired audio device</string> 
```

我们在运行 Android 11 开发者预览版 2 的 Pixel 设备上测试了这两个功能，看看它们是否有效。多设备媒体输出在 Pixel 4 XL 上不工作，而有线耳机媒体传输在带有 Type-C 耳机的 Pixel 3a XL 和带有或不带有连接的蓝牙设备的 3.5 毫米耳机上不工作。除了新的字符串，我们在反编译的设置应用中没有找到任何一个功能的对应代码，所以这些功能似乎还没有完成。我们不知道多设备媒体输出功能是否可能在任何现有的 Pixel 设备上得到支持，或者是否需要对蓝牙堆栈和/或硬件进行更改，这可能会出现在未来的 Pixel 设备上。我们也不知道这些功能是否只针对像素，即使字符串在 SettingsGoogle 当谷歌在几个月后公布源代码时，我们很可能会发现它是否是一个通用的 Android 11 功能。