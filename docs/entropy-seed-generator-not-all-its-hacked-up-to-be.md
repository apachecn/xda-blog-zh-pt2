# 熵种子发生器并不像它被攻击的那样

> 原文：<https://www.xda-developers.com/entropy-seed-generator-not-all-its-hacked-up-to-be/>

与许多人的想法相反，我们报道的内容并不总是完美的。虽然我们做了很多正确的事情，并且有一个伟大的开发团队不断地将设备提升到一个新的高度，但有时我们会强调收益未知的解决方案。我们最近发表的一篇关于 Nexus 7 和其他设备上游戏的[黑客的文章就是这样一个例子。](http://www.xda-developers.com/android/reduce-game-lag-on-nexus-7-and-other-devices-with-seeder-entropy-generator/ "Reduce Game Lag on Nexus 7 and Other Devices with Seeder Entropy Generator")

黑客攻击的前提是，您可以通过在 Android 文件系统的一个部分( [/dev/random](http://en.wikipedia.org/wiki//dev/random) )中充满随机位来减少延迟，这样系统就不必等待文件系统生成它们。从理论上来说，这听起来很棒，并且在某些明显滞后的领域向[展示了一些成功，但是这也给](http://forum.xda-developers.com/showpost.php?p=36266768&postcount=888)[带来了其他各种各样的问题](http://forum.xda-developers.com/showthread.php?p=36265300#post36265300)。

正是出于这些考虑，我们不建议使用此修复程序。这种疗法本身绝不会造成伤害，其效果近乎安慰剂。CyanogenMod 开发者 arcee [发布了关于修复的信息](https://plus.google.com/115049428938715274412/posts/GWr72W9zmY2),声明

/dev/random 的唯一用户是 libcrypto(用于 SSL 连接、ssh 密钥生成等加密操作)、wpa_supplicant/hostapd(用于在 AP 模式下生成 WEP/WPA 密钥)以及在使用 ext2/3/4 格式时生成随机分区 id 的库。这三个用户都不在应用程序执行的路径上，所以从 urandom 获取 random 除了产生 random 之外什么也不做...良好的...不太随机

关于延迟和 Android 操作系统如何处理它们有一些合理的担忧，Android 代码中目前正在进行关于这一点的讨论，但是这个修复并没有解决这些问题，而是通过提高 CPU 速度来提高性能。开发人员自己表示，这实际上可能会减少电池寿命，因为黑客每秒钟都在唤醒 CPU。

一如既往，您在 XDA 使用的任何东西都由您自己承担风险，并且您为自己的行为承担所有责任。也就是说，有时候我们会传递不准确的信息，这就是其中之一。我们为所有开发人员努力寻找解决困扰他们的问题的方法而喝彩。然而，我们在这一点上操之过急，没有进行充分的讨论和测试。

[ *图片改编自[/dev/urandom thinks](http://philipp.knechtges.com/)。* ]