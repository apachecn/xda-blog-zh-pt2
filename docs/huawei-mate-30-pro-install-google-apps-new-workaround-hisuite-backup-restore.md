# 华为 Mate 30 Pro 可以通过这种新的解决方法再次运行谷歌应用程序

> 原文：<https://www.xda-developers.com/huawei-mate-30-pro-install-google-apps-new-workaround-hisuite-backup-restore/>

**更新 1 (10/08/19 @美国东部时间上午 4:10):**我们得到通知，该线程不再有华为 Mate 30 Pro 的可下载资源。这种方法在概念上仍然有效。

全世界都把目光投向了华为 Mate 30 系列的[发布，寻找这个问题的答案:“*当你在今年最受期待的手机之一上把谷歌从安卓手中夺走时，会发生什么？*“正如我们担心](https://www.xda-developers.com/huawei-mate-30-pro-rs-porsche-design-specifications-features-pricing-availability/)[和期待](https://www.xda-developers.com/huawei-mate-30-without-google-play-apps-services/)的那样，华为 Mate 30 和它的兄弟姐妹在没有预装谷歌服务的情况下登台亮相，仅仅依靠[华为的 AppGallery](https://www.xda-developers.com/appgallery-huawei-alternative-google-play-store-android/) 作为应用分发的主要媒介。然而，这种情况很快就消失了，因为谷歌服务助手(Google Services Assistant)是一种“变通方法”，这种应用允许用户在华为的 EMUI 和 Mate 30 系列以及 Honor 9X Pro 上下载 Google Play 服务和附带的组件。谷歌服务助手应用程序托管在一个名为[LZPlay.net](https://www.lzplay.net/#/)的网站上，因此这种方法通常被称为 LZPlay。

## 旧的解决方法:谷歌服务助手和 LZPlay

由于谷歌服务助手是一种在没有谷歌应用程序的设备上安装谷歌应用程序的变通方法，这种变通方法是如何产生的是一个合理的问题。

过去，中国的原始设备制造商已经发布了 GMS(谷歌移动服务)安装程序，以方便侧装，但鉴于前所未有的复杂政治局面，这样的解决方案对华为来说并不现实。这些 GMS 安装程序通过更新由 OEM 预加载到系统中的 GMS“存根”来工作(GMS 应用程序需要特殊的权限才能正常运行，并且该权限仅适用于系统应用程序)。正如你已经知道的，非根设备上的应用程序只能在现有应用程序的基础上更新，前提是它们已经由相同的签名签名。因此，存根和应用程序必须带有相同的谷歌签名，由于美国的禁令，华为基本上无法预载谷歌签名的存根。

一旦我们从设备上拿到软件，我们发现这些设备实际上并没有预装任何 GMS 存根。这表明，无论谷歌服务助手使用何种方法来安装 Play 服务，都是不寻常的，值得在开发社区中进一步研究其可能的用途。XDA 认出了因与 Magisk 合作而闻名的开发者[top johnwu](https://forum.xda-developers.com/member.php?u=4470081),[调查了这一异常行为](https://medium.com/@topjohnwu/huaweis-undocumented-apis-a-backdoor-to-reinstall-google-services-c3a5dd71a7cd)。

事实证明，谷歌服务助手利用了华为的一组 API，这些 API 旨在用于移动设备管理(MDM——企业用来管理员工设备)。此[华为安全授权 SDK 的完整 API 参考已经向公众开放](http://obs.cn-north-1.myhwclouds.com/consumer/docattachment/c8d57ff88c03fdcda9f4286204c045109bee5cc99bc6558430860e4e418a9467/APIs.pdf)，因此企业用户可以了解并受益于对其业务组织中设备的全方位控制方法。真正的问题在于一些 MDM APIs 的形式，它们只是最近才被记录下来，并且这些文档只有在您签署合法协议以访问 SDK 时才可用。

```
 <uses-permission android:name="com.huawei.permission.sec.MDM_INSTALL_SYS_APP"/>
<uses-permission android:name="com.huawei.permission.sec.MDM_INSTALL_UNDETACHABLE_APP"/> 
```

这些 MDM APIs 允许*允许的应用*安装“系统应用”，即使手机有锁定的引导加载程序，启用了 Android 验证引导，并使用[华为的只读文件系统 EROFS](https://www.xda-developers.com/huawei-erofs-linux-file-system-android/) 格式化。实际发生的情况是，一个允许的应用程序，在这种情况下是谷歌服务助手，被允许将用户应用程序标记为不可移动的系统应用程序，即使这些应用程序或存根实际上不存在于只读分区上。“允许的应用程序”据称受到华为的严格控制——开发人员必须签署法律协议，提交许可请求和许可请求的理由，并将每次发布的 APK 二进制文件发送给华为进行检查。只有在华为同意的情况下，应用程序才会使用华为的特殊密钥进行签名，允许它使用这些 API。

因此，谷歌服务助手的存在是在华为 MDM API 的严格限制之内，并且暗示他们并不知情。然而，华为否认与 LZPlay 有牵连，[发表了以下声明](https://www.theinquirer.net/inquirer/news/3082169/huawei-mate-30-lzplay-shutdown-backdoor):

> #### 华为最新的 Mate 30 系列并没有预装 GMS，华为与 www.lzplay.net 也没有任何瓜葛

正如人们在复杂的政治场景下所预料的那样，谷歌服务助手和 LZPlay 的存在将是短暂的。随着这种变通方法越来越受欢迎，感兴趣的团体似乎注意到了这一点。托管谷歌服务助手的网站 LZPlay 已经离线，侧装谷歌服务助手应用程序不再获取谷歌应用程序，该应用程序从华为获得的特别许可也有可能被撤销。谷歌肯定也注意到了这一点，因为 SafetyNet 也收到了一个更新，从他们的白名单中撤销了华为 Mate 30 的构建指纹，这意味着 SafetyNet 将失败，不允许已经设法下载谷歌应用的设备能够使用谷歌支付等应用。

* * *

## 新的解决方法:HiSuite 还原

**更新:**链接的线程不再有可下载的资源。然而，假设您已经获得了可下载的资源，那么该方法在概念上仍然有效。

对许多人来说，运行谷歌应用程序的能力是一件大事，因此人们将永远有兴趣在如此强大的硬件上下载谷歌应用程序。XDA 资深成员[张洋 _ 哈哈](https://forum.xda-developers.com/member.php?u=4878612)已经想出了一个[不同的变通办法](https://forum.xda-developers.com/mate-30-pro/how-to/method-confirmed-to-install-google-t3979091)，一个本质上涉及从一个设备恢复备份镜像的方法，该设备设法从后面使用谷歌服务助手安装谷歌应用程序。此外，请注意，该方法似乎是针对华为 Mate 30 Pro 的，因为备份的图像来自该设备——我们无法确认同样的方法是否可以在华为 Mate 30 或 Honor 9X Pro 上工作。

**[在华为 Mate 30 Pro - XDA 线程上安装 Google Apps 的新变通方法](https://forum.xda-developers.com/mate-30-pro/how-to/method-confirmed-to-install-google-t3979091)**

虽然这种方法不像安装谷歌服务助手并让它做所有事情那么简单，但它仍然有效——警告 SafetyNet 将继续失败，因为这是谷歌的服务器端变化。

1.  用户需要将他们的文件备份到 PC 上的 HiSuite 中，并对他们的手机进行出厂重置。
2.  在[线程](https://forum.xda-developers.com/mate-30-pro/how-to/method-confirmed-to-install-google-t3979091)中安装可下载 zip 中提供的 Google apps。
3.  将提供的备份映像 zip 文件解压缩到 PC 上的 HiSuite backup 文件夹中。
4.  将备份恢复到您的设备，确保您也将“系统设置”从备份映像恢复到您的手机。
5.  一旦提供的备份已经“恢复”(又名安装)在您的手机上，您需要重新启动您的设备。
6.  接下来，确保你进入应用程序设置，清除你安装的谷歌应用程序的所有数据，并授予这些应用程序请求的所有权限。
7.  为了更好的措施重新启动。
8.  在手机连接互联网的情况下启动谷歌 Play 商店。

对于何时可以恢复以前的数据，该线程不会立即清除。大多数用户将在新的华为 Mate 30 设备上使用这种方法，因此数据损失应该不会很大。请注意，安全网仍然会失败，而且很可能会继续失败，直到政治形势有所改善。目前，如果你想在你的新设备上安装谷歌应用程序，这个新的解决方案是你最好的选择。

**[华为 Mate 30 XDA 论坛](https://forum.xda-developers.com/mate-30) || [华为 Mate 30 Pro XDA 论坛](https://forum.xda-developers.com/mate-30-pro)**