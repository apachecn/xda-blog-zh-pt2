# 在任何国家启用 Pixel 4 动作感应手势，风险自负

> 原文：<https://www.xda-developers.com/enable-pixel-4-motion-sense-gestures/>

谷歌的 Pixel 4 智能手机是首批搭载谷歌 Soli 雷达的商业产品。Soli 雷达为新款 Pixel 智能手机上的各种运动感应手势提供动力，包括跳过媒体曲目和静音来电、定时器或闹钟的手势。由于 Soli 雷达的工作频率为 60GHz，因此其在 Pixel 4 中的使用需要得到各国电信部门的监管批准。这就是为什么在发布时，只有当你的 Pixel 4 连接到 53 个白名单区域中的 [1 的运营商时，运动感应手势才有效。但是，使用 root 访问权限，您可以绕过这一限制。](https://www.xda-developers.com/google-pixel-4-motion-sense-list-countries-supported-apps/)

事实上，在 Pixel 4 发布之前，我们自己就发现了这种方法，但因为它可以在未经授权的频率上传输无线电波，我们不想鼓励人们在不受支持的国家非法使用它。不过，既然事情已经败露，这种变通方法就无法真正得到控制，主要是因为它太容易做到了。负责处理动作感应手势的应用 OsloFeedback 有一个隐藏的调试标志，可以禁用所有的区域检查。将此调试标志设置为真，无论 SIM 卡连接到哪家运营商，Pixel 4 都将允许您使用手势。

为了设置这个标志，你需要首先[解锁引导程序并用 Magisk](https://www.xda-developers.com/google-pixel-4-root-magisk/) 启动你的手机。然后，你可以运行这里列出的 shell 命令[或者安装这里提到的](https://forum.xda-developers.com/showpost.php?p=80729593&postcount=5)[模块](https://forum.xda-developers.com/pixel-4-xl/themes/success-enable-soli-china-t3994917)。如果你使用前一种方法，我建议你使用 [MagiskHide Props Config](https://forum.xda-developers.com/apps/magisk/module-magiskhide-props-config-t3789228) 来设置道具，这样它就可以跨引导持续存在。如果您选择后者，那么您必须安装 Riru 核心和 EdXposed Magisk 模块，如这里的[所述](https://forum.xda-developers.com/pixel-4-xl/how-to/xposed-discussion-thread-t3992607)。无论哪种方式，你最终都会绕过谷歌对动作感应手势的区域限制。

[**像素 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**像素 4 论坛**](https://forum.xda-developers.com/pixel-4-xl)

在不受支持的国家使用这个应该没有太大的危害，因为它是如此的短距离，但是如果你选择这样做，你仍然在冒险。