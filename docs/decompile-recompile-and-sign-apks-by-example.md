# 反编译、重新编译和签名 apk 的例子

> 原文：<https://www.xda-developers.com/decompile-recompile-and-sign-apks-by-example/>

上个月，我们看到了[一个新工具](http://www.xda-developers.com/android/decompile-and-recompile-classes-dex-with-ease/)，它使编辑 Classes.dex 的内容变得不那么痛苦。如果你被这种前景所吸引，但却不能很好地完成工作，我想你会喜欢效仿 XDA 认可的主题/贡献者 [Rizal Lovins](http://forum.xda-developers.com/member.php?u=4666531) 的做法。他后退一步来看更大的画面，给出了反编译、编辑、重新编译和签署 APK 文件的从头到尾的演练。必要的工具几乎是一样的(Windows、Java、Android SDK、Apktool 和一个文本编辑器)，这样你就可以继续你的 *smali* 和 *Baksmali* 编辑实验。

要使用 Apktool 反编译一个 APK，你还需要有它使用的支持包(即: *framework-res.apk* )。发出几个命令后，Apktool 会把隐藏在里面的文件吐出来，是时候开始编辑了。然后，Rizal 继续展示如何将所有东西打包备份，并重新提交编辑过的应用程序。检查出[的原始线程](http://forum.xda-developers.com/showthread.php?t=2195680)的全部细节。

出版这样的指南最大的好处是社区可以学习和改进它们。XDA 认出了他们，并照做了。[他的帖子](http://forum.xda-developers.com/showthread.php?t=2251719)提到了 Rizal 的工作作为参考，演示了如何使用相同的技术来更改字体颜色和编辑应用程序的活动标题栏。