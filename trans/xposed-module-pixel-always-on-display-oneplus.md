# Xposed 模块为一加设备增加了类似像素的始终显示

> 原文：<https://www.xda-developers.com/xposed-module-pixel-always-on-display-oneplus/>

“永远显示”已经成为一个很酷的功能，我们可以在几款主打有机发光二极管显示的旗舰产品上看到。始终显示(AOD)背后的基本思想是让某一组信息始终显示在您的设备上，同时消耗最小的功率。尽管想法是一样的，但 aod 的实现在不同的 OEM 厂商之间有所不同，很多用户更喜欢 Google Pixel 的实现。现在，一个 Xposed 模块有望为一加设备带来类似像素的永远显示实现。

在开始之前，您应该知道这个模块主要是中文的。除非你懂这门语言，否则你需要一些帮助来了解这个“常亮显示”模块的各种设置。第一个帖子有翻译文本的截图，随后在论坛帖子中的[帖子](https://forum.xda-developers.com/showpost.php?p=79912483&postcount=65)有该模块新版本的翻译文本。显然，该模块取代了设备上的环境显示选项。如上所述，“正在播放”功能依赖于手机上播放的音乐，而不是手机周围播放的音乐，因此这是功能上的一个差异。

**[像像素一样一直显示在一加设备上](https://forum.xda-developers.com/oneplus-6t/themes/exposed-pixel-display-oneplus-6t-t3947995)**

由于该模块在 Android Pie 上工作，您将需要非官方的 x exposed 框架，即[EDX exposed with Riru Core](https://www.xda-developers.com/xposed-framework-unofficial-port-android-pie/)。完成安装后，从上面链接的线程安装模块(2.5 版)，激活它，然后重启设备。[或者](https://forum.xda-developers.com/showpost.php?p=79923016&postcount=142)，你可以从 Magisk 安装太极模块，然后从太极库安装这个 AOD 模块。此外，请确保“设置”应用程序中的一加环境显示设置已为“触摸唤醒”打开

请记住，该模块不是开源的。试用该模块的成员声称，这种始终显示实现的电池消耗约为每小时 1.2%，这是一种高效的权衡。据说 AOD 元件还具有内置的防显示器老化保护。显示中的指纹扫描仪图形没有主题，所以你可以使用底层主题使其透明，或者使用 [Magisk 模块来达到相同的效果](https://forum.xda-developers.com/showpost.php?p=79899109&postcount=28)。如果你不喜欢使用 24 小时制，会员们已经[修改了模块](https://forum.xda-developers.com/showpost.php?p=79935015&postcount=173)来支持 12 小时制。