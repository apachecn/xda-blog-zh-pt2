# Google Camera mod 支持在 Razer Phone/2、Moto X4 和其他手机上使用辅助镜头

> 原文：<https://www.xda-developers.com/google-camera-mod-telephoto-lens-razer-phone-2-moto-x4/>

Google Camera mod 可能是近年来 Android 中自定义开发的最佳壮举之一。在许多手机上，它甚至不需要 root，但它允许你在智能手机上使用谷歌像素的相机处理功能，并拥有谷歌的一些最佳功能，如[夜视](https://www.xda-developers.com/google-camera-night-sight-xiaomi-poco-f1-mi-8/)。有一些不利因素，但没有一个会被认为是真正的交易破坏者。其中一个缺点是，由于谷歌 Pixel 智能手机没有第二个传感器，谷歌相机端口不能在 Razer Phone 2 或摩托罗拉 Moto X4 等受支持的智能手机上使用第二个相机镜头是有道理的。多亏了乌克兰开发人员 B-S-G 和另一位名叫 Alexander Deev 的开发人员的努力工作，这种情况将会改变。

[**雷蛇手机 2 XDA 论坛**](https://forum.xda-developers.com/razer-phone-2) [**Moto X4 XDA 论坛**](https://forum.xda-developers.com/moto-x4)

Alexander Deev 的发现使 B-S-G 能够启用第二个传感器，这是一个名为“vendor.camera.aux.packagelist”的系统属性。该属性包含一个应用包名称列表，该列表由系统列入白名单，以利用辅助后置摄像头，高通 Snap 相机就在该列表中。B-S-G 将其相机应用的包名重命名为“org.codeaurora.snapcam ”,以便将其列入白名单。然后，他修改了谷歌相机应用程序，允许用户在后置摄像头、长焦镜头和前置摄像头之间切换。我在我的 Razer Phone 2 上测试了这一点，你可以在下面看到它的工作原理。

[**下载最新版本的谷歌相机 mod**](https://www.androidfilehost.com/?fid=11410963190603879069)

长焦镜头对许多人来说并没有太大的用处，但它表明，尽管谷歌相机端口已经是一项惊人的成就，但至少可以进一步改进。特别是 Razer Phone 2，Google Camera mod 将相机从普通的[变成了一个真正像样的射手](https://www.xda-developers.com/google-camera-port-razer-phone-2/)。当你第一次下载并安装这个应用程序时，你需要启用 B-S-G Mod 设置下的“给相机开关添加辅助”选项。你可以看看下面是什么样的。

一旦你启用，重启应用程序，并尝试在前后摄像头之间切换！如果你想跟上谷歌相机应用的最新发展，一定要看看我们下面的论坛。

[**谷歌相机 mods XDA 论坛**](https://forum.xda-developers.com/apps/google-camera-mods)