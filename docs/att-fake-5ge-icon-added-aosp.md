# 美国电话电报公司的假 5GE 图标已经被添加到 AOSP

> 原文：<https://www.xda-developers.com/att-fake-5ge-icon-added-aosp/>

# 美国电话电报公司的假 5GE 图标已经被添加到 AOSP

美国电话电报公司的假 5GE 图标代表“5G 演进”即 4G LTE-Advanced 技术，已被添加到 AOSP，这意味着更多的设备将很快展示该图标。

当更新到 Android Pie 和 One UI [的三星手机开始在状态栏显示 5GE 图标](https://www.xda-developers.com/samsung-android-pie-att-fake-5g-logo/)时，美国电话电报公司误导性的“5GE”活动成为了 Android 的一部分。这是 AT & T 的一种不诚实的做法，因为这造成了一种错觉，即在这种情况下，所指的技术与 5G 一样优越，而事实上，它只是略微好于 4G，并没有接近真正的 5G 技术。

美国电话电报公司营销的“5G 演进”只不过是 4G LTE-Advanced:具有载波聚合、256 QAM(正交幅度调制)和 4x4 MIMO 的 4G LTE。事实上，美国电话电报公司实际上是 4G LTE-A 派对的迟到者，报告显示& T 的 5GE 实际上比 T-Mobile 和威瑞森的 4G 要慢。Sprint 甚至继续前进，[在& T 起诉他们误导性的品牌](https://www.xda-developers.com/sprint-suing-att-5g-e-branding/)，但最终解决了争端。

现在，美国电话电报公司的假 5GE 图标已经被添加到了 AOSP。这意味着 5GE 图标被正式认可为 Android 的一个有效选项。当手机从 AT & T 连接到 LTE 网络时，该图标可能会显示，前提是他们已经设置了必要的设备特定配置来实际显示该图标。这就带来了一种可能性，所有的 Android Q 智能手机都可能会在状态栏中显示 5GE，这很有可能最终会发生。[代码](https://android-review.googlesource.com/c/platform/frameworks/base/+/950576/1/packages/SystemUI/src/com/android/systemui/statusbar/policy/MobileSignalController.java#615)中的方法表明，显示图标的阈值可以简单到在某个载波上使用载波聚合(可能在& T)，而不重视我们初步检查的实际速度。因此，虽然你的手机可能会自豪地显示“5GE”，但不能保证这比仅仅是表面上的改变更好。

你对 AOSP 增加一个 5GE 图标有什么想法？请在下面的评论中告诉我们！

*感谢 XDA 公认的开发者 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 的提示！*