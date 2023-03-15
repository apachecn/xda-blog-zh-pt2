# 谷歌增加了 Brotli 压缩，以提供更快的 OTA Android 更新

> 原文：<https://www.xda-developers.com/google-brotli-compression-faster-ota-updates/>

OTA 更新的大小不是大多数人真正考虑的事情，因为更新通常会通过 WiFi 在后台自动下载，但它实际上是服务器后端的一个大问题。即使只保存几兆字节的数据也会产生巨大的影响，因为潜在的成千上万的用户会成倍地增加收益。为此，谷歌一直在努力将 T4 的 Brotli 压缩算法引入安卓系统，以加快 OTA 更新速度。

## 什么是 Brotli 压缩算法？

Brotli 是一种由少数谷歌员工开发的压缩算法，与 GZIP 等其他算法相比，它显著提高了压缩率，同时也展示了令人印象深刻的解压缩速度。缺点是用 Brotli 算法压缩文件相当慢，所以在压缩动态内容时一般避免使用。

*压缩基准。来源:[耶鲁安 Ooms](https://www.opencpu.org/posts/brotli-benchmarks/)*

另一方面，任何静态内容，如[网页](https://www.xda-developers.com/xda-external-link/brotli-a-new-compression-algorithm-will-help-speed-up-chrome/)都适合通过 Brotli 算法进行压缩。这包括从谷歌 Play 商店下载的应用程序文件。由于有超过 20 亿的安卓设备，当从 Play Store 提供补丁文件时，即使删除少量数据也会给谷歌带来巨大的收益。Brotli 算法用于 [Play Store 应用下载](https://students.googleblog.com/2017/02/intern-impact-brotli-compression-for.html?m=1)时，每天为用户**节省 1.5 Pb(150 万 GB)的数据**。

 <picture>![Brotli Compression Algorithm Play Store](img/26a5988c4d07bc297ba3fb034dd0785f.png)</picture> 

Brotli Compression Algorithm versus GZIP for Play Store Downloads. Credits: [Google Student Blog](https://students.googleblog.com/2017/02/intern-impact-brotli-compression-for.html?m=1)

## Brotli 将如何改进 OTA 更新？

现在，OTA 更新不像 Play Store 应用程序更新那样频繁地提供给用户，但相比之下，它们往往要大得多。例如，压缩前的完整 OTA 包的大小可以是 2gb。一个 OTA 包能保存多少数据？

摩托罗拉 Moto G4 的 LineageOS 开发者报告说，他们能够在非官方版本上节省 50 兆字节。考虑到 Moto G4 LineageOS 的平均容量约为 [350 兆字节](https://download.lineageos.org/athene)，这是一个相当大的改进。如果在每个 OTA 上节省了 10 MBs 的数据，那么带宽的总体减少可能是显著的，因为谷歌需要向成千上万的用户提供更新包。

此外，由于 Brotli 还提高了解压缩速度，这也意味着 OTA 更新可以更快地应用。OTA 更新作为档案发送到每个设备，因此在通过 [bsdiff](https://android-developers.googleblog.com/2016/07/improvements-for-smaller-app-downloads.html) 制作补丁之前，需要对档案进行解压缩。由于 Brotli 解压缩相当快，这意味着解压缩存档也将很快，从而更快地修补系统文件。

然而，使用 A/B 分区方案的设备的用户，如谷歌 Pixel/Pixel 2、Essential Phone、Razer Phone、 [Moto Z2 Force](https://www.xda-developers.com/moto-z2-force-ab-seamless-updates/) 和[小米 Mi A1](https://www.xda-developers.com/xiaomi-mi-a1-android-ab-partition/) 可能不会注意到这一特别的改进，因为更新无缝地应用于后台的非活动分区。尽管如此，即使对于这些设备，由于 Brotli 压缩，较小的 OTA 更新包也会导致用户带宽减少。

* * *

*感谢 XDA 退休论坛版主/公认开发者 [cybojenix](https://forum.xda-developers.com/member.php?u=4584140) 的提示！*