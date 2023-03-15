# 开发者将 Pixel 启动器和 Google Now 面板移植到非 root 设备上

> 原文：<https://www.xda-developers.com/developer-ports-the-pixel-launcher-with-the-google-now-panel-for-unrooted-devices/>

不久前，谷歌从开发 Google Now 启动器(之前称为谷歌体验启动器)转向为其智能手机和平板电脑开发新的 Pixel 启动器。谷歌停止使用 Google Now 是有道理的，但这肯定不会让很多人高兴。随着 Pixel Launcher 被谷歌 Pixel、Pixel XL 和 Pixel C 独占，人们开始寻找其他安装方式。

我们在去年 9 月讨论了如何侧装 [Pixel Launcher，然后就在上个月，当 Android O 开发者预览版 2](https://www.xda-developers.com/googles-upcoming-pixel-launcher-available-for-download-unofficially/) 的[更新版本发布时。这些端口有缺点，因为一些重要的特性被忽略了，除非它们作为系统应用程序安装——这需要 root 访问。然而，一个社区开发者开始研究这个问题，当他们看到偏执的 Android 如何实现 Google Now 面板，即使它是作为一个常规应用程序安装的。](https://www.xda-developers.com/pixel-launcher-for-android-o-dev-preview-2-ported-to-6-0-1-devices/)

在 Reddit 上被称为 AmirZ 的开发者开始研究 Pixel Launcher 和 AOSP 的 Launcher3。他们花了很多时间将 Pixel Launcher 中的一些代码导入 Launcher3，然后发现另一名开发人员已经开始从事类似的项目。这位开发者自称 *DeleteScape* ，两人在 Telegram 上搭讪讨论此事。DeleteScape 很好地分享了他的部分解密代码，这使得 *AmirZ* 取得了很大的进步。

AmirZ 表示，这种 Pixel Launcher 端口的一个限制是，它必须与实际的 Pixel Launcher 具有相同的包名。如果不这样做，天气窗口小部件将无法工作，所以在你尝试安装 Pixel Launcher 之前，你需要**确保它没有被安装**。他们说 A/B 测试和麦克风图标不包括在内，也没有任何切换功能。但是，这个版本确实有一个工作的 Google Now 面板，G pill 动画，向上滑动应用程序抽屉，天气窗口和日期窗口。

* * *

[**来源:/r/Android**](https://www.reddit.com/r/Android/comments/6gn8f9/rootless_pixel_launcher_port/)