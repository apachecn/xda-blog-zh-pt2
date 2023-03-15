# 提高微软 Surface 的触摸屏响应能力

> 原文：<https://www.xda-developers.com/increase-touch-screen-responsiveness-on-the-microsoft-surface/>

说到一些事情，平台的选择并不重要。电池寿命永远是一场斗争，有些东西永远会滞后，[史蒂夫·鲍尔默永远是个疯子](https://www.youtube.com/watch?feature=player_embedded&v=Wn_XI3dU-kU)。不管你用的是 iOS、Android 还是 Windows Phone，这些陷阱肯定会在未来一段时间内伴随着我们。

最近，由于 XDA 论坛成员[塔玛拉苏](http://forum.xda-developers.com/member.php?u=2211879)的努力，发布了一种有助于提高[微软 Surface](http://forum.xda-developers.com/forumdisplay.php?f=1624) 上触摸反应的方法。这不是一个特别难做的修改，因为这只是一个注册表修改，大多数用户应该能够没有任何麻烦。这是如何做到的:

> 发现了一个触摸预测键，当编辑时，它在键盘响应和小项目操作方面有显著的改进，例如经典桌面、文件浏览器等。
> 
> 关键是:HKEY _ LOCAL _ MACHINE \ SOFTWARE \ Microsoft \ touch predict ion
> 
> 编辑从 8 到 2 的延迟键。
> 
> 将采样时间从 8 点编辑为 2 点
> 
> 重新开始

如上所述，这很容易做到。到目前为止，每个尝试过的人都证实它非常有效。不过，有一些警告。XDA 知名开发者 [GoodDayToDie](http://forum.xda-developers.com/member.php?u=3529492) 指出，对于重度用户来说，这可能会明显影响电池寿命，因为系统必须更加频繁地轮询屏幕。有些人没有注意到下降，但很可能随着触摸屏的使用频率增加，电池电量会增加。如果你想提高 Surface 触摸屏的响应速度，并且不介意缩短寿命，这是值得一试的。

更多信息，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=2091867)。