# 谷歌取消了未认证设备页面上 100 台设备的注册限制

> 原文：<https://www.xda-developers.com/google-removes-100-device-registration-limit-uncertified-device-page/>

# 谷歌取消了未认证设备页面上 100 台设备的注册限制

我们最近了解到，谷歌将开始阻止任何未经认证的设备访问 Google Play 应用和服务。我们现在有了新的信息:用户现在可以注册的白名单不再有 100 个设备的注册限制！

今天对 Android 社区来说是个好消息:谷歌已经听到了我们的担忧。当我们第一次爆料谷歌将[开始阻止 Google Play 未经认证的设备访问谷歌应用和服务](https://www.xda-developers.com/google-blocks-gapps-uncertified-devices-custom-rom-whitelist/)时，对于这对用户来说意味着什么，有很多困惑。起初，网页似乎根本无法工作，然后它使用 IMEI 值工作，*然后*我们被告知它接受 Google Play 服务框架设备 ID(但*只接受十进制格式*)。用户，尤其是开发人员，关心的最后一件事是这个页面似乎只允许 100 个 id 加入白名单。然而，一名谷歌代表已经证实，他们正在从[未经认证的设备注册页面](https://www.google.com/android/uncertified/)中移除这一限制，并且该网页现在**接受原始十六进制格式的 GSF id**。

Google Play 服务框架设备 ID(简称 GSF ID)是由 Google Play 服务生成的唯一设备标识符。有人担心，通过擦除你的设备(这种情况经常发生在测试 rom 的开发人员和经常刷新新 rom 的用户身上)，你最终会浪费一个用于将你的设备列入白名单的令牌。在白名单页面上，目前没有办法删除活跃的设备注册，所以人们担心，如果用户不想意外填充列表，他们将不得不保存他们的 GSF id。

然而，现在官方的未认证设备页面已经取消了 100 个设备注册的限制，再也不用担心令牌用完了。你可以在你的谷歌账户下注册和重新注册，次数不限。这是谷歌的一个好举措，因为它解决了社区对该表单的主要担忧，同时仍保持了其最初的目的:防止设备制造商绕过谷歌的 CTS，并在不应该的时候预装谷歌应用和服务。

如果你感兴趣，我们已经用这个新信息更新了关于[如何修复未认证设备错误的教程。如果有任何与未认证设备注册页面相关的新进展，我们一定会通知大家。](https://www.xda-developers.com/how-to-fix-device-not-certified-by-google-error/)