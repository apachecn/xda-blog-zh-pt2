# 用 Freecygn 从 CyanogenMod 中删除谷歌

> 原文：<https://www.xda-developers.com/remove-the-google-from-cyanogenmod-with-freecygn/>

CyanogenMod 是最流行的多设备 rom 之一。它也是 XDA 许多定制 rom 的基地。它支持一长串的设备，这使它成为最容易识别的定制 rom 之一。

当然，CyanogenMod 是一个源自 AOSP 的 ROM，这意味着该项目的大部分内容来自谷歌 Android repos 上的源代码。它也是开源的，任何人都可以免费获得它的源代码。不幸的是，并不是 CM 的每个元素都是开放的，因为一些应用程序和库是作为专有的二进制文件交付的。例如，这些文件大多来自谷歌服务，用于 CMAccount。

并不是每个用户都特别关心谷歌的专有部分及其随处放置的倾向。因此，XDA 的资深成员 MaR-V-iN 已经创建了一个脚本来清除所有 CM10+rom 中的谷歌专有二进制文件。Freecyngn 拆卸了 CyanogenMod 设置应用程序，并用免费的 NoAnalytics 替换了谷歌分析库。整个过程不会破坏设置应用程序，并把你的设备变成一个谷歌免费的。

安装非常简单。您只需将文件复制到 SD 卡或设备的内部存储器中。然后，只需通过自定义恢复来刷新它。

拥有一个没有谷歌的安卓系统是一个有趣的想法。如果你喜欢的话，就去[原始线程](http://forum.xda-developers.com/showthread.php?t=2550769)获取最新版本的脚本。此外，不要忘记看看我们之前关于[向谷歌应用程序](http://www.xda-developers.com/tag/say-sayonara/)说再见的系列报道。