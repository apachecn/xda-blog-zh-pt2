# 如何将视频设置为启动动画

> 原文：<https://www.xda-developers.com/set-video-boot-animation/>

# 如何将视频设置为启动动画

本指南解释了将视频文件设置为启动动画需要做的事情。

如果你想让你的手机真正独一无二，你可以考虑添加一个漂亮的开机动画。引导动画只不过是一组 PNG 文件，当操作系统加载时，这些文件以所需的帧速率一个接一个地播放。各种 OEM 厂商把自己的动画，并经常在启动过程中添加声音，使他们的设备更酷。

将一个视频分割成这么多单个文件会降低流畅性，因为设备必须处理每个文件。来自摩托罗拉的家伙决定改变这种行为，并编译了一个新的 bootanimation 二进制文件，在启动过程中使用 MP4 视频文件。XDA 资深会员 [devilex94](http://forum.xda-developers.com/member.php?u=4271299) 注意到了这一点，并为 [XDA 大学](http://forum.xda-developers.com/general/xda-university)写了一本有趣的指南，解释如何在运行 KitKat 的设备上使用视频引导动画。

提供的方法非常简单，需要你做三件事:启动你的设备，复制补丁的 bootanimation 二进制文件，并设置正确的权限以使其工作。在完成这三个不那么具有挑战性的任务后，你的设备就可以处理视频文件了，作为对你当前选择的 ROM 的一个很好的介绍。

视频作为开机动画无疑是一个很棒的想法。如果您有一个大的系统分区，您可以推送一些非常大的文件，使您的设备看起来独一无二。但是首先，你需要访问 [Set Video as bootanimation 论坛线程](http://forum.xda-developers.com/general/xda-university/guide-set-video-bootanimationtesters-t2915445)来了解更多信息。