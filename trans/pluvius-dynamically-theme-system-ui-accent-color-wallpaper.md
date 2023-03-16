# 基于壁纸的 Pluvius 主题系统用户界面和强调色[赠品]

> 原文：<https://www.xda-developers.com/pluvius-dynamically-theme-system-ui-accent-color-wallpaper/>

在 Android 8.0 Oreo 中，谷歌引入了索尼的原生主题框架，称为覆盖管理器服务(OMS。)可以构建覆盖图来针对任何应用程序的资源，包括 SystemUI 和 Android 框架，并用它们自己的值覆盖它们。这让我们可以在 Android 8.0 和 Android 8.1 上随心所欲地对 Android 的几乎任何部分进行主题化。不幸的是，谷歌[在 Android P 中阻止了对 OMS API 的访问](https://www.xda-developers.com/rootless-custom-themes-android-p/)，声明 OMS 仅供原始设备制造商使用。然而，如果你[有 root 权限](https://www.xda-developers.com/magisk-v16-6-samsung-galaxy-s9-project-treble-gsi-root-loss/)比如通过 Magisk，你仍然可以[在 Android P](https://www.xda-developers.com/custom-themes-android-p-root-substratum/) 上安装自定义主题。一款名为“Pluvius”的新应用刚刚发布，它以一种非常聪明的方式使用了 OMS:**根据当前壁纸动态主题化系统 UI 和强调颜色**。它需要 root 访问权限才能工作，但如果你通过了这个基本要求，那么你就可以在任何 Android 8.0 Oreo、Android 8.1 Oreo 或 Android P 设备上享受个性化主题，如 Google Pixel 2 或 Essential Phone。

*顶部截图:谷歌 Pixel 2 XL 运行[安卓 P Beta 3/开发者预览版 4](https://www.xda-developers.com/android-p-beta-3-google-pixel/) 。底部截图:运行 Android 8.1 奥利奥的必备手机。*

正如你在上面的一组截图中看到的，系统 UI 的主题是基于我选择的壁纸。(我这里用的壁纸是 Google Pixel 壁纸，可以通过非官方端口安装在任何设备上[。)在我的截图(最上面一行)中，我分别为自适应系统口音和自适应系统 UI 主题选择了“亮色”和“动态暗色”选项。你可以在应用程序中选择更多的颜色，根据自己的喜好动态调整你的 Android 设备。看看下面开发者的视频，看看这款应用的运行速度有多快。](https://forum.xda-developers.com/android/apps-games/port-live-earth-wallpapers-t3481640)

该应用程序使用 [Android 调色板 API](https://developer.android.com/training/material/palette-colors) 从壁纸中选择颜色。app 处理这个的逻辑可以在[这里](https://pastebin.com/ABYpA6bQ)找到。不幸的是，没有从动态壁纸中获取颜色的统一 API，所以该应用程序不能基于动态壁纸动态选择主题。

对于 Android P 支持，该应用程序的功能就像底层一样，它将覆盖放在/system/app 中。每个覆盖图的大小约为 5-6KB(覆盖图只包含 manifest 和 colors.xml 来主题化系统和框架),因此不应该担心系统存储空间会耗尽。您可以随时从应用程序的设置中卸载旧的覆盖图。Pluvius 安装的覆盖图包含自定义元数据，使它们可以被应用程序动态获取，因此它们可以被添加/删除/更新。

如果你经常更换壁纸(也许你使用像 [Muzei](https://www.xda-developers.com/muzei-v2-3-adds-runtime-permissions-direct-boot-support-next-artwork-quick-settings-tile-and-more/) 或 Chainfire 的 [500 Firepaper](https://forum.xda-developers.com/showthread.php?t=2522588) 这样的应用程序)，那么你肯定会喜欢这个出色的应用程序带来的额外定制。我已经[放弃了我在夜灯](https://www.xda-developers.com/enable-android-p-dark-theme-night-light/)上触发的自动黑暗主题，取而代之的是这个。

## 多种特征

*   独立的应用程序，不需要安装底层或仙女座菌株。
*   动态主题系统用户界面(快速设置面板，音量面板，电源菜单等)。)以及框架强调颜色(设置、滑块、按钮、切换等)。)基于当前壁纸。
*   **自适应系统色彩**选项:鲜艳、亮艳、暗艳或定制颜色
*   **自适应 SystemUI 主题**:暗、黑、自定义颜色、动态光、动态暗
*   支持安卓 8.0 奥利奥、安卓 8.1 奥利奥、安卓 P(都需要 root 权限)设备。可能无法在一些经过大量修改的 OEM 皮肤上工作。
*   可选的 Magisk 模块，只有想要通过 SafetyNet 的 Android P 用户才需要。Android Oreo 方法(PackageManager)不修改/system，因此它将通过 SafetyNet。

**计划功能:**

*   动态主题化通知
*   Android 8.0 和 Android 8.1 Oreo 的无根主题化(将需要一个附加应用程序和 ADB 命令)

## 下载并安装 Pluvius

您可以从谷歌 Play 商店下载该应用程序。有一个 **14 天的免费试用期**，之后你必须通过应用内购买(2 美元)来解锁应用。)

[**访问 XDA 论坛线程**](https://forum.xda-developers.com/android/apps-games/app-pluvius-dynamic-oms-framework-t3814394)

## Pluvius 解锁代码赠品

~~开发者慷慨赠予 *XDA 开发者*100 个解锁码给用户！我将**在评论中随机发布代码**，所以即使你没有立即看到这篇文章，你仍然可以要求一个代码！~~代码已全部发出，感谢各位留言评论！

* * *

*注意:本文不以任何方式得到 Pluvius 开发者的赞助。开发者是我们论坛上的活跃贡献者，出于礼貌，我们通常会涵盖活跃成员所做的应用程序、修改或其他任何我们认为读者可能感兴趣的内容。如果你在我们的论坛上分享了一些你认为值得在门户上大声喊出来的东西，[给我们发一条提示](https://www.xda-developers.com/tip-us/)。*