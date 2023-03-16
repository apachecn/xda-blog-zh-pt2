# 三星 Galaxy Tab S4 也可能获得堡垒之夜手机在安卓上的独家授权

> 原文：<https://www.xda-developers.com/samsung-galaxy-tab-s4-fortnite-mobile-on-android/>

广受欢迎的免费皇家战役游戏《堡垒之夜》将很快在安卓系统上推出。人们普遍预计这款游戏将作为三星 Galaxy Note 9 的 30 天独占游戏推出，但它可能会作为三星 Galaxy 独占游戏在[再持续 3 个月](https://www.xda-developers.com/fortnite-mobile-android-samsung-galaxy-exclusive/)。因此，三星 Galaxy S7、三星 Galaxy S8、三星 Galaxy S9 和三星 Galaxy Note 8 的用户应该可以在三星 Galaxy Note 9 发布 30 天后玩游戏。然而，最近推出的[三星 Galaxy Tab S4](https://www.xda-developers.com/samsung-galaxy-tab-s4-official/) 的用户可能不必在 Galaxy Note 9 发布后等待 30 天才能在 Android 上享受堡垒之夜移动。 *XDA 开发者*已经获得了堡垒之夜移动安卓安装程序 APK 的访问权限，这表明游戏[不仅是三星 Galaxy Note 9 的专属](https://www.xda-developers.com/fortnite-mobile-on-android-samsung-galaxy-note-9-exclusive)，而且最初也可能在三星 Galaxy Tab S4 上提供。

包名为“com.epicgames.fortnite”的 APK 首先是由 XDA 的初级成员[the bros](https://forum.xda-developers.com/member.php?u=8761459)发现的，他是我们的常驻数据挖掘专家。APK 的反编译和分析是与 XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 合作完成的，他也被称为 [Mighty Quinn Apps](https://kieronquinn.co.uk/) 的 Kieron Quinn。我们获得的 APK 文件是堡垒之夜 5.20 版本的安装程序，该版本将于本周在其他平台上线。APK 和所有需要的堡垒之夜皇家战役数据可以下载和安装，但游戏不能在任何没有被 Epic Games 列入白名单的账户上运行。无论如何，APK 文件本身在游戏在 Android 上发布之前提供了一些有用的信息。

## 安卓系统上的堡垒之夜手机-可用于三星 Galaxy Tab S4？

该游戏有几项检查，如移动 GPU、制造商和型号，以决定是否允许设备运行该游戏。虽然三星 Galaxy S7 之后的旗舰设备能够启动游戏的主要活动，但这些设备目前还不能真正玩游戏。一种检查设备品牌、代号和功能集并将其与三星 Galaxy Note 9 或三星 Galaxy Tab S4 进行匹配的方法似乎阻止了其他三星设备玩游戏。

如显示反编译应用程序代码的屏幕截图所示，该方法检查设备的系统属性，以查看是否满足以下所有条件:

*   `ro.vendor.product.device`以“gts4l”开头
*   `ro.vendor.product.brand`是“三星”
*   `com.sec.feature.spen_usp`被定义为 Android 特性。这项功能可以让任何 Android 应用程序知道该设备支持三星的 S Pen。

因此，该方法检查该设备是否是以“gts4l”开头的代码名称的三星品牌设备。这些代号的设备是三星 Galaxy Tab S4 的许多变种。最后，方法检查是否存在 S Pen。这要么是一种额外的检查，目的是让人们更难在自己的设备上欺骗堡垒之夜，要么是 Epic Games 确认 S 笔存在并激活更多功能的一种方式。有趣的是，这个方法会检查标准 S 笔的存在，而我们发现的检查三星 Galaxy Note 9 的存在的方法[会检查新的](https://www.xda-developers.com/fortnite-mobile-on-android-samsung-galaxy-note-9-exclusive/)[启用蓝牙的 S 笔](https://www.xda-developers.com/samsung-galaxy-note-9-s-pen-bluetooth-controller/)。

* * *

这是我们第一次听说堡垒之夜移动在安卓系统上也可以与三星 Galaxy Note 9 一起在三星 Galaxy Tab S4 上推出。Galaxy Tab S4 是在上周悄悄宣布的，此前[提前宣布，以避免过度饱和即将到来的三星 Unpacked 事件](https://www.xda-developers.com/samsung-galaxy-note-9-august-9/)。我们自己的消息来源没有提到 Galaxy Tab S4 是否会在发布会上支持堡垒之夜移动，但我们被告知我们的消息来源没有得到堡垒之夜发布会本身的简报，而只是关于 Galaxy Note 9 的发布会。

新发布的三星 Galaxy Tab S4 采用了高通骁龙 835 片上系统，是首款支持三星 DeX 的三星平板电脑。它还具有虹膜扫描仪和 S 笔支持。有关该平板电脑的更多信息，如完整的规格列表和介绍视频，您可以[访问我们关于其发布的文章](https://www.xda-developers.com/samsung-galaxy-tab-s4-official/)。请继续关注 XDA，我们将从堡垒之夜手机为您带来更多关于安卓 APK 泄露的信息。如果你感兴趣，这里有相关的文章: