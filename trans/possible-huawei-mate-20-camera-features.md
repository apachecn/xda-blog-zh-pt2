# EMUI 9 软件中详述的华为 Mate 20 相机可能的功能

> 原文：<https://www.xda-developers.com/possible-huawei-mate-20-camera-features/>

下个月，我们将见证多项备受瞩目的智能手机发布。我们期待看到 LG V40 ThinQ、谷歌 Pixel 3、Razer Phone 2、新的三星 Galaxy A 手机、华为 Mate 20、[一加 6T](https://www.xda-developers.com/oneplus-6t-forums/) 和 Honor Magic 2。虽然我们[基本上知道关于 Pixel 3](https://www.xda-developers.com/google-pixel-3-xl-specs-features-pics-rumors/) 的一切，但其他智能手机并没有得到很好的记录。由于[之前的泄露](https://www.xda-developers.com/huawei-mate-20-mate-20-pro-real-life-photos/)，我们知道了华为 Mate 20 的[基本设计](https://www.xda-developers.com/huawei-mate-20-notch-render-specifications/)和[硬件](https://www.xda-developers.com/huawei-mate-20-specifications-features-rumor/)，现在我们可以分享一些关于其相机应用可能功能的见解。我们不能保证这些功能将与华为 Mate 20 一起推出，但这些新的 EMUI 9 相机功能肯定会在未来的华为或 Honor 设备中出现。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

*特别感谢 PNF 软件为我们提供了 [JEB 反编译器](https://www.pnfsoftware.com/?aid=xdadev)。JEB 使我们有可能反编译和分析 EMUI 9 相机应用程序的代码。我们分析的华为 Mate 20 固件(日期为 9 月 13 日)是由 [FunkyHuawei.club](https://funkyhuawei.club/) 提供给我们的，这是一项允许用户付费更新、 [unbrick](https://funkyhuawei.club/unbricking) 或 [rebrand](https://funkyhuawei.club/rebranding) 华为和 Honor 手机的服务。FunkyHuawei 计划全力支持即将到来的华为 Mate 20 系列，目前正在为 XDA 读者提供[销售](https://funkyhuawei.club/xdaspecial)。*

* * *

## 水下模式

这是迄今为止我在 EMUI 9 相机应用中发现的最奇怪的新功能。华为 P20 Pro 的防尘和防水等级为 IP67，但它并不完全防水，因此当你试图在水下拍摄视频时，你可能会毁了你的手机。我们不知道即将到来的华为 Mate 20 或华为 Mate 20 Pro 是否会防水，但这似乎并不重要，因为这种水下模式旨在使用或不使用防水手机。

根据我找到的字符串，水下模式旨在帮助您“在水下环境中拍摄清晰的照片。”您可以按下音量下调按钮来拍照，按下音量上调按钮来拍摄视频，按下电源按钮来打开/关闭相机，或者按住底部的按钮来退出。所有这些都可以通过防水手机壳在屏幕上点击来完成，显然，华为自己也将提供这种手机壳。尽管如此，该公司警告称，任何因未正确遵循说明而导致的手机损坏都不在保修范围内。

我发现了一个水下模式的相关图形，它看起来像一个包里的手机的图片。华为鼓励你把真正昂贵的智能手机放在包里，浸入水下，拍出精彩的照片。你们中的一些人可能会觉得这很酷，但我想我会通过。

下面的两个截图显示了我们如何使用 JEB Decompiler 来帮助我们发现这个特性。左边的屏幕截图显示了代码中的 image 字段与实际资产的交叉引用，而右边的屏幕截图显示属性`ro.hwcamera_underwater_enable`必须设置为 true，该特性才可用。我们检查了/product/etc/prop 中的 local.prop，但是，该标志丢失了。华为 Mate 20 可能不会推出这项功能，但由于我们检查了预发布软件，我们不知道华为是否会在稍后的日期翻转开关。水下模式似乎不需要特殊的硬件(如新的海思麒麟 980)来工作，因为应用程序中没有定义华为相机功能标志。

## 爱影院

下一个功能并不令人惊讶，因为华为在海思麒麟 980 的发布会上明确告诉我们，由于其双 npu，该芯片组将能够在视频中进行实时物体识别。它被称为“人工智能影院”，看起来该功能将在视频录制过程中实时应用某些滤镜。可用的滤镜有 AI 颜色、背景模糊、清新、复古和悬疑。下图显示了华为在 EMUI 9 相机应用程序中包含的每个滤镜的样本图形。

下面是我用来获得每个过滤器的真实名称的字符串。

```
 <string name="ai_cinema_effect_none">None</string>
<string name="ai_cinema_effect_bokeh">Background blur</string>
<string name="ai_cinema_effect_color">AI color</string>
<string name="ai_cinema_effect_fresh">Fresh</string>
<string name="ai_cinema_effect_nostalgia">Vintage</string>
<string name="ai_cinema_effect_hitchcock">Suspense</string>
<string name="ai_cinema_color_tip_select">Touch to select colors.</string> 
```

最后，要启用此功能，必须将`ro.hwcamera.aimovie_enable`设置为 true。在我目前看到的版本中，情况并非如此，但考虑到麒麟 980 的功能，如果在设备发货时还没有启用这样的功能，我们会感到惊讶。麒麟 980 应该支持人工智能电影功能，但是，因为它的相机功能标志已定义。

## 空气变焦

如果你很难找到完美的变焦水平来拍摄出色的照片，那么华为的 AI 变焦功能可能适合你。字符串表示该功能将自动调整缩放级别，以保持您的主题居中。除此之外，字符串并没有告诉我们更多关于这个特性的信息。

```
 <string name="title_smart_zoom">AI zoom</string>
<string name="remark_smart_zoom">Automatically adjust the zoom level to keep your subject centered</string>
<string name="toast_smart_zoom_enter">AI zoom enabled.</string>
<string name="toast_smart_zoom_quit">AI zoom disabled.</string>
<string name="toast_smart_zoom_fail">Unable to lock on to subject.</string>
<string name="toast_smart_zoom_first_tip">Touch the padlock to lock on and enable AI zoom.</string> 
```

深入研究代码，我们可以看到启用该特性有三个要求:

*   视频录制分辨率必须至少为 1080p。
*   AI 影院必须启用。
*   美颜等级必须为 0(关)。

我们还可以看到，字符串引用的“主题”是一个人的脸，这是通过引用 FaceDetectionExtension 类中的 Smart Zoom (AI Zoom)来判断的。最后，我们可以看到，如果算法放大错误的对象，可能会对人工智能变焦进行手动补偿。部分代码提到了抓取触摸或轻击位置，然后计算要放大的矩形。

要启用人工智能变焦，必须将`ro.hwcamera.smartzoom_enable`设置为 true。同样，这个功能在我看到的版本中没有启用，但海思麒麟 980 肯定有这个功能，所以我不会惊讶地在华为 Mate 20 上看到这个功能。

## 视频散景

散景是通过模糊主体周围的背景来突出前景主体的过程。散景效果在背景中放置形状，如星星或圆圈，这产生了灯光的错觉。华为将提供多种视频散景效果，如下图所示。

视频散景，像人工智能变焦和人工智能影院，将需要相机 HAL 的支持。具体来说，必须定义`videoBokehSpotShapeSupported`和`videoBokehSpotShapeValueSupported`摄像机功能。我们相信 Mate 20 将支持这一功能，尽管我们无法确认该功能是否真的在设备上启用。

* * *

这是我们从华为 Mate 20 固件转储中的 EMUI 9 相机应用程序中可以了解到的所有信息。如果我们了解更多关于华为 Mate 20 或华为 Mate 20 Pro 的信息，我们会让大家知道。我们为我们的读者准备了一些特殊的好东西，不需要你拥有华为或 Honor 设备就可以欣赏，请继续关注！

[**加入华为 Mate 20 论坛**](https://forum.xda-developers.com/mate-20)

[**加入华为 Mate 20 Pro 论坛**](https://forum.xda-developers.com/mate-20-pro)