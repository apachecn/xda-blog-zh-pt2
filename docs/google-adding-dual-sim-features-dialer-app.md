# 谷歌正在其拨号应用程序中添加双 SIM 卡功能

> 原文：<https://www.xda-developers.com/google-adding-dual-sim-features-dialer-app/>

双卡智能手机在世界许多地方都很受欢迎。双 SIM 卡手机有两个 SIM 卡插槽，这意味着用户可以在一个设备中使用两个不同运营商的 SIM 卡。曾经，很少有 Android 智能手机支持双卡。然而，在过去的几年里，这一功能越来越受欢迎，在印度、中东和非洲等许多地区，双 SIM 卡插槽的手机已经很普遍了。

这导致智能手机制造商针对特定市场发布了双 SIM 卡手机。其他原始设备制造商则更进一步，为他们所有的智能手机配备了双 SIM 卡插槽。在印度等一些国家，如今用户很难找到只有一个 SIM 卡槽的智能手机，因为所有流行的手机现在都有两个 SIM 卡槽。[用户也接受了这一功能](https://www.xda-developers.com/what-are-the-benefits-to-having-a-dual-sim-phone/)以受益于灵活性、更便宜的价格(例如，通过使用一家运营商的呼叫服务和另一家运营商的移动数据)，以及携带一台设备而不是两台独立的“工作”和“个人”设备。

不过，这一功能从未在西方流行起来。这是由多种原因造成的，但主要原因是，在美国等市场，手机主要是由运营商销售的——运营商没有兴趣销售带有两个 SIM 卡插槽的手机，以便让消费者锁定他们的服务。一加等原始设备制造商确实在美国销售不上锁的双卡手机，但总体而言，这一功能在西方市场仍然是一个利基市场。

这就是为什么谷歌仍然没有在其 Pixel 手机中支持双 SIM 卡。Nexus 设备也不支持双 sim 卡。该公司也没有为通常支持双卡的地区单独发布 Pixel 和 Pixel 2 的双卡版本，这使得三星等其他原始设备制造商的旗舰产品更具吸引力。

然而，现在我们已经看到 AOSP 接受了三项承诺。这些承诺证实了谷歌正在为其拨号器应用程序添加双 SIM 卡功能，尽管 Pixel 设备上缺乏双 SIM 卡。应该注意的是，有多种双 SIM 卡智能手机使用相对普通的 Android，因此即使谷歌没有在下一代 Pixel 中实现两个 SIM 卡插槽，其他手机也将受益，因为原始设备制造商不必自己添加功能。

[提交号 541646](https://android-review.googlesource.com/#/c/platform/packages/apps/Dialer/+/541646/) 的标题为:**实现首选 SIM 卡**。该描述指出:

"*在提示用户选择 SIM 之前，CallingAccountSelector 将查找备用首选 SIM 数据库，查看是否已经设置了首选 SIM 并绕过选择。如果号码在联系人列表中，用户还可以选择将选定的 SIM 卡存储为首选。*

这意味着谷歌正在实施一个首选 SIM 数据库，这将意味着用户不必一直选择他们的首选 SIM 卡。CallingAccountSelector 将查看是否已经设置了首选 SIM，如果是，它将绕过选择。应该注意的是，多个原始设备制造商已经在其 rom 中添加了该功能。

第二个提交编号为 541790 ，标题为:**实现建议的 SIM** 。该描述指出:

这个 CL 增加了一个模块，可以查询提供商，以帮助用户选择使用哪种 SIM 卡进行呼叫。

commit 实现建议的 SIM 功能，其中拨号器将通过查询提供商来建议用户使用哪个 SIM 来实现任何功能。

最后，[提交号 541802](https://android-review.googlesource.com/#/c/platform/packages/apps/Dialer/+/541802/) 的标题为:**将首选 SIM 元数据添加到拨号器清单**。它的描述指出:

"*联系人需要检查元数据，以决定是否应该显示首选的 SIM 卡用户界面。*

联系人应用程序将检查首选 SIM 卡元数据，以决定是否向用户显示首选 SIM 卡用户界面。与第一次提交相关，这意味着如果元数据显示用户已经选择了他们的首选 SIM 卡，则不会显示 UI。

这些功能现在已经合并到 AOSP 拨号器中。考虑到双卡安卓智能手机的流行不会很快消失，它们是一个受欢迎的补充。谷歌甚至可能有计划为未来的 Pixel 系列配备两个 SIM 卡插槽，至少针对特定地区。