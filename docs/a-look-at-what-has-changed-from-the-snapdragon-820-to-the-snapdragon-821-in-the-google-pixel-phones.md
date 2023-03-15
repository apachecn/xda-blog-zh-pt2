# 看看谷歌 Pixel 手机从 Snapdragon 820 到骁龙 821 有什么变化

> 原文：<https://www.xda-developers.com/a-look-at-what-has-changed-from-the-snapdragon-820-to-the-snapdragon-821-in-the-google-pixel-phones/>

我们来到高通，以便更好地了解即将亮相的骁龙 821 处理器 [【谷歌像素](http://forum.xda-developers.com/pixel)[像素 XL](http://forum.xda-developers.com/pixel-xl)[华硕 ZenFone 3 豪华版](http://forum.xda-developers.com/zenfone-3-deluxe)[小米 Mi 5s](http://forum.xda-developers.com/mi-5s) 以及 [由于 Pixel 手机中的骁龙 821 与常规 Snapdragon 820 的时钟速度相同，许多人都在问新 SoC 带来了什么好处，如果他们不打算使用它可以带来的更高时钟速度，为什么要选择它。](http://forum.xda-developers.com/le-pro3)

[![Google Pixel Press Image Vertical Very Silver](img/629acddcc9e1750404d55e268de4cf44.png)](http://static1.xdaimages.com/wordpress/wp-content/uploads/2016/10/Google-Pixel-Press-Image-Vertical-Very-Silver.png) 当 Android 平台的性能负责人提到谷歌的 [ 没有欠频 ](https://twitter.com/t_murray/status/783345275096199168) 骁龙 821(与普遍的看法相反)时，我们的兴趣被激起了，因此暗示他们使用的版本在默认情况下与 Snapdragon 820 的主版本以相同的速度运行。

简而言之，骁龙 821 的设计与 820 相比并没有太大的变化，但我们在这个过程中有了一些有趣的发现。骁龙 821 是类似于骁龙 801 和 800 的修订版，主要是通过提高产量实现的。

这些产量的提高使得高通发布了骁龙 82x 的基本修订版，它可以在与原始版本相同的时钟速度下减少 5%的功耗，或者在大约与 820 相同的功耗下调整为略高的时钟速度。这是紧跟 Snapdragon 800 和骁龙 801 的脚步，产量的提高使高通能够在正常开发周期的中途发布 800 的稍微改进版本。

高通告诉我们，骁龙 821 确实有两个版本。一个运行在宣传的最大 CPU 和 GPU 时钟速度 2.34 GHz 和 653 MHz(分别)，另一个运行在主 Snapdragon 820 中相同的 2.15 GHz 和 624 MHz。Pixel 手机使用的是后者，我们被告知这款手机名为 MSM8996 Pro-AB。虽然我们尚未能够获得关于更高时钟型号名称的确认，但如果它与 Snapdragon 800 和 801 芯片采用相同的型号，它可能是 MSM8996 Pro-AA 或 MSM8996 Pro-AC。

需要注意的一点是，尽管有相反的传言，谷歌没有选择骁龙 821 是因为骁龙 VR SDK。虽然绝对是一个很好的工具，但它在 Snapdragon 820 和 821 上都可以工作，并且不是这两种芯片之间的区别特征。



随着谷歌大力推动 Pixel 手机摄像头的改进，我们认为可能会有一些图像信号处理器的改进，乍一看似乎是有的，Snapdragon 820 被列为能够处理 30 Hz 的 25 MP 图像，骁龙 821 被列为能够处理 30 Hz 的 28 MP 图像；但这被证明是一个打印错误，已经被纠正了。两个 SOC 中的高通频谱 ISP 能够在 30 Hz 下处理相同的 28 MP。

相反，谷歌通过使用 [高通的六边形矢量扩展](https://developer.qualcomm.com/blog/high-res-image-processing-low-power-consumption-qualcomm-hexagon-vector-extensions-vx) ，找到了更好地利用高通的六边形 DSP 的方法，从而寻求提高他们的 HDR+处理速度。谷歌正在将 HDR+的大部分处理工作卸载到 Hexagon DSP，该 DSP 过去由 CPU 本身处理，在减少处理 HDR+照片所需的时间以及允许 Pixel 手机继续拍摄 HDR+照片方面发挥了重要作用，DXOMark 发现它可以无限期地每三秒钟拍摄一张 HDR+照片。这与 [索尼 Exmor RS IMX378](http://www.xda-developers.com/sony-imx378-comprehensive-breakdown-of-the-google-pixels-sensor-and-its-features/) 图像传感器带来的更快拍摄能力完美结合，打造出一款出色的相机。

虽然与处理器本身没有直接关系，但谷歌提到他们已经投入大量工作来帮助改进 Pixel 手机中的调度程序，这是一个了不起的消息，因为调度程序是用 [约翰·普尔](http://www.xda-developers.com/geekbench-ceo-fireside-chat-pt-3/) ， *“极其复杂的代码片段”* 的话说的，小的改进可以对现实世界的性能产生重大影响。

总的来说，骁龙 821 应该是一个坚实的修订，但如果你想在性能上有一个大的飞跃，你必须再等几个月才能看到真正的下一代芯片开始出现在明年的旗舰手机中(传言中的 Snapdragon 830)。虽然还没有透露太多关于下一代 Snapdragon 800 系列芯片的信息，但高通刚刚宣布将使用他们新的 [X16 LTE 调制解调器](http://www.xda-developers.com/qualcomm-announces-x16-and-x50-modems-for-next-generation-snapdragon-8xx-devices-and-5g-connectivity/)。新的调制解调器尤其令人感兴趣，因为它将带来一些实质性的改进，如 LTE 双卡双活、16 和 13 类下行链路和上行链路、多载波 4x4 MIMO、4x20 载波聚合以及 1 Gbps 的理论峰值下载速度。

你觉得骁龙 821 怎么样？你对它在 Pixel 手机中的使用感到兴奋吗，或者你更期待明年的 Snapdragon 830 和 X16 LTE 调制解调器旗舰产品？