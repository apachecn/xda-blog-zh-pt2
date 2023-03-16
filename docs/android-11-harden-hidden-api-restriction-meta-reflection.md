# Android 11 将强化隐藏的 API 限制，并移除元反射

> 原文：<https://www.xda-developers.com/android-11-harden-hidden-api-restriction-meta-reflection/>

对于那些不知道的人来说，谷歌在 Android 9 Pie 中引入了一个相当恼人的变化，这涉及到那些希望推动 Android 可能性边界的狂热开发者。当然，我说的是添加隐藏的 API 黑名单。为了促进应用程序的稳定性，谷歌阻止了对大多数隐藏 API 的访问——这些 API 存在于 Android 框架中，但没有记录在 Android SDK 中。在 Android 9 Pie 之前，这些 API 可以通过反射来访问，目前，仍然可以使用元反射工作区来访问。

如果你不知道我在说什么，你可能应该[看看我几个月前写的关于这个话题的文章。它将解释你需要知道的关于元反射及其工作原理的一切。不幸的是，看起来谷歌注意到了这个变通办法(哎呀)。在对 AOSP 的新承诺中，谷歌引入了代码来“强化”Android 的隐藏 API 检查。这基本上意味着元反射将不再工作。](https://www.xda-developers.com/android-development-bypass-hidden-api-restrictions/)

当然，这不会影响所有的 app。就像最初的 API 黑名单一样，只有针对 Android 11 (API 级别 30)或更高版本的应用才会受到影响。您仍然可以将 API 级别 29 或更低作为目标，并使用元反射。随着 Play Store 的[逐渐提高最低目标 SDK 要求](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)，这将不会是一个长期有效的解决办法。

目前，我还不知道任何针对 API 30 的应用程序的解决方法。然而，Android 11 还有很长的路要走，所以很有可能有人会找到恢复访问的方法。与此同时，如果你正在使用隐藏的 API，你可能想申请在 Android 11 中公开它们。如果你擅长分析 C++和 Java，并且你想尝试“修复”这个小小的黑名单情况，[看看相关的提交](https://android-review.googlesource.com/c/platform/art/+/1203343)。