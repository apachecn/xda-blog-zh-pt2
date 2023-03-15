# 据报道，安卓安全网现在会被解锁的引导程序触发

> 原文：<https://www.xda-developers.com/android-safetynet-now-reportedly-tripped-by-unlocked-bootloaders/>

对于开发者和高级用户来说，周三都是坏消息。愉快的一天被几个报告打破了，这些报告称，Android 安全网的新更新不仅导致现有的 su 隐藏机制停止工作(正常情况下)，而且开始对甚至没有根的设备产生不利影响！

[![Android Pay](img/efb2d3a68073edfc1f39ade8f3cb5650.png)](http://static1.xdaimages.com/wordpress/wp-content/uploads/2016/10/gFWepB2r-e1476884820287.png) 从 [Reddit 的 Nexus 6P 论坛](https://www.reddit.com/r/Nexus6P/comments/586bq7/android_pay_stopped_working_on_nonrooted_device/)开始，然后在几个地方引起反响，包括 [Reddit Android 论坛](https://www.reddit.com/r/Android/comments/587ss9/psa_android_safetynet_now_tripped_by_unlocking/)，我们自己的 [Nexus 6P 论坛](http://forum.xda-developers.com/nexus-6p/help/party-bootloader-unlocked-rooted-pay-t3483229)和 [suhide](http://forum.xda-developers.com/apps/supersu/suhide-t3450396) 和 [Magisk](http://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445) 的线程，用户发现，如果他们有一个解锁的引导加载程序，安全网的最新更新会导致设备无法通过检查。用户已经尝试了修改场景和屏蔽方法的不同组合，但是大多数情况下失败的共同因素归结为引导装载程序被解锁。

解锁引导程序是大多数设备非官方修改的第一步。如果最新的 SafetyNet 更新确实检查了引导程序的状态，这可能意味着一个人可以运行 Android Pay 和其他基于 SafetyNet 的应用程序以及 root 和通过使用屏蔽技术暴露的日子结束了。

Magisk 开发者 [topjohnwu](http://forum.xda-developers.com/member.php?u=4470081) [对早期的情况](http://forum.xda-developers.com/showpost.php?p=69196610&postcount=5)进行了评论，指出安全网在此次更新后可能会失败:

*“请记住，在几个小时后刚刚发生的安全网的最新更新中，谷歌似乎在加紧游戏，它可能已经到了不允许修改的地步，并且可能无法绕过。*

*目前在我的 HTC 10 上， **无论我对开机镜像做了什么，哪怕只是一个重新包装的 100%库存开机镜像** ，安全网在任何情况下都不会通过。另一方面，我的 Nexus 9 运行库存牛轧糖似乎没有问题，根和模块都启用了，工作正常。引导验证可能会因 OEM 而异，HTC 的实现可能只是第一批被纳入安全网的实现之一，但最终所有主要 OEM 的方法都将被纳入，**到那时，我认为任何 Android“mod”，包括自定义内核，都将打破安全网。这些验证应该被编码到 bootloader 中，不容易被破解。所以结论是，我以后不会花那么多时间绕过安全网。”***

早在 suhide 被释放的时候，Chainfire 已经[预测了一些类似的事情](http://forum.xda-developers.com/showpost.php?p=68424605&postcount=2):

最终，信息将由 boot loaders/trust zone/secure boot/TIMA/TEE/TPM 等提供和验证。(三星已经通过他们的诺克斯/TIMA 解决方案做到了这一点)。我们无法轻易触及或修补设备的某些部分，因此总有一天这些检测旁路可能不再可行。

由于形势仍在发展，事情可能比表面上看起来更复杂。如果这件事有新的进展，我们会及时通知我们的读者。