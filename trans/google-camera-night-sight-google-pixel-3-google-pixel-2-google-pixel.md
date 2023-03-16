# 在 Pixel 3、Pixel 2 和 Pixel 上下载带夜视功能的谷歌相机

> 原文：<https://www.xda-developers.com/google-camera-night-sight-google-pixel-3-google-pixel-2-google-pixel/>

本月早些时候，谷歌发布了 Pixel 3 和 Pixel 3 XL。由于大量的泄露，谷歌已经没有什么可以给我们惊喜的了。然而，有一个新的谷歌相机功能在发布前没有泄露:夜视。夜视使用长曝光时间和一些谷歌软件魔法来大大增强弱光摄影。谷歌 Pixel 3 或 Pixel 3 XL 没有搭载该功能，但据说将在下个月的某个时候更新。Pixel 3 附带的谷歌相机 6.1 APK 的早期端口声称已经启用了夜视功能，但似乎该功能只是部分工作。现在，我们在一个几乎没有修改的谷歌相机应用程序中有了一个似乎更具功能性的夜视版本，该应用程序可以在谷歌 Pixel 3，谷歌 Pixel 3 XL，谷歌 Pixel 2，谷歌 Pixel 2 XL，谷歌 Pixel 和谷歌 Pixel XL 上工作。

 <picture>![Get Google Camera with Night Sight for the Google Pixel 3 and Google Pixel 2](img/da2ac63540a88090b992917f42a7319d.png)</picture> 

Apple iPhone Xs versus Google Pixel 3 with Night Sight. Source: [Google](https://www.youtube.com/watch?v=KVqt4IDdD6Y).

在谷歌 Pixel 3 发布后，谷歌相机应用程序已经有了 3 个新版本。Pixel 3 的零售单元上安装了 6.0 版本，但最终被遗忘，因为它被 6.1.009.215420794 版本所取代，后者安装在评论者的单元上，并且是当前带来[部分工作夜视和谷歌镜头建议](https://www.xda-developers.com/pixel-3-google-camera-port-night-sight-live-google-lens/)的 mod 的基础。6.1.009.215420794 版本也是几年来第一个暗示[延时功能](https://www.xda-developers.com/google-camera-6-1-time-lapse-mode/)可能真的要来了的版本。现在，版本 6.1.013.216795316 今天开始在谷歌 Play 商店推出第一代和第二代谷歌 Pixel 智能手机，它带来了[新 UI](https://www.xda-developers.com/google-camera-pixel-3-apk-download/) 。但它也是第一个带来功能性夜视功能的版本，正如 XDA 资深成员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 首次确认的那样。

[cstark27](https://forum.xda-developers.com/member.php?u=2712580) 是一名谷歌相机改装师，因其在 OnePlus 6 和 [LG 设备](https://www.xda-developers.com/google-camera-hdr-lg-v30-wide-angle-lens/)上的工作而闻名。他发现在最新的相机版本中启用夜视功能非常简单。他所做的只是将 0x0 的`Camera.enable_cuttlef`值改为 0x1(乌贼是应用程序中夜视模块的代号)。他把改装后的 APK 发给我们让我们测试，我们在 Pixel 3 XL、Pixel 3、Pixel 2 XL 和 Pixel 上进行了测试。不过，我们假设它也适用于 Pixel 2 和 Pixel XL。

## 在谷歌相机应用程序中使用夜视功能

下面是一些展示该功能如何工作的截图。当你打开相机应用程序，它检测到你处于弱光环境中，它会提示你“尝试夜间模式”你可以进入新模式，方法是进入“更多”，然后选择“夜晚”在这里，相机快门有一个月亮图标，当按下时，它会要求你在“收集光线”时保持不动在谷歌照片应用程序中，你可以通过右上角的月亮图标看到哪些照片是用夜视拍摄的。

下面是 XDA 团队捕捉到的一些快速样本镜头。我们大多数人在美国，那里不是晚上，所以我们只能在室内展示这个功能。不过，我们的一位英国作家捕捉到了他的第一代 Pixel 的前后对比。正如你所看到的，启用该模式对你在光线不好的情况下能看到多少细节有很大的影响。我们很快就把这些对比照片放在了一起，但是一旦美国进入夜间，我们会做更彻底的测试。敬请期待更好的样张，或者下载下面的改装应用程序亲自尝试！

更新:我们拍了更多的照片来展示夜景有多迷人。[在这里查看它们](https://www.xda-developers.com/google-pixel-night-sight-google-camera-review/)！

## 下载像素 3/像素 2/像素的带夜视功能的谷歌相机

注意:由于该功能将于下个月正式发布，谷歌仍有可能在内部对算法进行调整。因此，你用这个早期的谷歌相机模型得到的夜视效果可能没有下个月官方更新得到的好。

如果你想试试 cstark27 的这个应用，你可以在下面找到下载链接。它是用他的密钥而不是谷歌的密钥签名的，并且有一个不同的包名，所以它不会安装在原来的相机应用程序上。这是一个独立的应用程序，你必须从应用程序抽屉中打开它。你可以从下面的 AndroidFileHost 下载。

[**谷歌相机 6.1 Mod 带夜视功能像素，像素 2，像素 3**](https://www.androidfilehost.com/?fid=11410932744536985875)