# 精灵宝可梦 GO 的根检查现在寻找 TWRP 文件夹的存在

> 原文：<https://www.xda-developers.com/pokemon-go-aggressive-root-checking-twrp-folder/>

Pokémon GO 于 2016 年推出，由于其一鸣惊人的推出，它极大地促进了 AR 作为一种类型的流行。我们相信你已经很熟悉它了，但对于初学者来说，这几乎是一个游戏，你可以自己成为神奇宝贝训练师，走进现实世界，找到神奇宝贝。随着谷歌 Play 商店上超过 1 亿次安装，它在全球范围内也取得了很大程度的成功，这是一个简单而令人兴奋的前提，任何人都可以轻松访问。好吧，提醒你，除了根用户/修改用户之外的任何人。为了清除骗子，这款游戏已经变得对被修改的用户非常不友好，这是出了名的。这款游戏的很大一部分开发工作是阻止这些用户并实现更好的根检测方法。

此列表中的最新检测方法[由 Redditor fw85](https://www.reddit.com/r/pokemongodev/comments/f3xzyc/pok%C3%A9mon_go_abusing_filesystem_access_permissions/) 首先报告，它可能会滥用文件系统访问权限来寻找 TWRP 的存在，这是目前最流行的自定义恢复。Pokémon GO 似乎正在检查你的外部存储中是否存在 TWRP 文件夹，如果它设法找到了它，那么游戏会将你锁定在外。许多人使用 TWRP 来安装 Magisk 以获得 root 访问权限，这就是 Niantic 首先阻止它的原因。但是考虑到 TWRP 可以用来安装大量与根方法无关的东西，这看起来还是有点牵强。此外，我们被告知，该应用程序也在寻找一个钛备份文件夹的存在；钛备份，如果你没有听说过，是最受欢迎的根应用程序，使您的应用程序的完整备份。

此外，根据 XDA 公认的开发者 quinny 899 T1 的说法，Pokémon GO 应用程序还可以找到 TWRP 和钛备份文件夹，即使该应用程序没有读取外部存储的权限。这意味着只要这些文件夹在那里，你就不能访问 Pokémon GO，即使你撤销了该应用程序的存储权限，因为据报道，该游戏正在利用其文件夹检测检查的漏洞。

可能有简单的方法可以绕过这种检查，比如 TWRP 版本或 Titanium 备份更新将文件夹命名为其他名称。但在这一点上，这确实成为了一场猫捉老鼠的游戏，因为 Niantic 将不断适应检查 TWRP 和其他定制恢复，以及钛备份，(谁知道他们还将这扩展到什么)，开发者可能会试图绕过最新的检测。看起来 Niantic 并不打算在短时间内放弃积极检查 Pokémon GO 的 root 访问权限。因此，如果你真的真的关心这个游戏，为了你的虚拟口袋怪物，你可能会想完全保留股票。

**[【poke mon go】&【magik-xd 讨论线程】](https://forum.xda-developers.com/apps/magisk/discussion-pokemon-magisk-discussion-t3465722/page438)**

* * *

**来源:[Reddit](https://www.reddit.com/r/pokemongodev/comments/f3xzyc/pok%C3%A9mon_go_abusing_filesystem_access_permissions/)**

*更新 1(美国东部时间 2020 年 2 月 18 日 12:28 PM):这篇文章被更新为注意到钛备份也被检测到。*