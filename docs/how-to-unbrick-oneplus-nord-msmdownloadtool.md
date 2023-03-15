# 以下是如何用 MSMDownloadTool 解除一加诺德的锁定

> 原文：<https://www.xda-developers.com/how-to-unbrick-oneplus-nord-msmdownloadtool/>

一加手机以其可攻击性而闻名，新发布的一加诺德手机当然也不例外。经典的中型游侠已经[收到了](https://www.xda-developers.com/unofficial-pixel-experience-and-twrp-are-already-available-for-the-new-oneplus-nord/)一个有点工作的 TWRP 版本以及一个非官方的 Pixel Experience ROM 版本，因此我们非常有信心会有更多的版本。然而，有时你可能会在摆弄你闪亮的新一加诺德时遇到“砖头”，在这种情况下，你甚至不能访问快速启动界面来恢复股票固件。虽然在这种情况下，您可以联系一加支持人员，让他们在您的设备上远程执行低级闪存，但我们经验丰富的一加情报人员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 已经成功获取了适用于该设备的 unbrick 软件包，以便您可以独自恢复您的砖砌一加诺德。

**[一加诺德 XDA 论坛](https://forum.xda-developers.com/oneplus-nord)**

**[一加诺德点评:性价比超高](https://www.xda-developers.com/oneplus-nord-review/)**

该工具被称为“MsmDownloadTool”，它利用高通的**E**emergency**D**own**l**oad 模式(EDL)来完成刷新任务。你需要一台运行微软 Windows 7 或更新版本的电脑才能使用这个闪光器，因为它与 Linux 和 macOS 不兼容。你还需要一个兼容的高通驱动程序，可以直接从微软的更新服务器下载。

如果你的一加诺德已经被阻止，连接设备到你的电脑上的 USB 端口应该在设备管理器下显示为“QDLOADER 9008”(或者“QHUSB_BULK”，如果驱动程序没有正确安装)。最终用户也可以手动触发一加诺德上的 EDL 模式，如果你想降级其中已安装的 OxygenOS 版本，这是特别有用的。你所需要做的就是关掉 Nord，然后按住音量增大和音量减小按钮，将手机插入你的电脑。

请记住，一加北部有 3 种不同的区域变体:印度(AC01DA)、全球(AC01AA)和欧洲(AC01BA)。你需要为你的模型选择正确的 EDL 闪光器，尽管交叉闪光是非常可能的。在尝试这种交叉闪存之前，请创建“持久”分区的备份，以避免指纹注册问题。

**[一加诺德——XDA 螺纹的 MsmDownloadTool](https://forum.xda-developers.com/oneplus-nord/how-to/opnord-unbrick-tool-to-restore-device-t4148415)**

请注意，目前发现的一加北部 EDL 闪光器基于 [OxygenOS 10.5.2](https://www.xda-developers.com/oxygenos-10-5-2-for-the-oneplus-nord-adds-oneplus-buds-support/) ，而不是最新的 [OxygenOS 10.5.4](https://www.xda-developers.com/oneplus-nord-oxygenos-10-5-4-enhances-low-light-selfie-macro-camera-photos/) 。一旦您有了与您的变体相对应的正确闪光器，请按照以下步骤进行解锁:

*   启动 MsmDownloadTool V4.0.exe。
*   在登录提示上，从下拉菜单中选择“其他”，然后单击“下一步”。
*   等待几秒钟，直到主窗口出现。
*   点击目标按钮，使用全球工具时选择 O2，使用印度工具时选择印度，使用欧洲工具时选择欧盟。
*   按下开始按钮(这样做是为了让工具自动“捕获”设备，而不是在 10 秒钟后返回正常启动)
*   当手机处于高通 EDL 模式时，用普通的一加线把它插到你的电脑上。
*   等~300 秒。

就是这样！手机会自动重启进入你刚刚恢复的氧气系统。