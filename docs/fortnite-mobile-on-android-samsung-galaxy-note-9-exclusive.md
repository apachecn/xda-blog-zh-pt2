# 堡垒之夜移动安卓 APK 确证三星 Galaxy Note 9 排他性

> 原文：<https://www.xda-developers.com/fortnite-mobile-on-android-samsung-galaxy-note-9-exclusive/>

当 Android 发烧友社区正在等待三星 Galaxy Note 9 即将于 8 月 9 日发布的[时，游戏玩家们正在猜测 Epic Games 将于何时在 Android 上推出他们广受欢迎的免费游戏《堡垒之夜》。根据开发者的说法，这款游戏应该在今年夏天](https://www.xda-developers.com/everything-we-know-samsung-galaxy-note-9/)发布，但是有消息来源[告诉 *XDA 开发者*和 *9to5Google*](https://www.xda-developers.com/samsung-galaxy-note-9-launch-fortnite-mobile-ninja/) 这款手机游戏将随着三星 Galaxy Note 9 的发布而发布。到目前为止，唯一能证明堡垒之夜 Android 手机将在三星 Unpacked 2018 期间发布的证据是从可靠来源提供给 *XDA* 和*9 到 5* 的信息。现在， *XDA 开发者*已经获得了堡垒之夜移动在安卓安装程序 APK 上的访问权限，这证实了三星 Galaxy Note 9 的排他性。

包名为“com.epicgames.fortnite”的 APK 首先是由 XDA 的初级成员[the bros](https://forum.xda-developers.com/member.php?u=8761459)发现的，他是我们的常驻数据挖掘专家。APK 的反编译和分析是与 XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 合作完成的，他也被称为 [Mighty Quinn Apps](https://kieronquinn.co.uk/) 的 Kieron Quinn。我们获得的 APK 文件是堡垒之夜 5.20 版本的安装程序，该版本将于本周在其他平台上线。APK 和所有需要的堡垒之夜皇家战役数据可以下载和安装，但游戏不能在任何没有被 Epic Games 列入白名单的账户上运行。无论如何，APK 文件本身在游戏在 Android 上发布之前提供了一些有用的信息。

## 安卓版堡垒之夜手机-三星 Galaxy Note 9 独家配件

该游戏有几项检查来确定设备是否能够运行该游戏。有对移动 GPU、制造商、型号等的检查。我们试图在 Essential Phone 和谷歌 Pixel 2 XL 等设备上运行该应用程序，但在最新的内部发布中，这两种情况下都没有通过闪屏，因为这些设备没有通过制造商和型号的检查。三星 Galaxy S7、三星 Galaxy S8、三星 Galaxy S9 和三星 Galaxy Note 8 等三星 Galaxy 设备能够通过闪屏，因为有一个内部白名单(我将在另一篇文章中详细介绍)，但这些设备目前还不能实际玩游戏。原因在于一种检查设备品牌、代号和功能集并确定它是否与三星 Galaxy Note 9 匹配的方法。如果没有，游戏主活动关闭。(为简洁起见，省略了与此方法相关的附加代码。)

正如上面反编译代码的截图所示，该方法检查 Android 设备的系统属性。检查以下属性:

*   `ro.vendor.product.device` =以“皇冠”开头
*   `ro.vendor.product.brand` =“三星”
*   `SEC_FLOATING_FEATURE_COMMON_SUPPORT_BLE_SPEN`，这是一项三星特有的功能，仅在三星 Galaxy Note 9 上提供，可用于支持蓝牙的 S Pen

因此，很明显，该方法检查设备是否是代码名称以“crown”开头的“Samsung”设备我们已经知道“皇冠”是三星 Galaxy Note 9 在[和](https://www.xda-developers.com/list-upcoming-xiaomi-samsung-oppo-huawei-devices/)的代号。该方法检查任何其他三星设备——BLE 的笔——上不存在的三星体验功能的存在。感谢 [FCC 文件](https://www.xda-developers.com/samsung-galaxy-note-9-s-pen-bluetooth-controller/)和[对最新 AirCommand 应用](https://www.xda-developers.com/samsung-galaxy-note-9-s-pen-features-samsung-galaxy-tab-s4-firmware/)的分析，该应用来自安卓 8.1 Oreo 发布在[三星 Galaxy Tab S4](https://www.xda-developers.com/samsung-galaxy-tab-s4-official/) 上，支持蓝牙的 S Pen 的存在在这里并不令人惊讶。但事实上，Android 上的堡垒之夜移动应用程序检查它的存在是有趣的。这表明该应用程序要么检查其存在以提供一些额外的集成，要么只是检查其存在作为该应用程序正在 Galaxy Note 9 上运行的另一个确认步骤。

* * *

由于这个 APK 的泄漏，我们有更多的堡垒之夜移动相关的新闻来了。以下是我们目前发现的总结: