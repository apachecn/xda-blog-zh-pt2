# 如何从一加 8 系列和一加北部删除脸书膨胀软件

> 原文：<https://www.xda-developers.com/how-to-remove-facebook-bloatware-from-oneplus-8-8-pro-nord/>

Android 和膨胀软件是自从 OS 出现以来就共存的两个领域。故事[始于运营商](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)将各种无用或功能重复但质量低劣的应用捆绑到他们网络下销售的智能手机上。从那时起，故事扩展到原始设备制造商自己捆绑复制应用，甚至脸书和微软的应用被捆绑到智能手机上。我们随处可见膨胀器*，以至于[它的存在不再是惊喜](https://www.xda-developers.com/tcl-plex-android-10-update-bloatware/)，但它的不存在绝对是惊喜。一加通过在一加 8、一加 8 Pro 和一加 Nord 上捆绑脸书拥有的应用程序，参与了臃肿软件的混乱。但值得庆幸的是，有一种方法可以从这些设备中删除脸书膨胀软件。*

 ***XDA 论坛:[一加 8](https://forum.xda-developers.com/oneplus-8) || [一加 8 Pro](https://forum.xda-developers.com/oneplus-8-pro) || [一加诺德](https://forum.xda-developers.com/oneplus-nord)**

膨胀软件的定义是不断变化的，会因用户而异——一个人认为膨胀的东西实际上可能对其他人有用。考虑到这一点，一加智能手机现在打包的应用程序可能会也可能不会为所有用户增加效用，这并不是什么新闻。自 OnePlus 3 以来，一加一直在捆绑其[社区应用](https://www.xda-developers.com/oos-debloater-helps-remove-unwanted-applications-for-the-oneplus-3-and-oneplus-3t/),你也可以发现 Kindle 应用和其他一些类似的应用已经有好几代了。但是大部分都很容易卸载，所以没什么大不了的。

然而，[正如 *Android Police* 证实的](https://www.androidpolice.com/2020/08/05/oneplus-is-poisoning-its-phones-with-facebook-bloatware/)，一加 8、一加 8 Pro 和一加诺德(至少)上的 OxygenOS 现在打包了脸书应用安装程序、脸书应用管理器和脸书服务作为系统应用，与主要的脸书应用、Facebook Messenger、Instagram 和 Netflix 一起。在[对其](https://forums.oneplus.com/threads/allow-user-to-choose-which-stock-apps-they-want-to-install-during-set-up.1174902/#post-21557915)[创意活动](https://www.xda-developers.com/5-new-oxygenos-features-oneplus-working-on/)下的一项功能建议的回复中，一加解释说，预装这些应用程序可以确保脸书上更好的电池效率，并增强网飞上的 HDR 播放，尽管我们并不接受。众所周知，应用预加载是一个赚钱的机会，原始设备制造商经常与应用合作，将应用预加载到他们的智能手机上，我们认为这也是正在发生的事情。你可以卸载脸书、Messenger 和 Instagram 等面向用户的应用，但后台服务不能卸载，只能禁用。

**XDA 点评:[一加 8](https://www.xda-developers.com/oneplus-8-xda-review/) || [一加 8 Pro](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/) || [一加诺德](https://www.xda-developers.com/oneplus-nord-review/)**

嗯，你仍然可以卸载它们，但你需要亚行。对于如何在没有 root 访问权限的情况下移除运营商和 OEM 臃肿软件，我们有长期的指导[，这些经验仍然适用。你可以按照指南清理你的手机(任何 Android 手机)，但如果你正在寻找从一加 8 系列和一加诺德删除脸书应用程序的具体命令，XDA 资深成员](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)[赛格](https://forum.xda-developers.com/member.php?u=4480489) [指出，这些是你需要通过 ADB 运行的命令](https://forum.xda-developers.com/oneplus-nord/how-to/guide-how-to-remove-facebook-bloatware-t4143489):

```
 adb shell
pm uninstall -k --user 0 com.facebook.appmanager
pm uninstall -k --user 0 com.facebook.services
pm uninstall -k --user 0 com.facebook.system 
```

这些命令应该可以让你 900 美元的新智能手机摆脱预装的“不可卸载”的脸书膨胀软件。你可能需要对每一个 OTA 都重复一遍这些步骤，但总比完全没有解决方案要好。

**从 Amazon.in 购买:[一加 8](https://www.amazon.in/Test-Exclusive-237/dp/B071Z97T2C/?tag=xdaportalin-21) || [一加 8 Pro](https://www.amazon.in/Test-Exclusive-542/dp/B078BN55WZ/?tag=xdaportalin-21) || [一加诺德](https://www.amazon.in/OnePlus-Nord-Gray-128GB-Storage/dp/B08695ZSP6/?tag=xdaportalin-21)***