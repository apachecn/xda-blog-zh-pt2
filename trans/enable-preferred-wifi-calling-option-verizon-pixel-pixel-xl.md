# 如何在威瑞森 Pixel & Pixel XL 上启用首选 WiFi 通话选项

> 原文：<https://www.xda-developers.com/enable-preferred-wifi-calling-option-verizon-pixel-pixel-xl/>

目前，WiFi 通话已经成为智能手机上一项受欢迎的功能，因为它们可以提高通话质量，尤其是在信号很差的时候。考虑到大多数手机语音通话都是使用过时的技术发送的，这就是为什么大多数标准电话通话听起来不如 Skype 等 VoIP 客户端清晰明了。VoLTE 技术在很大程度上缩小了通话质量的差距，但并不是所有的手机都支持 VoLTE，也不是每个人都可以使用它的计划或网络。

由于 WiFi 通话，我们可以利用强大的 WiFi 网络连接来拨打电话，而不是依赖无法穿透到您的办公楼或家中的劣质蜂窝无线电。如果你的手机支持 WiFi 通话，如谷歌 [Pixel](https://forum.xda-developers.com/pixel) 和 [Pixel XL](https://forum.xda-developers.com/pixel-xl) ，你可能会在拨号器设置中找到选项，将通话设置为尽可能使用 WiFi。然而，威瑞森无线已经在他们出售给客户的 Pixel 手机上禁用了这种切换，所以你不能以通常的方式启用它。

不过值得庆幸的是，有一种方法可以绕过它，我们甚至不需要 root 访问权限——您所要做的就是发送一个简单的 ADB 命令。

* * *

### 启用 Wifi 呼叫的首选 WiFi

1.  为你的设备安装 USB 驱动程序(谷歌在这里有一些通用 USB 驱动程序的列表)。根据您的操作系统，这可能不是必需的。
2.  为您的特定操作系统下载 [ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)([Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)、 [Mac](https://dl.google.com/android/repository/platform-tools-latest-darwin.zip) 、 [Linux](https://dl.google.com/android/repository/platform-tools-latest-linux.zip) )。这些链接将下载最新版本，所以没有必要搜索网页！
3.  将 zip 文件解压缩到一个可以快速访问的文件夹中，例如下载文件夹。
4.  在您的手机上，输入设置并点击“关于手机”。向下滚动，找到内部版本号，然后点击它 7 次，以启用开发者选项。
5.  进入开发者选项，找到 USB 调试，然后启用它。
6.  将手机插入电脑，从“仅充电”模式切换到“文件传输(MTP)”模式。这并不总是必要的，但大多数手机不允许您在仅充电模式下使用 ADB。
7.  在您的计算机上，浏览到您解压缩 ADB 二进制文件的目录，比如在下载中。
8.  在 ADB 文件夹中打开命令提示符。对于 Windows 用户，这可以通过按住 Shift 并右键单击，然后选择“在此打开命令提示符”选项来轻松完成。
9.  打开命令提示符或终端后，输入以下命令:`adb devices`
10.  如果这是您第一次运行 ADB，您将会在手机上看到一个提示，要求您授权与计算机的连接。去批准吧。
11.  现在尝试重新运行 adb 设备命令，终端将打印您的设备的序列号。如果是的话，那么你已经准备好继续前进了。
12.  接下来输入以下命令:`adb shell`
13.  最后在 ADB shell 提示符下执行以下命令:`settings put global wfc_ims_mode 2`
14.  不会有成功消息，但是应该已经生效了。请阅读以下步骤来验证这一点。
15.  打开和关闭飞行模式。
16.  打开设置应用程序，转到 WiFi 部分。
17.  查看“更多”部分，您应该会看到 WiFi 首选是活跃的。这种改变在重启和飞行模式切换中持续存在！

* * *

### 说明

正如这里提到的，这是包含在 Pixel 和 Pixel XL 的 Android 软件中的东西，但威瑞森无线已经禁用了这种切换。无线运营商对智能手机上的软件功能拥有最终决定权(这就是为什么这么多智能手机充斥着臃肿软件)。因此，像其他无线运营商(甚至一些 OEM)一样，他们会选择隐藏该型号基础软件中包含的各种软件功能。

但在某些情况下，启用该功能在技术上仍然是可能的。在这种情况下，我们所要做的就是从上述指南的步骤 13 发送一个 ADB 命令。默认情况下，该选项设置为 1，这意味着禁用，我们无法打开它，因为它是灰色的。如果我们可以打开它，它会将该选项更改为 2(这也是我们用 ADB shell 命令手动完成的)。所以 XDA 资深成员[阿布蒂诺](https://forum.xda-developers.com/member.php?u=336570)是[能够通过执行“设置列表全局”ADB 命令找到这个选项](https://forum.xda-developers.com/pixel-xl/how-to/verizon-want-wifi-preferred-wifi-calling-t3622700)。

本教程和许多其他类似的教程都是基于寻找隐藏的设置命令，可以通过 ADB shell 发送。查看我们在 XDA 门户网站上的[教程提要](https://www.xda-developers.com/category/tutorials/)以获得更多类似的帖子。