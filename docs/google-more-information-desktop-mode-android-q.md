# 谷歌在 Android Q 中公布了更多关于桌面模式的信息

> 原文：<https://www.xda-developers.com/google-more-information-desktop-mode-android-q/>

通过 Android Q，谷歌继续努力将 Android 扩展到传统智能手机、平板电脑、智能手表和电视之外。[三星 Galaxy Fold](https://www.xda-developers.com/samsung-galaxy-fold-specifications-pricing-availability/) 和[华为 Mate X](https://www.xda-developers.com/huawei-mate-x-5g-foldable-smartphone-specifications/) 可折叠智能手机吸引了我们对 Android Q 的[可折叠外形原生支持](https://www.xda-developers.com/smartphone-foldable-display-android/)的大部分注意力，但谷歌正在悄悄地要求开发者修改他们的应用程序，以支持另一种多显示器场景:桌面和显示器。

华为和三星分别推出了 [Easy Projection](https://www.xda-developers.com/emui-9-review-features-apps-huawei-honor-android-pie/) 和 [DeX](https://www.xda-developers.com/tag/samsung-dex/) ，引领了弥合智能手机和台式电脑之间差距的潮流。按照传统，谷歌正在把 OEM 软件的精华部分慢慢整合到 AOSP。在 Android Q 中，该公司正在[增加对“桌面模式”的原生支持。](https://www.xda-developers.com/android-q-desktop-mode/)“然而，你不会知道，因为该公司从未在他们的任何谷歌 I/O 主题演讲中提到过它，而是将其降级为一个为可折叠和多显示器外形(又名桌面模式)构建应用的会议的一小部分。

在题为“为可折叠、多显示器和大屏幕设备构建应用”的演讲中，Android Framework WindowManager 团队中从事多显示器工作的软件工程师 Andrii Kulian 分享了开发人员如何为多显示器环境准备应用的详细信息。

> #### “可折叠手机可能有几个屏幕，但你也可以在汽车上，在桌面模式下连接到更大屏幕的手机上，在 Chrome OS 上，等等。”——谷歌的安德里·库连。

## 在 Android Q 中开发新的桌面模式

如果您有兴趣更新您的 Android 应用程序以支持桌面环境，您应该观看本文结尾嵌入的会话。不过，我将总结一下要点:

*   为了让您的应用程序支持在主屏幕(电话)和辅助屏幕(显示器)上同时使用，您的应用程序必须支持多个实例。通过意向标志 [NEW_TASK](https://developer.android.com/reference/android/content/Intent.html#FLAG_ACTIVITY_NEW_TASK) 和 [MULTIPLE_TASK](https://developer.android.com/reference/android/content/Intent.html#FLAG_ACTIVITY_MULTIPLE_TASK) ，Android Q 可以在辅助显示屏上创建应用的第二个窗口。
*   新的[多重恢复行为](https://www.xda-developers.com/android-q-splitscreen-multitasking-multi-resume/)也适用于多重显示场景。因此，您可以将您的应用程序配置为在另一个应用程序获得焦点时运行。
*   如果您认为您的应用程序应该主要在主显示器或辅助显示器上启动，您可以检查标志、指标和状态，以找到启动活动的正确显示器。请注意，系统可能会限制在私人显示器上启动活动，为此谷歌在 Android Q 中添加了一个新的 API，以检查呼叫者是否可以在特定活动上启动活动。
*   谷歌在 Android Q 中增加了在副屏幕上显示软件键盘窗口的支持。虽然仍然可以一次只有一个软件键盘窗口，但是窗口可以在显示器之间移动。
*   壁纸和动态壁纸可以在多显示器上分开。
*   如功能图所示，桌面模式在辅助屏幕上支持第三方启动器。谷歌在意向过滤器中增加了一个[新类别，为二级屏幕提供专门的活动。该活动必须有一个启动模式，该模式不会阻止多个实例，并适应不同的屏幕大小。用户可以在设备上设置他们选择的启动器，如果当前选择的启动器有一个用于辅助屏幕的专用活动，它将被系统放在那里。](https://developer.android.com/reference/android/content/Intent#CATEGORY_SECONDARY_HOME)
*   开发人员可以通过启用“强制桌面模式”在辅助屏幕上测试他们的应用程序，该模式在所有支持的屏幕上打开系统声明，并在那里显示鼠标指针，而不是当前显示，并“启用[自由形式窗口](https://www.xda-developers.com/android-nougats-freeform-window-mode-what-it-is-and-how-developers-can-utilize-it/)以允许浮动应用程序窗口。但是，要使更改生效，您需要重新启动设备。如果你有一个谷歌像素，你可以通过在开发者选项中启用模拟显示来尝试桌面模式。在支持通过 HDMI 显示输出的其他设备上，如果您有 USB-C 转 HDMI 适配器，可以尝试桌面模式。例如，基本手机[只需将它插入显示器，就可以启动 Android Q 中新的桌面模式](https://www.reddit.com/r/essential/comments/bm5g2a/desktop_mode_works/)。

我在这里做了一个大胆的猜测，但我认为即将到来的 Pixel 4 将支持通过 HDMI 显示，因此谷歌可以将 Android Q 的新桌面模式作为一个功能来宣传。我们将在 5 个月后谷歌推出新像素时找到答案。

感谢 XDA 资深会员 farmerbb 对本次演讲的提醒！