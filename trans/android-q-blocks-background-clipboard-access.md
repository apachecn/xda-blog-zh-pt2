# RIP 剪贴板管理器:Android Q 阻止后台剪贴板访问

> 原文：<https://www.xda-developers.com/android-q-blocks-background-clipboard-access/>

# RIP 剪贴板管理器:Android Q 阻止后台剪贴板访问

在之前版本的 Android 上，任何应用程序都可以访问剪贴板。这可能会导致严重的安全问题。Android Q 正在改变这一点。

我们都认为 Android P 代表隐私，但在揭露了 Android Q 提供的一些 T2 好东西后，它显然击败了 Android Pie。第一个 Android Q 测试版于昨天[发布，但是我们一直在努力识别所有看不到的新变化。其中一项改变是阻止不需要剪贴板的应用程序访问剪贴板。在你们大多数人可能使用的 Android 的早期版本上，任何应用程序都可以访问剪贴板数据。正如你所想象的，这可能会导致严重的安全问题。Android Q 正在改变这一点。](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/)

我们在大约两个月前的独家 Android Q expose 中第一次谈到了这个变化。Android 开发者网站现在发现，Android Q 将阻止剪贴板访问所有在后台运行的应用程序。目前唯一的例外是输入法编辑器(ime)，因此主要是键盘应用程序。在[我们的测试](https://www.xda-developers.com/android-q-privacy-permission-controls/)之后，我们确认到目前为止没有一个剪贴板管理器能够看到剪贴板的内容。谷歌的网站提到，这些变化只会影响专门针对 Android Q 的应用程序，但我们的测试显示了不同的结果，因为我们测试的应用程序都没有针对 Android Q，但他们的剪贴板访问仍然受到限制。

虽然这是安全方面的巨大胜利，但它将影响许多第三方开发者。我相信你会同意，让每一个应用程序访问你的剪贴板，在那里你复制敏感数据，如密码和信用卡信息，不是一个好主意。但是有一些[合法应用](https://www.xda-developers.com/join-2-1-0-beta-install-local-android-apps-remote-devices/)很好地利用了这个功能。Gboard 在 7.7 版本中也得到了[剪贴板管理器](https://www.xda-developers.com/gboard-clipboard-manager/)的支持。这将是少数几个被 OEM 授权使用剪贴板管理器的应用程序之一，因为它是一个输入法编辑器。

[**了解更多安卓 Q**](https://www.xda-developers.com/tag/android-q/)

* * *

[**来源:安卓开发者**](https://developer.android.com/preview/privacy/data-identifiers#clipboard-data)