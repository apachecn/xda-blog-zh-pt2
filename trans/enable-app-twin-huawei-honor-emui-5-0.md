# 如何在采用 EMUI 5.0 的华为& Honor 设备上启用 App Twin 功能

> 原文：<https://www.xda-developers.com/enable-app-twin-huawei-honor-emui-5-0/>

# 如何在采用 EMUI 5.0 的华为& Honor 设备上启用 App Twin 功能

如果你运行 EMUI 5.0 的华为或 Honor 设备没有 App Twin 功能，这里有一种方法可以在你拥有 rooted 权限的情况下启用它。

EMUI 5.0 与华为 Mate 9 一起发布，它带有一个名为 App Twin 的功能。App Twin 允许您克隆某些应用程序，以便您可以设置多个帐户。App Twin 让你克隆的应用程序的原始列表相当有限，但我们想出了如何让它与任何启动器上的任何应用程序和[一起工作](https://www.xda-developers.com/how-to-use-emuis-app-twin-feature-on-any-launcher/)[。](https://www.xda-developers.com/how-to-clone-any-application-with-emuis-app-twin-feature-no-root/)

不过，并非所有安装了 EMUI 5.0 的设备都支持 App Twin，尤其是那些收到更新的设备。该功能仍然存在，但似乎该公司出于某种原因隐藏或禁用了它。谢天谢地，XDA 资深会员 [shashank1320](https://forum.xda-developers.com/member.php?u=6714681) 已经找到了一种方法，让你可以在各种 EMUI 5.0 设备上启用这个功能。

这个方法确实需要 root 访问权限，因为我们正在/system 分区中编辑系统属性文件。您要做的是使用一个支持 root 的文件浏览器，比如 MiXplorer，来编辑这个路径中的文件:/system/emui/lite/prop。

[appbox xda com.mixplorer]

您将编辑 local.prop 文件(确保复制该文件并将其保存在其他地方，以防出错！)更改以下行:

```
fw.max_users=1 to 2

fw.show_multiuserui=0 至 **1** 

ro . config . HW _ support _ clone _ app = false to**true**
```

* * *

[**查看我们论坛的完整指南**](https://forum.xda-developers.com/honor-6x/how-to/guide-enable-app-twin-feature-emui-5-0-t3691166)