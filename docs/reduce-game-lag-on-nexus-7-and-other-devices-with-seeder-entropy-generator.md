# 使用播种熵生成器减少 Nexus 7 和其他设备上的游戏延迟

> 原文：<https://www.xda-developers.com/reduce-game-lag-on-nexus-7-and-other-devices-with-seeder-entropy-generator/>

**更新:**由于可疑的收益和固有的缺点，我们建议用户在继续之前请先阅读[这一解释](http://www.xda-developers.com/android/entropy-seed-generator-not-all-its-hacked-up-to-be/)。

尽管有一些真正顶级的硬件，一些高端 Android 设备[似乎仍然有一些游戏](http://www.xda-developers.com/android/cpu-boosting-application-makes-gaming-on-one-x-even-better/)的问题。有一些 mod 可以修复这些延迟问题，因为潜在的原因通常等同于处理器没有发挥其全部能力的一些问题。T2 Nexus 7 T3 设备现在有了一个新的补丁来帮助减少游戏延迟。

XDA 资深成员 [lambgx02](http://forum.xda-developers.com/member.php?u=1107425) 最初发布 Seeder 熵生成器是为了在各种 Android 设备上停止滞后。运行前提是大多数游戏延迟是由熵引起的。正如 lambgx02 所解释的:

> 因此，我经历了重大的滞后，就像我们所有人时不时会经历的那样，于是我决定要弄清事情的真相。
> 
> 经过几个小时的追踪调试，我发现了安卓 90%的滞后的根源。一句话，熵(或缺乏熵)。
> 
> Google 的 JVM 和 Sun 的一样，从/dev/random 中读取。对于所有随机数据。是的，使用非常有限的熵池的/dev/random。
> 
> 随机数据被用于各种东西..UUID 生成、会话密钥、SSL..当我们用完了熵，这个过程就阻塞了。这表现为滞后。该过程不能继续，直到内核生成更多高质量的随机数据。
> 
> 所以，我交叉编译了 rngd，并使用它以 1 秒的间隔将/dev/urandom 输入/dev/random。

解决这个问题的结果是游戏运行更加流畅。XDA 公认的贡献者 [bradman117](http://forum.xda-developers.com/member.php?u=3527846) 测试并确认它适用于 Nexus 7，并发布在更多用户可以看到的地方。到目前为止，用户已经报告了极好的结果。安装也很容易，因为这是一个简单的压缩闪存恢复。

然而，如果你决定试一试，请注意**非常真实的警告**由于劣质随机数生成导致安全性降低，以及电池寿命缩短。如 lambgx02 所述:

> *   存在(理论上的)安全风险，因为用/dev/urandom 播种/dev/random 会降低随机数据的质量。实际上，这种被密码利用的几率远远低于有人攻击操作系统本身的几率(一个简单得多的挑战)。
> *   这可能会对电池寿命产生不利影响，因为它每秒钟都会唤醒一次。它不支持唤醒锁，所以它不应该有很大的影响，但如果你认为它会引起问题，请让我知道。我可以在代码中添加一个阻塞读取，这样它只在屏幕打开时执行。另一方面，我们许多人把滞后归因于缺乏 CPU 能力。由于这种方法消除了几乎所有的延迟，因此不需要超频，从而潜在地降低了电池消耗。

虽然 lambgx02 指出，由于 *urandom* - > *随机*播种而被利用的风险很低，但在我们的书中，任何增加的风险对于日常驱动的设备来说都太大了。不过，我们建议所有对此感兴趣的人三思，因为这有潜在的风险。然而，我们理解为什么在严格控制的环境中，加密强度不是很重要，有些人可能想尝试一下。要了解更多信息，请查看 [Nexus 7 螺纹](http://forum.xda-developers.com/showthread.php?t=2077086)以及[原始螺纹](http://forum.xda-developers.com/showthread.php?t=1987032)。