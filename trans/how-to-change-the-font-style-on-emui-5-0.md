# 如何在 EMUI 5.0 上改变字体样式[无根]

> 原文：<https://www.xda-developers.com/how-to-change-the-font-style-on-emui-5-0/>

华为 Emotion UI (EMUI)的一个关键特性是能够在设备上安装自定义主题。

主题可以打包成。然后可以由 EMUI 的主题管理器应用程序应用的 hwt 文件。用户可以自定义锁屏风格、壁纸、图标、背景颜色，最后是字体。

然而，一些升级到基于 Android 7.0 牛轧糖的最新版本 EMUI 5.0 的用户，却发现**“字体样式”选项少了****。此外，看起来这些用户甚至不能通过应用已经打包了他们自己的字体的定制主题来改变他们的字体。我可以证实，[华为 Mate 9](https://forum.xda-developers.com/mate-9) 就是这种情况，其他[很多](https://forum.xda-developers.com/mate-9/themes/how-add-change-download-fonts-mate-9-t3535714)也是如此。**

 **幸运的是，有一个非常简单的方法可以重新启用字体样式切换，**，并且不需要 root** 。如果您在 EMUI 5.0 上安装了华为设备，但在设置- >显示或系统主题管理器的定制菜单中找不到“字体样式”选项，那么您需要做的就是发送以下 ADB shell 命令:

`adb shell settings put system hw_hide_font_style false`

(注意:如果你不能让 ADB 工作，确保你安装了正确的驱动程序。安装 [HiSuite](http://consumer.huawei.com/minisite/HiSuite_en/index.html) 会自动获取正确的驱动程序。)

重启，现在你应该可以在运行 EMUI 5.0 的华为设备上编辑字体了！我希望这个技巧对你有用。这似乎不是每个运行 EMUI 5.0 的设备都存在的问题(我在 Mate 8、P9 和 Honor 8 论坛上看到了不同的报告)，但如果你还不能编辑你的字体，希望这对你有用。对我来说的确如此！

想尝试一些新字体吗？看看 XDA 资深会员 [venom007](https://forum.xda-developers.com/member.php?u=6139794) 为 EMUI 收集的[字体！这些可以作为常规安装。hwt 主题文件，所以它们不需要使用第三方主题管理器。](https://forum.xda-developers.com/mate-8/themes-apps/noroot-font-styles-updated-02-09-16-t3453559)**