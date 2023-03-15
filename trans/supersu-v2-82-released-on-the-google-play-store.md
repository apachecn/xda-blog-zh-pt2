# SuperSU v2.82 在谷歌 Play 商店发布

> 原文：<https://www.xda-developers.com/supersu-v2-82-released-on-the-google-play-store/>

XDA 资深公认开发者 [Chainfire](https://forum.xda-developers.com/member.php?u=631273) 宣布 SuperSU 正在更新到 2.82 版本。最新的应用程序应该已经可以在谷歌 Play 商店上为大多数用户所用，因为该应用程序于上周开始推出。

这是在一些更新导致一些用户出现[个问题之后发生的。Chainfire 和 CCMT 公司发布了一个快速漏洞修复程序，但并不是所有问题都得到解决。SuperSU v2.80 导致一些运行旧版本 Android 的 Xperia 设备出现引导循环。游戏商店 **提供的版本没有修复它。仍然面临这个问题的用户应该更新 Chainfire 服务器上的最新 ZIP 文件，我们在下面链接了这个文件。**](https://www.xda-developers.com/chainfire-recommends-staying-in-supersu-2-79-for-xperia-users/)

除此之外，新版本包含了许多错误修复和改进，大多数变化都集中在 Android Nougat 用户的稳定性上。Android 7.0+对 SELinux 处理进行了重大修改。所需的规则集已经减少，二进制文件现在在它们自己的 *supersu* 上下文中运行和执行命令。

根据 Chainfire 的说法，最新版本的 SuperSU 应该可以在一些装有 Android O 开发者预览版 2 的设备上运行，尽管一些设备(主要是谷歌 Pixel 和 Pixel XL)还不支持。Chainfire 建议为 SR1 或 SR2 版本多等一会儿。

引导映像签名尚未集成，但应该会在即将发布的 SR1 版本中找到它的位置。提醒一下，从 5 月份发布安全更新开始，谷歌最近开始要求所有启动映像在谷歌 Pixel 和 Pixel XL 上签名。如果你打算在你的 Pixel 上安装最新的 SuperSU，你必须在刷新下面链接的 SuperSU zip 之后重启之前**刷新[verified bootsigner zip](https://forum.xda-developers.com/android/software-hacking/signing-boot-images-android-verified-t3600606)**。****

最后，SuperSU 团队决定放弃对 Android 2.1 艾克蕾尔和 2.2 Froyo 的支持。Android 2.3 姜饼现在是最老的支持设备。官方统计数据显示，少量设备运行这些旧版本的 Android，因此考虑到测试每个更新的兼容性可能需要花费大量时间，取消支持是有道理的。

* * *

[**来源:chain fire(Google+)**](https://plus.google.com/+Chainfire/posts/4iCwWhRLtoT)[**获取最新可闪 SuperSU ZIP**](https://download.chainfire.eu/supersu)