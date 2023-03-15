# 使用 Zip 创建器轻松创建恢复兼容归档

> 原文：<https://www.xda-developers.com/easily-create-recovery-compatible-archives-with-zip-creator/>

如果你曾经想做一个 flashable ZIP，你肯定知道写一个合适的*更新脚本*需要做多少工作。不久前，我们推出了一款 [Windows 专用工具](http://www.xda-developers.com/android/fix-edify-syntax-errors-with-edisense-code-editor/)和 [Geany 插件](http://www.xda-developers.com/android/check-edify-syntax-on-every-os-with-geany-plugin/)来查找你所有的语法错误，但你仍然必须自己输入所有的命令。

你的更新脚本噩梦已经结束，因为 XDA 论坛成员 [OrglCe](http://forum.xda-developers.com/member.php?u=5182342) 创建了一个非常有用的仅限 Windows 的应用程序，该应用程序自动化了使用适当的*更新脚本*和二进制文件创建 flash ZIP 的过程。然后利用 *DotNetZip* 库对归档文件进行压缩。

使用 Zip Creator，您可以轻松地为用户应用程序、系统应用程序、框架文件和启动动画创建可刷新的 Zip。你也可以用它来编辑*更新脚本。*在即将推出的版本中，可以使用多个应用程序创建拉链。

该应用程序非常容易使用，所以即使是初学者也应该能够创建一个恢复兼容的 ZIP 文件。这个工具唯一的缺点是它不能和 KitKat 一起正常工作。然而，这是因为谷歌在最新版本的 Android 中对*更新程序脚本*的处理做了一些改动。

希望获得 Zip Creator 最新版本的 Windows 用户应该使用[实用线程](http://forum.xda-developers.com/showthread.php?t=2629989)。