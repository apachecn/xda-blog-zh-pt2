# Snapchat 又开始屏蔽 Root 用户了——但是能持续多久呢？

> 原文：<https://www.xda-developers.com/snapchat-is-at-it-again-and-blocks-root-users-but-for-how-long/>

尽管过去存在许多安全问题，Snapchat 仍然是智能手机上最受欢迎的社交媒体服务之一。据[报道](http://venturebeat.com/2015/05/26/snapchat-has-100m-daily-users-65-of-whom-upload-photos/)，它拥有 1 亿活跃用户，其中 65%上传照片。

如果我们以人口作为衡量标准，Snapchat 用户将轻松成为世界上第 13 大国家。

Snapchat 将照片分享给当时多位好友的快捷方式备受用户推崇。然而，你们中的许多人，Snapchat 用户，很快就会面临一个严重的不便，因为 Snapchat 将停止在你们的设备上工作。是的，Snapchat 无法在根设备上运行。

最新的更新带来了新的安全检查。登录后，应用程序现在在系统中寻找超级用户的存在。XDA 资深成员 [MaaarZ](http://forum.xda-developers.com/member.php?u=4024698) 对这个问题做了一个很好的解释，他也是 [Snapprefs](http://forum.xda-developers.com/xposed/modules/app-snapprefs-ultimate-snapchat-utility-t2947254) 的创造者，这是一个暴露的框架模块，增强了有限的 Snapchat 的效用。[据 MaaarZ](http://forum.xda-developers.com/xposed/modules/app-snapprefs-ultimate-snapchat-utility-t2947254/post63928302#post63928302) 报道，Snapchat 现在正在进行几项测试，如果其中至少有一项测试结果是肯定的，那么当在系统中找到超级用户时，一个应用程序就会自我杀死。不用说，目前 XDA 上大多数可用的定制 rom 都包含 root，所以这一变化可能会影响成千上万的人。

从用户的角度来看，安全性应该始终保持在最高级别。然而，阻止根设备上的应用程序是一个非常糟糕的举动。成千上万的用户将寻找替代品，而不是让他们的设备处于香草状态。社交媒体市场非常紧张，很容易找到一个没有这些可笑障碍的好的替代品。我敢打赌，许多开发人员或公司都期待着交付一个类似的、写得更好的、考虑到所有用户的软件替代品，这将很快填补空白。

我不是安全专家，所以我请我们自己的资深公认开发人员 [pulser_g2](http://forum.xda-developers.com/member.php?u=2178960) 分享他对这一举措的看法。他是这么说的:

> 任何试图加强客户端安全性的应用程序，作为其核心用例的一部分，都是有根本缺陷的。如果您将数据交付给用户，他们拥有这些数据，您必须假设他们永远拥有这些数据。如果这是一个业余爱好者的“有趣”项目，这将是可以接受的-好吧，当然，有人可以截图，或存储它们，但这是足够公平的。这不是一个爱好应用程序，它试图做一些无法实现的事情。他们想在静止图像上实现 DRM，而即使是内容制作者也没有成功实现有效的 DRM。唱片公司放弃了——这个主意行不通。
> 
> Snapchat 最好把时间放在改进应用程序上——他们不会阻止人们截屏 snapchat(不提醒其他人)，如果有人真的想这样做——接下来，有人会直接连接到内核并转储帧缓冲区输出。祝你好运发现或阻止它。

这种不便将导致许多用户放弃 Snapchat，并寻找一些替代产品，这些产品将更加用户友好，可定制，并且希望在不应用这些奇怪的“补丁”的情况下更加安全。然而，如果你计划坚持使用 Snapchat 或 root，你可能需要尝试一下 [Snapprefs](http://forum.xda-developers.com/xposed/modules/app-snapprefs-ultimate-snapchat-utility-t2947254) 。MaarZ 承诺提供一个更新，将从应用程序中删除根检查。XDA 总会有办法的！

**Snapchat 的决定正确吗？您是否要停止使用此应用程序？请在下面的评论中告诉我们！**