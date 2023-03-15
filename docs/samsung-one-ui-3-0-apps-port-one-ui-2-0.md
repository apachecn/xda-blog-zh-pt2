# 一个 UI 3.0 应用程序移植到运行一个 UI 2.0 的三星 Galaxy 设备

> 原文：<https://www.xda-developers.com/samsung-one-ui-3-0-apps-port-one-ui-2-0/>

# 在运行 One UI 2.0 的 Galaxy 设备上安装三星 One UI 3.0 应用程序

现在，您可以在任何运行 One UI 2.0 的三星 Galaxy 设备上运行 One UI 3.0 测试版固件中的更新股票应用程序。继续阅读，了解更多信息！

三星的 One UI 很大程度上被认为是用户友好的 OEM 皮肤，尤其是考虑到它的前辈，即 TouchWiz 和三星 Experience 之后。这种定制界面的最新版本——One UI 3.0(T1)——基于 Android 11，目前[在 Galaxy S20 系列](https://www.xda-developers.com/samsung-announces-android-11-one-ui-3-public-beta-galaxy-s20/)上提供公测版。不过，那些没有 Galaxy S20 但想体验三星最新软件的人很幸运，因为测试版固件中的一系列股票应用程序已经成功移植到其他运行一个 UI 2.0/2.1/2.5 的 Galaxy 设备上。

由 XDA 知名开发商 [AlexisXDA](https://forum.xda-developers.com/member.php?u=6114446) 发布，该端口可作为一组两个可恢复的闪存 ZIP 文件使用。第一个是删除目标应用程序的现有版本所必需的，而第二个是将移植的应用程序推到/system 分区。下面你可以找到软件包中包含的移植股票应用程序的完整列表:

*   时钟
*   信息发送
*   数字福利
*   键盘
*   联系人
*   走廊
*   新 Bixby 例程
*   新的三星通话设置
*   链接共享
*   探测器
*   快速板
*   实时分享
*   三星浏览器

要安装修改后的应用程序，你需要解锁你的 Galaxy 智能手机/平板电脑的引导加载程序，并用像 TWRP 这样的定制恢复来替换股票恢复映像。请记住，仅解锁引导程序就足以**触发 KNOX** ，因此**将永远无法访问 Samsung Pay** 和安全文件夹等安全功能。如果这没有困扰到你，请点击下面的 XDA 主题链接，按照第一篇文章中的说明，让应用程序在你的设备上运行起来。

**[One UI 3.0 移植应用— XDA 下载讨论线程](https://forum.xda-developers.com/galaxy-s9-plus/themes/oneui3-0-ported-apps-v0-5-t4174153)**

请务必注意，上述步骤适用于全局解锁变体。大多数美国运营商都不允许解锁引导加载程序，因此无法在运营商品牌的三星 Galaxy 设备上刷新自定义恢复。限制[可以绕过](https://www.xda-developers.com/samsung-galaxy-note-20-ultra-root-us-unlocked-snapdragon-865/)，但这不是每个人都喜欢的。