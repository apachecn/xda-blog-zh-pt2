# 在没有谷歌浏览器的非像素设备上启用谷歌视距

> 原文：<https://www.xda-developers.com/enable-google-stadia-any-android-smartphone/>

# 如何在没有谷歌浏览器桌面模式的非像素设备上播放谷歌 Stadia 游戏[Root]

以下是如何让谷歌 Stadia 游戏流媒体在任何 Android 智能手机上运行，而不仅仅是谷歌 Pixel 设备。需要根目录。

经过[个月的等待](https://www.xda-developers.com/google-stadia-games-pricing-availability/)，谷歌的云游戏服务终于上线了。总而言之，公平地说，谷歌对 Stadia 承诺过多，交付不足。然而，尽管事实上许多功能在发布时缺失，对于许多预购的用户来说，发货和代码都被延迟了，而且[游戏没有以](https://www.eurogamer.net/articles/2019-11-25-google-issues-statement-after-stadia-owners-say-it-broke-promises-over-game-performance)承诺的 4K60 质量运行，这项服务本身似乎运行得相当顺利。

我还没有机会在上面玩游戏，但 XDA 撰稿人 Max Weinbach 对 Stadia 目前为止很满意。他与我分享了他的好友通行证，这样我可以在下个月旅行时尝试 Stadia，但我不打算带着 Pixel 4，因为它的电池寿命很差。不幸的是，如果你想使用 Android 应用程序将游戏直接传输到智能手机，谷歌要求你拥有 Pixel 2、Pixel 3、Pixel 3a 或 Pixel 4。可以在桌面模式下使用谷歌 Chrome 启动游戏，但不幸的是，控制器不会这样工作。因此，我想看看我是否可以欺骗 Stadia 应用程序，让我在任何 Android 设备上玩游戏。幸运的是，这很容易做到。以下是方法。

**要求:**

*   [谷歌 Stadia 应用安装](https://play.google.com/store/apps/details?id=com.google.stadia.android)。要求安卓 6.0+。
*   基于 Magisk 的 Android 设备。
*   (可选)安装了 ADB 的 PC 或手机上的终端模拟器应用程序。

启用 Stadia 支持的最简单方法是简单地打开 Magisk 管理器并安装我制作的 Magisk 模块。或者，您可以按照以下步骤手动设置系统属性:

**步骤**

1.  打开 MagiskManager 并查找 MagiskHide Props 配置模块。
2.  安装模块并重启手机。
3.  现在，在 ADB shell 或您的终端应用程序中键入以下命令，进入 MagiskHide Props Config 的命令行界面:

    ```
     props 
    ```

4.  键入“`5`”添加/编辑自定义道具。
5.  键入“`n`”添加新的自定义道具。
6.  键入“`ro.product.model`”来设置这个道具。
7.  键入“`Pixel 4`”，将其设置为“`ro.product.model`”的值
8.  键入“`y`”接受道具更改。
9.  键入“`n`”，因为我们现在还不想重启。
10.  现在，重复步骤#5-8，但这次将“`ro.product.manufacturer`”设置为“`Google`”。
11.  最后，重启手机。启动后，通过输入以下命令，检查“`ro.product.model`”和“`ro.product.manufacturer`”是否分别设置为“`Pixel 4`”和“`Google`”:

    ```
     getprop ro.product.model
    getprop ro.product.manufacturer 
    ```

现在，你应该可以在任何 Android 手机上启动 Stadia 中的游戏了！我们在一加 7 Pro 上进行了测试，正如你在上面显示的特色图片中看到的那样。Stadia 应用程序只检查两个系统属性，以确定您的设备是否有资格传输游戏。我们只是伪造了这两个属性，所以 Stadia 应用程序会认为它运行在谷歌的 Pixel 4 上。这是一个非常简单的调整，但如果它在 Stadia 应用程序的未来更新中被打破，我不会感到惊讶。如果教程需要调整，我们会更新这篇文章，但我们希望 Stadia 很快推广到其他 Android 设备，这样就没有必要了。