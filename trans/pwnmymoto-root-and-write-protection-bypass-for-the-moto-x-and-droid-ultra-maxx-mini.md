# 用于 Moto X 和 Droid Ultra / Maxx / Mini 的 PwnMyMoto Root 和写保护旁路

> 原文：<https://www.xda-developers.com/pwnmymoto-root-and-write-protection-bypass-for-the-moto-x-and-droid-ultra-maxx-mini/>

当 Moto X 发布时，许多人不安地得知，尽管谷歌在开发过程中发挥了积极的影响，但这款设备仍然没有真正开放。老实说，关于摩托罗拉对开发者的友好程度，从来没有任何虚假的借口。然而，看起来黑客大师和 XDA 精英公认的开发者 [jcase](http://forum.xda-developers.com/member.php?u=2376614) 又成功了。

不久前，jcase 为机器人阵容创造了 [MotoRoot。这利用了之前](http://forum.xda-developers.com/showthread.php?t=2442585)[报道的](http://www.xda-developers.com/android/xposed-patch-for-master-key-and-bug-9695860-vulnerabilities/ "Xposed Patch for Master Key and Bug 9695860 Vulnerabilities") Android bug 9695860 来获得系统用户。然后，jcase 自己创建的一个 symlink 攻击被用来获取 root 访问权限。然而今天，一个更好的解决方案出现了。

再次感谢 jcase，PwnMyMoto 首先使用 bug 9695860(就像它的前身一样)来获得系统用户。它还利用 MotoRoot 中的符号链接攻击来获取根用户访问权限。然而，对于 PwnMyMoto 来说，接下来发生的事情是新的:获得 root 后，bootloader 漏洞被利用，允许绕过 */system* 分区上的写保护。在这个过程中，库存恢复被删除，防止不需要的未来 OTA 干扰根状态。

自然，任何未经授权的修改都带有固有的风险。但是，如果您希望 root，您必须冒这些风险才能释放您的设备。首先，请浏览下面的链接。再次祝贺 jcase 的伟大工作！

非常感谢 jcase 的提示！]