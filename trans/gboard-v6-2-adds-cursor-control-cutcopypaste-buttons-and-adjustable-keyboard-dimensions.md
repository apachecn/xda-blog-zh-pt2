# Gboard v6.2 增加了光标控制、剪切/复制/粘贴按钮，并为手写支持做准备

> 原文：<https://www.xda-developers.com/gboard-v6-2-adds-cursor-control-cutcopypaste-buttons-and-adjustable-keyboard-dimensions/>

就在我们发布了如何在 Android O 的导航栏中添加[键盘光标的教程后的短短几天，谷歌似乎终于主动为 Gboard 应用程序的所有用户带来了这一功能以及更多功能。Gboard 版本现在正在谷歌 Play 商店推出，更新终于带来了用户多年来一直想要的功能支持:**光标控制**，**剪切/复制/粘贴**按钮，以及更多的**可调键盘尺寸控制**。此外，我们对最新更新进行了 APK 拆解，并发现有证据表明 Gboard 应用程序可能很快会提供独立的手写支持，而不需要谷歌手写输入应用程序。](https://www.xda-developers.com/how-to-add-leftright-cursors-to-the-nav-bar-during-text-input-on-android-o/)

* * *

## Gboard v6.2 更新——新特性的宝库

### 光标控制和文本编辑按钮

首先，Gboard 更新到 6.2 版带来了期待已久的键盘光标以及剪切/复制/粘贴按钮等。当你的键盘显示在任何文本栏中，你按下 Gboard 应用程序上的谷歌标志时，在顶行的中间会出现一个新图标，看起来像文本输入光标，两侧有两个箭头。点击这个按钮，你现在应该会看到一个新的屏幕，在键盘上添加了一些整洁的东西。现在，键盘光标允许您在输入字段中向左、向右、向上或向下移动。还有一个“全选”按钮，两个用于导航到文本输入栏开头或结尾的键，一个典型的退格键和一个粘贴键。突出显示某些文本后，“全选”会变成“剪切”，并且可以选择“复制”按钮。

### 可调尺寸

除了流行的 Gboard 应用程序的这些主要功能外，还有一些新功能可以进一步定制键盘的大小和位置。当你打开允许你将键盘移动到屏幕左侧/右侧的菜单时，底部有一个新按钮，允许你调整键盘的大小或将其移动到键盘当前以最大尺寸显示的任何区域。拖动中间的光标可以移动键盘的位置，而拖动四个角上的矩形可以扩大或缩小键盘的大小。一旦你找到一个你喜欢的位置，你可以按下勾号让键盘停留在那个位置，直到你使用“扩展”按钮重置它。

另一件让我印象深刻的事情是对键盘 UI 的小调整。我注意到每个键周围的边缘似乎更圆。我不太确定我是否喜欢新的外观，但它确实符合谷歌在 Android 7.1+上推出的整个“圆形图标”的东西。

### 手写支持

虽然 APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都有可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

在 APK，我们发现有证据表明 Gboard 的未来更新可能会带来键盘手写支持，这并不奇怪，因为谷歌[已经在 Play Store 上提供了手写输入法](https://play.google.com/store/apps/details?id=com.google.android.apps.handwriting.ime&hl=en)。目前，如果你从谷歌下载并安装手写输入法，你可以通过按下 Gboard 上的地球图标来来回切换。但现在，在获得了大量有价值的反馈并改进了手写识别算法后，谷歌似乎正在将其输入法整合到一个键盘上。

### Gboard 手写支持

```
 <string name="handwriting_speed_fast">Fast</string>
<string name="handwriting_speed_midfast">Mid-fast</string>
<string name="handwriting_speed_midslow">Mid-slow</string>
<string name="handwriting_speed_normal">Normal</string>
<string name="handwriting_speed_slow">Slow</string>
<string name="handwriting_speed_very_fast">Very fast</string>
<string name="handwriting_speed_very_slow">Very slow</string>
<string name="handwriting_stroke_extra_thick">Extra thick</string>
<string name="handwriting_stroke_extra_thin">Extra thin</string>
<string name="handwriting_stroke_midthick">Mid-thick</string>
<string name="handwriting_stroke_midthin">Mid-thin</string>
<string name="handwriting_stroke_normal">Normal</string>
<string name="handwriting_stroke_thick">Thick</string>
<string name="handwriting_stroke_thin">Thin</string> 
```

我们可以从 APK 的几个新布局和 smali 文件中看到这种新手写功能的进一步证据。添加了以下新布局文件:

 `*   setting _ 手写输入. xml
*   extension _ emoji _ 手写. xml
*   hide _ 手写 _keys.xml
*   全屏 _ 手写 _ 面板 _ 开 _ 手写 _ 开始. xml
*   全屏 _ 手写 _ 面板 _ 开 _ 手写 _ 结束. xml
*   show _ 手写提示. xml
*   hide _ 手写提示. xml
*   show _ 手写 _keys.xml

实现手写功能的相应 smali 文件也存在，这表明该功能在这个版本中至少部分实现了，尽管我们还不能在没有单独安装 Google 手写输入的情况下在 Gboard 应用程序上使用任何类型的手写功能。不过，我们会继续关注这个功能何时上线，并相应地更新我们的读者。

* * *

如果我在实时构建中或者通过 APK 的拆除发现了什么有趣的东西，我会继续挖掘并更新这篇文章。如果你正在寻找 Gboard 应用程序的最新版本，你现在可以在 APKMirror 下载。`