# 如何收费解锁华为和 Honor 设备的 bootloader

> 原文：<https://www.xda-developers.com/huawei-honor-unlock-bootloader-fee/>

改造我们的智能手机和平板电脑是 XDA 的使命。我们的网站是最大的 Android 爱好者论坛的所在地，他们喜欢摆弄他们的设备，这有时会导致与制造这些设备的公司发生冲突。一些公司，如谷歌和一加，对修改者很友好，而其他许多公司则对我们的社区视而不见。然而，其他公司打击修改设备上的软件的能力，因为他们感到第三方经销商损害他们的声誉的威胁。例如，华为最近[停止为他们所有的智能手机和平板电脑提供引导程序解锁码](https://www.xda-developers.com/huawei-stop-providing-bootloader-unlock-codes/)，引发了来自社区的[反弹](https://www.xda-developers.com/xda-huawei-decision-stop-bootloader-unlocking/)。虽然华为的子品牌[Honor 在有限的试验中重新开放了](https://forum.xda-developers.com/honor-view-10/development/honor-bootloader-unlocking-limited-t3837880)引导加载程序解锁，但只有一种方法可以解锁你的华为或 Honor 设备的引导加载程序，但这需要你付出代价。

对于那些不知道的人，引导程序是负责在设备上启动操作系统及其内核的代码。通常，引导加载程序将只加载由设备制造商签名的引导映像。使用解锁的引导加载程序，您可以安装未经设备制造商签名的引导映像。这包括引导基于 AOSP 的 ROM 所需的定制映像、为支持 Magisk root 而修补的引导映像等等。解锁谷歌、一加、Essential、Razer 和其他一些设备制造商的智能手机上的引导程序非常简单，只需将你的手机连接到 PC，在开发者选项中启用“OEM 解锁”，然后在你的手机处于引导程序菜单中时输入几个 fastboot (fastboot 是一种从 PC 向设备的引导程序发送命令的协议)命令。其他设备要求您拥有设备特定的引导加载程序解锁代码，然后才能解锁引导加载程序。通常，请求引导加载程序解锁代码需要填写一个包含 IMEI、帐户信息和其他详细信息的表格。华为曾经提供过这样一个表格，但是他们在七月下旬关闭了这个表格。

这意味着不再有官方途径来获取你的华为或 Honor 智能手机或平板电脑的引导加载器解锁代码。还没有人弄清楚这些引导程序解锁代码是如何生成的，所以自己生成一个是不可能的。最有可能的是，这些代码是为工厂中的每个设备创建的，而华为表单只是从内部数据库中查找您设备的代码。因此，除非华为利用漏洞或突然来个 180 度大转弯，否则如果你执意要用定制内核、定制 rom、Magisk 等改造华为或荣誉产品，就不要指望它们。然而，如果你已经拥有一台华为或 Honor 设备，并且你真的*不顾一切地*解锁引导加载程序，那么还有最后一招:第三方付费服务。

## 非正式解锁华为和 Honor 智能手机的 Bootloader

**注意:XDA 开发商不支持使用第三方服务来解锁您设备的引导程序。我们不从下列任何服务中赚取任何利润。无法保证这些服务使用起来是安全的，如果您选择使用这些服务，您的设备将面临风险，因为华为和 Honor 可能不会在出现任何问题时为您提供支持(除非法律要求)。)**

你过去可能听说过一个叫做 [FunkyHuawei.club](https://funkyhuawei.club/) 的服务。我们已经泄露了关于 [Honor View 10](https://www.xda-developers.com/honor-v10-specifications-leaked/) 、[华为 Mate 10 Pro](https://www.xda-developers.com/exclusive-att-huawei-mate-10-pro-firmware/) 、[华为 Mate 20](https://www.xda-developers.com/possible-huawei-mate-20-camera-features/) 和许多其他设备的信息，这要感谢他们提供的固件版本的早期访问。FunkyHuawei 也有 unbricking 或 [rebranding](https://funkyhuawei.club/rebranding) 华为和 Honor devices 的服务，但他们最近增加的服务是 [bootloader 解锁](https://funkyhuawei.club/bootloader)。它为所有华为和 Honor 设备生成引导加载器解锁代码——甚至是最近发布的设备，如 Honor Note 10、华为 Mate 20 和 Honor Magic 2。其他付费服务，如 [DC 解锁器](https://www.dc-unlocker.com/)在最近的设备上停止工作，但如果你有一台旧的华为或 Honor 设备，你也可以尝试一下。我个人只在我的 Honor Magic 2 上尝试过 FunkyHuawei 的 bootloader 解锁服务，在我发送 IMEI 和型号后，解锁代码过了几分钟才到达我的收件箱。我还没有试过 DC 解锁器，但我听说它可以在华为 MediaPad M5 等设备上工作。*(免责声明:FunkyHuawei 向我提供了一个免费的代码，所以我可以验证他的服务实际工作。*)

至于价格，FunkyHuawei 的单个解锁码是 55 美元。是的，很贵。DC-解锁器更便宜，但它不能在新型号上工作。我不相信来自第三方的引导加载器解锁代码的可用性将挽救定制 rom 社区，因为很少有开发者愿意为华为或荣誉设备的发展而烦恼。然而，如果你只是想安装 Magisk 或尝试一个项目 Treble GSI，那么你必须付钱，因为像这样的服务是唯一的方式来解锁引导加载程序，我们知道。FunkyHuawei 告诉我，他们还出售从香港进口的设备，这些设备要么是预装的，要么带有引导程序解锁代码，以防你想走这条路。同样，你将支付比你通常为该设备支付的更多的费用，但华为 bootloader 解锁表单的关闭让你几乎没有选择。