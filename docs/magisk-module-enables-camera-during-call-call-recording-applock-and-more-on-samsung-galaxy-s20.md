# Magisk 模块支持 Galaxy S20 上的通话记录、应用锁定等功能

> 原文：<https://www.xda-developers.com/magisk-module-enables-camera-during-call-call-recording-applock-and-more-on-samsung-galaxy-s20/>

# Magisk 模块可以在三星 Galaxy S20 上进行通话、通话录音、应用锁定等操作

新的 Magisk 模块可用于在 Galaxy S20 上支持通话期间的摄像头、通话录音和其他特定于地区的功能。请继续阅读！

OEM Android 皮肤，如小米的 MIUI 或一加的 OxygenOS，通常具有[多个区域变体](https://www.xda-developers.com/oneplus-announces-india-specific-features-oxygenos/)。虽然一些地区专属服务可以从服务器端控制，但一些制造商更喜欢在固件中提供一整套功能，通过普通用户看不到的隐藏参数来控制对地区功能的选择性访问。在三星的例子中，他们通过他们的消费者软件定制文件( [CSC](https://forum.xda-developers.com/wiki/Csc) )来定义这些特性。摆弄 CSC 不是每个人都喜欢的，所以 XDA 高级成员[奥路菲](https://forum.xda-developers.com/member.php?u=813614)为三星 Galaxy S20 系列开发了一个有趣的 Magisk 模块，名为*Decoded _ CSC _ Features _ Files*，可以解锁一系列在某些地区不可用的功能。

**三星 Galaxy XDA 论坛:[S20](https://forum.xda-developers.com/galaxy-s20)| |[S20+](https://forum.xda-developers.com/galaxy-s20-plus)| |[S20 超](https://forum.xda-developers.com/galaxy-s20-ultra)**

**从 Amazon.in 购买—三星 Galaxy:[S20](https://www.amazon.in/Samsung-Galaxy-Storage-Additional-Exchange/dp/B08445DF23/?tag=xdaportalin-21)| |[S20+](https://www.amazon.in/Samsung-Galaxy-Storage-Additional-Exchange/dp/B084451YSS/?tag=xdaportalin-21)| |[S20 超](https://www.amazon.in/Samsung-Galaxy-Storage-Additional-Exchange/dp/B08444S68Q/?tag=xdaportalin-21)**

正如你所料，这个 mod 需要一个解锁的引导程序，因此它只能安装在三星 Galaxy S20 的 Exynos 驱动的变种上。最新的金丝雀版本的 Magisk 能够修补这款手机的启动映像，其程序与 T2 Galaxy S10 root guide T3 非常相似。一旦 Magisk 启动并准备就绪，闪烁*解码 _ CSC _ 功能 _ 文件*模块可以解锁以下功能:

*   禁用快门声音菜单
*   启用 AppLock 保护菜单
*   启用实时网络速度
*   通话时启用摄像头
*   启用通话录音(仅限常规语音通话)
*   快速面板上的数据使用视图
*   阻止呼叫号码菜单
*   启用 eSIM 支持

这个模块基于 XDA 资深成员 [m8980](https://forum.xda-developers.com/member.php?u=1614889) 的[工作](https://forum.xda-developers.com/showpost.php?p=82222203)，但是奥路菲在此基础上进一步扩展，增加了许多其他功能，例如[对 eSIM](https://forum.xda-developers.com/showpost.php?p=82298927) 的支持。该软件包与 Galaxy S20 系列的最新官方固件( *G98xFXXU1ATCT* )兼容，应该可以在未来的软件版本中工作，几乎不需要修改。安装此模块后，操作员软件版本可能会更改为“G981B”，但这是一个无害的副作用，可以忽略。

**[下载解码 _CSC_Features_Files Magisk 模块— XDA 线程](https://forum.xda-developers.com/galaxy-s20/development/magisk-module-decodedcscfeaturesfiles-t4082445)**

此帖子包含代销商链接，如果你通过它们购买，XDA 将获得佣金。