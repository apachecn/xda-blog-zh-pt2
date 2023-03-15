# 如何在三星 Galaxy S8/S8+上安装 Android Oreo(exy nos)

> 原文：<https://www.xda-developers.com/how-to-install-android-oreo-on-the-samsung-galaxy-s8-s8-exynos/>

在经历了[漫长的等待](https://www.xda-developers.com/android-8-0-oreo-google-released/)和多次[测试版发布](https://www.xda-developers.com/android-oreo-beta-galaxy-s8-india-germany-france/)之后，三星终于发布了针对 Exynos 三星 Galaxy S8 和 S8+的[官方 Android Oreo 更新](https://www.xda-developers.com/samsung-galaxy-s8-android-oreo-project-treble/)。这是第一个适用于任何三星设备的 Android 8.0 稳定版本，它带来了大量的新功能和改进。除了 Android Oreo 带来的所有新功能，如[画中画模式](https://www.xda-developers.com/picture-in-picture-mode-desktop-google-chrome/)、[通知频道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)、[后台应用优化](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)、通知休眠等，还有大量针对三星的变化[三星体验 9.0](https://www.xda-developers.com/samsung-experience-9-0-beta-android-oreo-features/) 。

例如，有内置贴纸和 gif 的新键盘，三星 Galaxy Note8 的[应用对功能](https://www.xda-developers.com/galaxy-note-8-software-spen-apps/)(三星 Galaxy note 8 的[尚未收到自己的官方奥利奥发布](https://www.xda-developers.com/samsung-galaxy-s8-note8-android-oreo-february-security-patches/)，等等。该版本带有最新的[二月安全补丁](https://www.xda-developers.com/february-android-pixel-security-bulletins-factory-images-otas/)，因此您可以放心，您的手机已经针对所有已知的主要安全漏洞进行了修补，包括 [BlueBorne](https://www.xda-developers.com/bluetooth-vulnerability-blueborne-impacts-android-ios-windows-and-linux-devices/) 、 [KRACK](https://www.xda-developers.com/wpa2-wifi-protocol-vulnerability-krack/) 和 [Spectre/Meltdown](https://www.xda-developers.com/android-security-bulletin-january-2018-ota-factory-images/) 。最后，对于我们论坛的成员来说，你也应该知道这次更新包括了对 OMS 的原生支持，这是底层背后的主题引擎。以前，你必须使用 [Sungstratum 插件](https://www.xda-developers.com/sungstratum-samsung-substratum-touchwiz/)来应用漂亮的主题，但是有了 OMS 主题支持应该比以前稳定多了。

听起来不错吧？想要立即在您的三星 Galaxy S8 或 Galaxy S8+ Exynos 机型上安装更新吗？如果是这样，那么你很幸运。我们论坛中的一些成员能够获得更新，允许您通过库存恢复来安装它。以下是如何为您的 Exynos Galaxy S8/S8+安装官方 Android Oreo 更新的说明和链接！如果你担心安全，如果这个版本是合法的，那么不要担心，因为股票恢复不能够安装非官方的 OTA 更新，以保证这些版本是真实的！

这一更新可能会在未来几天甚至几周内推出，因此遵循本教程将确保您可以立即将您的设备升级到最新的 Android 8.0 Oreo 版本。本教程将适用于除韩国和 Duos Exynos 用户之外的几乎所有 Exynos Galaxy S8 和 Galaxy S8+设备。

**一句警告**:如果你的手机目前运行的是安卓牛轧糖，那么这个应该会很顺利。然而，如果你的手机运行的是 Android Oreo 测试版，那么按照这种方法将需要恢复出厂设置/数据擦除。我们建议无论如何都要备份重要数据。

* * *

## 如何用奥丁更新:

1.检查你的手机型号，看看它是 G950F (Galaxy S8 Exynos)还是 G955F (Galaxy S8+ Exynos)。这些模型是唯一一个可以闪现奥利奥产品的模型。如果您没有这两种型号，**不要继续**。

2.如果你有 G950F，那么下载这个文件: [CRB7 Odin](https://mega.nz/#!CZdSkLrA!_hF6bamESDj-bOl5yla0rOOMNti5ydYJM3e5Bbr_rgo) 。如果你有 G955F 型号，那么下载这些文件: [CRB7 Odin](https://androidfilehost.com/?fid=890129502657584963) 。

3.提取之前链接的 Odin 固件。这将是一个压缩格式。

4.关闭设备电源，然后按住 **Bixby 按钮+音量降低+电源**，重新启动设备进入下载模式。

5.下载 [Odin](https://forum.xda-developers.com/attachment.php?attachmentid=4431749&d=1519672710) 工具，将手机插上电脑。Odin 是三星的**官方工具，可以将三星官方固件刷新到三星 Galaxy 设备上。在右边的奥丁中，你会看到 5 个部分，但是其中只有 4 个会被使用。**

6.单击 BL 按钮并导航到您提取文件的 Odin 固件文件夹，然后单击以 BL 开头的文件。对 AP、CP 和 HOME_CSC 执行相同的操作(不要使用 CSC_XXX，它会删除您的数据)

7.点击奥丁底部的**开始**。

8.享受安卓奥利奥！

* * *

就是这样！现在你的 Exynos Galaxy S8/S8+机型应该运行的是 Android Oreo 官方发布的版本！你甚至不用等！你的设备将来可以接受官方 OTA 更新，KNOX 也不会受到影响。尽情享受吧！