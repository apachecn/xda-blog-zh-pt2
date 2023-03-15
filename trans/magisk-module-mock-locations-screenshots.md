# Magisk 模块允许位置模拟，在任何应用程序中截图，并禁用系统签名验证

> 原文：<https://www.xda-developers.com/magisk-module-mock-locations-screenshots/>

Magisk 是 Android 设备的无系统根和模块主机。通过使用 Magisk，用户可以在不破坏 SafetyNet 的情况下修改他们的 Android/系统分区。这是因为 Magisk 在不覆盖实际系统文件的情况下在 RAM 中进行更改，这意味着 build.prop 编辑和更多操作都是可能的。Magisk 模块只是预打包在 flash zip 中的/system 修改，它将其数据安装到数据分区中的 Magisk.img 文件中。

我们已经看到 Magisk 的一些成就非常惊人，我们论坛上最新发布的一个允许你隐藏你的应用程序中启用的模拟位置( [hello Pokémon Go 玩家](https://www.xda-developers.com/xda-pokemon-go-cheats-traffic-increase-in-location-spoofing-threads-as-cheaters-flock-to-our-forums/))，在 DRM 保护的应用程序中截图，并禁用已安装应用程序的签名检查。所有这些都要感谢 XDA 知名开发商[福梅](https://forum.xda-developers.com/member.php?u=1620550)。

更具体地说，这将允许你用应用程序欺骗你的位置，如 FlyGPS 和应用程序将无法告诉，你可以截图应用程序，如网飞，你可以安装修改后的系统应用程序超过预装的。

它的工作原理非常简单，你安装应用程序，它将检测你的设备并获取你的 services.jar。然后它将下载最新的 Magisk 模块模板，修改你的 services.jar 文件的副本以应用更改，然后创建一个 Magisk 模块。这可以在你恢复的时候闪现。

如果你对以上功能有兴趣，那就来看看吧！狂热的 Pokémon Go 玩家可能会喜欢它(或者厌恶它，如果你反对这种事情的话)，但截图特定应用程序的能力可能会很好，即使只是轻松地制作电影或电视节目中美好场景的壁纸。你所需要的就是 Magisk，所以现在就去下面试试吧！

* * *

在我们的论坛上查看这个 Magisk 模块！