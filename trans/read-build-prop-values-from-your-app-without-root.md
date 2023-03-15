# 从您的应用程序读取 Build.prop 值，无需 Root 用户

> 原文：<https://www.xda-developers.com/read-build-prop-values-from-your-app-without-root/>

我们在过去推出了许多工具，允许最终用户修改自己的*版本*。我们还为[应用开发者提供了一套工具来整合](http://www.xda-developers.com/android/build-prop-tools-library-for-app-development/ "Build.prop Tools Library for App Development")，允许应用程序修改文件。这些(显然)都需要 root 访问权限，因为您正在修改系统设置。然而，到目前为止，我们还没有从应用程序中读取 *build.prop* 的方法。

应用程序开发人员希望只读访问设备的 *build.prop* 有很多原因。无论是了解它的软件或硬件配置，还是简单地查看一些系统设置，查看这个信息宝库对应用程序开发人员来说都可能非常有用。然而，从用户的麻烦和安全的角度来看，要求 root 用户访问是不必要的。

XDA 论坛成员[鱼雷穆罕默迪](http://forum.xda-developers.com/member.php?u=4820832)写了几行代码，并与社区分享。他做这件事的方式可以用他的解释来概括:

> **1。创建一个从“/system/bin/getprop”目录执行“getprop”的进程，并初始化我们想要获取的字符串(示例中为 ro.board.platform)。**
> 
> 2.创建一个 BufferedReader，它通过从 inputStreamReader()中检索数据来获取值(字符串)。
> 
> 3.将 BufferedReader 转换为 String。

前往[原始线程](http://forum.xda-developers.com/showthread.php?t=2375952)开始，复制代码，并将其实现到您的应用程序中。