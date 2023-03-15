# Android Oreo 允许应用程序读取来自运营商的 USSD 信息

> 原文：<https://www.xda-developers.com/android-oreo-ussd-codes-carriers/>

USSD 是一种通过 GSM 发送数据的协议，类似于 SMS。它最常用于回拨服务，检查数据/分钟，互动新闻，铃声销售，甚至支付方式。这是一种在智能手机和功能手机中普遍可用的基本服务，其可靠性是 USSD 自 1991 年首次实施 GSM 以来没有发生一点变化的主要原因。虽然它们一直存在于任何 Android 拨号器应用程序中，但 USSD 消息总是以对话框或基本的系统主题菜单的形式出现。至少到目前为止，没有其他应用程序可以与这些 USSD 消息进行交互。

Android Oreo 增加了一个新类**允许应用程序与 USSD 请求**交互。电话经理。UssdResponseCallback 类用于在网络成功完成 USSD 请求时，或者在完成请求时出现故障时，通知 sendUssdRequest 的调用方。在这些情况下，如果请求成功完成，将调用 onReceiveUssdResponse，如果请求失败，将调用 onReceiveUssdResponseFailed。

虽然系统仍将使用现有实现管理所有 USSD 消息，但这应该是应用程序开发人员开始与 USSD 请求交互的起点。考虑到在以前的 Android 版本中，读取 USSD 消息的唯一方式是实现一个[高性能的可访问性服务](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)来读取所有窗口内容，这个新的 API 现在是一个更干净的访问这些消息的方式。

目前 USSD 协议还没有替代品，考虑到你的运营商通过 USSD 码提供了多少关于你的移动计划的信息，这个新的 API 在未来会有很大的用处。例如，阅读 USSD 代码响应比安卓的本地数据报告系统提供了更准确的信息。这是因为原生系统不能考虑到一些细微差别，如 [T-Mobile 的狂欢](https://support.t-mobile.com/docs/DOC-4041)功能。

你可以在 Android Developers 网站查看这个类的文档和用法，这样你就可以开始修改它，并把它部署到你的应用上。Android Oreo 引入了许多小而重要的新的、未公开的变化和 API，我们会随时通知你我们发现的任何其他东西。