# 电池修复:Google Play 服务唤醒锁- XDA 论坛

> 原文：<https://www.xda-developers.com/psa-google-play-services-wakelock-affects-many-5-x-roms/>

唤醒锁是电池意识的祸根，这个唤醒锁错误已经困扰 Android ROMs 一段时间了。是的，这个问题既不是新的也不是独特的，除非谷歌站出来，否则它不会得到永久解决，但最近推出的 CyanogenMod 12 和 CyanogenOS(以及其他产品)引发了人们对 Google Play Services 7 . x SystemUpdateService wake lock bug 的新一轮兴趣。好消息是，CM12 昨天看到了一个修复程序，CyanogenOS 应该会在下周得到修补。坏事吗？每一个其他的 ROM 制造商仍然需要考虑最新的问题，根本原因是一如既往的错误。这不是我们最后一次进行这样的对话，但现在让我们讨论这个问题，指出补丁&的进度报告，并让我们的电池恢复战斗状态。

# Bug？什么虫子？

很容易看到手机电量下降的速度比它应该下降的速度快，但是哪些手机/rom 受到了影响，根本原因是什么？先说后一个问题。Google Play Services 包含一个名为 SystemUpdateService 的 OTA 更新检查器，它的工作是寻找并响应空中请求。在定制 ROM 上，更新来自 ROM 制造商，而不是谷歌或运营商，所以这项服务除了碍事什么也不做。例如，不断应对无法安装的更新是最大限度利用数据计划的快速方法，这是另一个常见问题。类似地，更新检查唤醒电话并耗尽电池。解决这两个问题的简单方法是让 ROM 制造商禁用这项服务，然后就此打住，这正是大多数人(包括 Android 5.x)所做的事情。不幸的是，Lollipop 给这项工作带来了麻烦。

从 Android 5.0 和 Gooogle Play Services 7.x 开始，更新机制包括唤醒锁检查器。本质上，电话现在被唤醒以执行检查，未能联系(禁用的)系统更新服务，并继续无限期地等待永远不会到达的响应。这显然是一个问题，并导致电池电量骤降的截图和实实在在的“清醒”线充斥着每个论坛。回到最初的问题，这种病毒的全球性意味着它的传播范围也同样广泛。*任何运行*任何* ROM 的*设备，或者没有限制系统更新服务，或者在没有棒棒糖特定补丁的棒棒糖上将会看到这些唤醒锁。但是不要担心，对于最近一轮的麻烦，解决方案已经就位。

# 狐狸

有几种方法可以解决这个恼人的问题，从 Play 服务的定制 Play 版本到更具弹性的官方 rom 补丁。Cyanogen 解决方案优雅地重新启用了 SystemUpdateService，但是限制了它的接收者。最终结果是，当服务检查更新时，它会立即失败并终止。显然这仍然是不完美的，但这是一个聪明的把戏，有希望很快出现在其他棒棒糖 rom 中。对于您的电池需求，这里是您的补丁选项的完整纲要，从最有效到最无效。

*   这是一个已知的问题。谷歌的解决方案是确保这篇文章永远不需要后续报道的唯一方法。没有关于运动的词。
*   上个月解决的-。更新你的 ROM。
*   **CyanogenMod 12.0** - [昨日折入稳定回购](http://review.cyanogenmod.org/#/c/91579/ "Change 91579 - CyanogenMod Code Review")。更新你的 ROM。
*   **CyanogenMod 12.0 Nightly**-[昨日折入回购](http://review.cyanogenmod.org/#/c/94759/ "94759 - CyanogenMod Code Review")。每晚更新你的。
*   蓝藻 -下周修复？请继续阅读临时解决方案，并查看 Cyanogen 以了解更多细节。
*   如果你在邮件中已经做到了这一步，我同情你和你的电池。知名开发商 [Calkulin](http://forum.xda-developers.com/member.php?u=1188493) 在 OnePlus One 论坛上发布了[的部分修复，但也有一些警告。这个可刷新的文件不是更好的系统级解决方案，而是 Play Services 的一个修改版本，删除了违规代码。就其本质而言，该文件将在下次推送 Play 服务更新时被 Google 覆盖，再次悄无声息地杀死您的设备。每当这种情况发生时，卡尔库林都慷慨地保证更新他的帖子，但这是一项艰巨的任务，需要每个人保持警惕。更麻烦的是，这个文件是特定于型号&操作系统的。当前版本 Google Play Services v7.3.27-438 为 7.3.27 版本，适用于 Android Lollipop (4)、armeabi-v7a 架构(3)、480 DPI displalys (8)。如果这是你，太好了！如果没有，你要自担风险，因为依赖这些服务的应用程序(大多数)可能包含 hickups。要检查你的设备使用的三位数标识符，请在 Android 的“应用程序”设置部分找到“Google Play 服务”，并在版本号中查找最后三位数(例如:版本 7.0.99 (1809214- **430** ))。祝你好运！](http://forum.xda-developers.com/oneplus-one/themes-apps/mod-google-play-services-update-wake-t3078082 "Google Play Services with System Update Wakelock Fix - XDA-Developers Forum")

电池问题很烦人，成本也很高，但至少这是我们熟悉的歌舞。耐心是这里最有效的美德。耐心，和一个反应灵敏的 ROM 开发者。一个反应灵敏的谷歌也不会有什么坏处，但这可能要求太高了。