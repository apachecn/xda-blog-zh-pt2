# 使用 Xposed 轻松定制您的索尼 Xperia Z 的启动器和锁屏

> 原文：<https://www.xda-developers.com/easily-customize-your-sony-xperia-zs-launcher-and-lock-screen-with-xposed/>

到目前为止，定制 Xperia 启动器和锁屏一直很麻烦，通常包括反编译 APK，进行编辑，然后重新编译。因此，如果你想在主屏幕上增加一行或一列图标，你必须闪烁*这个*，如果你想淡化主屏幕指示器，你必须闪烁*这个*，如果你想摆脱应用程序 dock，你必须闪烁*这个*，等等。对于你想要的每一个小的改变，都有一个你必须刷新的单独的模块，如果你想要很多的改变，这肯定会成为一个负担。

这可能就是为什么 XDA 论坛成员 [greg2001](http://forum.xda-developers.com/member.php?u=5597043) 开发了一个 Xposed 模块，将这种美学上的变化应用到[索尼 Xperia Z](http://forum.xda-developers.com/xperia-z) 的启动器和锁屏上。有了它，人们不再需要创建、查找和刷新过多的增量修改来制作自己的启动程序和锁屏。相反，XDA 认为开发者 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 的 [Xposed 框架](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/)会为你做所有的工作。

启动器和锁屏的完整调整列表如下:

*   发射器调整
    *   浓缩字体
    *   透明的状态/导航栏
    *   桌面网格大小
    *   桌面上的多行标签
    *   自动隐藏桌面上的页面指示器
    *   文件夹列
    *   文件夹中的多行标签
    *   打开文件夹时禁用启动器背景变暗
    *   停靠栏
    *   隐藏停靠舞台
    *   隐藏 dock 倒影
    *   大型码头倒影
    *   透明抽屉
    *   抽屉网格大小
    *   隐藏抽屉背板
*   锁屏调整
    *   透明状态栏
    *   启用支持动态壁纸的标准 AOSP 锁屏，可通过 GravityBox 定制
    *   隐藏快捷图标
    *   隐藏解锁提示箭头
    *   自定义/隐藏解锁提示文本
    *   自定义/隐藏运营商标签
    *   小百叶窗

因为这是一个曝光的模式，恢复到以前的设置很简单，只需轻敲几下，比以前方便得多。必须指出的是，该模块只能与运行官方 Android 4.3 固件的 Xperia Z 配合使用。

如果你想看看这个，请前往[原始线程](http://forum.xda-developers.com/showthread.php?t=2603569)获取更多信息。