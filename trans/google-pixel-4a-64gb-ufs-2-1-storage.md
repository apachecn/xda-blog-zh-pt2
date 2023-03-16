# 搭载 UFS 2.1 的谷歌 Pixel 4a 提供了比 Pixel 3a 更快的存储速度

> 原文：<https://www.xda-developers.com/google-pixel-4a-64gb-ufs-2-1-storage/>

谷歌去年在谷歌 I/O 2018 上推出了第一批中端 Pixel 智能手机。Pixel 3a 和 Pixel 3a XL 因其价格而被广泛认为是优秀的智能手机，特别是因为它们提供了谷歌的恒星相机应用程序、Android 软件功能和每月更新支持。不过，Pixel 3a 的内部硬件没有什么值得大书特书的，它有中端高通骁龙 670 处理器、4GB 内存、单个后置和前置摄像头、FHD+ AMOLED 显示屏和 64GB eMMC 闪存。今年，谷歌预计将在 Pixel 3a 的基础上推出“ [Pixel 4a](https://www.xda-developers.com/tag/pixel4a/) ”，这款新设备将在处理器、内存和设计方面进行相当明显的升级。我们最初认为不会升级的一个组件是存储，但我们现在有证据表明，谷歌 Pixel 4a 将拥有改进的 UFS 2.1 闪存芯片。

**[谷歌像素 4a 论坛](https://forum.xda-developers.com/pixel-4a)**

我们在 YouTube 频道 [*的朋友 TecnoLike Plus*](https://www.youtube.com/channel/UCSExLh16bM4dOYec9D6zx8g) ，由 YouTube[Julio Lusson](https://twitter.com/julio_lusson)运营，与我们分享了设备的 bootloader 屏幕。引导程序屏幕显示一行“Ufs: 64GB SKHynix。”此外，从“fastboot getvar all”的输出中，我们确定这个预生产谷歌 Pixel 4a 中使用的特定存储芯片是 SK 海力士的 64GB UFS 2.1[h 9 HQ 53 aecmmdar-KEM](https://www.skhynix.com/products.do?ct1=53&ct2=54&lang=eng)。

 <picture>![Google Pixel 4a bootloader](img/a57bfee6d122cc95844102f8ed93f511.png)</picture> 

Pixel 4a bootloader. Photo credits: [Julio Lusson](https://twitter.com/julio_lusson) from YouTube channel [TecnoLike Plus](https://www.youtube.com/channel/UCSExLh16bM4dOYec9D6zx8g).

那么这到底意味着什么呢？通用闪存存储(UFS)是一种闪存存储标准，设计时考虑了移动设备的功耗限制。从理论上讲，从 Pixel 3a 中的 64GB eMMC 存储芯片迁移到 Pixel 4a 中的 64GB UFS 2.1 存储芯片应该会提高文件传输的读写速度和能效，但对用户来说最重要的是这次升级对应用程序加载和安装速度的影响。将应用程序加载到内存中可能需要读取大量小文件，这就是为什么存储的随机读取性能是一个至关重要的指标。如果你将 Pixel 3a 及其 64GB eMMC 存储的随机读取性能与 OPPO R17 进行比较，OPPO R17 也有骁龙 670 处理器，但[有 128GB 的 UFS 2.1 存储](https://benchmarking.ihsmarkit.com/605577/teardown-oppo-r17-pbem00)，你会注意到 OPPO R17 的随机读取性能[略高](https://www.giznp.com/wp-content/uploads/2018/09/9d43737957fe4312b052eae89187a5c7.jpeg.webp)。(H/t 至[giz NPT7 为 OPPO R17 AndroBench 编号。)下面是我的 Pixel 3a XL 的 AndroBench 结果供比较:](https://www.giznp.com/2018/09/07/oppo-r17-review/)

 <picture>![Pixel 3a XL AndroBench](img/d0bf34475a0bf404f59b5f7201357c52.png)</picture> 

AndroBench is a fairly old benchmark with an equally dated design, but it’s still the go-to for storage testing. It tests the speed of sequential read/write, random read/write, and SQLite insert, update, and delete operations. A sequential read/write is an operation that involves reading/writing storage blocks that are contiguous, while a random read/write involves reading/writing randomly scattered storage blocks. SQLite describes a type of database management system; developers dealing with large databases often have to make SQLite calls to retrieve or modify the database. We can get a good idea of the storage performance of an Android device with AndroBench. By default, the benchmark writes a 64MP file with either 32MB or 4KB buffer sizes for sequential and random read/writes respectively, and an SQLite transaction size of 1\. The speed of the former operation is measured in MB/s while the latter in Queries Per Second (QPS).

即使使用 Pixel 3a 的 eMMC 存储，随机读取速度也没有那么差。Google 对 F2FS 文件系统做了很多改进来提高文件 I/O 性能，概述的有 [*Anandtech*](https://www.anandtech.com/show/13474/the-google-pixel-3-review/2) 和 XDA 公认开发者 [arter97](https://forum.xda-developers.com/member.php?u=4898097) 。Pixel 3a 在随机写入速度上轻松击败了 OPPO R17，也许是因为文件系统的差异，但不幸的是，我不知道 OPPO 在 R17 上的/data 分区使用的是什么文件系统。(作为参考，OPPO 在 Find X2 Pro 上使用 F2FS 用于/data，但在国际 Reno3 Pro 上使用 EXT4 用于/data。)

无论如何，这里的主要观点是，谷歌 Pixel 4a 应该比 Pixel 3a 提供明显更快的应用程序加载和安装时间。我们说“应该”,因为我们不知道谷歌是否会在 Pixel 4a 零售设备中真正使用这个组件，但我们不认为这个原型设备和零售设备之间会有任何实质性的硬件差异。遗憾的是，我们不知道实际存储容量是否会升级，因为 *TechnoLike Plus* 得到的泄露设备只有 64GB 的存储容量，与 Pixel 3a 的容量相同。幸运的是，似乎至少 Pixel 4a 的价格将与 Pixel 3a 相同(399 美元)，至少根据 Evan Blass 的说法[。](https://twitter.com/evleaks/status/1237674053655318528)

* * *

关于 Pixel 4a 的更多信息，[请查看我们之前的文章](https://www.xda-developers.com/google-pixel-4a-hands-on-video-snapdragon-730/)，它报道了由*technolike Plus*拍摄的视频泄露。或者，只看本文底部嵌入的视频。

**谷歌 Pixel 4a 传闻规格**

*   处理器:高通骁龙 730
*   GPU: Adreno 618
*   内存:6GB
*   内部存储:64GB UFS 2.1
*   显示屏:单孔 5.81 英寸显示屏，2，340 x 1，080 分辨率，443 dpi，60Hz 刷新率
*   后置摄像头:12 MP 传感器+ LED 闪光灯+ 4K 视频录制
*   前置摄像头:800 万像素，带视频稳定功能
*   连接:4G，双卡，GPS，WiFi 5，蓝牙，GLONASS
*   端口:USB Type-C、3.5 毫米耳机插孔
*   安全性:后置指纹传感器
*   电池:3080 毫安时
*   软件:安卓 10