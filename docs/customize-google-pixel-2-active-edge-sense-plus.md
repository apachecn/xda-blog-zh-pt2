# 定制谷歌 Pixel 2 的 Active Edge，用 Edge Sense Plus 做任何动作[XDA 聚光灯]

> 原文：<https://www.xda-developers.com/customize-google-pixel-2-active-edge-sense-plus/>

谷歌和 HTC 一直在 Pixel 2 上合作，这不是什么秘密。这两家公司最近[达成了一项大规模交易](https://www.xda-developers.com/google-completes-acquisition-htc-engineers-google-pixel-2/),毕竟，这项交易见证了核心 HTC 工程师向谷歌的转移。鉴于谷歌对 Pixel 智能手机的设计和开发控制得如此严格，有时很难看出谷歌的合作伙伴 OEM 可能在哪些方面产生了影响。Pixel 2 的 Active Edge 功能就不是这样了，它显然受到了 HTC 的 Edge Sense 的影响。谷歌和 HTC 的实现之间的一个主要区别是 HTC 的是[更加可定制的](https://www.xda-developers.com/new-edge-sense-beta-u11-customization/)。然而现在，由于 Edge Sense Plus，Pixel 2 的主动边缘定制可能性是无限的。

Edge Sense Plus 是 XDA 公认的开发者[j to 4n](https://forum.xda-developers.com/member.php?u=4905624)的一款应用，最初是为配备 HTC 的 Edge Sense (因此得名)的[设备开发的，最近](https://www.xda-developers.com/edge-sense-expands-htc-u11-functionality/)[对其进行了更新](https://www.xda-developers.com/edge-sense-plus-updated-support-google-pixel-2-active-edge/)，以支持谷歌 Pixel 2 和 Pixel 2 XL。该应用程序不仅允许您对 Pixel 2 的单次挤压执行**自定义操作**，而且它还开放了对设备的**双次或长时间挤压**执行操作的能力。

正如你在上面显示应用程序配置设置的截图中看到的，你可以在你的设备上设置单次、长时间和两次挤压的动作。这些操作也可以根据设备的物理方向进行定制，或者当手机在口袋中时完全禁用(以防你喜欢更高的灵敏度，并且在从口袋中取出手机时意外挤压手机。)

这款应用充满了各种功能，尽管双重挤压和方向检测需要购买该应用的高级版本，开发者让你选择你想花多少钱来解锁高级版本(1.49€，2.49€，3.99€和 5.49€将完全解锁该应用)。考虑到它所能提供的东西，这要求并不多。为了让它更有吸引力，开发者今天宣布，他已经将 **Tasker integration** 添加到他的应用程序中，这意味着你可以通过挤压你的 Pixel 2 来做**任何你想做的事情**。

开发者将在本文的评论部分给出 15 个推广代码，所以请务必留下评论，链接到你的 XDA 个人资料或提及你的 XDA 用户名，这样他就可以给你发送一个带有推广代码的 PM！

## 边缘检测和 Tasker 集成

对于那些没有听说过 Tasker 的人来说，这是谷歌 Play 商店最受欢迎的自动化应用。它由“概要文件”和“任务”组成，它们可以集中到一个“项目”中。配置文件由一个或多个条件(在 Tasker 中称为“上下文”)组成，当满足这些条件时，将启动一个任务，这是一组用户定义的操作。例如，如果您使用“Wi-Fi 连接”上下文创建了一个配置文件，当连接到您的家庭 SSID 时会触发该配置文件，您可以启动一个任务来更改您的默认壁纸。

*使用 Tasker 获得 Edge Sense Plus 的步骤。从左到右。*

Tasker 集成非常酷，尽管学习曲线可能非常陡峭。这些年来，我们制作了许多与任务相关的教程，我们的[任务提示&技巧](https://forum.xda-developers.com/u/tasker-tips-tricks)论坛仍然很强大。如果你进入 Tasker，你将会在你的设备上开启你从未想过的定制。如果没有，不要担心，因为 Edge Sense Plus 还有更多 **lot** 可以提供。

* * *

## 边缘感知加动作

以下是应用程序中可用操作的列表，为了方便起见，我按类别进行了分类:

### 航行

*   背部
*   主页
*   最近的应用
*   分画面银幕
*   展开/折叠状态栏
*   展开状态栏
*   以前的应用程序
*   向上滚动
*   向下滚动

### 连通性

*   蓝牙
*   无线保真
*   国家足球联盟
*   全球（卫星）定位系统
*   同步切换
*   同步所有帐户

*   播放/暂停媒体播放器
*   上一首曲目
*   下一首曲目

### 设置

*   自动旋转
*   聪明
*   请勿打扰
*   震动
*   保持清醒

### 快捷指令

*   应用快捷方式
*   补充报道
*   手势面板
*   HTC Edge 启动器
*   启动应用程序
*   谷歌助手
*   手电筒

### 行动

*   每个应用程序的操作
*   屏幕上显示程序运行的图片
*   清除所有通知
*   接受呼叫
*   结束通话
*   全屏模式
*   外壳命令
*   屏幕开/关
*   Tasker 集成(**新**)

* * *

## 边缘感知增强 vs 按钮映射器

你们中的一些人可能听说过由 XDA 知名开发者开发的按钮映射器。过去我们已经在门户网站上[报道过它](https://www.xda-developers.com/xda-spotlight-button-mapper-an-app-to-remap-your-phones-hardware-buttons/)。你可能已经看过我们之前的一篇文章，讲述了[如何使用按钮映射器在谷歌 Pixel 2 上重新映射活动边缘](https://www.xda-developers.com/remap-active-edge-squeeze-google-pixel-2/)。那么，按钮映射器不需要 root 访问就能工作，这有什么区别呢？Edge Sense Plus 需要 root 访问权限。但这并不代表 Edge Sense Plus 就低人一等。事实上，恰恰相反，原因如下。

Active Edge 是[硬编码的](https://www.xda-developers.com/google-pixel-2-squeeze-hardcoded-assistant-remapping-difficult/)，只允许在手机[不处于沉浸式模式、不在谷歌相机应用中或者正在打电话的时候](https://www.xda-developers.com/google-pixel-2-active-edge-squeeze-immersive-m/)挤压来启动谷歌助手、解除警报或者静音来电。由于这些限制，按钮映射器必须使用变通方法来重新映射挤压功能。它实现了一项服务，该服务读取您设备上的系统日志，同时过滤称为“ElmyraService”(Active Edge 的代号)的东西。一旦找到这一行，按钮映射器就会执行您选择的操作。正如您所料，这可能会对设备性能造成影响，许多用户都这样反映过。

Edge Sense Plus **不会导致任何性能问题**，因为这个应用程序要求你安装一个 Magisk 模块，用一个经过修改的模块来替换你手机上的股票系统 UI APK，该模块可以拦截 ElmyraService，将所有事件发送到 Edge Sense Plus。本质上，股票活跃边缘功能是*实际上*重新映射，而非根按钮映射器解决方案只是给了一个这样做的幌子。显然，代价是 **Edge Sense Plus 需要 root 访问权限**，这意味着可能会有更少的用户愿意安装它。

* * *

## 如何在谷歌 Pixel 2 和 Pixel 2 XL 上安装 Edge Sense Plus

既然你已经知道了关于重新映射 Pixel 2 的 Active Edge 功能的所有信息，为什么不试一试呢？你需要做的第一件事是从 Play Store 安装应用程序。它可以免费安装，尽管如前所述，双挤压和运动传感器功能需要在应用内购买。此外，如果你想要 Tasker 集成，你必须安装 Tasker，它只提供 7 天免费试用(它是那些完全值得它的价格的应用之一)。

接下来，你需要 **root** 你的设备。我们有一个关于如何做的指南[这里](https://www.xda-developers.com/how-to-unlock-bootloader-and-root-the-google-pixel-2-and-pixel-2-xl/)或者你可以使用自动工具链接[这里](https://www.xda-developers.com/bootloader-unlock-root-pixel-2-skipsoft-toolkit/)。最后，你需要为你的设备安装 **Magisk 模块**。你**必须**为你的设备安装下面链接的合适的 Magisk 模块，否则你会在引导循环中结束！

[**下载谷歌 Pixel 2**](https://forum.xda-developers.com/showpost.php?p=75126124&postcount=3) 的 Edge Sense Plus Magisk 模块

[**下载谷歌 Pixel 2 XL 的 Edge Sense Plus Magisk 模块**](https://forum.xda-developers.com/showpost.php?p=75126467&postcount=3)

一旦你安装了 Magisk 模块并重启了你的手机，你应该可以打开应用程序并开始根据你的需要定制 Active Edge。尽情享受吧！

* * *

*注意:本文不以任何方式得到 Edge Sense Plus 开发者的赞助。开发者是我们论坛上的活跃贡献者，出于礼貌，我们通常会涵盖应用程序、修改或活跃成员所做的任何我们认为我们的读者可能感兴趣的事情。如果你在我们的论坛上分享了一些你认为值得在门户上大声喊出来的东西，[给我们发一条提示](https://www.xda-developers.com/tip-us/)。*