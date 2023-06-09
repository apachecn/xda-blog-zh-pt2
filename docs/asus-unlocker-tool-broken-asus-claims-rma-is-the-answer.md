# 华硕解锁工具损坏，华硕声称军事革命是答案

> 原文：<https://www.xda-developers.com/asus-unlocker-tool-broken-asus-claims-rma-is-the-answer/>

又来了。最近，在 bootloader 方面，似乎公司的立场摇摆不定。你有[锁定引导程序的三星设备](http://www.xda-developers.com/xda-tv-2/verizon-galaxy-s3-unlocked-cm9-stable-and-nexus-7-phone-calls-xda-developer-tv/)和[解锁引导程序的摩托罗拉设备](http://www.xda-developers.com/android/motorola-photon-q-4g-lte-rooted-with-custom-recovery/)。华硕是一家通常会满足客户需求的原始设备制造商。我们已经给你带来了他们的[经常发布的解锁工具](http://www.xda-developers.com/android/asus-unlocks-tf300t-bootloaders-all-rejoice/)的新闻。结果是，其中一个不起作用。

几个月来，华硕 Transformer Prime 的用户在使用他们的解锁工具版本时遇到了麻烦。起初只是一些人有问题，后来已经膨胀成一个相当大的问题。这个问题的原因是未知的，但最重要的是，用于 Prime 的引导加载器解锁工具不起作用。尝试时，用户会收到以下错误消息:

> 出现未知错误，这可能是网络连接问题。
> 
> 请稍候，稍后再试

XDA 资深会员 nhshah7 就此事发了一个帖子，看看有多少用户受到了影响。事实证明，相当多的是。开发者和成员都被这些问题弄得不知所措，所以他们开始寻找解决问题的方法。

那么，这给每个人留下了什么？由于有了 [logcat](http://www.xda-developers.com/android/dont-know-how-to-logcat-try-logcat-tool/) 的帮助，用户和开发人员已经将问题缩小到以下方面:

> d/keybox service(10158):= = = status code:SC _ UNAUTHORIZED！
> 
> d/keybox 服务(10158): === OTA BEGIN
> 
> E/KeyBoxService(10158): ===连接 http://wvdrm.asus.com 被拒绝
> 
> d/keybox service(10158):= = = 600 秒后重试。
> 
> D/KeyBoxService(10158): === OTA 结束

令人欣慰的是，公众抗议或请愿可能不是必要的，因为华硕正在试图解决这个问题。最近，截至 2012 年 9 月 10 日，华硕实际上在主题本身中进行了评论，让用户知道加拿大和美国客户的平板电脑可以修复，但需要 RMA。说[华硕 _ 美国](http://forum.xda-developers.com/member.php?u=4029265):

> 我不能代表其他国家或地区，但如果您在美国或加拿大，我们的设施可以修复解锁错误。然而，正如梅森所说，它确实需要你把它送到军事革命。
> 
> 呼叫中心和技术支持可能不知道，但我们的技术人员已经知道如何修复它的程序。我向所有试图通过呼叫中心获得 RMA 的人道歉。他们被告知不要帮助解决解锁设备的问题——我们都是这样。但是，我们理解这是一个特殊问题，并已为受影响的平板电脑建立了维修流程。

当然，这只适用于美国和加拿大的客户。然而，这是向前迈出的积极一步，也可能导致对其他国家的支持。更多信息，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=1764917)。