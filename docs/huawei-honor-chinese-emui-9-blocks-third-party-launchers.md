# 中国 EMUI 9 阻止华为和 Honor 设备上的第三方启动器

> 原文：<https://www.xda-developers.com/huawei-honor-chinese-emui-9-blocks-third-party-launchers/>

用户定制是 Android 相对于 iOS 的关键优势之一。虽然大多数人除了添加自定义图标包、壁纸、小工具或启动器之外，不会自定义他们的设备，但其他人会全力以赴地使用自定义字体和系统主题。不幸的是，华为 EMUI 9 软件的最新中文版本似乎阻止了用户将第三方启动器设置为默认。这意味着 Honor 和华为从中国购买的(或重新品牌化为中国软件)运行 EMUI 9 的设备不能轻易切换到 Nova Launcher、Action Launcher、[rootle Pixel Launcher](https://www.xda-developers.com/rootless-pixel-launcher-google-play-store-pixel-bridge/)、 [Niagara Launcher](https://www.xda-developers.com/niagara-launcher-minimalist-notifications/) 等启动器。

运行 EMUI 9.0.0.128 的[荣誉魔法 2](https://forum.xda-developers.com/magic-2) (TNY-AL00)上的【默认 app】设置。尽管安装了 Nova 启动器，但它不能作为默认启动器。

需要明确的是，这个*只影响了*的 EMUI 9 设备的中国版本(其中很少，比如[华为 Mate 20 系列](https://www.xda-developers.com/huawei-mate-20-huawei-mate-20-pro-specs-pricing-availability/)、 [Honor Magic 2](https://www.xda-developers.com/honor-magic-2-honor-watch-magic-honor-flypods-pro-launch/) ，或者任何运行 [EMUI 9 beta](https://www.xda-developers.com/emui-9-beta-android-pie-huawei-honor/) 的进口设备)，而没有影响全球的 EMUI 9 软件。根据我们论坛上[成员的说法，这一限制的原因是**据称是为了打击中国一些第三方零售商**的不正当行为(我们已经看到小米在](https://forum.xda-developers.com/huawei-p20-pro/how-to/emui-9-removes-default-launcher-options-t3853441)[多个](https://www.xda-developers.com/xiaomi-anti-rollback-protection-brick-phone/) [场合](https://www.xda-developers.com/flash-miui-global-locked-bootloader-xiaomi-brick/)处理过这个问题)。据称，华为看到非官方零售商预装了装载广告和恶意软件的假 EMUI 发射器。正如你所想象的，这将会给华为服务中心带来很多麻烦。对高级用户来说不幸的是，华为的解决方案是屏蔽第三方启动器。

据称，用户的强烈反对促使该公司推出了一个更新，以恢复改变默认启动器的能力，但我们无法证实华为的意图。如果我们收到一个 EMUI 9 更新，取消了对我们的荣誉魔术 2 的限制，我们会让你们都知道。在那之前，这里有一个变通办法，让你使用 Nova launcher(或任何其他第三方 Launcher ),代价是能够轻松切换回华为 Launcher，并失去水平的最近应用程序屏幕。您所要做的就是通过发出以下 ADB 命令为当前用户卸载股票启动器([完整说明在此](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)):

`adb shell pm uninstall -k --user 0 com.huawei.android.launcher`

如果你想恢复默认的启动器，你必须手动加载它，然后重新启动。

* * *

本书出版后不久，标题进行了更新，增加了这一变化背后的所谓原因。