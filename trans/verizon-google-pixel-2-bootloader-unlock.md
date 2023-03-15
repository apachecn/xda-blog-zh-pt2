# 多名威瑞森谷歌 Pixel 2 用户报告称他们的 Bootloaders 可以解锁

> 原文：<https://www.xda-developers.com/verizon-google-pixel-2-bootloader-unlock/>

谷歌 Pixel 2/2 XL 是我个人最喜欢的 2017 年智能手机，尽管定制开发场景相当稀疏。普通的像素体验足以让许多死忠的 Android 修改者决定放弃运行定制 ROM 或内核。然而，在我们的论坛上仍然有相当多的用户喜欢解锁他们的引导程序，安装 Magisk，并刷新各种修改。那些仍然走这条路线的用户倾向于避免从运营商那里购买他们的手机，因为运营商的手机往往会被锁定。在威瑞森无线上出售的谷歌 Pixel 2 就是这样，引导程序无法解锁，然而我们论坛上的多个用户今晚报告说，他们已经成功解锁了威瑞森谷歌 Pixel 2 的引导程序。

一个名叫 [D3RP_](https://forum.xda-developers.com/member.php?u=7357565) 的 XDA 成员在我们的 [Pixel 2 论坛](https://forum.xda-developers.com/pixel-2)上发了一个帖子，看看是否有可能解锁该设备的引导程序。去年的威瑞森谷歌 Pixel 和 Pixel XL 由于漏洞而无法解锁[，但最新一代 Pixel 2 智能手机系列没有发现这样的漏洞。然而，似乎根本没有必要利用漏洞。只需在威瑞森谷歌 Pixel 2 上发送一个简单的快速启动命令(对不起 Pixel 2 XL 的用户！)出现，调出菜单解锁引导加载程序。](https://www.xda-developers.com/verizon-pixelpixel-xl-bootloader-unlock-has-been-released/)

以下是在你自己的威瑞森谷歌 Pixel 2 上尝试这个的步骤:

1.  为你的电脑下载最新的亚行&快速启动二进制文件。
2.  转到开发者选项并启用 USB 调试。如果你还没有启用开发者选项，你需要进入设置->系统->关于手机，然后点击“内部版本号”7 次。然后，开发者选项会出现在设置->系统中。
3.  在您的计算机上，打开命令提示符或终端并输入:`adb reboot bootloader`
4.  这将重新启动您的引导加载程序。现在输入:`fastboot flashing lock_critical`
5.  尽管我们从未启用 OEM 解锁，但这应该有望调出引导装载程序解锁屏幕。使用音量键选择“解锁引导程序”选项。
6.  按下电源按钮进行确认。**这将清除您内部存储器上的所有数据。**
7.  一旦完成，你现在可以闪现 TWRP 和 Magisk！

到目前为止，我们已经从 XDA 成员 [D3rp_](https://forum.xda-developers.com/pixel-2/help/maybe-stupid-question-verizon-pixel-2s-t3726294) 、[津哈尔克](https://forum.xda-developers.com/showpost.php?p=74994986&postcount=20)、[恩兹恩](https://forum.xda-developers.com/showpost.php?p=74995992&postcount=35)、[阿布鲁特](https://forum.xda-developers.com/showpost.php?p=74997052&postcount=47)、[莱特宁](https://forum.xda-developers.com/showpost.php?p=74997177&postcount=48)、 [Ips1014](https://forum.xda-developers.com/showpost.php?p=74997735&postcount=59) 、[西班牙人 85](https://forum.xda-developers.com/showpost.php?p=74998189&postcount=67) 、[多登德米斯](https://forum.xda-developers.com/showpost.php?p=74998497&postcount=69)、[马马卡](https://forum.xda-developers.com/showpost.php?p=74998495&postcount=68)和[博霍 11](https://forum.xda-developers.com/showpost.php?p=74998691&postcount=75) 处确认我们不知道为什么会这样，但这在威瑞森模型上肯定是不可能的，所以我们不认为这会持续很久。

不过，有可能这 10 名用户不知何故都拿到了来自威瑞森的 Pixel 2 手机，而这些手机实际上与谷歌出售的普通手机是同一批。这将意味着这是孤立的，只有少数幸运的用户。我们将尝试找出这到底是如何工作的，但如果你拥有一台威瑞森谷歌 Pixel 2，并希望你的引导程序解锁，现在可能是你唯一的机会。试试这个，让我们知道它是否对你有用！

* * *

### 更新#1:用户在哪里购买手机的细节

一名用户在我们的论坛上报告他们成功解锁了他们的威瑞森 Pixel 2 的引导加载程序，他说他们从威瑞森的一家公司商店购买了他们的手机[，并且没有收到 RMA 更换。另一名用户在](https://forum.xda-developers.com/showpost.php?p=74998668&postcount=73) [Reddit](https://www.reddit.com/r/GooglePixel/comments/7ms5ke/verizon_pixel_2_bootloader_unlock/drwctrw/?context=3) 上发帖称，这在他们今天从百思买购买的全新威瑞森 Pixel 2 上有效。这意味着，也许所有的威瑞森像素 2 单位可能是引导加载解锁。