# PSA:你可以优化你的 Note 4 的最近菜单和内存

> 原文：<https://www.xda-developers.com/psa-you-can-optimize-your-note-4s-recents-menu-ram/>

Note 4 从来没有最快的最近菜单，尽管它有 3GB 的内存，但它的应用程序保存能力在 Lollipop 上只会变得更差。困扰 S6 的臭名昭著的 RAM 错误确实是 Note 4 的 5.0.X ROMs 的烦恼。关于更新以解决所有这些问题的传言得到了俄罗斯 Note 4 5 . 1 . 1 更新的[第一份报告的证实，该更新似乎改善了最近的菜单和 RAM 管理。](https://www.youtube.com/watch?v=5HFxN1Rp1Ag)

但是，在每个地区和每个运营商版本都收到这个版本之前，还需要很长时间，在此之前，我们几乎没有办法解决这个问题。Galaxy S6 [通过简单的 build.prop 编辑修复了其 RAM 管理](http://www.xda-developers.com/fix-for-galaxy-s6-memory-issues/)。事实证明，该修复也可以移植到 Note 4 上，实际上是逐行移植，以实现非常相似的效果和额外的优化。你可以在这个 XDA 帖子上找到如何做的指南[，这个帖子](http://forum.xda-developers.com/note-4/general/galaxy-s6-build-prop-ram-fix-note4-t3150862)[是在这个 Reddit 帖子](https://www.reddit.com/r/galaxynote4/comments/39a7s2/galaxy_s6_ram_fix_works_on_note_4/)之后发的。我建议您在开始之前阅读这两篇文章，但是您会发现应用修复程序相当容易:

你所需要的只是 root 和一个 [build.prop 编辑器](https://play.google.com/store/apps/details?id=com.jrummy.apps.build.prop.editor&hl=en)，比如在 [ROM Toolbox Lite](https://play.google.com/store/apps/details?id=com.jrummy.liberty.toolbox&hl=en) 上找到的那个。或者，您可以使用其他文本编辑器来编辑 build.prop。此修复已被确认可以在骁龙和 Exynos 变体(尽管结果略有不同)和多个 rom 上工作，但**请确保进行备份。**此外，**确保读取两个线程**。之后，您应该进入 build.prop 编辑器的编辑模式，向下滚动到#DHA Properties 部分。在那里，您必须像这样编辑这一行:

 `ro 。 配置 。DHA _ empty _ max=36

 `然后添加以下内容:

 `ro 。 配置 。DHA _ cached _ max=12

`ro.config.dha_th_rate=2.3`

`ro.config.dha_lmk_scale=0.545`

`ro.config.sdha_apps_bg_max=70`

`ro.config.sdha_apps_bg_min=8`

`ro.config.oomminfree_high=7628,9768,11909,14515,16655,20469`

如果您没有#DHA 属性，也没有上述任何一行，您可以在文件底部添加所有行。完成后，点击保存按钮并重启。或者，XDA 资深会员 [Near_07](http://forum.xda-developers.com/member.php?u=6008647) 为用户提供了一个[的可闪拉链](http://forum.xda-developers.com/showpost.php?p=61733327&postcount=21)让这个过程更容易。我已经尝试了这两种方法，它们都在我的 SM-910T 上运行[TEKodus from](http://forum.xda-developers.com/note-4-tmobile/development/rom-boc4-tekxodus-n4-urv1-4-14-15-note4-t3082085)时完美地工作。

用户报告了两个主要好处:1 .最近菜单打开的速度要快得多。和 **2。手机整体感觉更流畅。**现在，我们都知道有许多“安慰剂”build.prop 编辑，但我可以保证这一点:我的 Note 4 的最近菜单打开*明显更快，几乎是即时的*，手机似乎比以前更流畅更快。我不能向你保证后一种说法对你的设备绝对正确，但我的经历与前面提到的许多用户的经历相符。

最后， **RAM 管理**据称得到了改进，**但是**用户报告表明它在 Exynos 变体上工作得更好，SM-N910C 似乎是这个修复的典范。话虽如此，这一调整让我的 T-Mobile(骁龙)Note 4 略胜一筹，但就将应用程序保存在内存中而言，我看不出*有什么明显的*好处(它似乎仍然只能保存大约 8 个应用程序)。

你知道这个补丁吗？这对你有用吗？下面就让我们知道吧！```