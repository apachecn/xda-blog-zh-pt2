# 使用 scrcpy 从 PC 上免费控制您的 Android 智能手机

> 原文：<https://www.xda-developers.com/scrcpy-control-android-on-pc/>

# 使用 scrcpy 从 PC 上免费控制您的 Android 智能手机

一个名为“scrcpy”的新工具可以让你只通过 USB 连接和 ADB 在电脑上显示手机屏幕。不需要根目录。

智能手机是现代生活中必不可少的一部分。对一些人来说，电话甚至比标准电脑更重要。很多人整天坐在电脑前，但他们仍然需要查看手机上的某些信息。一个名为“scrcpy”的新工具可以让你只通过 USB 连接和 ADB 在电脑上显示手机屏幕。不需要根目录。

开发者说 scrcpy 可以在 Windows、Mac 和 Linux 上运行。它通过在设备上执行服务器来工作。scrcpy 通过 adb 隧道上的套接字与服务器通信。您的屏幕以 h.264 视频的形式流式传输，然后由 scrcpy 解码并显示。键盘和鼠标输入被发送到服务器并推送到设备。scrcpy 侧重于轻量级、高性能、高质量、低延迟、快速启动和非侵入性。下面是如何设置它。

1.  从 Github 下载[最新的 zip 文件并解压。](https://github.com/Genymobile/scrcpy/releases/latest)
2.  在您的机器上设置 [ADB 访问。](https://www.xda-developers.com/install-adb-windows-macos-linux/)
3.  在之前提取的文件夹中打开命令提示符或终端，输入`scrcpy`。就是这样！

正如你所料，与手机交互是一件简单的事情。只需单击以点击，然后单击并拖动以滑动。App 定向也要翻译到屏幕上。

* * *

[**来源:罗的博客**](https://blog.rom1v.com/2018/03/introducing-scrcpy/)

[**指令:Reddit**](https://www.reddit.com/r/Android/comments/834zmr/introducing_scrcpy_an_app_to_display_and_control/dvfcz0j/)