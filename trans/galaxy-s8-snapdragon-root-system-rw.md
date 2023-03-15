# 银河 S8+骁龙根接入，系统读写已实现

> 原文：<https://www.xda-developers.com/galaxy-s8-snapdragon-root-system-rw/>

# 银河 S8+系统读写的骁龙根访问已经实现

社区开发者表示，在 SuperSU root 正常工作的情况下，他们已经能够获得 Galaxy S8+上/system 分区的读/写访问权限。

三星通常会发布两种不同版本的旗舰智能手机，它们自己的 Exynos SoC 在大多数全球市场使用，骁龙 SoC 在美国(和其他一些地方)使用。该公司专注于他们产品的安全性，正如他们在 KNOX 上所做的工作所证明的那样，但很容易解锁他们使用 Exynos 芯片组的[设备的引导加载程序。](https://www.xda-developers.com/samsung-exynos-and-aosp-explained-a-story-of-betrayal/)这不是骁龙版本的情况，但一些开发者已经宣布，Galaxy S8+已经实现了 root。

对于那些没有跟进的人，XDA 资深成员 [Acoustichayes](https://forum.xda-developers.com/member.php?u=6316811) 几个月前在 XDA 银河 S8 论坛上创建了一个帖子。这个线程的目标是跟踪三星 G950U/G955U 骁龙智能手机的 root 访问的当前进度( [Galaxy S8](https://forum.xda-developers.com/galaxy-s8) 和 [Galaxy S8+](https://forum.xda-developers.com/galaxy-s8+) )。到目前为止，这个帖子已经有 140 多页了，但是昨晚晚些时候，当 XDA 资深成员[博特森](https://forum.xda-developers.com/member.php?u=3903209)更新了他们的进展时，一些重大的新闻出来了。

这篇文章是为了通知社区/system 分区已经以读/写方式挂载，开发团队需要时间来打包。几个小时后，同一个开发者又发了一个帖子，显示 SuperSU 已经安装并以 root 权限正常运行。然后，我们发现团队中有人说他们拥有 Galaxy S8+的 root 访问权限，并且[他们正在等待一些文件，以便他们可以开始在 Galaxy S8 上工作](https://www.reddit.com/r/GalaxyS8/comments/6skqt7/root_close_for_snapdragon_s8_on_xda/dle7ztr/)。

从我们收集的信息来看，这种方法可能是由于一个漏洞，这并不意味着引导装载程序以任何方式解锁；软件包和说明应该会很快发布，但是不要发垃圾邮件询问 ETA，并且在提问之前搜索你的问题。

由于这不会解锁引导加载程序，这意味着 TWRP 或任何未签名的图像不能被刷新到设备上(即使在它被根化之后)。虽然这对于一些人来说是令人失望的，但该团队也表示，这意味着 KNOX 因为他们使用的漏洞而完好无损。

* * *

[**/系统挂载为读写确认**](https://forum.xda-developers.com/galaxy-s8/how-to/current-root-progress-g950u-g955u-t3623444/post73336318#post73336318)

[**SuperSU 安装并工作**](https://forum.xda-developers.com/galaxy-s8/how-to/current-root-progress-g950u-g955u-t3623444/post73338376#post73338376)