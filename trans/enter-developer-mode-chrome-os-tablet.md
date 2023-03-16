# 如何在 Chrome OS 平板电脑上进入开发者模式

> 原文：<https://www.xda-developers.com/enter-developer-mode-chrome-os-tablet/>

# 如何在 Chrome OS 平板电脑上进入开发者模式

你可以像在你的安卓设备上一样摆弄 Chrome OS 系统。可以通过进入开发者模式来实现。换句话说，有一种方法可以“root”你的 Chrome OS 设备。以下是方法。

英特尔冰湖架构出现在 Chromium Gerrit 上

众所周知， [Chrome OS](https://www.xda-developers.com/tag/chrome-os/) 是谷歌最初为笔记本电脑设计的操作系统。它被构建得简单而高效，因此看起来似乎没有太多的定制选项。那实际上不是真的。在 Chrome OS 平板电脑或笔记本电脑上进入开发者模式后，你将拥有与 Android 上 root 用户相同的权限。您将能够修改系统，刷新另一个操作系统，等等。在本教程中，我将向您展示如何进入开发者模式。

请记住，所有的荣誉都属于基思·I·迈尔斯。[他在自己的网站](https://kmyers.me/blog/chromeos/entering-developer-mode-on-the-hp-chromebook-x2-and-other-chrome-os-tablets/)上发布了说明，并允许我们在 XDA 上分享。最初，他为[惠普 Chromebook X2](https://www.xda-developers.com/hp-chromebook-x2-detachable-chrome-os-tablet/) 编写了说明，但他指出，这种方法应该适用于所有未来的 Chrome OS 平板电脑。

## 在 Chrome OS 平板电脑上进入开发者模式

遵循此过程会导致数据丢失。说明还包括禁用操作系统验证，这是 Chrome 操作系统内置的一项安全措施。禁用它*可能会*让你的 Chromebook 易受攻击。已经警告过你了。

事不宜迟，让我们开始吧:

1.  首先，你必须关闭 Chromebook 的电源。
2.  为了舒适地遵循说明，请将平板电脑从键盘基座上拆下(如果您有这种 Chrome OS 设备)。
3.  按住**音量增大+音量减小+电源按钮**约 7 秒钟。
4.  当您在 Type-C 端口上方的充电指示灯上看到白色闪光时，请释放。这将把你带到 Chrome OS 恢复菜单。
5.  按下**音量降低**按钮一次。这会带你到菜单。
6.  按下**调高音量+调低音量**。这将显示禁用操作系统验证的提示。
7.  按下**调高音量**。确保选择了“确认禁用操作系统验证”。
8.  按下**电源按钮**确认。

就是这样。按照说明操作后，您的设备将自行恢复出厂设置。设备现在处于出厂模式。你会看到一个关于操作系统验证和操作系统不安全的警告，就像你在 Android 手机上解锁引导程序时看到的一样。

## 启动时要做什么

每次启动设备时，您都会看到一个带有上述警告的新启动屏幕。有三种方法可以继续引导进入 Chrome 操作系统:

*   在键盘上按下 **Ctrl + D** 。
*   导航到开发者选项并选择“从内部硬盘启动”
*   等待 10 秒钟。

正如你所看到的，你现在也可以从 USB 闪存驱动器或 SD 卡启动。正如我已经说过的，这些说明最初是为惠普 Chromebook X2 公司编写的，但它应该适用于所有未来的 Chrome OS 平板电脑。快乐改装！