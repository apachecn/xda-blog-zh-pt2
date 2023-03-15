# Android 13 将允许用户甚至在锁定的手机上使用一些设备控制

> 原文：<https://www.xda-developers.com/android-13-smart-home-device-controls-unlocking/>

在 Android 11 中，谷歌引入了一个新功能，帮助用户快速控制他们的智能家居设备。该功能添加了设备控制快速设置磁贴和锁屏快捷方式，让用户无需打开应用程序即可控制他们的智能家居设备。但要使用快速设置磁贴或锁屏快捷方式，用户首先必须解锁他们的设备。这给该过程增加了一个不必要的步骤，对于总是锁定设备的用户来说，这种实现不太理想。令人欣慰的是，据报道，谷歌正在进行一项改变，将允许用户在 Android 13 中无需解锁手机即可访问设备控制。

据*斯珀*报道，Android 13 DP2 引入了一种新的 API，可以控制你是否需要解锁你的设备来控制智能家居设备。Google 关于新的 isAuthRequired 方法的文档指出，如果该方法返回“true”，则相关联的设备控件不可用，直到设备被解锁。

利用这些信息，XDA 高级会员兼 Tasker 开发者 [joaomgcd](https://forum.xda-developers.com/m/joaomgcd.4805489/) 为自动化应用程序添加了一个新的开关，允许用户创建一个自定义的设备控制，即使在设备锁定时也可以使用。查看下面嵌入的视频，了解它的实际应用。

*斯珀*进一步指出:*“由于这种行为可以按控件设置，应用程序可以阻止用户在手机锁定时与某些智能家居设备进行交互。”*

虽然该功能在最新的 Android 13 开发者预览版中可用，但谷歌尚未更新 Google Home 应用程序来支持该功能。因此，我们必须等待一段时间，才能在锁定的手机上访问启用助手的设备的设备控制。

值得一提的是，该功能不会让用户选择在手机锁定时可以使用哪些设备控制。相反，应用程序开发人员将不得不选择某些设备控制是否可以在锁定的手机上使用。因此，在开发人员更新他们的应用程序以支持该功能之前，该功能将不可用。

* * *

**来源:** [谷歌](https://developer.android.com/reference/android/service/controls/Control#isAuthRequired())

**Via:** [斯珀](https://blog.esper.io/android-dessert-bites-17-control-devices-without-auth-19481628/)