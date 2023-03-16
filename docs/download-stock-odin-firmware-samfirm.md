# 获取固件来降级、升级或恢复您的三星 Galaxy

> 原文：<https://www.xda-developers.com/download-stock-odin-firmware-samfirm/>

# 如何下载 Odin 固件来降级、升级或恢复您的三星 Galaxy

如何使用 SamFirm 下载 stock Odin 固件来降级、升级或恢复您的三星 Galaxy 智能手机或平板电脑。

三星 Galaxy 智能手机是市场上最受欢迎的 Android 智能手机。他们拥有最高的市场份额，在大多数地方，一个容易解锁的引导加载程序。在三星 Galaxy 手机上不容易得到的一个东西是 Odin 闪存固件，你可以通过闪存来降级、升级或恢复你的手机。Odin 固件文件就像 Google Pixel 的工厂映像，只是放入一个. tar 文件中，并通过 GUI 工具而不是 fastboot 命令终端来轻松使用。

SamFirm 是一款由资深会员 [zxz0O0](https://forum.xda-developers.com/member.php?u=3975929) 为微软 Windows 个人电脑制作的免费工具，可以帮助你为任何三星 Galaxy 智能手机或平板电脑下载股票 Odin-flash 固件。虽然它已经被弃用，但直到今天它仍然工作得很好。这个工具将下载 Odin 固件文件直接从三星服务器与所有需要的文件。用它下载固件非常简单容易。您所需要的只是您的型号和 CSC 值，我们将向您展示如何操作

## 如何用 SamFirm 下载 Odin 固件文件

1.  从谷歌 Play 商店下载三星的手机信息。这是为了找出你当前有效的 CSC 值是多少。如果您已经知道它是什么，请跳到步骤 3。
2.  打开**手机信息三星**，进入 **CSC 代码**标签。它应该显示一个选项，上面写着**激活 CSC 代码**。请记住这 3 个字符的代码，因为您将在后面的步骤中用到它。
3.  在您的电脑上下载并安装 [Microsoft Visual C++ 2008 可再发行软件包(x86)](http://www.microsoft.com/en-us/download/details.aspx?id=29) 和 [Microsoft Visual C++ 2010 可再发行软件包(x86)](http://www.microsoft.com/en-us/download/details.aspx?id=5555) 。这些是 SamFirm 下载您的固件所必需的。
4.  下载 [SamFirm v0.3.6](https://forum.xda-developers.com/attachment.php?attachmentid=3803841&d=1467715462) 。这是最新版本，可以下载所有三星 Galaxy 固件文件。这个程序和 Odin 一样需要 Windows，所以在下载这些文件的时候要记住这一点。
5.  解压缩并打开您刚刚下载的 zip 文件。这将包含 SamFirm 工作所需的所有文件。
6.  打开 SamFirm。一旦它打开，确保您选择了该区域下的**自动**选项。这将使下载文件自动进行，所以你不需要每次下载一个内部版本号。
7.  在显示“型号”的地方输入您的型号。这要从 SM 说起。您需要确保包括 SM-否则它不会下载您的文件。
8.  接下来，在 region 部分下，输入之前的三个字符的 CSC 值。然后点击**检查更新**。这将为您的设备查找最新的更新。如果没有显示更新，这可能是因为您使用的运营商没有使用 Samsung 的服务器进行更新，因此没有存储 SamFirm 可以下载的任何内容。如果是这种情况，请尝试在 AndroidFileHost 上搜索您选择的固件。一般会上传到那里。
9.  点击**下载**并选择文件位置。这将开始下载和解密。这可能需要一段时间，取决于您的网络速度和 CPU 速度。当文件准备好被提取并用于闪存时，SamFirm 将在日志窗口中告诉您解密已经完成。

这些 Odin 固件文件有时很难得到，所以很高兴看到一个开发人员站出来，制作一个程序来帮助找到人们需要的东西。