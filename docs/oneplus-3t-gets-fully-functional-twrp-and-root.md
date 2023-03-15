# OnePlus 3T 获得全功能 TWRP 和 Root

> 原文：<https://www.xda-developers.com/oneplus-3t-gets-fully-functional-twrp-and-root/>

# OnePlus 3T 获得全功能 TWRP 和 Root

OnePlus 3T 现在拥有自己的 TWRP 恢复功能，以及一种简单的 root 方法。请继续阅读，了解更多最新消息！

随着第一批 OnePlus 3T 开始发货，用户拿到了新设备，他们现在可以直接进入定制 rom 的世界，而不必再考虑复杂的程序或其他困难。

多亏了 XDA 公认的开发者 jcadduono 的努力，OnePlus 3T 的用户可以刷新 TWRP 3.0.2 的完整工作和稳定版本。如上所述，恢复可以做所有的任务，尽管它是这款手机的第一个版本发布。

快速恢复很容易，包括 Nexus 用户非常熟悉的步骤。您可以在手机的开发选项中启用 oem 解锁，然后通过电脑上的快速启动，使用“快速启动 OEM 解锁”命令来解锁您的启动加载程序。然后使用“fastboot flash recovery recovery . img”命令通过 fast boot 刷新恢复...就是这样。要获得 root，只需启动恢复并刷新必要的 root 包(如 [SuperSU](https://download.chainfire.eu/1013/SuperSU/SR4-SuperSU-v2.78-SR4-20161115184928.zip) )。

由于此次恢复是针对 OnePlus 3T 的，所以暗示(甚至明确提到，以防万一)它与常规的 [OnePlus 3](http://forum.xda-developers.com/oneplus-3) 不兼容。另一点需要注意的是，OnePlus 3T 的股票启动映像已启用 dm-verity，因此如果你在 TWRP 上滑动以启用系统修改，而不打算通过 SuperSU 进行根操作，你将无法启动回系统。你需要按照线程中提到的步骤回到你的系统，无论是根还是其他。您可以向右滑动，只闪烁 SuperSU，或者向右滑动，闪烁 dm-verity disabler zip，以便能够引导回系统。

如需下载链接、源代码和进一步的详细说明，请前往[论坛链接](http://forum.xda-developers.com/oneplus-3t/development/recovery-twrp-oneplus-3t-t3507308)！

**您收到 OnePlus 3T 了吗？你试过上面提到的 TWRP 并获得根吗？请在下面的评论中告诉我们！**