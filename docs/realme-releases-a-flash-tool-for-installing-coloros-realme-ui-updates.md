# Realme 发布安装 ColorOS/Realme UI 更新的 flash 工具

> 原文：<https://www.xda-developers.com/realme-releases-a-flash-tool-for-installing-coloros-realme-ui-updates/>

Realme 可能已经从其母公司 OPPO 分离出来，但在定制 Android 皮肤方面，两家公司在内部使用一个共同的基础。到目前为止，Realme UI 仍然是 OPPO ColorOS 之上的一层新鲜涂料，它肯定不会像 Realme 首席执行官最初承诺的[那样*接近库存 Android* 。事实上，Realme 仍然在利用 OPPO 专有的 **OZIP** 文件格式来打包他们的更新包。您不仅必须强行将这些 OZIP 包](https://www.xda-developers.com/coloros-7-for-realme-phones-will-be-closer-to-stock-android/)[提取 AES 密钥](https://bkerler.github.io/reversing/2019/04/24/the-game-begins/)以便[将它们](https://github.com/bkerler/oppo_ozip_decrypt)转换为常规恢复可闪存 ZIP 文件，而且您也不能使用标准快速启动接口直接使用它们来执行干净闪存。

围绕 Realme 设备的定制开发社区正在[迅速](https://www.xda-developers.com/realme-x-development-updates-first-custom-kernel-5-new-roms-available/)扩张，主要是因为它们给智能手机领域带来了低成本革命。realme[发布内核源代码](https://www.xda-developers.com/realme-x50-pro-5g-realme-x2-realme-x2-pro-android-10-kernel-source-code-now-available/)并允许[引导加载程序解锁](https://www.xda-developers.com/realme-6-pro-bootloader-unlock-tool-unofficial-twrp-now-available/)，这在售后开发场景中充当了强大的催化剂。然而，在移植定制 ROM 或尝试新模式的过程中，手机本身可能会因为一些原因而被阻塞，并且官方闪存工具的不可用使得恢复一切变得复杂。flash 工具的缺乏基本上迫使用户访问服务中心来执行简单的解锁工作，这根本不受社区的欢迎。

但是现在，在戏弄他们的 flash 工具[一年多一点之后](https://c.realme.com/in/post-details/1110451594350034944)，Realme 终于拿出了一些有成效的东西。 **Realme Flash 工具**的初始版本现在可以下载，尽管 [Realme X50 Pro](https://forum.xda-developers.com/realme-x50-pro) 是迄今为止唯一兼容的设备。用户可以用这个工具刷新 **OFP** 包，这个工具不同于[公司下载门户](https://www.realme.com/in/support/software-update)上列出的 OZIP 固件。闪存过程将完全擦除目标设备，因此您应该在使用闪存工具之前备份您的个人数据。

如你所见，Flash 应用的 UI 与小米开发的 Mi Flash 工具非常相似。然而，Realme Flash 工具没有被编程为与[高通紧急下载模式](https://www.xda-developers.com/oneplus-8-pro-unbrick-tool-now-available/) (EDL)一起工作。它更像是快速启动二进制文件的 GUI 包装器，因此您必须在刷新之前解锁目标设备的启动加载程序。Realme India Francis Wang[承诺](https://twitter.com/FrancisRealme/status/1244605958078083072)在 bootloader 解锁后，Realme 手机上损坏的指纹传感器问题将随着 flash 工具的发布而得到解决，尽管我们目前无法验证这一说法的真实性。

值得一提的是，该工具不支持降级到较低的 Android 版本，尽管如果底层 Android 层保持不变，您应该可以切换到较低版本的 ColorOS 或 Realme UI。与 Realme 声称的相反，这款只支持 Windows 的工具并没有特别绑定到印度版本的 Realme X50 Pro。你应该可以用这个闪光器闪任何骁龙或联发科驱动的 Realme 手机，只要你有合适的 OFP 软件包。该公司正计划通过在未来发布所需的 OFP 文件，将更多手机从其产品组合中添加到受支持的设备列表中。

**[下载 Realme Flash 工具](https://download.c.realme.com/flash/Flash_tool/realme_Flash_Tool.zip)**

* * *

**来源:Realme 社区( [1](https://www.realmebbs.com/post-details/1271082970484060160) ， [2](https://c.realme.com/in/post-details/1271381271037083648) )**