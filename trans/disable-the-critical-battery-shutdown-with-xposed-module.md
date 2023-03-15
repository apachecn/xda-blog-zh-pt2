# 使用暴露的模块禁用关键电池关闭

> 原文：<https://www.xda-developers.com/disable-the-critical-battery-shutdown-with-xposed-module/>

与非智能手机设备相比，基于 Android 的设备在处理极低电池电量方面往往有很大不同。当电池电量接近 1%时，设备会自动关闭。当然，这并不意味着电池完全耗尽，准确判断电池储备容量需要校准。校准良好的电池通常可以让你的设备多工作一个小时。

为了正确校准您的电池，您需要将它完全放电并充电至 100%。当您的电池最近被更换时，这一点尤其重要。当然，从长远来看，这些深度循环对你的电池寿命是有害的，所以你应该尽量少用。

XDA 资深成员 [zst123](http://click.xda-developers.com/api/click?format=go&key=f0a7f91912ae2b52e0700f73990eb321&loc=http%3A%2F%2Fwww.xda-developers.com%2Fandroid%2Fcontrol-your-in-app-fonts-with-perappfonts-xposed-module%2F&v=1&libId=a0dd9613-6592-4660-ae1c-19f1945cd02a&ref=http%3A%2F%2Fwww.xda-developers.com%2F&title=Rid%20Yourself%20of%20the%20Ugly%20Black%20Navigation%20Bar%20with%20Xposed%20%E2%80%93%20xda-developers&txt=zst123&jsonp=vglnk_jsonp_13881604059316&out=http%3A%2F%2Fforum.xda-developers.com%2Fmember.php%3Fu%3D5402474) ，其他曝光模块如[软键淡出模式](http://www.xda-developers.com/android/rid-yourself-of-the-ugly-black-navigation-bar-with-xposed/)和[每应用字体](http://www.xda-developers.com/android/control-your-in-app-fonts-with-perappfonts-xposed-module/)的作者，做了一个简单的模块，当 Android 检测到临界电池水平时，禁用设备的自动关机。当设备试图关机时，会弹出一个特殊的通知，其中包含有关此尝试的信息。自然，因为这是一个 Xposed 模块，你的手机必须是根的，并且安装了之前由 XDA 认可的开发者 [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 开发的[x posed 框架。](http://www.xda-developers.com/android/say-goodbye-to-custom-stock-roms-and-hello-to-xposed-framework/)

如果你的电池寿命异常短，并且你觉得不正确的校准可能是罪魁祸首，那么去[模块线程](http://forum.xda-developers.com/showthread.php?t=2583320)那里试试吧。请注意，当设备关闭时，您将不可避免地丢失您正在处理的任何数据，如果设备正在修改/system 文件或者您遭受 NAND 损坏，您甚至可能会损坏您的操作系统。此外，请记住，锂离子/聚合物电池的重复深度循环会显著增加其磨损，因此请谨慎使用。