# Magisk Canary 增加了对 EMUI 9 上扎根华为/Honor 设备的支持

> 原文：<https://www.xda-developers.com/magisk-canary-root-huawei-honor-devices-emui-9/>

# Magisk Canary 增加了对 EMUI 9 上扎根华为/Honor 设备的支持

Magisk Canary 现在增加了对运行 EMUI 9 的华为和 Honor 设备的支持。现在不建议安装它，但是你可以。

华为采取了强硬的立场，阻止你修改你的智能手机，从 7 月起不再提供 bootloader 解锁代码。虽然不再可能正式解锁你的华为或 Honor 智能手机([尽管如果你住在印度](https://www.xda-developers.com/honor-india-support-service-centers-unlock-bootloader/)可能会解锁，但你*可以*通过 [FunkyHuawei](https://www.xda-developers.com/huawei-honor-unlock-bootloader-fee/) 非正式解锁。这会让你付出代价，但它确实能让你扎根于你的智能手机，并完全控制它。只有一个问题:EMUI 9 通过修改内核的 ramdisk 来防止根用户访问，即使你的引导程序没有锁定。XDA 公认的开发者和公认的贡献者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 已经找到了解决这个问题的方法，Magisk 现在在最新的金丝雀版本中使用 EMUI 9。

给你一个警告:使用金丝雀版本你会受到其他错误的影响。除非你确切地知道你在做什么，否则使用它并不是一个好主意。如果你愿意接受这些风险，你可以越过[前往论坛主题](https://forum.xda-developers.com/apps/magisk/dev-magisk-canary-channel-bleeding-edge-t3839337)下载最新版本。对于大多数用户，我们建议等待下一个稳定版本。

在 EMUI 9 上获得 root 访问权限被证明是困难的，最终的解决方案意味着您不能再在设备上安装自定义恢复。当启动智能手机时，要获得 root 权限，你需要按住调高音量按钮。这将启动自定义恢复，Magisk 可以在此运行并正常启动您的设备。因此，在 EMUI 9 上，Magisk 现在被安装到 recovery_ramdisk 分区，这是 TWRP 通常会去的地方。您可以查看最新 Magisk Canary 版本的变更日志和下面的最新 Magisk 管理器。

### Magisk 金丝雀 18003 变更日志

*   支持 EMUI 9.0:使用 Magisk 管理器修补“recovery_ramdisk.img ”,并使用“fast boot flash recovery _ ramdisk<patched image="">”进行安装。为了使用 Magisk 进行引导，您必须始终重新引导以进行恢复(引导时按下 volume up)。</patched>
*   简化的“su_info”缓存系统
*   删除系统 C++ STL 的要求，使用内部“新建”和“删除”实现

### Magisk Manager 170 Changelog

*   支持 EMUI 9.0
*   如果检测到 EMUI 9.0，“重新启动”按钮将重新启动以进行恢复