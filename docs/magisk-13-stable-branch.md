# Magisk 版本 13 进入稳定分支，新功能和兼容性

> 原文：<https://www.xda-developers.com/magisk-13-stable-branch/>

经过一个多月的测试版测试，XDA 承认贡献者和开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 的 Magisk v13 正在向稳定分支迈进。稳定的 v13 版本将带来 Android O 兼容性、统一的二进制文件以及一系列错误修复和对所有先前测试版的改进。

正如 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 在[的论坛帖子](https://forum.xda-developers.com/showpost.php?p=72976777&postcount=2698)中提到的，Magisk 的新稳定版本将在几小时后上线。因此，Magisk 的 beta 线程现已关闭，因为不再需要它。该线程将在下一个测试版到来时开放，但在此之前，稳定版的[线程将作为主线程继续运行。](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)

最新版本的官方和完整的变更日志还没有发布，但是我们可以跟踪以前测试版中发生的变化。主要亮点是与最新版本的 Android O 兼容，以及将 MagiskSU、magiskhide、resetprop 和 magiskpolicy 合并为一个统一的二进制文件。现在已经支持 addon.d survival，默认情况下 magiskhide 也应该是启用的。Magisk v13 还需要最新的 Magisk Manager 应用程序，该应用程序支持新的 Magisk 统一二进制文件，并为 SafetyNet 增加了基本的完整性检查。

由于谷歌 Play 商店不再提供 Magisk Manager，你需要前往[论坛主题](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)获取最新版本。或者，你也可以[通过我们自己的 XDA 实验室](https://labs.xda-developers.com/store/app/com.topjohnwu.magisk)安装 MagiskManager。我们会尽快在这里附上完整的更新日志，所以请继续关注论坛！

* * *

### **更新:**

稳定分支获得版本 13.1 作为它的最新版本。由于 v12.0 和 v13.x+之间的巨大差异，很多东西不再向后兼容。停留在旧版本上会导致您错过大量的修复和改进。

这次更新还带来了新的 Magisk 模块模板 v4，这反过来又带来了正确的 Android O 处理和许多闪烁的修复。flash 脚本中的命令现在大大减少了，只剩下基本命令和函数调用。该脚本现在依赖于正确的 Magisk v13.1 安装，因为 busybox 不再捆绑。由于这一变化以及更新帖子、**中提到的其他变化[，Magisk 模块在没有/data access](https://forum.xda-developers.com/showpost.php?p=72979751&postcount=23)** 的自定义恢复中不再可刷新，因此您将需要一个带有/data access 的正确配置的恢复，或者必须在 Magisk Manager 本身中刷新。管理器的未来版本将过滤掉模板版本低于 v4 的 repo 上的模块，因此要求开发人员尽快更新他们的模块！

以下是 Magisk v13.1 的官方变更日志:

*   [常规]将 MagiskSU、magiskhide、resetprop、magiskpolicy 合并为一个二进制文件
*   [常规]添加 Android O 支持(在 DP3 上测试)
*   【通用】从系统中动态链接 libselinux.so、libsqlite.so 来大大减小二进制文件的大小
*   [常规]删除捆绑的 busybox，因为它会引起很多问题
*   [常规]解锁所有块设备以获得读写支持，而不仅仅是 emmc(只是认为并非所有设备都使用 emmc lol)
*   [脚本]通过 flash 脚本中的 magisk 二进制文件运行所有 ext4 映像操作
*   [脚本]更新了脚本以使用 magisk 本地命令来提高兼容性
*   [脚本]添加 addon.d 生存支持
*   【脚本】介绍 util_functions.sh，用作各种安装的全局 shell 脚本函数源
*   [MagiskBoot]将引导修补程序逻辑移动到 MagiskBoot 二进制文件中
*   [MagiskSU]不会为每个请求派生新进程，而是添加新线程
*   [MagiskSU]增加了多用户支持
*   [MagiskSU]引入新的超时队列机制，防止编写不良的 SU 应用程序影响性能
*   [MagiskSU]多个设置从属性检测移到数据库
*   [MagiskSU]添加名称空间模式选项支持
*   [MagiskSU]添加主安装选项
*   【resetprop】更新到最新 AOSP 上游，支持道具从 5.0 到 Android O
*   [resetprop]重命名了所有函数，以防止从外部 libc 调用函数
*   [magiskpolicy]从官方 SELinux repo 更新了 libsepol
*   【magiskpolicy】增加了 xperm 补丁支持(为了让 Android O 正常工作)
*   [magiskpolicy]更新了 Android O 和 Liveboot 支持的规则
*   [magis hide]删除伪许可模式，直接隐藏许可状态
*   [magis hide]删除不可靠的列表文件监视器，更改为守护程序请求模式
*   [magis hide]magis hide 现在默认启用
*   [magis hide]更新卸载策略，在 SafetyNet 中传递 CTS！
*   [magis hide]添加更多隐藏道具
*   [MagiskHide]删除后台 MagiskHide 守护进程，生成用于卸载目的的短生命周期进程
*   抛弃了基于 shell 脚本的挂载，使用合适的 C 程序来解析和挂载文件。速度显著提高

以下是 Magisk 管理器的官方变更日志:

*   v5.0.4
*   v5.0.3
    *   修正了安卓系统启动时的错误
    *   适应 Android O 广播限制:在 Android O 上禁用更新时重新验证应用程序
*   v5.0.2
    *   重写 zip 签名部分，从回购下载的 zip 将被正确签名和调整为自定义恢复
*   v5.0.1
    *   添加命名空间模式选项
    *   修正了经理 OTA 系统的一个错误
*   v5.0.0
    *   支持新的 Magisk 统一二进制文件
    *   正确处理应用程序安装/卸载根管理问题
    *   添加多用户模式支持
    *   添加应用程序升级重新认证功能
    *   为安全网添加基本的完整性检查
    *   将安装片段和状态片段合并到 Magisk 片段中
    *   修复主题切换故障
    *   更新翻译

你安装了最新版本了吗？请在下面的评论中告诉我们你的经历！

* * *

[**在我们的社区应用论坛中查看 Magisk！**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445) [**通过 XDA 实验室下载 Magisk Manager！**](https://labs.xda-developers.com/store/app/com.topjohnwu.magisk)