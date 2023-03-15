# 如何立即在 Google 相册中启用 Google Lens[Root]

> 原文：<https://www.xda-developers.com/enable-google-lens-in-google-photos-right-now/>

羡慕新[谷歌 Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 车主？鉴于[最近一些用户遇到的显示问题](https://www.xda-developers.com/google-pixel-2-xl-display-burn-issues/)，也许你的嫉妒已经有所减弱。尽管如此，还是有一些 Pixel 独有的软件功能，你可能真的想试试，比如[谷歌镜头](https://www.xda-developers.com/google-lens-preview-state-pixel-2/)。这是一个非常巧妙的功能，它利用谷歌的机器学习技术来扫描图像，以显示相关信息。例如，它认出了这只 Redditor 的特殊猫品种 T7。在过去的无数[场合](https://www.xda-developers.com/try-google-lens-launcher-google-photos/)[中，我们尝试过让谷歌镜头工作——尽管每次谷歌都很快关闭了这个方法。我们再次带来了另一种在 Google 相册中启用 Google Lens 的方式**。**](https://www.xda-developers.com/enable-google-lens-in-google-assistant-right-now/)

* * *

## 谷歌镜头是什么？

这项功能是在今年的谷歌 I/O 上宣布的，它允许你通过谷歌助手(Google Assistant)对准相机或分析现有图像(通过谷歌照片)来提供关于你正在看的东西的有用信息。在舞台上，该公司展示了分析花朵的镜头，以显示它是哪种花，将手机摄像头对准餐馆以查看最近的评论等信息，或者扫描 WiFi 网络贴纸以连接网络。许多人将它与谷歌眼镜相提并论，但它可以被视为谷歌眼镜的精神继承者。

根据我们不久前对 Google 相册进行的 APK 拆解，以下是 Google Lens 目前的功能:

**识别**:

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

**执行:**

*   从名片添加联系人
*   语言翻译
*   查找产品信息
*   在浏览器中打开网址
*   植物和动物识别
*   将海报中的日期保存到日历中

* * *

## 立即在 Google 相册中试用 Google Lens

就像以前的方法一样，我们将欺骗谷歌照片应用程序，使其认为手机是谷歌 Pixel 2。我们通过在/system/etc/sysconfig 中添加 Google Pixel 2 独有的文件来做到这一点。我确认了这些文件在设备的[工厂映像中的存在。这些文件名为 pixel_2017.xml 和 pixel_2017_exclusive.xml，包含以下行:](https://www.xda-developers.com/google-factory-images-pixel-2-xl/)

### pixel_2017.xml

```
 <?xml version="1.0" encoding="utf-8"?>

<config>

<feature name="com.google.android.feature.PIXEL_2017_EXPERIENCE" />
</config> 
```

### pixel_2017_exclusive.xml

```
 <?xml version="1.0" encoding="utf-8"?>

<config>

<feature name="com.google.android.apps.photos.PIXEL_2017_PRELOAD" />
</config> 
```

用户以前只需在这个目录中添加一个名为“nexus.xml”的文件就可以了，但现在看来它已经不再单独工作了。但是随着/system/etc/sysconfig 中包含了这两个文件，Google Photos 中的 Google Lens 现在就可以工作了。

那么你实际上是做什么的呢？就这么简单！按照以下步骤在根 Android 设备上的 Google 相册中启用 Google Lens(在我的 OnePlus 5 上测试，运行 Android 7.1 牛轧糖上的 OxygenOS):

### 如何启用谷歌镜头

1.  下载 XDA 成员 [ZeevoX](https://forum.xda-developers.com/member.php?u=6375026) 制作的[本帖](https://forum.xda-developers.com/oneplus-3/themes/flashable-zip-google-lens-pixel-2-t3693859)中的 flash zip 文件
2.  重新启动进入 TWRP 恢复
3.  恢复时刷新压缩文件
4.  重新启动安卓系统，打开谷歌照片

根据 ZeevoX 的说法，你甚至不需要清除谷歌照片中的应用程序数据！他制作了一个简短的屏幕记录，展示了激活谷歌镜头的过程。请注意，虽然他在 OnePlus 3 论坛上发布了这一点，但对 OnePlus 3 的这一修改没有任何具体或独特之处，因此它应该可以在任何根 Android 设备上工作！

现在就试试 Google Lens，让我们知道你的想法吧！谷歌可以很容易地通过在未来几小时或几天内更新谷歌照片来修补这种方法，但鉴于 Pixel 2 智能手机已经上市，Android Nougat 的 [Xposed 框架已经推出](https://www.xda-developers.com/official-xposed-framework-android-nougat/)，他们很难继续与我们玩这种猫捉老鼠的游戏。