# 使用 ArduinoDroid 对 Arduino 板进行编码和编程

> 原文：<https://www.xda-developers.com/code-for-and-program-arduino-boards-using-arduinodroid/>

爱好电子产品的爱好者将会很高兴地得知 Android 的 Arduino IDE 的到来，该 IDE 支持将草图上传到流行的微控制器开发板。几天前，ArduinoDroid 登陆了 Google Play，我一有机会就尝试了一下。

APK 很小，安装很快，当你第一次打开应用程序时，软件包的大部分都会被下载。这第二个下载包含 SDK，当所有说的和做的时候，它在你的 SD 卡上占据大约 100 MB。在那里，你会看到一个主窗口，在那里你的草图会被显示出来。但是如果你不擅长从第一行开始，不要烦恼。您习惯在桌面 IDE 中找到的代码示例和支持库可以通过应用程序的文件菜单获得。我很高兴 Anton Smirnov 在编辑器中加入了语法高亮功能。你可能对在你的手机上写一个巨大的草图不感兴趣，但是如果你知道你有一个 bug，并且有一些时间可以消磨，你可以加载代码，然后一行一行地苦读。

要将代码加载到 Arduino 板上，您需要一个支持 USB On-The-Go (OTG)的 Android 设备。在这一点上，我有点搞不清到底支持哪种板，因为有相互冲突的信息。安东网站的[介绍页面提到，到目前为止，它只对基于 FTDI 的电路板进行编程，但该应用程序的配置设置包括整个家庭，直到莱昂纳多。](http://arduinodroid.blogspot.com/2013/04/introduction.html)

这张截图显示，免费应用程序是广告支持的，可以选择支付广告删除费用。一旦广告空间与开放式键盘相结合，在 7 英寸平板电脑上，几乎没有空间来查看横向的代码区域。但是我想，如果你在上面做任何严肃的代码工作，你还不如使用外接键盘。首先，请访问 [ArduinoDroid Google Play 列表](https://play.google.com/store/apps/details?id=name.antonsmirnov.android.arduinodroid)。