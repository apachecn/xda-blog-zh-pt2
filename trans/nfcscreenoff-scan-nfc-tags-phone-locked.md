# 当你的安卓手机锁定时，NFC 屏幕关闭模式可以扫描 NFC 标签

> 原文：<https://www.xda-developers.com/nfcscreenoff-scan-nfc-tags-phone-locked/>

# 当你的安卓手机锁定时，NFC 屏幕关闭模式可以扫描 NFC 标签

NFCScreenOff 是一个 Magisk 模块，即使在 Android 智能手机锁定的情况下，也可以扫描 NFC 标签。点击此处了解更多信息！

你有没有想过在手机屏幕关闭的情况下也能扫描 NFC 标签？这是不可能的，因为这样做有安全风险——想象一下，如果有人可以在屏幕关闭时从你的智能手机触发移动支付？还有其他安全风险，但底线是，无论如何，当你的智能手机屏幕关闭时，不可能激活和读取 NFC 标签。也就是说，没有 root 访问权限。XDA 成员的 NFC screen off[lap wat](https://forum.xda-developers.com/member.php?u=6471406)是一个 Magisk 模块，你可以在你的手机上启用它，即使你的屏幕被锁定，它也可以始终读取 NFC 标签。

虽然这可能对那些在家中使用 NFC 标签实现自动化的人有用，但你不能在店内使用它进行非接触式支付，因为它会破坏 [SafetyNet](https://www.xda-developers.com/google-pay-tests-safetynet-status-protecting-online-purchases-pin/) 。它不是无系统的修改，因为它直接修补和修改系统 NfcNci.apk，以便在轮询屏幕是否解锁时总是返回 true。它应该可以在大多数 Android 9 和 Android 10 设备上运行，尽管它可能无法在特定的智能手机上运行。开发者希望在未来，mod 可以实现无系统化，以支持移动支付。

如果你想安装 NFCScreenOff Magisk 模块，你可以查看下面的 XDA 线程和 GitHub 库。您可以像对任何其他模块一样简单地刷新 Magisk 模块！

**[nfcscreenov XDA 线程](https://forum.xda-developers.com/apps/magisk/module-nfcscreenoff8-t4034903)|****[nfcscreenov GitHub](https://github.com/Magisk-Modules-Repo/NFCScreenOff)**