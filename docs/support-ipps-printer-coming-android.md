# Android 将支持 IPPS 专用打印机

> 原文：<https://www.xda-developers.com/support-ipps-printer-coming-android/>

互联网打印协议，或称 [IPP](https://en.wikipedia.org/wiki/Internet_Printing_Protocol) ，[最初是由 Android Oreo](https://www.xda-developers.com/android-oreo-print-service-ipp/) 支持的。Mopria 与谷歌合作开发的，旨在使打印尽可能简单和通用。它允许设备发送多个打印作业，查询打印机的状态等。IPP 还可以在互联网上运行，这意味着一些支持 IPP 的打印机将允许你在家里用自己的打印机打印，即使你不在身边。

然而，IPP 是使用 HTTP 标准实现的，包括其所有的流和安全特性。众所周知，HTTP 不是很安全，很容易被拦截，IPP 也是如此。如果你在家或外出时想用你的打印机打印，你应该使用 IPPS 而不是 IPP。IPPS 是通过 HTTPS 实现的，这意味着安全连接。

问题是安卓奥利奥不支持 IPPS，*或者至少现在还不支持*。当连接到 Android Oreo 上的 IPPS 专用打印机时，它根本无法工作。它不能发现它们，也不能连接到它们，如果你担心你的数据的隐私，那么 IPP 的实现是没有用的。谢天谢地，[Mopria 开发者的 Android Gerrit 中已经出现了一组提交](https://android-review.googlesource.com/#/q/topic:ippsSupport+(status:open+OR+status:merged))，他们声称要增加对 IPPS 的支持。它们被标记为合并，这意味着 Android 的下一个迭代版本(可能是 Android 8.1)应该会支持更安全的 IPPS。

很高兴看到设备和打印机的统一，因为几年前设置打印机是一种可怕的体验，不管它是手机还是电脑。IPP 以一种 5 到 10 年前不可能的方式统一了设备，很高兴看到我们将在不久的将来获得对更加安全的 IPPS 的支持。