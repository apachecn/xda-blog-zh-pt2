# 运行 Android 10 的威瑞森谷歌 Pixel/Pixel XL 可以 bootloader 解锁

> 原文：<https://www.xda-developers.com/how-to-unlock-bootloader-verizon-google-pixel-xl-running-android-10/>

# 下面介绍如何解锁运行 Android 10 的威瑞森谷歌 Pixel/Pixel XL 的 bootloader

运行 Android 10 的谷歌 Pixel 和谷歌 Pixel XL 的威瑞森版本现在可以解锁引导程序。继续阅读，了解更多信息！

早在 2016 年，威瑞森就与谷歌达成了一项运营商独家协议，在美国销售第一代谷歌 Pixel 和 Pixel XL。与 Pixel/Pixel XL 的常规版本不同，从运营商处购买的设备带有永久锁定的引导加载程序。一个名为 [dePixel8](https://www.xda-developers.com/verizon-pixelpixel-xl-bootloader-unlock-has-been-released/) 的免费引导加载程序解锁漏洞很快被释放，但谷歌在随后的安全更新中关闭了该漏洞。[另一种绕过技术](https://www.xda-developers.com/unlock-bootloader-verizon-google-pixel-xl/)在 2018 年出现在我们的论坛上，它已经以类似的方式打了补丁。看起来社区现在已经设法发现了另一种有趣的绕过方法，可以用来永久解锁威瑞森出售的第一代谷歌 Pixel 和 Pixel XL 的引导加载程序。

**[谷歌像素 XDA 论坛](https://forum.xda-developers.com/pixel) ||| [谷歌像素 XL XDA 论坛](https://forum.xda-developers.com/pixel-xl)**

事实上，新发现的过程在很大程度上类似于以前的旁路方法。在这两种情况下，您都必须使用 ADB 从当前用户中卸载股票电话应用程序(软件包名称:`com.android.phone`)。新方法的主要优点是，即使你的手机运行的是安卓 10 固件，你也可以执行整个绕过程序，继续解锁引导程序。

## 如何解锁运行 Android 10 的威瑞森谷歌 Pixel/Pixel XL 的 bootloader

基于 XDA 成员[DJ adred 704](https://forum.xda-developers.com/member.php?u=9295007)的[发现](https://forum.xda-developers.com/showpost.php?p=83064933)，以下一组指令由 XDA 成员 [RaspberryPiBen](https://forum.xda-developers.com/member.php?u=8460301) 编译。

### 先决条件

### 绕过引导加载程序解锁限制的步骤

1.  在手机上，打开设置>系统>重置选项，将手机重置为出厂设置。它应该说“重新启动”或类似的东西。
2.  当屏幕变黑时，按住音量降低键，直到进入引导模式。使用音量键导航到“恢复模式”，并使用电源按钮选择它。
3.  按住音量降低键大约一分钟(当它复位时)，直到你看到一个机器人躺下的图形。
4.  按住电源按钮，然后按一次调高音量按钮。它会给你一份菜单。
5.  使用音量和电源按钮选择“擦除数据/恢复出厂设置”。
6.  一旦完成，选择一个选项说“侧载 OTA”。
7.  将您的手机连接到计算机，并键入以下内容。对于谷歌 Pixel:

    ```
     adb sideload sailfish-ota-qp1a.191005.007.a3-394b5899.zip 
    ```

    对于谷歌 Pixel XL:

    ```
     adb sideload marlin-ota-qp1a.191005.007.a3-23002a57.zip 
    ```

8.  从恢复模式再次恢复出厂设置。
9.  重新启动系统。
10.  虽然它只是显示 G，按下电源按钮，直到手机重新启动。
11.  一旦它启动，跳过所有的步骤，但禁用向谷歌发送信息的选项。
12.  轻按“内部版本号”七次，启用开发人员选项。
13.  在开发人员选项中，启用 USB 调试。
14.  在您的计算机上，运行`adb shell pm uninstall --user 0 com.android.phone`
15.  重启两次。
16.  连接到 Wi-Fi。
17.  在 Chrome 中打开[google.com](https://www.google.com/)。
18.  检查开发人员选项，看看您是否可以启用 OEM 解锁。
19.  如果不能，请从“最近通话”菜单中滑动设置，然后返回 Chrome。
20.  在 Chrome 里，打开一堆网站。每次打开后，再次检查 OEM 解锁选项，然后关闭设置。
21.  一旦您可以启用它，就这样做吧！现在你可以解锁引导程序了。

### 解锁威瑞森谷歌像素和像素 XL 上的引导加载程序

1.  当屏幕变黑时，重新启动并按下音量降低键
2.  在计算机上，键入`fastboot flashing unlock`

到目前为止，我们论坛上的多个用户报告说，他们已经使用这种方法成功解锁了威瑞森谷歌 Pixel 和 Pixel XL 的引导加载程序。显然，在这些机型上侧装最新的固件和卸载手机应用程序就足以阻止[“呼叫总部”程序](https://forum.xda-developers.com/showpost.php?p=82867549)。虽然旁路的本质本身有点挑剔，但如果你有一台威瑞森谷歌 Pixel/Pixel XL，并希望你的引导程序解锁，现在可能是你最后的机会。一定要试一试，让我们知道它是否对你有效！