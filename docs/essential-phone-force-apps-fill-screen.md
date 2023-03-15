# 如何让应用程序填满手机屏幕

> 原文：<https://www.xda-developers.com/essential-phone-force-apps-fill-screen/>

当安迪·鲁宾(Andy Rubin)第一次推出基本款手机(Essential Phone)时，许多人都对该公司能够推出的无边框设计感到惊讶。一个突出的特点是显示屏顶部的摄像头和传感器。夏普和小米等其他原始设备制造商决定将摄像头和传感器嵌入他们无边框手机的底部下巴边框，但 Essential 走了一条不同的路线。事实上，当一些人第一次看到智能手机时，他们认为这个功能会分散他们的注意力。

评论纷至沓来，很多人说摄像头和传感器的切口并不像他们最初认为的那样令人分心。该设备的当前所有者表示，你的眼睛开始忽略它，你不再注意它，直到某些应用程序使它的存在变得太明显而无法忽略。虽然某些应用程序被允许融入基本手机的状态栏，但并不是每个应用程序都能做到这一点。

这里有一个例子，当一个应用程序不覆盖屏幕顶部时，它在基本手机上是什么样子。应用程序的其余部分看起来和功能都正常，但是状态栏上方有一个令人分心的空间，看起来很丑。谢天谢地，有一种不需要 root 就能解决这个问题的方法。Essential 实际上有一个允许充分利用状态栏区域的应用程序的白名单，谢天谢地，我们有一个编辑白名单的方法。

* * *

## 让应用程序充满基本手机的屏幕

最简单的方法是使用谷歌 Play 商店上的一个名为“布局白名单编辑器”的应用程序。

这是一个由 Reddit 用户 TsFreddie 在/r/Essential subredit 上制作的[开源应用](https://github.com/TsFreddie/EssentialLayoutWhitelist/releases)，它可以让你在应用列表中添加或删除单个应用。[多亏了 XDA 资深会员](https://forum.xda-developers.com/essential-phone/themes/essential-layout-whitelist-editor-t3671285) [tw1tch175](https://forum.xda-developers.com/member.php?u=3397810) 这才引起了我们的注意。你所要做的就是安装应用程序，然后通过 ADB 授予它一个隐藏的权限，我们会告诉你怎么做。

1.  从上面的 Play Store 链接下载并安装“布局白名单编辑器”。
2.  [按照本教程中的概述设置 ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) 。
3.  打开命令提示符/终端，输入以下命令:`adb shell pm grant in.tsdo.elw android.permission.WRITE_SECURE_SETTINGS`
4.  就是这样！现在打开应用程序，开始将你想要的任何应用程序加入白名单，以填充基本手机的状态栏！

一旦你选择了想要加入白名单的应用程序，你应该会看到这些应用程序(尤其是第三方启动器)开始占据你的设备的整个屏幕。如果没有，建议您继续并重新启动智能手机，但它应该立即工作。这样做之后，应用程序看起来应该会更好。第三方启动器(如 Action Launcher)的壁纸现在应该扩展到显示器的顶部，这样它将创建一个更加身临其境的体验。

 <picture>![essential phone after](img/accc59cb4c4f43b28cf8e1281f8cfdf4.png)</picture> 

Credit: Reddit user [heyitzrj](https://www.reddit.com/user/heyitzrj)

我在这里说应该是因为在某些情况下，并不是所有的应用程序都能很好地使用这个设置。我们论坛中的一些人表示 Tapatalk 无法正常工作，但另一个人说[这种冲突是由于应用程序的黑暗主题](https://forum.xda-developers.com/essential-phone/themes/fix-apps-filling-screen-nova-included-t3670404/post73788608#post73788608)选项。

* * *

## 说明

Essential Products 希望确保添加到此白名单中的应用程序和游戏能够正常工作，并且看起来像它们应该的样子。目前，开发者必须请求加入白名单，虽然公司正在努力改善这种情况，但你最喜欢的应用程序可能需要一段时间才能加入白名单。甚至流行的 Nova Launcher 也只是刚刚被添加到基本手机的白名单中。谢天谢地，我们有办法绕过软件设置的限制。

使用上面的应用程序，我们能够手动修改 Essential 设置的白名单。该应用程序所做的是使用逗号分隔的包名列表写入名为`Settings.Global.ESSENTIAL_LAYOUT_WHITELIST`的首选项，这些包名代表您想要加入白名单的应用程序。这与我们在之前的教程中概述的许多技巧没有什么不同，但该应用程序使这一过程变得简单得多，因为当你想修改这个白名单时，你不需要随时处理命令行。

所以你有它。安迪·鲁宾的第一部智能手机几乎不可能完全符合所有人的要求，但至少它的一些最突出的问题有一些解决办法。人们对这款手机的另一个抱怨是相机，但[有一个解决办法，至少可以提高相机的质量(即使它忽略了单色传感器)。](https://www.xda-developers.com/essential-phone-camera-quality-fix/)