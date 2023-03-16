# 一加发射器暗示威瑞森和一加 8 的 NFC 壁纸

> 原文：<https://www.xda-developers.com/oneplus-launcher-oneplus-8-verizon-nfc-wallpapers/>

一加今天在谷歌 Play 商店推出了一加发射器 4.3.3，做了一些面向用户的改变，比如隐藏图标标签的能力和货架的 AMOLED 黑色主题。然而，我们分析了 APK，发现了一些关于即将推出的一加 8 智能手机系列的有趣发现。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**威瑞森一加 8 号基本上确认了**

AndroidPolice 已经两次报道了威瑞森出售一加手机的计划。他们最早在 2019 年 9 月[报道称](https://www.xda-developers.com/oneplus-7t-pro-5g-mclaren-edition-verizon-2020/)威瑞森签署了一项在 2020 年运营一加手机的协议。然后在今年 1 月，他们跟进了[一份更具体的报告](https://www.xda-developers.com/oneplus-8-verizon-5g-ultra-wideband/)，声称一加 8 将在威瑞森推出，支持运营商的毫米波“超宽带”网络。一加最初通过与 T-Mobile 的合作关系进入美国市场，去年他们通过与 Sprint 合作开发一加 7 Pro 5G 扩大了他们的市场份额。与威瑞森签约是一加合乎逻辑的下一步行动，假设一加 8 即将推出的传言是真的，我们可以看到威瑞森一加 8 5G 在几周内推出。

虽然我们没有关于这一合作关系的任何其他细节可以分享，但我们对一加发射器版本 4.3.3 的分析基本上确认了下一款一加智能手机确实会有一个威瑞森·SKU。在最新的一加发射器 APK 中，我们可以找到多项证据。首先，一加为威瑞森文件夹添加了一个新字符串，这表明预装的威瑞森应用程序将出现在主屏幕上的一个单独的文件夹中。(向 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 致敬，感谢他让我们注意到这个问题。)

```
 <string name="verizon_folder_title">Verizon</string> 
```

接下来，在“SkuHelper”类中，我们发现了一个名为“isVerizon”的方法，如果软件类型是“威瑞森”，该方法将返回 true 这表明威瑞森模式将运行独立的软件，如现有的 T-Mobile 一加 6T/7 Pro/7T Pro 和 Sprint 一加 7 Pro 设备。最后，DeviceHelper 类中的一个 switch 语句明确地将“OnePlus8VZW”列为其中一种情况。这与“OnePlus8TMO”和其他一加设备并列。这是威瑞森·一加 8 号存在的最清晰的证据。

**NFC 壁纸定制**

因为这只是一个启动器应用程序，所以没有太多关于实际设备的信息。然而，我们确实发现了一加 8 的一个正在开发的新功能。这项功能可能会让你扫描一个 NFC 标签来设置一个独特的壁纸。一加发射器 4.3.3 增加了两个新字符串，一个说“嘿，你找到了一个全新的壁纸！”当你扫描一个标签和另一个写着“设置壁纸”的标签时，它可能会出现在让你将该图片设置为当前壁纸的按钮上。

```
 <string name="nfc_customization_wallpaper">Hey, you've found a brand new wallpaper!</string>
<string name="setting_nfc_customization_wallpaper">Set wallpaper</string> 
```

清单中还有一个名为 net . oneplus . launcher . WALLPAPER . customizationwallpapernfcreceiver 和意向操作过滤器 net . oneplus . launcher . action . customization _ WALLPAPER _ NFC _ DETECTED 的新广播接收器。该接收器允许一加发射器检测何时扫描到预先格式化以发送该意图的 NFC 标签。在 CustomizationWallpaperNFCReceiver 和 LauncherSettings 类中，我们可以看到该功能仅限于新的一加 8 系列(在 DeviceHelper 中有对一个名为“isAtLeastOP8DeviceVersion”的方法的调用)，并且共有 3 种壁纸可供选择。也许一加将出售内置 NFC 标签的外壳，当扫描时，会改变一加 8 的壁纸以匹配外壳。几年前，谷歌曾经用真实案例来做这件事[。我们不知道一加计划如何向用户展示这些壁纸，但我们可能会在手机发布时知道。](https://www.xda-developers.com/google-nexus-pixel-live-cases-nfc-dropped/)

根据来自 *@Onleaks* 的一组可信泄露，一加 8 系列将有 3 款设备:[一加 8 Lite](https://www.xda-developers.com/oneplus-8-lite-leaked-renders-mid-range-phone/) 、[一加 8](https://www.xda-developers.com/oneplus-8-punch-hole-display-triple-cameras-leak/) 和[一加 8 Pro](https://www.xda-developers.com/oneplus-8-pro-leaked-renders-show-quad-camera-setup-punch-hole-display/) 。8 Lite 预计将配备 90Hz 显示屏和[联发科天玑 1000L](https://www.xda-developers.com/mediatek-dimensity-1000-7nm-soc-integrated-5g/) 处理器，而 8 和 8 Pro 预计将配备 [120Hz 显示屏](https://www.xda-developers.com/oneplus-confirms-120hz-display-refresh-rate-tech/)和[高通骁龙 865](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/) 。预计这三款设备都将有打孔显示屏，无线充电也可能最终在左右得到支持。当我们了解到更多关于一加 8 系列的信息时，我们会及时通知您。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*