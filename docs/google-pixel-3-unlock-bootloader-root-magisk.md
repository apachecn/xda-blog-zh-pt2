# 用 Magisk 解锁 Bootloader 和 Root 谷歌 Pixel 3

> 原文：<https://www.xda-developers.com/google-pixel-3-unlock-bootloader-root-magisk/>

像谷歌 Nexus 系列一样，谷歌 Pixel 智能手机是最容易解锁引导加载程序、root 以及安装定制 rom 和内核的设备之一。2018 款谷歌 Pixel 3 和谷歌 Pixel 3 XL 将不会有什么不同。事实上，由于流行的无系统根工具 Magisk 的最新更新，Pixel 3 和 Pixel 3 XL 已经可以根了。他发布了 Magisk 的 17.3 版本，你可以在这里阅读发行说明[。解锁 Pixel 3 系列的引导加载程序需要几秒钟，启动并运行 Magisk 需要几分钟。如果你曾经解锁过谷歌 Nexus、谷歌 Pixel 或一加设备的引导程序，那么解锁 Pixel 3 和安装 Magisk 应该不会有任何问题。对于那些需要复习的人，这里有一个教程来指导你完成这个过程。](https://forum.xda-developers.com/showpost.php?p=77933549&postcount=47)

*特别感谢 XDA 认可开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) ，Magisk 的首席开发者，感谢他所做的一切工作。没有他，这是不可能的。请考虑在《T4》中支持他。[在 Twitter 上关注他](https://twitter.com/topjohnwu)，了解他即将推出的作品的预告。*

## 第 1 部分-解锁谷歌像素 3 的引导加载程序

**注意:解锁引导程序将会清除你设备上的所有数据。这包括保存到设备内部存储器的所有媒体，如图片、视频、音乐、文档等。在继续之前，请将所有重要文件备份到您的电脑或云存储中。**

1.  打开**设置** app。
2.  进入**系统**。
3.  点击**关于电话**。
4.  向下滚动并点击 7 次直到它显示你现在是一名开发者。
5.  返回上一页，在列表底部附近，您应该看到“**开发者选项**”
6.  无需向下滚动，您应该会看到一个“ **OEM 解锁**选项。启用它。为了安全起见，它可能会要求您输入您的锁屏 PIN/密码(如果您有一套的话)。
7.  向下滚动一点，直到看到“ **USB 调试**”启用它。
8.  将 Pixel 3 插入电脑。按照这些步骤在你的电脑上设置 **ADB 和快速启动**。如果你只有 Chromebook，你可以按照[这个指南](https://www.xda-developers.com/adb-fastboot-chromebook-chrome-os/)在 Chrome OS 上设置 ADB 和 Fastboot。
9.  确保您的 PC 能够识别您的 Pixel 3，方法是在保存 ADB 和 Fastboot 二进制文件的同一目录中打开命令提示符/Power Shell/Terminal，并根据您的操作系统输入以下命令: **Windows 命令提示符:**

    ```
     adb devices 
    ```

    **Windows Power Shell:**

    ```
     .\adb devices 
    ```

    **MAC OS/Linux Terminal:**

    ```
     ./adb devices 
    ```

    (对于本教程的其余部分，请根据您的操作系统使用相同的命令前缀。)如果您看到您的设备的序列号并显示“已授权”，那么您就可以使用了。如果这是您第一次为该设备设置 ADB，那么您可能会在您的手机上看到提示，以便为您的 PC 启用 USB 调试。授予它许可。如果你无法让你的 Windows 电脑识别你的设备，尝试安装最新的[谷歌 USB 驱动](https://developer.android.com/studio/run/win-usb)。
10.  现在，**重启到引导程序**菜单。您可以在启动时按住电源和音量降低按钮，或者输入以下 ADB 命令:

    ```
     adb reboot bootloader 
    ```

11.  一旦你在引导菜单上，你现在必须切换到使用快速启动命令与你的设备通信。要**解锁 Pixel 3 的引导程序**，输入以下命令:

    ```
     fastboot flashing unlock 
    ```

12.  现在，您应该会在屏幕上看到文本，警告您解锁引导程序的潜在风险。在电源和音量按钮旁边的屏幕上，您应该会看到一些文本。**按下音量增大键**，直到它显示“解锁引导程序”一旦它这样说，**按下电源按钮**。
13.  手机将解锁引导加载程序，并重新启动回到引导加载程序菜单。这一次，引导程序将显示一个红色警告图标和“解锁”文本。
14.  现在，**重启**你的手机回到 Android 9 Pie 操作系统。您可以通过发送下面的 fastboot 命令来做到这一点:

    ```
     fastboot reboot 
    ```

15.  恭喜你，你的谷歌 Pixel 3 或谷歌 Pixel 3 XL 现在有一个解锁的引导加载程序了！你会看到一条警告信息，提示你的手机引导程序在每次启动时都被解锁，但是不要担心，因为这不会影响你的日常使用。

## 第 2 部分——用 Magisk 开发 Google Pixel 3

使用解锁的引导加载程序，您现在可以引导修改后的引导映像。为了让 Magisk 工作，你需要修补 Pixel 3 的启动映像。最简单的方法是在您的设备上安装一个像 TWRP 这样的自定义恢复程序，这样您就可以使用 Magisk 安装程序脚本。

1.  由于你的设备已经被清除，你需要返回并重新启用开发者选项，然后**重新启用 USB 调试**。确保您的电脑仍能识别您的 Pixel 3。
2.  下载 TWRP 图片(。img 文件),并将该文件保存到您电脑上 ADB 和 fastboot 二进制文件所在的同一目录下。
    1.  [下载谷歌 Pixel 3(“蓝线”)TWRP 图片](https://dl.twrp.me/blueline/)。
    2.  下载谷歌像素 3 XL(“交叉线”)TWRP 图像。
3.  下载最新的 Magisk 安装程序 zip。zip 文件)并将其保存到 Pixel 3 或 Pixel 3 XL 上的下载文件夹中。
4.  *(可选)*从上面的 TWRP 页面下载 TWRP 安装程序脚本。zip 文件)，如果你想安装 TWRP，而不是每次从引导加载程序启动。将其保存到 Pixel 3 或 Pixel 3 XL 上的下载文件夹中。
5.  重新引导至引导程序菜单。
6.  在 bootloader 屏幕上，输入下面的 fastboot 命令来**临时引导**TWRP 补丁的引导镜像:

    ```
     fastboot boot <insert_name_of_TWRP_image_here>.img 
    ```

7.  几秒钟后，您的手机应该退出引导程序菜单，并重新启动 TWRP 恢复。
8.  点击安装。
9.  *(可选)*如果你想安装 TWRP，这样你就不用每次都“快速启动”了，按照以下步骤操作:
    1.  找到保存在下载文件夹中的 TWRP 安装程序脚本。
    2.  点击它，并使用滑块安装它。
    3.  重新启动操作系统，让它一直启动。
    4.  重新启动引导程序。
    5.  使用音量键滚动，直到您看到“恢复”按下电源按钮，现在启动回到 TWRP。
10.  找到保存在下载文件夹中的 Magisk 安装程序脚本。点击它，并使用滑块安装它。
11.  现在，重新启动回到操作系统，打开 Magisk Manager 检查您的根目录的状态。

## 第 3 部分-我现在做什么？

使用 Magisk 后，您可以使用 Pixel 3 或 Pixel 3 XL 做哪些事情？以下是我想出来的一个简短清单:

*   安装**活动边缘模块**以完全[定制 Pixel 3 上的挤压手势](https://www.xda-developers.com/customize-google-pixel-2-active-edge-sense-plus/)。(注意:这个还没有更新到支持 Pixel 3，但是开发者正在努力！)
*   通过[底层主题引擎](https://www.xda-developers.com/custom-themes-android-p-root-substratum/)为系统应用或第三方应用安装**自定义主题**。类似地，你可以使用像 Pluvius 这样的应用程序，根据当前的壁纸动态地为你的系统设置主题。
*   使用 Titanium Backup 制作**完整的 app 备份**。
*   重新启用**通话录音**因为安卓派[把它拿走了](https://www.xda-developers.com/android-pie-blocks-non-root-call-recording-apps/)给非 took 用户。
*   想念安卓牛轧糖的 **blob 表情符号**？你可以用 [Blobmoji](https://forum.xda-developers.com/apps/magisk/module-notocoloremoji-blob-patch-t3677992/page4) Magisk 模块把它们拿回来。
*   Magisk 模块报告中有大量的音频模块。查看它们以获得更好的音乐播放体验！
*   喜欢股票 Gboard 键盘 app？看看这些 **Gboard 主题**。
*   谷歌应用和服务的忠实粉丝？有了 root，你可以在面向公众推出之前启用许多正在开发的功能。查看[我们的教程](https://www.xda-developers.com/category/tutorials/)中的大量例子。
*   不是谷歌 Pixel Launcher 的粉丝？你可以使用像 Lawnchair 一样的第三方启动器，但是使用 root，你可以[将其集成到最近的应用概述](https://www.xda-developers.com/lawnchair-android-pie-recent-apps-integration-root/)和手势导航中。
*   定制默认的**系统媒体、字体、启动动画**等，为您的软件增添一点趣味。
*   获取 YouTube advanced——Android 版 YouTube 应用程序的增强版本。
*   如果你喜欢更强烈的颜色，我们制作的这个应用程序可以让你定制显示的饱和度**。**

 **你可能听说过解锁引导加载程序并用 Magisk 启动你的设备意味着你将无法玩某些游戏，如 [Pokémon Go 和 Fate/Grand Order](https://www.xda-developers.com/fate-grand-order-fortnite-mobile-magisk/) 或使用银行应用程序。然而，有一些像 MagiskHide 这样的功能可以隐藏你的设备被修改的事实，这样你就可以继续使用你最喜欢的应用和游戏了！解锁引导程序*会*影响你更新的方式。你需要学习如何[下载每月安全补丁更新](https://www.xda-developers.com/flash-monthly-security-update-google-pixel/)，这实际上很容易做到。

最后，如果你想对你的设备有更多的控制，你可以在你的 Pixel 3 上闪存定制的 rom 和内核，一旦它们可供这两个设备使用。定制 rom 可以提供许多股票软件上没有的选项。自定义内核允许您调整设备的性能，以延长电池寿命或在您最喜爱的游戏中获得更多帧数。由于谷歌 Pixel 3 和 Pixel 3 XL 刚刚在[发布](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-specs-features-pricing-availability/)，目前还没有任何定制的 rom 或内核可供该设备使用。但是，如果您对定制开发感兴趣，请关注这两种设备的 XDA 论坛。

[**加入谷歌 Pixel 3 论坛**](https://forum.xda-developers.com/pixel-3)

[**加入谷歌 Pixel 3 XL 论坛**](https://forum.xda-developers.com/pixel-3-xl)

最后，由于 Pixel 3 和 Pixel 3 XL 支持 [A/B 双分区以实现无缝更新](https://www.xda-developers.com/list-android-devices-seamless-updates/)，如果这是你第一次使用 A/B 设备，你应该阅读一下[对修改](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)的影响。**