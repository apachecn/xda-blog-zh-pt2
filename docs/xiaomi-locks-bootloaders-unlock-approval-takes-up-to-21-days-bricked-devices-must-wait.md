# 小米锁定 Bootloaders，解锁可能需要 3 周时间

> 原文：<https://www.xda-developers.com/xiaomi-locks-bootloaders-unlock-approval-takes-up-to-21-days-bricked-devices-must-wait/>

在 XDA，我们对小米又爱又恨:我们喜欢他们和其他中国制造商给智能手机竞赛带来的[低成本革命](http://www.xda-developers.com/brace-yourselves-more-great-smartphone-prices-are-coming/)，但绝对厌恶他们[在多个场合违反 GPL v2](http://www.xda-developers.com/gplv2-and-its-infringement-by-xiaomi/)。

GPL 的情况一直在来回摇摆，某些设备的源代码被释放，而其他设备被忽略和推后。这让我们看到小米更多的时候是负面的。

最近，小米似乎又回到了违背开发者群体利益的老路上去了。这一切都始于 MIUI 论坛的一则公告:

> 嗨，米耶，
> 
> 为了保护用户数据安全，我们从红米 Note 3 上市开始就锁定了 bootloader。正如我们之前所说的，我们将逐步为其他 Mi 设备做出同样的改变。现在，该列表还将包括 Mi 4c 和 Mi Note Pro。

论坛帖子继续解释为什么小米必须做出这样的决定。由于非官方经销商添加了恶意软件，以及运输所有带有未锁定引导加载程序的设备相关的安全性损失，小米不得不考虑消费者的最佳利益，决定为 mi 设备锁定引导加载程序。

很公平。一个未锁定的引导加载程序会带来一些安全风险(T1)，这对普通消费者来说是不值得的(T2)。即使从定制 rom 社区的角度来看，拥有一个锁定但不可锁定的引导加载程序也比所有设备默认安装一个未锁定的引导加载程序要好。前者给有意愿的用户一个选择，如果他们希望沿着“黑暗”的道路冒险，并且仍然保持普通用户受到保护，而后者只是让每个人都面临风险，而不管他们是否需要解锁的引导加载程序。

即使是 Nexus 设备(旨在作为开发人员参考设备)也带有锁定的引导加载程序，如果用户愿意，可以解锁该程序。一个可解锁的引导程序场景也比一个完全锁定引导程序并且无法解锁的设备有利得多。

小米确实提供了解锁 bootloader 的方法。事实上，他们还通过 MIUI 论坛帖子详细介绍了官方解锁工具和教程。解锁锁定的引导加载器设备的引导加载器的步骤包括下载 zip 文件并通过 MIUI 上的更新器应用程序运行它，在设备上登录具有解锁权限的 Mi 帐户，当解锁工具提示时在 PC 上登录相同的 Mi 帐户，然后在引导加载器模式下将设备连接到 PC。对于第一次接触的人来说，这看起来很复杂，而且不必要的复杂。然而，对于任何其他有经验的用户来说，这一系列的说明并不难理解。还有一个带图像说明的[简体英语指南](http://en.miui.com/forum.php?mod=viewthread&tid=204866)来指导用户完成整个过程。

那么，关键在哪里？小米选择锁定其设备的 bootloader，并给用户解锁的选项，这有什么问题？

问题不在于解决方案，而在于执行。解锁引导程序并不像表面上看起来那样简单和容易。真正的障碍在于从小米那里获得解锁码。该程序足够复杂，需要一个代码申请过程的[逐步指南。](http://en.miui.com/thread-210153-1-1.html)

第一个问题是，[该网站是中文的](http://www.miui.com/unlock/)，所以你可能不得不使用谷歌翻译，不仅要浏览解锁请求网站，还要填写细节，包括你的**“解锁原因”**描述——是的，你必须向他们解释你为什么要解锁引导程序，所以*这真的是*一个申请过程。不仅如此，确认还需要 3 到 21 天才能到达，因为所有请求都是由开发人员手动**批准**。所以现在，别人控制着你的引导程序解锁。

然而，快速浏览一下论坛，尤其是 XDA 爱好者之间的对话，就会发现整个困境更糟糕的一面。面临[引导循环](http://forum.xda-developers.com/showpost.php?p=64814159&postcount=39)的用户，包括那些通过更新到新的引导加载程序锁定的 rom 而进入该状态的用户，只能通过解锁引导加载程序来解决问题。XDA 资深会员[法兰克布利](http://forum.xda-developers.com/member.php?u=2989622)T4 解释道:

> 你需要意识到从 6.1.14 开始，锁定的引导程序意味着没有快速引导可用。在 OTA 之后，人们在官方 miui 论坛上到处举报砖块，但根本没有提供解决方案。
> 
> 这是小米不可原谅的。

此外，许多用户反映，如果你想让你的请求在合理的时间窗口内获得批准，你必须在 MIUI 论坛上排名靠前，并谈论“钻石”用户获得优先待遇。鉴于申请过程是通过小米网站完成的，并且请求是人工批准的，这不是不可想象的。XDA 资深会员 [chickentuna](http://forum.xda-developers.com/member.php?u=4492200) [向一名陷入 bootloop 无法解决的用户解释了问题](http://forum.xda-developers.com/showpost.php?p=64814301&postcount=40):

> 你需要在他们的论坛上达到一定的地位，小米才能批准你的解锁请求。最有趣的部分是，一旦获得批准，你需要等待他们的短信包含解锁代码，你才能真正解锁你的设备，这可能需要 15 天或更长时间，根据一些尝试解锁的用户。

截至目前，受影响的用户是那些故意为小米设备闪存较新的 rom 并在不知情的情况下锁定其 bootloaders 的用户。但这将成为一个强制标准，也将通过在线旅行社发布，因此在某些时候，这将影响更大部分的用户群；如果保持下去，最终会在大部分小米设备上。最大的打击来自于这样一个事实:你的引导装载器解锁必须被请求和批准(通过一个据称有偏见的过程)，并且解锁请求可能需要几天才能完成。

总而言之，这对所有小米粉丝来说都是一个很悲哀的发展。凭借他们提供的价值，他们已经成为新兴市场的驱动力，就硬件而言，他们的设备似乎难以抗拒。但当你考虑到他们的 MIUI/软件，更糟糕的是，他们的 GPLv2 违规*和现在的*，他们试图将用户锁在他们的设备之外，“你得到你所支付的”这句话开始变得更有意义。

在他们的一个常见问题中，小米问自己 *[“锁定 bootloader 是否违背了米的‘极客’精神？”](http://en.miui.com/thread-201477-1-1.html)* 而且，可笑的是，他们的回答完全回避了这个问题。而那是因为无法逃避的答案。我们希望小米能够解决所有这些问题，并找到一个更好的、公正的、通用的流程，一个不会让用户在几周内一无所知的流程。至少，我们希望那些受这一举措影响最大的用户能够找到快速解决他们的砖块问题的方法。

如果你想了解更多关于这个问题的信息，并与其他小米用户讨论，请查看[这个讨论主题](http://forum.xda-developers.com/mi-4c/general/warning-locked-bootloader-t3292891)。