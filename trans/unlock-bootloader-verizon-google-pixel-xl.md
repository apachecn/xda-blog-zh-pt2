# 已经为威瑞森谷歌 Pixel/Pixel XL 找到了引导加载器解锁方法

> 原文：<https://www.xda-developers.com/unlock-bootloader-verizon-google-pixel-xl/>

# 已经为威瑞森谷歌 Pixel/Pixel XL 找到了引导加载器解锁方法

威瑞森 Google Pixel 和威瑞森 Google Pixel XL 的引导加载程序解锁方法已被发现。这使得威瑞森 Pixel 用户可以刷新 TWRP，在手机上安装 Magisk，安装 Xposed 框架，以及安装定制的 rom。

在美国，威瑞森无线是第一代和第二代谷歌 Pixel 设备的独家运营商。众所周知，威瑞森对修改设备的用户不友好，因此从运营商处购买的任何设备都无法解锁其引导加载程序。解锁威瑞森谷歌 Pixel 设备的引导程序需要利用[漏洞](https://www.xda-developers.com/verizon-pixelpixel-xl-bootloader-unlock-has-been-released/)或[巧妙的绕过](https://www.xda-developers.com/verizon-google-pixel-2-bootloader-unlock/)，看起来 XDA 成员 [LeoTheRomRasta](https://forum.xda-developers.com/member.php?u=3902253) 和 [Qu3ntin0](https://forum.xda-developers.com/member.php?u=6807580) 在我们的论坛上发现了另一个巧妙的绕过方法。到目前为止，成员们报告说，它在威瑞森出售的第一代谷歌 Pixel 和 Pixel XL 上工作。

## 如何解锁威瑞森谷歌 Pixel/Pixel XL 的 bootloader

下面的说明归功于 XDA 成员 [Qu3ntin0](https://forum.xda-developers.com/member.php?u=6807580) ，他已经在这里发布[。XDA 资深成员](https://forum.xda-developers.com/showpost.php?p=76633532&postcount=138)[布尔杜里](https://forum.xda-developers.com/member.php?u=5642246) [重写了说明](https://forum.xda-developers.com/pixel-xl/how-to/how-to-unlock-bootloader-verizon-pixel-t3796030)并在今天早些时候向我们透露了这个方法，所以我们也感谢他。

**警告:解锁引导程序不仅会清除你**、**手机上的任何应用数据，还会清除/data/media 中存储的所有数据。如果您尚未备份任何文档、图像、音乐等，请进行备份。**

1.  移除谷歌账户和任何种类的锁屏(指纹、PIN、图案等。)从您的设备。
2.  从设备中弹出 sim 卡。
3.  重置您的设备。在设置向导中，跳过一切，**不要连接 WiFi，不要添加指纹或任何种类的锁屏。**
4.  转到开发者选项并启用 USB 调试。
5.  将您的手机连接到 PC。
6.  打开 adb 目录下的 CMD，输入:`adb shell pm uninstall --user 0 com.android.phone`
7.  重新启动您的设备。
8.  连接 WiFi，打开 Chrome，进入 google.com(或任何网站)。
9.  转到开发者选项并启用 OEM 解锁。
10.  重新启动引导程序并通过 CMD 运行:`fastboot oem unlock`或`fastboot flashing unlock`
11.  利润

如果我们可以猜测这里发生了什么，它看起来像是手机应用程序(com.android.phone)在第一次启动时检查设备是否不应该访问 OEM 解锁。然而，如果您完全禁用互联网接入，移除 SIM 卡，并禁用手机应用程序，那么它永远不会有机会执行检查，因此您可以解锁引导加载程序。

享受这种方法吧！