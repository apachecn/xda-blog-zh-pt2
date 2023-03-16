# 得益于谷歌 Chrome，Android 的 Nearby Share 文件共享功能可能支持 Chrome OS、Windows、macOS 和 Linux

> 原文：<https://www.xda-developers.com/android-nearby-share-file-sharing-chrome-os-windows-macos-linux-chrome/>

苹果的生态系统非常有凝聚力，隔空投送就是最好的例子之一。该功能使得在苹果设备之间共享文件变得非常简单，不需要任何人安装第三方应用程序。在 Android 方面，事情要复杂得多。虽然一加、Realme、黑鲨、魅族、OPPO、Vivo 和小米等一些最好的 Android 手机背后的公司已经加入了文件传输联盟，但索尼、LG 和摩托罗拉等其他原始设备制造商没有自己的内置解决方案。此外，三星和华为也有自己的文件共享解决方案。幸运的是，我们知道[谷歌正在开发自己的文件共享服务](https://www.xda-developers.com/nearby-sharing-airdrop-for-android-file-sharing/)，该服务可能适用于大多数装有谷歌应用的安卓智能手机。现在有证据表明，谷歌的解决方案也将支持向运行 Chrome OS、Windows、macOS 或 Linux 的个人电脑共享文件。

附近的共享已经发展了一段时间了。近一年前[被发现时，最初被称为“快速共享”。随着开发的继续，](https://www.xda-developers.com/fast-share-android-beam-airdrop-android/)快速分享[最终被更名为](https://www.xda-developers.com/fast-share-google-upcoming-airdrop-service-renamed-nearby-sharing/)附近分享，最近又更名为“附近分享”。该功能将通过 Google Play 服务提供，这意味着它将在 Android 设备中几乎无处不在*。Chromium Gerrit 最近的提交显示，它也可能在安装了谷歌 Chrome 的电脑上运行，包括 Chromebooks。*

早在 4 月份， [*ChromeUnboxed*](https://chromeunboxed.com/android-airdrop-nearby-sharing-feature-chrome-os-chromebooks/) 发现了一个[提交](https://chromium-review.googlesource.com/c/chromium/src/+/2133053)，它被合并到 Chromium Gerrit 中，添加了一个标记，描述为“启用附近共享功能”。Android 已经有了原生实现。”因此，这个标志是为了在非 Android 平台上使用 Chrome 浏览器实现附近共享。然后，上周合并的一个[提交](https://chromium-review.googlesource.com/c/chromium/src/+/2233898)透露了“附近共享”的设置将被整合到 Chrome OS 设置中。这一设置可以在下面来自 *[ChromeStory](http://www.chromestory.com/) 的* Dinsan Francis 的推文中看到。

另一个最近提交给 Chromium Gerrit 的 [commit](https://chromium-review.googlesource.com/c/chromium/src/+/2250098) 尚未合并，但它也揭示了附近的共享功能不会局限于桌面上的 Chrome OS。它应该可以在 Windows、macOS 和 Linux 上的谷歌 Chrome 浏览器设置中使用。根据这个[的承诺](https://chromium-review.googlesource.com/c/chromium/src/+/2187614/29)，该功能的网络用户界面将在**chrome://附近的**找到。

回到 Android 版的 Nearby Share，XDA 的米沙·拉赫曼最近分享了该功能最新版本的截图。自从今年早些时候我们第一次展示这个特性以来，用户界面已经有所改进。功能的[图标看起来类似于最近开始出现在 Chrome OS 设置中的图标。](https://twitter.com/MishaalRahman/status/1272655543820320768)

所有这些都表明，谷歌的隔空投送竞争对手将幸运地不仅限于 Android 手机之间的共享。听起来它可以在任何 Android 设备(带有 Google Play 服务)和带有 Google Chrome 桌面浏览器的 PC 之间工作，而不管平台如何。这是一件大事，因为这些选项涵盖了绝大多数互联网用户。虽然我们不确定非 Chromium 浏览器的用户如何加入，但我们仍然很高兴看到 Nearby Share 终于首次亮相。我们已经厌倦了谷歌不断地拿这个功能取笑我们。