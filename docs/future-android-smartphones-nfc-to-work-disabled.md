# 未来的 Android 智能手机可能允许 NFC 工作，即使用户关闭它

> 原文：<https://www.xda-developers.com/future-android-smartphones-nfc-to-work-disabled/>

NFC 生态系统一直在稳步发展，但仍有许多工作要做。在西方市场，由于基于 NFC 的支付解决方案，如 [Google Pay](https://www.xda-developers.com/google-google-pay-android-pay-google-wallet-unified-brand/) (以前的 Android Pay)，NFC 的使用越来越多。然而，在印度等国家，由于缺乏令人信服的使用案例，NFC 的使用仍然不存在。总的来说，[基于 NFC 的支付解决方案在许多发展中国家都没有使用](https://www.xda-developers.com/tez-google-payment-system-india/)。虽然 NFC 确实有更多涉及文件传输和自动化任务的用例，但这些任务可以通过替代技术更好地完成。

然而，这并不是说 NFC 不重要。如今，所有旗舰智能手机都支持 NFC，越来越多的中档和经济型智能手机也开始支持 NFC。自 2011 年以来，Android 本身就支持 NFC，尽管从那以后，我们没有看到 Android 中有多少 NFC 功能的重大增加。这在未来可能会改变，因为我们在 Android 开源项目中发现的新提交[表明 NFC HAL 正在更新，具有一些潜在的有趣含义。](https://android-review.googlesource.com/q/topic:NFC1.1+(status:open+OR+status:merged))

硬件抽象层(HAL)允许 Android 框架(OS)与底层硬件接口。在这种情况下，NFC HAL 允许 Android 与 NFC 芯片一起工作。

这里的新内容是 HAL 正在更新，支持“**断电用例**”如提交中所述，这允许 NFC 工作**，即使用户关闭它**。这些承诺提到了 NFC 断电期间需要的“供应商特定配置”，但没有详细说明这些配置可能是什么。

这种新的 NFC 断电状态很可能在低电池条件下工作良好，并且更加省电。即使用户已经关闭了 NFC，他们也不太可能特别希望 NFC 工作，但操作系统现在将能够区分用户因为不想使用 NFC 而关闭 NFC 的情况和由于设备关闭而关闭 NFC 的情况。

即使用户禁用了该选项，这也不会是第一个起作用的功能，因为 Android 在位置服务中有一个 Wi-Fi/蓝牙扫描，可以保持这些无线电活动，但不允许建立连接。移动支付也有可能发生类似的事情。例如，如果用户意外关闭了 NFC，那么他们仍然可以通过 Google Pay 进行支付(尽管显然完成支付需要用户认证。)

不过，目前这只是猜测，因为关闭 NFC 用例的细节还没有明确。我们期望在未来了解更多。