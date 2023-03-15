# 使用 SplashInjector 更改一加设备的闪屏

> 原文：<https://www.xda-developers.com/splash-screen-oneplus-splashinjector/>

# 使用 SplashInjector 更改一加设备的闪屏

一个名为 SplashInjector 的新工具可以帮助您更改所有一加设备(OnePlus X 除外)上的启动闪屏。

有许多方法可以自定义您的设备，如图标包、第三方启动器和主题。如果你是 boot 的话，你还可以改变开机动画，也就是 Android 开机前经常出现的彩色 logo。但是也有闪屏，这是在启动动画之前显示在你的设备上的第一个东西。它只持续几秒钟，通常只显示制造商的名称。定制闪屏通常比改变启动动画或其他任何东西更困难，但多亏了一个新的一加设备工具，改变闪屏真的很容易。

XDA 资深会员 [bobglaus](https://forum.xda-developers.com/member.php?u=6726470) 在 XDA 资深会员 [makers_mark](https://forum.xda-developers.com/member.php?u=5448769) 去年创建的[闪屏图像注入器](https://forum.xda-developers.com/oneplus-3/themes/mod-splash-screen-image-injector-t3441999)的基础上，创建了[【Splash Injector】](https://forum.xda-developers.com/oneplus-5/themes/mod-splashinjector-t3650374)一个基本的命令行界面工具。该工具支持除 OnePlus X 之外的所有一加设备**(指 OnePlus One、OnePlus 2、OnePlus 3、OnePlus 3T 和 OnePlus 5)，它的开发是为了轻松、无痛地修改启动闪屏，以实现额外的定制。**

开发人员表示，该工具主要支持基于 Unix 的系统，有点“笨拙”。版本 1.52 支持 Windows，但是，该工具失去了在各自的操作系统上打包文件的能力。开发者可以使用诸如[Android flash able Zip Creator](https://forum.xda-developers.com/android/software-hacking/tool-6-feb-android-flashable-zip-t3551772)这样的工具来弥补失去的能力。该工具(在其当前状态下)可以成功解码和编码所有支持的一加设备的“logo.bin”文件。它有额外的能力，包装闪光拉链自动。

所有需要做的是快速运行“解码”命令，然后对输出文件夹中的文件进行偏好驱动的编辑。“encode”命令会将所有内容打包备份。为了创建一个以上的包,“package”命令是必不可少的。使用说明已经方便地存放在 GitHub 的[这里](https://github.com/ethanbanker2428/SplashInjector)。

* * *

[**用喷溅喷射器**](https://forum.xda-developers.com/oneplus-5/themes/mod-splashinjector-t3650374) 改变喷溅画面