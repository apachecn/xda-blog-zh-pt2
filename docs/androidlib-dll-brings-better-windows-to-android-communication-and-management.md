# AndroidLib.dll 带来了更好的 Windows 到 Android 的通信和管理

> 原文：<https://www.xda-developers.com/androidlib-dll-brings-better-windows-to-android-communication-and-management/>

Android SDK 是在电脑上处理 Android 时的默认软件。绝大多数的 root 用户在使用曾经流行的 Android Debug Bridge，简称 ADB 时，都碰到过 SDK，不管他们知不知道。虽然 SDK 很好地实现了它的预期目的，并且工作得非常完美，但是任何为增强或帮助而创建的东西总是令人兴奋和有趣的。

正是考虑到这一点，XDA 资深成员 [regaw_leinad](http://forum.xda-developers.com/member.php?u=2326081) 开发了一个. dll 文件，允许 Windows 计算机使用. NET 更好地与 Android 设备通信。该文件包含 21 个类，其中两个被认为是主类。一个叫做 AndroidController，regaw_leinad 解释说:

> AndroidController 类是 ADB (Android Debug Bridge)二进制文件的半包装器，也将包含签名功能。ZIP 文件，便于闪存到您的设备。

文件中的第二个类称为 Device，它主要获取并显示连接到计算机的设备的信息。。NET 程序员可以添加这个。dll 作为对他们的项目的引用，并获得对一系列命令的访问。该文件的目的是帮助 Android 开发者减少 C#和。NET 代码，他们必须通过提供一个稳定的 API 来自己编写代码。这可以有很多很多的实现，它的用途只受到开发人员想象力的限制。

来展示一下。regaw _ leinad[为](http://forum.xda-developers.com/showthread.php?t=909258) [CDMA HTC Hero](http://forum.xda-developers.com/forumdisplay.php?f=641) 重写了 one click root 方法，比之前发布的任何 root 方法都更加稳定可靠。这个 API 的范围、深度和广度是惊人的。对 Android 感兴趣的. NET 或 C#开发人员真的应该在他或她的计算机上安装这个。

其他信息、下载链接和说明可以在[原始线程](http://forum.xda-developers.com/showthread.php?t=1512685)中找到。开始开发吧！