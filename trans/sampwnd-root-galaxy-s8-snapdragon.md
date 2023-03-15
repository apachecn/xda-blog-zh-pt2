# SamPWND 为骁龙银河 S8/S8+带来根

> 原文：<https://www.xda-developers.com/sampwnd-root-galaxy-s8-snapdragon/>

几天前，有消息称 [root 状态终于在三星 Galaxy S8 和 S8+的骁龙版本上实现了](https://www.xda-developers.com/galaxy-s8-snapdragon-root-system-rw/)。发布的新闻是几个月工作的进展报告，最终获得了三星旗舰产品美国版本的 root 访问权限。与 Exynos 的同行不同，他们可以解锁设备的引导加载程序，骁龙的 Galaxy S8 和 Galaxy S8+设备不能这样做，这使他们没有任何真正的选择，只能等待社区发挥其魔力。

有了[samp wnd](https://forum.xda-developers.com/galaxy-s8+/development/root-g955u-g955u1-snapdragon-sampwnd-t3658911),**G995U/g955u 1 三星 Galaxy S8+【骁龙变种】**的用户终于可以在他们的设备上享受 root 功能了。目前发布的作品**仅限于 Galaxy S8+** ，但我们认为我们应该很快就会看到 S8 的文件进入论坛。

SamPWND 背后的团队提到，他们实际上是在 ODIN 中更新一个修改过的 4 文件固件包，利用一些带有 SU 二进制文件和一个许可内核的二进制文件，并运行一些 ADB 命令。要获得对 root 更广泛的用例支持，还需要几个步骤，包括通过 FlashFire 刷新一个股票 system.img 和一个 root 脚本。如果您对进一步的本质细节感兴趣，开发人员会邀请感兴趣的团体来拆开分发的文件以了解更多信息。

虽然这种根方法有一些缺点。首先，设备的**引导加载器**状态保持不变，即**保持锁定**。这完全挫败了依赖于对 boot.img 的更改的修改，包括但不限于 Magisk、SUHide 和 systemless root。你也将**使安全网**失效，所以你也将失去几个需要安全网检查的应用和服务。三星还在设备上增加了一些限制，以劝阻用户尝试这种黑客行为，例如**在许可内核上限制电池充电至 80%**。所使用的工程固件还包含其他工具和二进制文件，如果您不按照步骤进行操作，它们可能会损害您的设备，因此了解您尝试的严重性是绝对必要的。我们也无法找到任何关于恢复到完全库存设备的说明，但这可能是我们的疏忽(但为了所有读者的利益，还是值得一提)。

如果这个根方法有这么多限制，为什么开发人员一开始就发布根方法呢？这个问题的答案在于社区的力量能够实现个人和个人小团队无法独自实现的目标。这些方法中面临的问题会吸引其他开发人员为了实现设备的稳定和可分发根的集体利益而尝试修复它们。当前格式的这个特定的根解决方案不是最终目标，而是朝着最终目标的又一步。

要获得三星 Galaxy S8+ 的**骁龙变种的完整和详细说明，请前往 [SamPWND 论坛主题](https://forum.xda-developers.com/galaxy-s8+/development/root-g955u-g955u1-snapdragon-sampwnd-t3658911)。我们建议在尝试该程序之前，通读说明书和第一篇文章。**

**你对三星 Galaxy S8+的 SamPWND root 有什么想法？请在下面的评论中告诉我们！**

[**在我们的三星 Galaxy S8+论坛中查看 SamPWND！**](https://forum.xda-developers.com/galaxy-s8+/development/root-g955u-g955u1-snapdragon-sampwnd-t3658911)