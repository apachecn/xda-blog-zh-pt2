# 如何添加多用户支持到任何 Android 设备上？道具模式

> 原文：<https://www.xda-developers.com/add-multi-user-support-android/>

对于许多人来说，三星和 LG 设备上的 OEM 软件的可取之处之一是它们大量的有用功能。然而，三星和 T-Mobile LG 设备似乎莫名其妙地删除了一个非常有用的 Android 常用功能——多用户。

多用户是很有用的，因为它允许你和你认识的人共用一部手机，就像在一台电脑上有不同的用户账号一样。该功能内置于安卓系统中，你会在任何谷歌设备上发现它，华为或 LG 的大多数手机都会有它，但出于某种原因，三星(和 T-Mobile LG 设备)已经删除了它。

但是你实际上可以重新启用它，使用一个旧的，众所周知的对 build.prop 系统文件的修改，这是 XDA 资深成员 [Christoph21x](https://forum.xda-developers.com/member.php?u=1786104) 最近建议的。为了做到这一点，**你将需要通过 Magisk 或 SuperSU 的根访问。**

* * *

## 在任何 Android 设备上添加多用户支持

首先，安装一个可以修改 build.prop 文件的应用程序。我推荐 Build.prop 编辑器。

现在，打开应用程序，授予超级用户访问权限并滚动到底部，添加以下两行。

```
 fw.max_users=3 
```

```
 fw.show_multiuserui=1 
```

现在保存文件并重新启动！

现在，您应该能够通过将通知阴影一直下拉到展开的开关来添加用户。右上角应该有多用户选项。然后，您可以按住电源按钮来切换用户，因为电源菜单将会扩展以适应这个新选项。

这是如何工作的，我们正在修改一个由 AOSP 的[UserManager.java](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/os/UserManager.java)文件定义的系统属性值。UserManager 在启动时从 build.prop 文件中读取这些属性值，因此通过修改属性，我们可以重新启用该功能，即使某些设备已经禁用了它。

这是 build.prop 修改实际起作用的极少数情况之一。你会发现很多很多对 build.prop 文件的修改建议，这些建议承诺让你的手机更快，但现实是大多数修改根本没有任何作用。这是因为原始设备制造商对软件进行了大量的修改，如果没有源代码，我们就无法知道哪个 build.prop 编辑实际上会起作用，而不需要反复试验。