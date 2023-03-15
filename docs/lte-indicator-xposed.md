# 用 x 曝光改变你的状态栏 LTE 指示器

> 原文：<https://www.xda-developers.com/lte-indicator-xposed/>

# 用 x 曝光改变你的状态栏 LTE 指示器

使用这个简单的 Xposed 框架模块选择如何在您的设备上显示 LTE 连接。4G 还是 LTE？你的电话！

在许多国家，LTE 已经慢慢成为移动互联网的标准。原始设备制造商总是试图纳入最新的硬件解决方案，因此拥有一部支持 LTE 的手机或平板电脑并不稀奇。因此，几乎所有旗舰设备都支持各种 LTE 频段。

默认情况下，Android 会指示当前的连接类型。这显示在屏幕的右上角，就在时钟旁边。一些原始设备制造商更喜欢显示 LTE，而另一些则简单地使用 4G 图标。如果你想在飞行中交换你的，XDA 资深会员 [hamzahrmalik](http://forum.xda-developers.com/member.php?u=5290145) 准备了一个曝光模块，让你毫不费力地做到这一点。你可以很容易地改变你的图标，而不需要重新编译你的 ROM 的整个系统界面。不要让 OEM 或者运营商来决定。相反，你可以自己做出选择！

自然，这个模块需要 Xposed 框架才能工作。您可以在专门的 Xposed 框架论坛中找到应用程序和模块集合。要使用它，您的设备当然必须是根设备。

如果您不喜欢您的 LTE 连接在设备上的显示方式，请前往 [4G LTE 状态栏暴露线程](http://forum.xda-developers.com/xposed/modules/mod-switch-4g-lte-statusbar-indicators-t2849912)并立即进行更改。4G 还是 LTE:由你决定！