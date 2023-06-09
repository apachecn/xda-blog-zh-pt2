# 索尼的开放设备计划发布了一个更新的指南，用于解锁 Xperia 设备的引导加载程序

> 原文：<https://www.xda-developers.com/sonys-open-device-program-releases-an-updated-guide-for-unlocking-bootloader-of-the-xperia-devices/>

在为社区发展提供支持和为用户提供真正拥有自己设备的工具方面，索尼是最好的原始设备制造商之一。开放设备计划为有兴趣为 Xperia 系列设备开发 AOSP 版本和定制软件的开发人员提供了有用的资源和指南。您可能已经知道，为了安装定制软件或对原始软件进行任何系统级更改，必须解锁设备的引导加载程序。

也就是说，索尼的开放设备项目发布了一个关于如何解锁 Xperia 设备引导程序的更新方法。为了解锁 Xperia 设备的引导加载程序，您需要生成一个唯一的代码，在解锁过程中您需要输入该代码。请求唯一代码的过程非常简单；点击这里进入官方页面[，从支持的设备列表中选择你的 Xperia 设备，然后点击继续。](http://developer.sonymobile.com/unlockbootloader/)

接下来，您将被要求提供一个有效的电子邮件地址；只需输入您的电子邮件地址，接受条款和条件，并点击提交按钮，即可收到确认链接。按照电子邮件中的链接，它会将您带到需要输入 IMEI 代码以生成唯一代码的页面。提交 IMEI 代码后，您将通过电子邮件收到您的唯一代码。

收到代码后，剩下的过程非常简单，因为你以前有解锁引导程序的经验。你需要在你的电脑上下载 Android SDK，以防你还没有安装它；或者，您也可以选择只下载 ADB/fastboot 二进制文件，因为下载整个 SDK 可能是一项繁琐的任务。

现在，在快速启动模式下将 Xperia 设备连接到 PC，并打开命令提示符窗口。导航到平台-工具文件夹并输入`fastboot devices` -如果它在重新运行中列出了您的设备 ID，您可以继续操作。现在，只需复制并粘贴命令与解锁代码，你收到索尼早些时候到命令窗口，并按下回车键。就这样，你的设备现在应该有一个解锁的引导程序了！

关于解锁 bootloader 的分步说明，你也可以查看下面的官方视频。

* * *

[button link = http://Developer . sonymobile . com/2017/02/10/updated-video-how-to-unlock-the-boot-loader-of-an-xperia-device/Icon = " Select a Icon " side = " left " target = " " color = " f 85050 " text color = " ffffff "]来源:索尼开发者博客[/button]