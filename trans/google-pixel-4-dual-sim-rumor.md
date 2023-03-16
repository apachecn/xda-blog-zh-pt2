# 2019 款谷歌 Pixel 4 可能会有更好的双 SIM 卡功能

> 原文：<https://www.xda-developers.com/google-pixel-4-dual-sim-rumor/>

虽然我们还不到 10 月，但我们已经听到了很多关于谷歌 2019 年智能手机计划的消息。这是因为谷歌正在开发谷歌 Pixel 3 智能手机的新“精简”型号。我们已经看到实物证据表明，谷歌正准备推出一款 [Pixel 3 Lite](https://www.xda-developers.com/google-pixel-3-lite-mid-range-specs-leak/) 和 [Pixel 3 Lite XL](https://www.xda-developers.com/renders-of-notchless-google-pixel-3-lite-lite-xl-with-3-5mm-headphone-jacks-leak-online/) ，一个可靠的消息来源称，这两款设备将于 2019 年初在威瑞森推出[。除了 2019 年末的谷歌 Pixel 4 将运行开箱即用的 Android Q 外，我们还没有听到关于即将到来的智能手机的任何其他消息。Android 开源项目 Gerrit 的一项新承诺告诉我们，Google 正在框架和电话服务中添加属性值，以判断设备是否支持 multiSIM 功能。我们更感兴趣的是一个谷歌人在其中一次提交中留下的评论。评论指出，2019 年的像素将具有双 SIM 卡功能。](https://www.xda-developers.com/pixel-3-lite-pixel-3-xl-lite-verizon-2019/)

对于一些背景，谷歌像素 2 和谷歌像素 3 都有一个常规的 SIM 卡插槽和一个 eSIM。根据谷歌在 Twitter 上的@ [MadeByGoogle](https://twitter.com/madebygoogle/status/1050121193829879808?s=19) 支持账户，虽然你可以[提供 eSIM 连接到许多受支持的运营商](https://www.xda-developers.com/google-expanding-pixel-3-pixel-2-esim-support-more-carriers/)，但你不能“同时使用物理 SIM 网络和 eSIM 网络”。这意味着 Pixel 2 和 Pixel 3 支持双卡单待(DSSS)。虽然您可以将两个 SIM 卡配置到两个不同的网络，但您不能接收非活动 SIM 卡插槽的来电或短信。另一方面，最新的 iPhones 和许多双 SIM 卡 Android 智能手机都支持双 SIM 卡、双待机(DSDS)。这意味着，只要主 SIM 卡插槽没有被用于相同的目的，另一个 SIM 卡就可以接收电话或短信。最后，还有双 SIM 卡，双活动(DSDA)，其中两个 SIM 卡插槽可以同时用于通话，短信或数据。虽然 Pixel 3 没有支持 DSDA 的硬件(它缺少第二个无线电)，但它应该能够像最新的 iPhones 一样支持 DSDS。自从 Pixel 2 发布以来，一些 Pixel 所有者一直要求更好的双 SIM 卡支持，因为拥有多条线路对那些经常出差的人来说很有用。

在[几个](https://android-review.googlesource.com/c/platform/frameworks/base/+/894753) [提交的](https://android-review.googlesource.com/c/platform/packages/services/Telephony/+/894716) [提交给【those 议会的声明中，谷歌正在定义 Android Q 中对“双卡模式”的支持。新的系统属性值旨在“区分支持双卡模式和不支持双卡模式的设备，即使它们有两张或更多的 SIM 卡。”如果“设备和运营商支持同时使用多个 SIM 卡在网络上注册(例如，双待机或双活动)，新函数将返回值 true。”在为这个新的布尔值设置 SELinux 策略的 commit 的注释中，Google ler](https://android-review.googlesource.com/c/platform/system/sepolicy/+/894477)[声明](https://android-review.googlesource.com/c/platform/system/sepolicy/+/894477/3#message-621af9588e4aa9003c1468168b4172eed7163e82)该布尔值“需要区分 2018 Pixel(它有 2 个 SIM 卡，但双卡功能仅限于狗粮)和 2019 Pixel(它将有双卡功能)。”

我的猜测是，2019 年底的谷歌 Pixel 4 将支持在双待机模式下使用 eSIM 和常规 SIM，就像最新的 iPhone 型号一样。这在 2017 年谷歌 Pixel 2 和 2018 年谷歌 Pixel 3 上是可能的，因为谷歌正在测试谷歌 Pixel 3 XL 上这一功能的软件稳定性。然而，我们不知道谷歌是否计划更新其早期型号，以更好地支持双 SIM 卡。我们也不知道即将推出的谷歌 Pixel 3 Lite 或 Pixel 3 Lite XL 是否会支持双卡双待。

*感谢 [@Aeeeb_Ping](https://twitter.com/Aeeeb_Ping) 的提示！*