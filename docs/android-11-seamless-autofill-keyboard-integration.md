# Android 11 通过键盘集成使自动填充更加无缝

> 原文：<https://www.xda-developers.com/android-11-seamless-autofill-keyboard-integration/>

从 Android 9 Pie 开始，Android 就有了自动填充 API，使得填写保存的地址和密码变得更加容易。不过，Android 的自动填充体验并不像 iOS 那样无缝。在 Android 上，自动填充建议显示在输入框附近，而在 iOS 上，它们显示在键盘正上方。随着 Android 11 的到来，谷歌正在修改自动填充功能，以便与键盘集成更加无缝。具体来说，他们增加了出现在键盘正上方的内嵌自动填充建议。

谷歌首先在 Android 11 Beta 1 的同时宣布了这项功能，但几天前，他们发布了一个开发者页面，更详细地解释了它的工作原理。正如[在谷歌的新开发者页面上对功能](https://developer.android.com/preview/features/ime-autofill)(首先由 [*和安卓警察*](https://www.androidpolice.com/2020/08/10/android-11-will-make-password-autofill-much-better-thanks-to-keyboard-integration/) 发现)的解释:

> 从 Android 11 开始，键盘和其他输入法编辑器(ime)可以在建议条或类似的东西中显示自动填充建议，而不是系统在下拉菜单中显示这些。由于这些自动填充建议可能包含私人数据，如密码或信用卡信息，因此这些建议在用户选择之前对 IME 是隐藏的。

ime 和密码管理器都需要更新，以利用新的内嵌自动填充建议功能。ime 的开发人员和密码管理员需要将 supportsInlinedSuggestions 属性设置为 true。如果 IME 或密码管理器不支持内嵌自动填充，则系统退回到旧的自动填充建议样式，其中建议显示在下拉菜单中。

Android 11 新的内嵌自动填充建议功能使填写表格、多因素验证码、智能回复和搜索查询更加无缝。

然而，由于 Android 11 仍未推出，大多数用户可能在一段时间内不会看到这一改进的自动填充 UI。Google 至少已经[在 Jetpack 的自动填充 API 中引入了](https://medium.com/androiddevelopers/whats-new-in-jetpack-1891d205e136#cbe2:~:text=Auto%2Dfill%20IME%20integrations)InlineSuggestionUI 类，以使开发者更容易实现内联自动填充建议。最新的 1Password 测试版与 Google 的 Gboard 应用程序相结合，支持这一新的 API。希望其他 ime 和密码管理器的开发人员实现这个漂亮的新自动填充 API。