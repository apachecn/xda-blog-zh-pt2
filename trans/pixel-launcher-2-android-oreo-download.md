# Android 奥利奥 AOSP 的 Pixel Launcher 2.0 现在可以下载了

> 原文：<https://www.xda-developers.com/pixel-launcher-2-android-oreo-download/>

# Android Oreo 的 Pixel Launcher 2.0 可用于非根设备

Pixel Launcher 的更新端口现在可用，它是从 Android Oreo 的 Launcher3 构建的，并在顶部添加了一些额外的功能。

几个月前，我们覆盖了 Pixel Launcher 的一个[端口，该端口对无法从 Play Store 安装它的设备](https://www.xda-developers.com/developer-ports-the-pixel-launcher-with-the-google-now-panel-for-unrooted-devices/)可用。这个端口整个月都在更新，但 Reddit 用户 AmirZ 说，一旦 Android Oreo 发布给公众，他们会回来再做一次。随着本周早些时候发生的事情，我们认为这一更新将需要更长的时间才能出来，但幸运的是情况并非如此，**2.0 版本的发射器现已推出**。

最初的移植做了很多工作，但在另一个名为 *DeleteScape* 的开发者的帮助下，他们能够为公众提供一些工作。凭借之前获得的经验，AmirZ 表示，他们在过去几天一直在不间断地工作，现在 Pixel Launcher 2.0 更新的初始版本已经发布。以前，他们带着“不要修复没坏的东西”的理念，只是为了发布最终产品。不过这一次，我们在这里加入了一些额外的功能。

所以开发者在 AOSP Launcher3 的基础上添加了以下像素特性。。。

*   带有透明矩形、谷歌药丸和日期/天气的 QSB
*   不同颜色的通知点
*   从应用列表中过滤谷歌壁纸和语音搜索
*   使用谷歌壁纸选择可用的壁纸
*   设备配置文件、边距、图标数量
*   禁用合作伙伴定制，如摩托罗拉的 4 列
*   Google Now feed 位于普通工作区的左侧
*   带有日期的 Google 日历应用程序图标

但是如前所述，这个版本中增加了很多额外的工作，包括。。。

*   下拉以获取通知
*   奥利奥主题被移植到旧版本的操作系统，并带有像素蓝色强调色
*   通知点反向传输到棉花糖
*   自动提示通知访问，这样您就不必翻遍设置菜单
*   修复 Android 8 检查，以便 Nexus 设备可以使用所有新功能
*   在未启用开发者设置的 Android 8 上显示图标形状
*   按下日期小工具会打开默认的日历应用程序
*   从任何应用程序返回主屏幕时，键盘会正确关闭
*   对称热点
*   从应用列表中过滤 Google Now 启动器
*   捏至概览
*   三星安全文件夹兼容性
*   圆形图标的背面端口

就像这个端口的上一个版本一样，你需要确保你没有安装真正的 Pixel 启动器。如果你试图在它上面安装这个，你会得到一个损坏的软件包错误。这是因为这个端口使用与原始 Pixel Launcher 相同的包名，这样做是为了让天气小部件正常工作。对于那些感兴趣的人，你可以在这里找到这个版本的[下载](https://github.com/amirzaidi/Launcher3/releases),[源代码可以在这里找到](https://github.com/amirzaidi/Launcher3/commits/o)和[一些截图也在这里](https://goo.gl/photos/C6kWrgMV3jMfL2Ld9)。

* * *

[**来源:/r/Android**](https://www.reddit.com/r/Android/comments/6vu2to/rootless_pixel_launcher_20_based_on_aosp_800/)