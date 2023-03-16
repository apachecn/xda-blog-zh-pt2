# Android 上打印的历史以及 Mopria 联盟如何改进它

> 原文：<https://www.xda-developers.com/history-of-printing-in-android/>

在 Android 8.0 Oreo 的默认打印服务亮相之前，在 Android 上打印文档说起来容易做起来难。谷歌的移动操作系统直到 Android 4.4 KitKat 才获得原生打印机支持，除了三星等第三方解决方案之外，设置打印机需要特定供应商的插件和驱动程序。但多亏了由智能手机和打印机制造商组成的联盟 Mopria Alliance，Android 与打印机的兼容性得到了突飞猛进的提高。Android Oreo 支持市场上 97%的打印机，数量超过 1 亿台，此外还支持双面打印、Wi-Fi 直接打印、定向和纸张大小调整等功能。

但是 Mopria 联盟和移动打印有什么关系，未来的 Android 版本会有什么变化？下面是 Android 打印框架的简史，以及正在进行的改进的预览。

## 使用 Android 4.4 KitKat 在 Android 上打印

 <picture>![](img/10eee0b196dd83c0ef1033bb68055a8f.png)</picture> 

Android KitKat print menu.

早期版本的 Android 本身不支持打印。从 KitKat 之前的 Android 智能手机或平板电脑上打印文档、图像或任何其他东西需要下载第三方工具，如 [Google Cloud Print](https://www.xda-developers.com/how-to-print-android/) ，在另一个应用程序中调出文档，并使用 Android 的共享菜单将其传递给前述工具。不用说，这不是一个优雅的解决方案——尤其是与苹果的 AirPrint 和其他新兴竞争对手相比。

Android 的打印机服务需要改头换面，谷歌在 2013 年开始着手这项工作。Android 4.4 KitKat 标志着管理打印机的 API 和原生 Android 打印平台的首次亮相。新生的 Android 打印框架有一个用户界面，带有用于打印机和页面选择的下拉菜单，还有一个打印管理器，可以将应用程序的打印请求传递给可用的打印机服务。

当然，打印机制造商并不局限于新的打印管理器。他们可以使用 API 来开发自己的打印服务，并通过 Google Play 分发，许多公司都这样做了，包括惠普、佳能、爱普生和 Brother。与此同时，应用程序开发人员可以自由地向应用程序添加打印操作，或者实施新的打印 API 来创建、取消和检查正在进行的打印作业的状态。

下面是 Android 的打印堆栈当时是如何工作的(很大程度上，它今天仍然是如何工作的):当用户从应用程序中启动打印作业时，应用程序对 Android 打印框架进行 API 调用，而 Android 打印框架又调用打印服务。(其中一个 API 调用是对 Google 的 PDF 渲染器的调用，它生成了要打印的文件的分页 PDF 版本。)然后，打印服务完成了与打印机的握手，从而开始了打印过程。

不幸的是，KitKat 的新打印平台是最基本的定义。 [Android 5.0 Lollipop](https://www.xda-developers.com/tag/android-5-0-lollipop/) 对其进行了改进，增加了一个以材料设计为灵感的菜单，带有打印预览和用于纸张大小、颜色、方向和页面范围的下拉选择器。 [Android 7.0 牛轧糖](https://www.xda-developers.com/tag/android-7-0-nougat/)带来了新的 API 调用，可以显示打印作业的状态，允许应用程序显示打印进度的指标。(在之前的 Android 版本中，这一点并不明显。)但是 Android 的打印堆栈直到奥利奥才开始发挥作用。

## 由于 Mopria 联盟，Android 8.0 Oreo 的打印功能得到了改进

全球非营利移动印刷标准机构 Mopria Alliance 可能没有多少品牌认知度，但它并不是这个街区的新成员。自成立以来的五年中，它已经招募了打印机和生产力巨头，包括 Adobe、柯尼卡美能达、[高通](https://www.xda-developers.com/tag/qualcomm/)、利盟、京瓷、戴尔和东芝，所有这些公司都致力于支持移动设备的核心打印技术、功能和服务。

Mopria 联盟指导委员会主席 Brent Richtsmeier 告诉 XDA 开发商，Mopria 的技术安装在超过 7.5 亿台不同的移动设备上，每天向打印机发送 140 万页。“随着世界联系越来越紧密...]很明显，一切都是相互关联的，移动性更强，但人们仍然需要打印，”里奇斯迈尔说。

为此，Mopria 与 Android 原始设备制造商合作，如 Mopria 联盟的创始成员[三星](https://www.xda-developers.com/tag/samsung/)、[中兴](https://www.xda-developers.com/tag/zte/)、[华为](https://www.xda-developers.com/tag/huawei/)和[亚马逊](https://www.xda-developers.com/tag/amazon/)，以 Mopria 的开发工具套件 Mopria Print Library (MLP)发布平板电脑和智能手机。其努力的一个成果是三星打印服务，这是一款用于 Android 打印框架的移动打印工具，预装在[三星 Galaxy S4](https://forum.xda-developers.com/galaxy-s4) 、 [S5](https://forum.xda-developers.com/galaxy-s5) 、 [S6](https://forum.xda-developers.com/galaxy-s6) 、 [S7](https://forum.xda-developers.com/galaxy-s7) 、 [S8](https://forum.xda-developers.com/galaxy-s8) 和 [S9](https://forum.xda-developers.com/galaxy-s9) 上。(Richtsmeier 先生说它有大约 4 亿月活跃用户。)另一款是[中兴的 Axon 7](https://forum.xda-developers.com/axon-7) 和 Axon 7 Max，在中国发货时预装了 Mopria 打印服务。

与此同时，Mopria 开始与谷歌合作，将其技术与安卓开源项目( [AOSP](https://www.xda-developers.com/tag/aosp/) )代码库融合。在 KitKat 发布后的几年里，它贡献了数千行代码，最终形成了 [Android Oreo 新的改进的默认打印服务](https://www.xda-developers.com/android-oreo-print-service-ipp/)。

[Android 8.0 Oreo](https://www.xda-developers.com/tag/android-oreo/) 中的默认打印服务支持标准打印设置，如颜色调整、媒体类型选择和复印。它免费且易于使用，但也不妨碍开发人员创建自己的 Mopria 认证产品。

据里奇斯迈尔说，走定制路线相对容易。加入 Mopria 联盟是第一步——需要支付少量许可费。然后，开发人员有几个选择:(1)用他们自己的代码编译 Mopria 库，(2)使用 Mopria 许可给 Mopria 联盟所有成员的代码库，或者(3)使用 Mopria 现有的 AOSP 代码来编写定制的解决方案。

一旦代码就绪，接下来就是测试了。Mopria 联盟成员可以访问合规性测试工具集，包括自动化设备特定测试和打印机测试。一旦运行了必要的测试并收集了数据，就必须将结果发送给 Mopria 工程师，他会对结果进行审查，以确保代码的行为符合预期，并检查所有必要的复选框。如果一切顺利，这款应用被认为通过了 Mopria 认证。

## Android 上打印的未来

自前 KitKat 时代以来，Android 的打印平台已经走过了漫长的道路，当时 janky 变通方法(通常涉及共享菜单)是打印东西的唯一方式——当然，除了将文件传输到连接打印机的 PC。

也就是说，Android Oreo 的默认打印服务明显缺乏企业功能，如打孔、折叠、装订、PIN 认证或会计功能。它也不支持“共享打印”——没有简单的方法从 Android 的共享菜单打印东西。(Richtsmeier 先生将后一个问题归咎于一年前 Android 的 WebView 类中的一个 bug，该 bug 延迟了实现。)

 <picture>![Android Printing Mopria](img/7ee5c10d6fe0955bb8fdc8f719ce4270.png)</picture> 

Feature difference between Android Oreo's Default Print Service and the Mopria app. Source: [Mopria](https://mopria.org/android-8-oreo-faq).

第三方打印服务，如 Mopria 自己的独立 Mopria 打印服务，可从[谷歌 Play 商店](https://www.xda-developers.com/tag/google-play-store/)免费获得，有助于填补功能空白，增加了输入托盘选择、蓝牙打印、临时 Wi-Fi 打印和直接 USB-OTG 打印等功能。但对于互联网基础设施不完善的国家或没有谷歌 Play 商店的国家的用户来说，这并不是什么安慰。

令人欣慰的是，改进的迹象即将出现，因为 Android P 将在某种程度上弥补功能差距。

Mopria 开发者在去年年底提交的 Android Gerrit 中的几项承诺指向对只支持 IPPS 打印机的支持。IPPS 是基于 HTTPS 的互联网打印协议(IPP)的安全实现，允许应用程序通过互联网连接的打印机发送打印作业、查询打印作业状态等。

今年 1 月，Mopria 的开发者开始为另一个不错的功能打基础:Wi-Fi 直接打印。目前，Android 上的默认打印服务仅支持通过路由器或热点的本地无线基础设施连接，但 [new commits](https://www.xda-developers.com/wi-fi-direct-printing-android/) 增加了对 Android 智能手机和平板电脑以及 Wi-Fi 直连打印机之间直接连接的支持。使用 Wi-Fi Direct，不需要配对，而且与 Wi-Fi 热点不同，一些打印机甚至不需要密码。

Richtsmeier 先生说，Mopria 的开发者也提供了手动添加打印机的代码。

“有研究表明，占劳动力大多数的 80%的千禧一代使用移动技术工作，但只有 33%的人表示这些移动技术满足了他们的需求，”里奇斯迈尔说，“人们认为打印是办公室里发生的一件重要事情。Mopria 正试图填补这一空白，满足这些需求。”