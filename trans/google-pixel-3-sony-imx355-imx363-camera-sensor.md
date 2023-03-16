# 谷歌 Pixel 3 的前置摄像头采用了新的索尼摄像头传感器

> 原文：<https://www.xda-developers.com/google-pixel-3-sony-imx355-imx363-camera-sensor/>

尽管索尼的移动部门[没有卖出那么多智能手机](https://www.xda-developers.com/sonys-mobile-communications-division-reports-21-9m-loss-as-sales-decline-in-q2-fy2017/)，但索尼的成像部门已经[大获成功](https://www.xda-developers.com/sonys-imx586-48mp-smartphone-camera/)。索尼的 Exmor 系列相机传感器广泛应用于智能手机行业。你很难找到一部没有摄像头的安卓智能手机——至少在拍照性能出色的智能手机中。虽然图像传感器本身并不能决定智能手机相机的好坏，但知道传感器确实可以告诉我们关于智能手机相机功能的相当多的信息。

例如，只有少数智能手机能够以 960fps 的速度录制慢动作视频。像[索尼 Xperia XZ2](https://www.xda-developers.com/sony-xperia-xz2-review/) 、三星 Galaxy S9/ [Galaxy Note 9](https://www.xda-developers.com/samsung-galaxy-note-9-specs-pricing-availability-features/) 和[华为 P20 Pro](https://www.xda-developers.com/huawei-p20-pro-update-960fps-slow-motion/) 这样的设备都能够以这种帧速率录制短视频。三星 Galaxy S9 能够录制 960fps 的视频，这要归功于索尼 IMX345 相机模块中的 DRAM 芯片，这就是为什么 [Galaxy S8](https://www.xda-developers.com/samsung-galaxy-s8-super-slow-motion-ar-emoji/) 和 [Galaxy Note 8](https://www.xda-developers.com/samsung-galaxy-note-8-super-slow-motion-ar-emojis/) 上的超级慢动作功能仅支持 480fps。在 Galaxy S9/Note 9 上，相机传感器将帧写入 DRAM，然后将帧传递到图像缓冲区，最后传递到存储器，这在以 960fps 拍摄时是必要的。Pixel 2 和 Pixel 3 中的摄像头传感器无法实现这一壮举，这就是为什么这两款设备的慢动作都被限制在 240fps。说到 Pixel 系列相机传感器，下面是我们对 Pixel 2 和 Pixel 3 上的相机的了解。

### 像素 2 摄像头

谷歌 Pixel 2 的单一后置摄像头传感器是索尼 IMX362，HTC U11、Moto G5 Plus、华硕 Zenfone 4 系列等也有这种传感器。相比之下，第一代 Pixel 拥有索尼 IMX 378。Pixel 2 的单一前置摄像头传感器是索尼 IMX179，与 Nexus 6P 和第一代谷歌 Pixel 上的传感器相同。尽管使用了相机硬件，但谷歌 Pixel 2 被广泛认为是市场上最好的智能手机相机(当然，直到谷歌 Pixel 3。)这要归功于谷歌图像工程师为优化谷歌相机应用所做的令人难以置信的工作。然而，我们能从今年的模型中期待什么呢？

### 像素 3 相机

谷歌 Pixel 3 在索尼 IMX363 中有一个稍微升级的后置摄像头，在小米 POCO F1、华硕 ZenFone 5Z 和其他产品中也有。Pixel 3 的前置摄像头比去年的型号有了重大改进，索尼 IMX355 增加了一个辅助广角镜头。(这实际上是在[谷歌像素板](https://www.xda-developers.com/google-pixel-slate-detachable-chrome-os-tablet/)中使用的[相同的前置摄像头传感器](https://www.xda-developers.com/unreleased-sony-camera-sensors-chrome-os-devices/)，现在看来这是显而易见的，但我没有看到任何人真正指出这一点。)不幸的是，索尼没有公布这两种相机传感器的数据表，所以除了带传感器的设备的规格表中显示的内容之外，我们不知道它们的全部功能。以下是谷歌官方对 Pixel 3 摄像头的说法:

*   后置摄像头(索尼 IMX363)
    *   1220 万像素双像素
    *   1.4μm
    *   双像素相位检测自动对焦
    *   光学+电子稳像
    *   光谱+闪烁传感器
    *   f/1.8 光圈
    *   视野:76°
    *   显像记录
        *   1080p @ 30fps，60fps，120fps，自动
        *   720p @ 30fps，60fps，240fps，自动
        *   4K @ 30fps
*   前置摄像头(索尼 IMX355)
    *   广角的
        *   800 万像素
        *   f/2.2 光圈
        *   视野:97°
        *   固定焦距
    *   常态
        *   800 万像素
        *   f/1.8 光圈
        *   视野:75°
        *   带相位检测的自动对焦
    *   显像记录
        *   1080p@30fps
        *   720p@30fps
        *   480p@30fps

### 4K@60fps 怎么了？

由于首次披露谷歌 Pixel 3 将不支持 60fps 的 4k 视频录制，一些用户猜测缺乏该功能是因为后置摄像头传感器。毕竟，高通骁龙 845 的 ISP 能够以 60fps 的速度处理 4k 视频。去年的谷歌 Pixel 2 拥有[高通骁龙 835](https://www.qualcomm.com/products/snapdragon/processors/835) ，因此，它无法支持 60fps 的 4k 视频录制。索尼 IMX363 有几款设备不支持 60fps 的 4k 视频，但也有几款支持:华硕 ZenFone 5Z 和 [Razer Phone 2](https://www.xda-developers.com/razer-phone-2-is-here-with-snapdragon-845-chroma-lighting-wireless-charging-and-huge-speakers/) 支持 4K@60fps，而小米 Poco F1 将在未来的[更新](https://twitter.com/jaimani/status/1045236513099796480?s=19)中支持它。因此，仍然不清楚为什么谷歌没有这个选项。也许是为了节省空间，因为谷歌提供了[免费无限的谷歌照片存储](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-specs-features-pricing-availability/)，或者也许谷歌的[融合视频稳定](https://www.xda-developers.com/google-explains-the-fused-video-stabilization-technique-used-in-the-pixel-2/)无法处理 4k@60fps(这是由著名的相机调制师 [defcomg](https://forum.xda-developers.com/member.php?u=377973) 提出的理论)，或者也许其他新的相机功能之一无法处理 4k@60fps。