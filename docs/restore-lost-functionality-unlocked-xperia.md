# 在解锁的 Xperia 设备上恢复丢失的功能

> 原文：<https://www.xda-developers.com/restore-lost-functionality-unlocked-xperia/>

如果你在最近的索尼 Xperia 设备上解锁了你的引导程序，你可能知道潜在的保修损失并不是你必须接受的唯一缺点。另一个相当隐蔽的问题与各种专有功能有关，如 X-Reality 色彩管理、BIONZ 图像处理器和主动噪声消除技术。

一旦您决定解锁您的引导加载程序，该过程还会删除一段称为 DRM 密钥的数据。这些与索尼提供的各种服务(如流媒体视频等)相关，但也是上述功能正常工作所必需的。简而言之，一旦钥匙不见了，你将面临诸如低光相机图像质量下降和缺乏 X-Reality 模式等问题。

然而，XDA 公认的贡献者[吉姆诺尔](http://forum.xda-developers.com/member.php?u=4699816)是来帮忙的。他开发了一个 mod，通过编辑系统文件来恢复大部分失去的功能。对于那些对如何恢复你的特征感兴趣的人，请越过[到线程](http://forum.xda-developers.com/crossdevice-dev/sony/xperia-z1-z2-z3-series-devices-drm-t2930672)。确保仔细阅读所有内容，并在您的恢复中详细闪存提供的 zip 文件。

对于对技术更感兴趣的人，我挖得更深一点，详细揭示了这个 mod 是如何工作的——更重要的是，这对最近的 Xperia 设备的所有者来说实际上意味着什么。所以我们先来看看 mod 到底触动了什么。zip 的内容大部分是修改过的系统文件，其中大部分是代码库，但也有一些二进制文件和一个 Android 包文件。以下是一些例子:

*   libdrmdecrypt.so
*   libdrmframework.so
*   libdrmdiag.so
*   drmserver
*   credmgrd
*   CredentialManagerService.apk

如您所见，所有这些文件都在某种程度上与您设备的 DRM 服务相关。虽然并不令人惊讶，但被修改的文件的数量(超过 30 个)非常突出。另一个需要注意的要点是，除了系统文件之外，没有任何东西被修改，没有对 TA 分区或其他类似的东西进行修改。mod 完全依赖于对系统分区的修改。

请在下面的评论中告诉我们你的想法，并查看[第二部分](http://www.xda-developers.com/android/restore-lost-functionality-on-your-unlocked-xperia-device-part-two/)了解更多信息。