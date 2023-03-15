# 使用 Google Lens Launcher for Google Photos 立即试用 Google Lens

> 原文：<https://www.xda-developers.com/try-google-lens-launcher-google-photos/>

**更新**:似乎在这篇文章发表后不久，谷歌有人扳动了服务器端的开关，使谷歌镜头不再工作。当它持续的时候它是有趣的！原文可以在下面阅读。

昨晚，谷歌开始推出谷歌照片应用程序 3.5.0.168271220 版本。正如对谷歌应用程序的任何升级一样，我们喜欢对应用程序进行所谓的“ [APK 拆卸](https://www.xda-developers.com/tag/apk-teardown/)”。通过反编译应用程序，我们可以查看尚未公开的隐藏字符串和资产。这些信息有助于我们确定在即将到来的应用更新中我们可能会期待什么功能。但昨天 APK 对谷歌照片应用的关闭有点不同寻常。我们不仅发现了[宣布的谷歌镜头集成](https://www.xda-developers.com/google-lens-introduced-at-io-allows-you-to-connect-to-a-wifi-network-by-pointing-your-camera/)的更多证据，而且我们发现该功能实际上是[完全功能化的，](https://www.xda-developers.com/google-lens-google-photos-functional/)前提是你对 Android 的意图系统有点熟悉。

然而，我们的许多读者都不是开发人员，所以我们决定让访问 Google 相册中隐藏的 Google 镜头功能变得更容易一些。这就是为什么我们自己的[杰夫·科克兰](https://www.xda-developers.com/interview-with-xda-labs-and-feed-developer-jeff-corcoran-app-rom-development-the-future-of-xda-apps-and-more/)，XDA 实验室和 XDA Feed 的首席开发者，炮制了一个我们称之为**谷歌镜头发射器**的应用。这是一个非常简单的应用程序，完全是为了一个目的而构建的:所以你可以**现在就在你的 Android 设备上试用谷歌眼镜**。

* * *

## 谷歌镜头是什么？

*在 Google I/O 2017 上宣布的 Google Lens 与 Google Photos 的集成*

对于那些不熟悉的人来说，谷歌镜头是一种利用谷歌机器学习技术的功能，以便根据它在图像中看到的内容来显示相关的上下文信息。例如，当谷歌在今年的谷歌 I/O 上展示该产品时，该公司展示了 Lens 分析花朵以确定它是哪种花。他们还展示了几个更有用的例子，例如将相机对准餐馆并接收相关信息，如评论，以及通过将相机对准路由器的标签来自动连接到 WiFi 网络。

可以把它看作是谷歌眼镜的精神继承者，尽管可以理解的是，谷歌眼镜和谷歌眼镜之间的界限目前还不太清楚，特别是因为我们迄今为止只有几个不完整版本的功能的早期实践体验。但多亏了最新的谷歌照片更新，我们现在可以尝试一下谷歌镜头的功能版本。

## Google Lens 能做什么？

虽然谷歌还没有正式发布谷歌镜头，但我们已经很好地了解了它目前的能力，这要感谢我们昨晚在 APK 的拆解。为了省去你再看一遍的麻烦，这里有一个镜头功能集的基本纲要:

**可以识别**:

*   艺术品
*   条形码
*   书
*   建筑物
*   陆标
*   媒体封面
*   电影
*   音乐专辑
*   涂漆
*   地方
*   兴趣点
*   状态
*   视频游戏

**可以执行:**

*   从名片添加联系人
*   语言翻译
*   查找产品信息
*   在浏览器中打开网址
*   植物和动物识别
*   将海报中的日期保存到日历中

如果 Lens 服务无法识别图像，它会依靠谷歌搜索引擎的能力让你自己查找。

## 使用 Google Lens Launcher for Google Photos 试用 Google Lens out

Google Lens Launcher 的工作方式相当简单。该应用通过使用一个[隐式意图过滤器](https://developer.android.com/guide/components/intents-filters.html#Receiving)在你的 Android 手机的共享菜单中注册自己，它接受与图像文件一起发送的[意图](https://developer.android.com/reference/android/content/Intent.html)。当用户将图片分享到 Google Lens Launcher 时，该应用程序将使用我们在之前的文章中找到的意图过滤器向 Google Photos 发送一个意图。具体来说，它以下列格式发送一个意图:

```
Action: com.android.camera.LENS

类别:默认

Mime 类型:image/*

data:file:///path/to/image/file

package:com . Google . Android . apps . photos

class:com . Google . Android . apps . photos . lens . OEM . lens activity
```

当 Google 相册收到这种格式的意向时，它会对其进行解析，并读取随其一起发送的图像文件。然后，它会自动开始使用谷歌的机器学习算法分析你发送的照片。基本上，我们的应用程序只是一个中间人，负责向 Google Lens 发送图像文件，直到 Google 正式推出与 Google Photos 的集成。在此之前，这个应用程序将为您提供一种方法来玩新功能，然后才是正式可用！

为了让它工作，你首先需要下载谷歌照片应用程序的**最新版本，如开头提到的**版本 3.5.0.168271220** 。你可以从 [XDA 实验室](https://labs.xda-developers.com/store/app/com.google.android.apps.photos)或[谷歌 Play 商店](https://play.google.com/store/apps/details?id=com.google.android.apps.photos)上下载这个应用程序。接下来，你需要**下载并安装谷歌镜头启动器应用**、[，可从 XDA 实验室的链接](https://labs.xda-developers.com/store/app/ca.mimic.lensflinger)获得。**

安装后，您可以通过使用内置的共享菜单将存储在设备上的任何图像文件共享给它，从而立即开始使用它。

请记住，我们在几个小时内就完成了这个应用程序。在这种情况下，它非常粗糙，并且不打算成为一个你可以长期使用的应用程序。我们会偶尔更新它，但不要对它期望太高，因为谷歌可以很容易地用另一个谷歌照片更新来关闭它。