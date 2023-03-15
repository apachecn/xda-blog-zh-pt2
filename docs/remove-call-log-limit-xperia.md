# 取消索尼 Xperia 设备上的通话记录限制

> 原文：<https://www.xda-developers.com/remove-call-log-limit-xperia/>

# 了解如何取消索尼 Xperia 设备上的通话记录限制

教程教你如何在你的索尼 Xperia 设备上手动取消 500 次通话的限制。

如果你是那些打电话次数特别多的人之一(使用手机的定义功能值得称赞)，你可能已经注意到你的 Android 设备上的通话记录被限制在 500 次。对于大多数人来说，这根本不是问题，但如果你是少数几个真正想知道过去 500 个电话以外的细节的人之一，或者如果你只是想尝试一些新的东西，有一个教程教你如何消除这种限制。

由 XDA 论坛成员 [pollob666](http://forum.xda-developers.com/member.php?u=3754641) 撰写的这份指南告诉你这种限制在代码中的确切位置，以及你需要做什么来改变或删除它。这是一个相当简单的过程，需要反编译 *framework.jar* 和一些小的编辑。这已经在[索尼 Xperia V 和 TX](http://forum.xda-developers.com/xperia-t-v) 上进行了测试，运行官方 ROM 或 OmniROM，尽管由于其简单性，其他 ROM 和设备，Xperia 或非 Xperia 也可以工作。不过，一定要做好备份，以防事情发生差错。

这个功能也可以通过一个 Xposed 模块来实现，但是采用手动的方式来修改从来都不是一件坏事，尤其是对于那些刚刚开始学习的人。如果您有兴趣尝试一下，请前往[调用日志限制移除教程线程](http://forum.xda-developers.com/xperia-t-v/general/guide-how-to-make-call-log-limit-t2866632)了解更多信息。