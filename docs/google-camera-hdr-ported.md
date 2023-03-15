# 带有 HDR+的谷歌相机移植到 Snapdragon 820/821 和 835 设备

> 原文：<https://www.xda-developers.com/google-camera-hdr-ported/>

尽管谷歌 Nexus 系列由于其开发的开放性而受到了广泛的好评，但智能手机因其拍照能力而受到了很多批评。然而，随着谷歌 Pixel 和 [Pixel XL](https://www.xda-developers.com/google-pixel-xl-xda-review-a-foundational-release-for-google-post-nexus-android/) 的发布，这种情况发生了变化(尽管[有些人会说它没有发生](https://www.xda-developers.com/vic-gundotra-iphone-android-photos/)),因为谷歌对其智能手机采取了更加以消费者为导向的方法，结果显示在相机部门，智能手机获得了 [DxOMark](https://www.dxomark.com/) 的最高分。谷歌最近在图像质量方面取得的成功部分归功于其智能手机独有的令人惊叹的 HDR+技术。对于普通用户来说，HDR+提供了一种令人难以置信的简单方法，无需学习[手动摄影](https://www.xda-developers.com/using-manual-camera-controls-improving-the-quality-and-versatility-of-your-photography/)或[编辑原始图像](https://www.xda-developers.com/a-guide-to-editing-raw-photography/)就能拍摄出令人惊叹的照片。现在，你可以利用**谷歌相机的 HDR+** ，这要归功于 APK 的修改版本，该版本可移植到**任何具有 Hexagon 680 ISP 的设备上(在 Snapdragon 820、821 和 835 SoCs 上找到)**。

谷歌相机应用对改装并不陌生。该应用程序的一个受欢迎的[零快门延迟(ZSL) HDR+ mod](https://forum.xda-developers.com/nexus-6p/themes-apps/mod-camera-nx-v4-google-camera-zsl-hdr-t3494435) 将谷歌 Pixel 的拍照速度带到了谷歌 Nexus 5X 和 Nexus 6P，我们做的一个[快速修改](https://www.xda-developers.com/google-camera-v4-2-from-the-pixel-system-dump-is-now-available-for-all-nougat-devices/)将谷歌相机 4.2(取自 Pixel 的 Android 7.1 牛轧糖系统转储)带到了上一代 Nexus 设备。但是，你很少看到谷歌摄像头被改装到其他非谷歌品牌的设备上。即使安装了 Magisk 的根用户也无法享受谷歌相机 HDR+的全部优势，但由于最近的一些发展，这种情况将会改变。

* * *

## 用 HDR+修改了谷歌相机 4.4

一个名为 [B-S-G](https://4pda.ru/forum/index.php?showuser=243055) 的乌克兰开发者在论坛 4PDA 上发布了一个谷歌相机 v4.4.012.156195200 的修改版本。这个谷歌相机应用程序与今年 6 月发布的第三个 Android O 开发者预览版中的应用程序相同。开发人员能够对其进行修改，以与任何使用 Hexagon 680 ISP 或更高版本的设备一起工作，包括那些使用 Snapdragon 820、骁龙 821 或 Snapdragon 835 SoCs 的设备。

我已经在以下设备上亲自测试了该应用程序，并确认其工作正常:

*   LG G6
*   一加 3
*   OnePlus 3T
*   一加 5
*   三星 Galaxy S8

支持 HDR+的修改后的谷歌相机应用程序似乎确实可以与谷歌的 HDR+技术配合使用，因为该应用程序正在处理 HDR 的通知出现在每张照片之后，处理完成后的照片有明显的差异。

*顶行:没有谷歌摄像头 HDR+的 OnePlus 3。最下面一行:带谷歌摄像头的 HDR+*

*用谷歌相机 HDR+在 OP3 上拍摄的其他样本照片*

我们独立确认了 APK 文件的安全性，这要感谢阿米尔·扎伊迪，他是无根 Pixel Launcher 应用程序的开发者，该应用程序将 Google Now 面板带到了无根设备上。他使用 APKTool 发布了一个[全差异图](https://github.com/amirzaidi/gcam/commit/2d07ee9d2ea8a53882ca9bc2d9120b15d35fef7b)，显示了对应用程序所做的微小更改，以查看是否有任何恶意插入 APK 文件的行为。我们没有发现这种情况，并且**可以确认安装**是安全的。有趣的是，你会看到开发者添加了大量对“muskie”和“Google Pixel XL 2”的引用，因此似乎他试图迫使 Google Camera 认为该应用程序正在下一代 Google Pixel 2 智能手机上运行。

我们联系了 B-S-G，并得到了开发者的直接许可，让他用 HDR+重新托管他修改过的谷歌相机 APK。我们已经将该文件上传到 AndroidFileHost，因此您可以轻松下载并在自己的设备上安装相机应用程序。

[**用 HDR+**](https://www.androidfilehost.com/?fid=889764386195922284) 下载谷歌相机 v4.4 Mod

* * *

## 与 B-S-G 的小型访谈

通过一名翻译(XDA 资深成员)我们与乌克兰开发商谈论了这个项目。首先，我们问他是如何让这个谷歌相机 HDR+修改工作的:

> #### 我拿 Nexus 6 当入门设备来恶搞。然后，你只需从 HDR 支持的设备(如 Nexus 5X/6P 或像素)列表中选择所需的设备，并替换所有必要的东西，以获得不同的处理。
> 
> #### 我花了大约 6-8 个小时让它工作。痛苦的两个晚上...

接下来，我们询问了他对这款应用的未来计划:

> #### 目前它只是测试版，我真的不知道哪个设备是最好的欺骗，以实现最令人印象深刻的 HDR+处理结果。目前，我正试图让前置摄像头与禁用的手电筒配合使用。只有在我找到解决办法后，我才会深入研究如何提高照片质量。

最后，我们询问了他对支持比 Hexagon 680 更老的设备的计划:

> #### 我没有计划支持任何特定的设备，但我可能会用不同的欺骗设备做一些版本的修改。每个设备使用 HDR+的效果都不一样，最好自己找到最喜欢的一个。我在论坛(4pda)上已经有了至少 5 个不同版本的处理算法(2 个混合，Nexus 6P，Pixel XL，Pixel 2 XL)。

所以你有它。这个精彩的修改是一个开发人员两个晚上的血汗和眼泪的结果。他努力让它工作在现在的位置，如果你喜欢这个修改，送他你所有的感谢！