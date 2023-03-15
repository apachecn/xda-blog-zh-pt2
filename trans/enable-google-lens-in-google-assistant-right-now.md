# 以下是如何在任何设备上启用 Google Assistant 中的 Google Lens[Root]

> 原文：<https://www.xda-developers.com/enable-google-lens-in-google-assistant-right-now/>

更新:看起来谷歌抓住了这个小技巧，并在他们的终端上禁用了对 Lens 的访问。希望你能在它持续的时候好好利用它！虽然本教程不再工作，我会留下下面的文章未经编辑。

本周，谷歌宣布了期待已久的第二代 Pixel 智能手机——谷歌 Pixel 2 和谷歌 Pixel 2 XL。与任何新的智能手机一样，通常会有该设备独有的新功能(至少目前如此)。一个这样的功能是谷歌镜头，据说[将在 Pixel 2 和 Pixel 2 XL 上的预览状态](https://www.xda-developers.com/google-lens-preview-state-pixel-2/)中推出。Google Lens 是一套基于视觉的计算能力，可以分析你正在看的东西——可以把它想象成 Google Goggles 的继任者。

[最初在 Google I/O 2017](https://www.xda-developers.com/google-lens-introduced-at-io-allows-you-to-connect-to-a-wifi-network-by-pointing-your-camera/) 上宣布，该功能被承诺最终将与另外两款谷歌产品集成:谷歌助手和谷歌照片。尽管在新的 Pixel 手机上推出了独家预览状态，但人们发现，谷歌助手中的谷歌镜头集成现在可以在任何植根于 Android 的设备上启用**。**

不久前，我们发现谷歌镜头集成在谷歌照片中功能齐全，尽管谷歌很快就为我们使用的方法打了补丁，当时我们[分享了一种访问谷歌镜头的简单方法。](https://www.xda-developers.com/try-google-lens-launcher-google-photos/)

但是 XDA 资深成员 [ani_me_sh](https://forum.xda-developers.com/member.php?u=7538540) 发现了一种[新方法](https://forum.xda-developers.com/redmi-note-3/themes/google-lens-t3684637)，允许根设备在谷歌助手中启用谷歌镜头。这个方法[类似于去年使用的一个技巧](https://forum.xda-developers.com/android/software/guide-how-to-enable-google-assistant-t3477879)在非谷歌设备上启用谷歌助手。我们将逐步指导您如何将谷歌镜头与谷歌助手集成。

* * *

## 教程-如何在谷歌助手中启用谷歌镜头

在我们开始之前，您需要有一个使用 SuperSU 或 Magisk 的**根**设备。然后，你需要一个根文件浏览器，比如我们论坛上的 MiXplorer。或者，您可以从 Play Store 下载 BuildProp Editor。

然后，按照以下步骤启用 Google Lens:

1.  安装最新的谷歌应用程序(版本 [7.13.21 测试版](https://www.apkmirror.com/apk/google-inc/google-search/google-search-7-13-21-release/)
2.  打开 BuildProp 编辑器，点击右上角的**铅笔图标**。这将允许您编辑/system 中的 build.prop 文件。
3.  找到(或添加，如果它不在那里)`ro.product.manufacturer`并改变任何有等于'**谷歌【T2]'**
4.  找到`ro.product.model`并将其更改为“ **Pixel 2 XL** ”
5.  最后，在任意位置添加下面一行:`ro.opa.eligible_device=true`
6.  点击**保存按钮**保存您的所有更改
7.  **重启**手机
8.  按下 home 键打开 Google Assistant，你现在应该会在右下角看到 Google Lens 按钮(如之前的截图所示！)

基本上，你是在欺骗谷歌应用程序，让它认为你的设备实际上是谷歌 Pixel 2 XL。似乎谷歌应用程序读取这些系统属性值来确定它在什么设备上运行，如果它返回 Pixel 2 XL，则启用谷歌镜头。

考虑到谷歌关闭先前方法的速度，我们并不指望这种变通办法永远有效，所以如果你现在想试用 Lens，我们建议你尽快试用它！我在运行最新 OxygenOS 的 OnePlus 5 上简单测试了一下，可以确认它确实有效。

### Google Lens 能做什么？

提醒一下，根据我们之前在 APK 对 Google 相册的拆除，Lens 应该能做些什么。

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

考虑到谷歌镜头是谷歌展示其机器学习技术的一个途径，我们推测谷歌将在久而久之添加更多功能。我们只是希望他们不要让这项功能成为 Pixel 2 的独家功能太久。目前，这种非官方的变通方法是你试用谷歌眼镜的最好机会！