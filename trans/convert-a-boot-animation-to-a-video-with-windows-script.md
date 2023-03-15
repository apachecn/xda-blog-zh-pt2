# 使用 Windows 脚本将启动动画转换为视频

> 原文：<https://www.xda-developers.com/convert-a-boot-animation-to-a-video-with-windows-script/>

开机动画是用户打开手机或平板电脑后看到的第一个东西。ROM 的这个介绍部分非常重要，直接影响我们对该 ROM 的体验。为此，Android 将 PNG 文件和一个 *desc.txt* 打包成一个 zip 文件。该文本文件包含分辨率和帧速率信息，以便引导动画以正确的大小和所需的速度显示。

制作开机动画的公开预览并不像听起来那么简单。用带摄像机的设备录像看起来肯定不专业，视频质量也有待提高。如果你曾经计划制作一个开机动画的视频，你绝对应该尝试一下 XDA 论坛成员 [makers_mark](http://forum.xda-developers.com/member.php?u=5448769) 编写的 Windows 专用工具。批处理脚本使用 ADB 从设备中下载启动动画。然后，它将 bootanimation 转换为 MP4 文件，准备上传到 YouTube 或类似的视频交付服务。该脚本使用诸如 7zip 这样的工具来解压归档文件，并使用 FFmpeg 将这些文件转换成视频。这个过程在线程中有详细的描述，并解释了引导动画中的特殊元素。

该工具只在 Windows 机器上运行，可以从[原线程](http://forum.xda-developers.com/showthread.php?p=50503915)下载。