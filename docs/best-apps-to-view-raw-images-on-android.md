# 在 Android 上查看原始图像的最佳应用

> 原文：<https://www.xda-developers.com/best-apps-to-view-raw-images-on-android/>

上周，我写了关于释放棒棒糖智能手机的[原始](https://en.wikipedia.org/wiki/Raw_image_format "Raw Image Format - Wikipedia")摄影能力的[最佳应用](http://www.xda-developers.com/top-4-camera-apps-for-lollipops-new-api/ "Top 4 Camera Apps for Lollipop’s New API")。所有四个相机都可以生成无损的 DNG 图像，Photoshop 等应用程序有很大的潜力来解锁这些图像，但如果你想在旅途中编辑或查看这些照片，该怎么办？QuickPic、Google Photos 和其他主流应用将原始图像视为不存在。这个纲要旨在填补空白，让你完全控制你的珍贵照片。

**免费还是付费？**尽管有大量可用的应用程序，但唯一能正面应对原始问题的是一些价格高昂的重磅套件，以及几个免费增值画廊和编辑器应用程序。但是不要被骗了——像 [PhotoMate R2](https://play.google.com/store/apps/details?id=com.tssystems.photomate2 "Photo Mate R2 - Google Play") 这样的优质产品一心要取代你的整个桌面工作流程，我毫不怀疑它们能胜任这项任务。我对付费套房的保留不是质量，而是成本。一方面，Adobe Creative Suite 的桌面许可证比任何 Android 应用程序都贵，但另一方面，像[GIMP](http://www.gimp.org/ "GNU Image Manipulation Program")和 [Raw Therapee](http://rawtherapee.com/ "Raw Therapee") 这样的编辑器是行业标准工具，可以免费获得。因此，问题变成了为手机的速度和移动性支付 10 美元，或者免费使用你已经熟悉和喜爱的笔记本电脑。问题是，不管在什么平台上，编辑无损文件都不是快速或移动的。这些是粒状图像，没有固有的颜色配置文件，在经过编辑之前，看起来总是比预处理的 jpegs 图像差。当你可以用鼠标和键盘的精度免费做同样的事情时，为什么要付费坐在你的手机上一个小时？

这就把我们带到了观众和精简版编辑面前。再多的后期处理也无法修复闪烁的家庭成员或取景不当的照片，所以我们必须看到我们捕捉到的东西。像 DNG 这样的原始格式是基于 T2 TIFF T3 的，不适合大多数画廊。为什么不坚持大部分相机生成的 jpeg 预览？首先也是最重要的，那些预告有时会说谎。

# 原始捕获延迟和撒谎的 Jpegs

正如 XDA 资深成员 [Ashcunak](http://forum.xda-developers.com/member.php?u=2539488 "Ashcunak XDA Developer Profile") 指出的，原始图像并不总是与它们的 jpeg“副本”相匹配的确，你的相机在压缩到较小的格式时会选择颜色、饱和度和白平衡，但这并不能解释为什么闪烁的圣诞灯在一种格式下看起来是“开”的，而在另一种格式下是“关”的。答案是*有的*相机 app 拍*两张*的！如果我们有办法查看相机胶卷中的两幅图像，看看它们是否需要重做，这不会太糟糕，但正如我们已经讨论过的，大多数画廊会过滤掉它们。这使得它们在我们回家之前是“看不见的”，也是今天讨论的主题。我们一会儿会介绍一些在手机上查看原始格式的应用程序，但现在让我们来看看哪些相机会延迟第二次拍摄，以及延迟多少。毕竟，如果文件与文件之间的组成保持相同，我们可以坚持 jpeg 预览。

为了测试这个镜头延迟，我让 [L 相机](https://github.com/PkmX/lcamera "L Camera - GitHub")、[手动相机](https://play.google.com/store/apps/details?id=pl.vipek.camera2 "Manual Camera - Google Play")和[相机 FV-5](https://play.google.com/store/apps/details?id=com.flavionet.android.camera.pro "Camera FV-5 - Google Play") 通过它们的步伐拍摄[这个秒表](http://jsfiddle.net/jw2z5eeu/ "JS Fiddle Stopwatch")，在高分辨率和低分辨率下，以及在光谱相反两端的快门速度下。连续的 jpeg 和 dng 拍摄可以清楚地捕捉不同的时间戳(从而量化延迟)，改变分辨率和快门有助于确定手机的读/写过程对问题的影响程度。我发现 L 相机和手动相机都没有任何延迟，这表明只拍摄了一张图像(DNG)，这张图像后来被处理成 jpeg。相比之下，相机 FV-5 拍摄两个不同的镜头:一个是所需像素分辨率的 jpeg，然后是几分之一秒后的全尺寸 DNG。这个 app 显然就是 Ashcunak 提到的罪犯。

你用相机 FV-5 经历的延迟会有所不同，取决于硬件和加密的存在(我正看着你，Nexus 6)。以下是我的结果:

**相机设置**

*   摩托罗拉 Nexus 6，未加密库存 Android 5.0.1
*   摄像机 FV-5 v2.41
*   快门 1/1000，ISO 3200
*   50 张 0.1 MP jpegs 的照片，下一张 13 MP 的照片。两组的 DNG 版本都是全尺寸的，这是有意义的，因为减少像素计数违背了原始传感器转储的无损性质。

**JPG 和 DNG 之间的延迟**

*   0.1 MP JPG: 0.034s，与平均值的平均偏差为 0.0018s
*   13mp JPG:0.032 秒，与平均值的平均偏差为 0.0056 秒

换句话说，闪烁的圣诞灯有百分之三秒的时间关闭并毁掉你的镜头。这种差距很小，但确实存在。更长的快门时间似乎使拍摄间隔更远，但我不能肯定；延长曝光时间必然会模糊秒表时间，取景器本身也不能计时，因为它的闪光和嗡嗡声意味着 UX 提示，而不是快门关闭的真正指示。

随着 FV-5 相机间隔拍摄，标准图像浏览器不显示 DNG 版本，我们应该如何在整个群体分散之前捕捉我们眨眼的家庭成员？哦，我有没有提到，你甚至没有一个更好的相机，从我们的纲要第四个应用 jpeg 回落？它输出 JPG *或* DNG，所以你在 raw 拍摄时是盲目的。

**结论**

*   l 相机和手动相机生成精确的 jpegs。不需要特殊的查看器，但是看看这些编辑器吧。
*   相机 FV-5 和更好的相机要么不能在标准图库中显示它们的图像，要么它们显示的 jpeg 预览不准确。请继续阅读修复该问题的图库。

# RAW 的免费图库应用程序

### 免费原始解码器

 **下载: [Google Play](https://play.google.com/store/apps/details?id=com.tssystems.rawdecoderfree "RAW Decoder Free - Google Play") (免费)

最后更新于 2013 年 11 月 30 日，并显示其年龄。

这个查看器将完成工作，但是它非常简单(而且不是以一种好的方式)。从根目录开始，一路点击到 camera 文件夹(通常是/storage/sdcard0/DCIM/Camera)。一旦到了那里，一个两宽的图标和文件名的按字母顺序排列的列表，没有可拖动的滚动条，向下延伸了几米。只有 jpegs 有缩略图。

一旦你找到了你想要的图像，这种体验就会改善。没有水印标记的照片，照片是全分辨率的，支持平移/缩放(如果有点小故障)。与应用程序的标题一致，装饰用户界面的唯一按钮被命名为“解码原始数据”，正如它在锡上所说的那样。

*   解码为全分辨率或半分辨率的 JPG 或 TIFF。
*   对于 TIFF，另外选择 8 或 16 位。

简单而有效。它也是唯一一个免费的 raw 图库，既提供了多种导出选项*又让你可以使用它们。没有水印是一个优点。我可以毫不费力地将 JPEG 和 dng 转换成不同分辨率的 TIFFs 和 JPEG，但是您的收获可能会有所不同；Google Play 上的一些评论者报告说，marquee 功能有问题。也许我的运气与我设备上的 3GB 内存和应用程序在解码时弹出的关于内存崩溃的警告有关。无论哪种方式，RAW Decoder Free 都是一个方便的免费工具。*

如果您使用的是更好的相机，导出到 jpeg 是在常规图库中弹出预览的一种有用方式。或者，导出，在您选择的应用程序中编辑，然后上传到脸书。不过，如果你正在这样做，你可能会考虑像 Photoshop Express 这样的编辑器，或者如果你真的很重视从你的手机上查看和编辑 raw，升级到一个更昂贵的产品，像 RAW Decoder 的老大哥-照片伴侣 R2(两者都在最后讨论了)。

### RAWDroid 演示

****

下载: [Google Play](https://play.google.com/store/apps/details?id=com.anthonymandra.rawdroid "RAWDroid Demo - Google Play") (免费)

RAWDroid 是一个功能强大的 5 美元画廊，旨在让专业摄影师将他们的 DSLR 照片导出到平板电脑上，以便快速向客户展示他们的作品。演示版做的差不多，但是是带水印的免费包。与 RAW Decoder 不同，这是一个真正的图库界面，包含 JPEG 和 dng 的缩略图(如果在设置中打开了 JPEG)。不幸的是，分类和过滤图像的工具还没有出现，jpegs 被作为一个块推到每个文件夹的底部。这使得并排查看 raw/jpeg 文件很困难。

图像浏览器本身非常健壮。诸如左右滑动以在相机胶卷中前进、RGB 直方图、元数据预览以及平移和缩放支持等功能可以快速检查构图问题。该演示确实限制了原始预览的分辨率，并在屏幕上添加了水印，但这些都是不改变功能的小让步。

如果需要，可以进行文件类型转换，尽管不如原始解码器那样健壮。在我的测试中，将图像转换成 jpegs 格式将像素从 1300 万减少到了 3.3 万。值得注意的是，记住 330 万像素仍然足以在脸书/Instagram 上分享，没有未经编辑的原始文件(或 jpeg 转换)会像谷歌相机的 HDR+照片一样好。你会希望[继续阅读](#alternatives)以获得轻量级编辑建议，从而在上传之前消除瑕疵、纹理和噪声。

**结论:**比起 RAW Decoder，它更像是一款精致的图库应用，但缺乏排序和过滤工具阻碍了它的发展。

### 组合原始照片管理器

 **下载: [Google Play](https://play.google.com/store/apps/details?id=com.BrainyLantern.slingShotPortfolio "Portfolio RAW Photo Manager") (免费)

排序，过滤，书签，颜色代码，并查看您的 jpegs 和 dng 在一起(作为图书馆，文件夹或相册)。这款应用满足了你对图片库的许多期望，并且是浏览你的 dng 的最好的免费方式。虽然它不会赢得任何风格的奖项，而且它不是物质的，但设计是精心策划的。

除了 RAWDroid 之外，图像查看器*还包含了*有用的信息:元数据、合成直方图、星级、书签颜色、旋转控件、电影胶片等。电影胶片和直方图可以通过单独的屏幕按钮进行切换，整个用户界面(保存顶部栏)在单次点击后消失。起初这看起来有些混乱，你很快就会喜欢上它的特性集和定制。此外，工具是你批判性审查缩略图所需要的。

与 RAWDroid 一样，小数字水印覆盖原始图像(尽管不是 jpegs)，而文件类型转换和高分辨率预览等更高级的功能只需付费。

# 功能齐全的编辑人员(&查看者)

在台式机/笔记本电脑方面，Adobe 的 Photoshop 和 Lightroom 等主流软件主导了我们对照片编辑器的看法，但也有许多免费的选择来编辑原始图像。其中比较受欢迎的有:

*   **[RAW Therapee](http://rawtherapee.com/ "RAW therapee")**——全面免费打包消除神器，添加颜色配置文件，一般把你的文件编辑成战斗形状。
*   [](http://www.gimp.org/ "GNU Image Manipulation Program")**-GNU 图像操纵程序。先进的照片编辑免费开源软件。这个软件包不像 Photoshop 那样用户友好，但功能集非常相似。**

 **另一方面，谷歌的 Play Store 坚定地分为两个阵营:快速有趣的过滤器和调整，以及高价的桌面替换软件。为了让你开始，这里是每个类别中最著名的应用程序(可以处理无损文件类型)。

*   **[Adobe Photoshop Express](https://play.google.com/store/apps/details?id=com.adobe.psmobile "Adobe Photoshop Express")**(免费增值)——非常适合快速编辑，但严肃编辑需要 Adobe Creative Cloud 帐户。没有自己的画廊。尽管它带有 Adobe 的名称，但不要期望在这里找到所有的花哨功能；重点是瑕疵控制和过滤器，而不是复制桌面体验。
*   [**照片伴侣 R2**](https://play.google.com/store/apps/details?id=com.tssystems.photomate2 "Photo Mate R2 - Google Play")(9.49 美元)——全套服务编辑器和查看器，是原始解码器演示的老大哥，如上图。评价、组织、标注、标记和编辑所有常见的属性，以制作出真正壮观的图像。

现在所有的基础都包括在内了，你觉得怎么样？我是否错过了折扣付费应用支持免费桌面版的机会？我错过了你最喜欢的编辑或观众之一吗？在评论中开始讨论吧！******