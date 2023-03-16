# 华为证实他们正在屏蔽中国 EMUI 9 版本的第三方启动器，称这是为了减少问题

> 原文：<https://www.xda-developers.com/huawei-confirms-blocking-third-party-launchers-chinese-emui-9/>

华为对 EMUI 的争议并不陌生，EMUI 是该公司内部开发的 Android 版本。就在最近，他们被指控在最新的 EMUI 9 中国版中阻止第三方启动器，但没有具体的信息说明原因。根据我们论坛上[成员的说法，这一限制的原因是**据称是为了打击中国一些第三方零售商**的不正当行为(我们已经看到小米在](https://forum.xda-developers.com/huawei-p20-pro/how-to/emui-9-removes-default-launcher-options-t3853441)[多个](https://www.xda-developers.com/xiaomi-anti-rollback-protection-brick-phone/) [场合](https://www.xda-developers.com/flash-miui-global-locked-bootloader-xiaomi-brick/)处理这个问题)。现在，该公司已经证实这是故意的，但可访问性启动器的合法开发者可以申请将他们的应用程序列入白名单。**这不影响任何运行 EMUI 9** 全球版本的人。

 <picture>![Huawei EMUI 9 blocking launchers in China](img/cbe660a45a065989eb08bc664d1c806a.png)</picture> 

“Default app” settings on the Honor Magic 2 (TNY-AL00) running EMUI 9.0.0.128\. Although Nova Launcher is installed, it cannot be made the default launcher.

一旦你考虑到中国市场，这种限制是有意义的，尽管如果普通开发者也能把他们的应用程序列入白名单，这种限制会更容易接受。EMUI 的启动器缺乏功能，用户不妨安装另一个启动器如 Nova 启动器、Action 启动器、[无根像素启动器](https://www.xda-developers.com/rootless-pixel-launcher-google-play-store-pixel-bridge/)、[尼亚加拉启动器](https://www.xda-developers.com/niagara-launcher-minimalist-notifications/)等等。这是必需的，因为华为声称第三方经销商会预装非官方的启动器，显示弹出广告，未经许可安装应用程序，并降低你的手机速度。我们无法核实这些说法的真实性，但正如之前所说，小米也面临过类似的问题。如果这是一个普遍的问题，那么你可以想象华为的服务中心可能会非常繁忙。

那么正常用户能做什么呢？之前卸载华为官方的启动器就足以让你选择第三方启动器来代替。不知道它是否还能工作，但是如果你愿意，你可以试一试。不过这需要 ADB，在那里你可以找到卸载你的智能手机可能附带的膨胀软件的完整教程[这里](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)。要仅卸载 Huawei launcher，请运行以下 ADB 命令。

```
 adb shell pm uninstall -k --user 0 com.huawei.android.launcher 
```

要拿回枪托，你需要侧装 APK。

* * *

[**来源:华为**](https://club.huawei.com/thread-18575701-1-1.html)