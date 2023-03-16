# Android 10 允许开发者在卸载之前询问用户是否想要保留应用数据

> 原文：<https://www.xda-developers.com/android-10-manifest-flag-developers-retain-app-data-before-uninstalling/>

Android 10 是谷歌对 Android 的最新更新，带来了对成熟操作系统的一些[改进。最新更新中的大多数变化和新功能要么在 Google I/O 期间被 Google 自己突出显示](https://www.xda-developers.com/android-10-new-features-video/)，要么在[公共源代码发布](https://www.xda-developers.com/android-10-source-code-aosp/)后不久被发现[。但是一些显著的变化往往会被忽略，几个月后当有人偶然发现它们时，这些变化就会浮出水面。这就是在这种情况下发生的事情，因为事实证明，Android 10 允许开发者在卸载应用程序之前询问用户是否希望保留应用程序数据。](https://www.xda-developers.com/google-android-10-dsu-try-ota-updates-without-committing/)

最近来自*和*T3 的[报告强调了这一功能。像](https://www.androidpolice.com/2019/11/06/some-apps-like-whatsapp-offer-to-save-app-data-when-uninstalled-in-android-10/) [WhatsApp](https://play.google.com/store/apps/details?id=com.whatsapp) 和 [ASR Voice Recorder](https://play.google.com/store/apps/details?id=com.nll.asr) 这样的应用已经开始向 Android 10 用户提供保留即将卸载的应用数据的选项。

选中上面显示的复选框，尽管应用程序被卸载，但仍会保留手机上的应用程序数据。当您重新安装应用程序时，您将回到应用程序中的相同状态，就像您从未在第一时间卸载它一样。

米莎尔对幕后发生的事情做了一些调查。要理解这一点，你首先需要了解 Android 上的应用程序如何在你的设备上存储文件，存储文件有三个主要位置:

*   内部存储(没有 root 用户无法访问)中的特定于应用程序的目录:这些文件夹位于 */data/data* 中，其他应用程序无法访问，或者用户通常将手机插入 PC 时也无法访问。在这个位置，应用程序不需要将文件写入它们自己的应用程序特定目录的权限。
*   外部(用户可访问)存储中的应用程序特定目录:这些文件夹位于*/data/media/{ user }/Android/data*中，其他具有适当权限的应用程序可以访问这些文件夹，当用户通常将手机连接到计算机时，用户也可以访问这些文件夹。应用程序不需要权限就可以将文件写入到该位置的应用程序专用目录中，但是它们需要权限才能从其他应用程序访问数据，如前所述。
*   外部(用户可访问)存储中的任何目录:应用程序可以请求访问外部存储的权限，允许应用程序在外部存储上创建任何需要的文件夹，以存储任何想要存储的内容。

延伸 WhatsApp 的例子，WhatsApp 在内存中的 App 专用目录驻留在*/data/data/com . WhatsApp*；其在外存中的 app 专用目录驻留在*/data/media/{ user }/Android/data/com . whatsapp*；而它在外存的自定义目录驻留在*/data/media/{ user }/WhatsApp*。

在 Android 10 和之前，在开发人员为他们的应用程序启用此功能之前，当用户卸载应用程序时，默认情况下会删除内部(*/数据/数据*)和外部(*/数据/媒体*)存储中的应用程序特定目录。外部存储上的额外目录不会被删除，您需要手动清除它们或使用类似于 [SD Maid](https://play.google.com/store/apps/details?id=eu.thedarken.sdm) 的应用程序来为您完成。

使用 Android 10，应用程序开发人员可以在他们的清单中添加一个特殊的标志，名为“*[hasFragileUserData](https://developer.android.com/reference/android/R.attr#hasFragileUserData)*”，允许他们在应用程序卸载时询问用户是否希望保留应用程序的数据，这就是你在上面的截图中看到的。当你卸载一个应用程序并选中复选框以保留应用程序数据时，Android 将保留而不是删除内部和外部存储中的应用程序特定目录。我们通过检查没有添加清单标志的应用程序的目录，以及像 WhatsApp 这样添加了清单标志的应用程序的目录来确认这一点。

* * *

从表面上看，拥有这个选项是有意义的，因为用户可以暂时卸载应用程序，并在重新安装时回到之前的状态，这应该可以省去在同一设备上备份和恢复应用程序的一些麻烦。但是，请记住，没有 root 用户是无法访问 */data/data* 的，因此作为用户，您无法跨设备使用此过程进行无 root 用户备份和恢复。没有 root 用户也无法删除遗留在 */data/data* 中的文件；因此，如果你想在未来清除这些文件，你需要重新安装该应用程序，然后卸载它而不勾选复选框。对太多的应用程序使用这个选项，你可能会忘记你作为用户选择了哪些应用程序。因为开发者可以选择加入，用户也可以选择加入，所以我们认为这是一个总体上积极的变化，给了最终用户更多的权力。