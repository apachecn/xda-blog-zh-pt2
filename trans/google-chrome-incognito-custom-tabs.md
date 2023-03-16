# Android 上的谷歌 Chrome 可能很快会支持匿名 Chrome 定制标签

> 原文：<https://www.xda-developers.com/google-chrome-incognito-custom-tabs/>

# Android 上的谷歌 Chrome 可能很快会支持匿名 Chrome 定制标签

谷歌 Chrome 可能很快会支持匿名定制标签——以匿名模式打开的 Chrome 定制标签不保存历史记录，也不支持截图。

谷歌 Chrome 浏览器是迄今为止安卓系统上最占主导地位的浏览器。毕竟，它预装在大多数 Android 设备上(这[最近让谷歌陷入了与欧盟](https://www.xda-developers.com/google-fined-5-billion-eu/)的麻烦中)，即使你使用另一种浏览器，它也可能仍然基于 Chromium。Android 的默认 WebView 客户端[在 Android 4.4 KitKat](https://developer.chrome.com/multidevice/webview/overview) 中变成基于 Chromium，然后 [Android Nougat 让 Chrome 应用程序接管 WebView 进程](https://developer.android.com/about/versions/nougat/android-7.0#webview)。似乎这还不够，谷歌 Chrome 45 推出了 [Chrome 定制标签](https://developer.chrome.com/multidevice/android/customtabs)，鼓励应用开发者在 Chrome 中打开浏览器链接，以改善用户体验。Chrome 自定义标签允许开发人员显示一个带有一些定制的 Chrome 标签，如主题化标题栏和在菜单中显示特殊按钮，但我们在 Chromium Gerrit 中发现的一个新的提交表明，Chrome 自定义标签将很快支持以匿名模式打开。

*XDA 实验室的 Chrome 定制标签*

标题为“引入匿名定制标签”的[提交](https://chromium-review.googlesource.com/c/chromium/src/+/1171225)，详细说明了这种定制标签的新变体将如何工作。这里有一个总结:

*   一个名为`enable_incognito_custom_tabs`的标志(用户无法访问，但在构建时可以访问)控制该特性是否应该为支付流之外的目的而启用。
*   另一个名为`allow_incognito_custom_tabs_from_third_party`的标志(用户也无法访问)控制第三方应用程序是否可以打开匿名自定义标签。ICT 是通过添加 intent extra `com.google.android.apps.chrome.EXTRA_OPEN_NEW_INCOGNITO_TAB`打开的，默认只能由第一方 Google apps 完成。
*   一旦一个 ICT 被打开，就会有一个名为“在隐名浏览器中打开”的新菜单项，它可以在浏览器中将标签重新打开为隐名标签。与常规 CCT 不同，应用程序选择器不会显示。
*   默认情况下，工具栏是灰色的，但应用程序开发人员可以覆盖它。
*   “关闭所有匿名标签”的通知也将关闭任何打开的 ICTs。
*   像常规的匿名模式标签一样，屏幕截图在 ICTs 中是不允许的，它们的内容也不会显示在最近的应用视图中。(这可以通过[修改 services.jar 来禁用安全标志](https://forum.xda-developers.com/apps/magisk/module-smali-patcher-0-7-t3680053)来绕过。)

这一变化的代码还没有合并，所以我们还不会在 Chrome 中看到它。一旦合并，该功能将在 Chrome Canary 中可用，然而，我们将不会看到它的运行，直到谷歌开始在他们的应用程序中实现它，或者可能为第三方应用程序开放它。我们将密切关注这一功能，并在它可用时随时向您更新。