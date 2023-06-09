# 谷歌通过新的安卓代码搜索工具让搜索 AOSP 变得更加容易

> 原文：<https://www.xda-developers.com/google-android-code-search-tool-aosp-open-source-project/>

# 谷歌通过新的安卓代码搜索工具让搜索 AOSP 变得更加容易

谷歌宣布了新的 Android 代码搜索工具，使得在 Android 开源项目(AOSP)中搜索代码变得更加容易。继续阅读，了解更多信息！

Android 的源代码驻留在 [Android 开源项目 Git 仓库](https://android.googlesource.com/)中，通过扩展，每个新 Android 版本的[源代码都在这里上传](https://www.xda-developers.com/android-10-source-code-aosp/)。虽然源代码开源并免费提供绝对是一个很大的优势，但迄今为止，在 AOSP 搜索并不是一件轻松愉快的事情。如果你想搜索某些类和方法是如何构造的，你可以克隆库并使用 grep 之类的工具手动搜索，或者你必须依赖在线工具，如 [AndroidXRef](http://androidxref.com/) 或 [Opersys](http://aosp.opersys.com/) 。[谷歌为 Android 开源项目](https://android-developers.googleblog.com/2019/12/code-search-with-cross-references-for-aosp.html)提供了[新的公开 Android 代码搜索工具，使得在 AOSP](https://cs.android.com/) 进行搜索变得更加容易。

克隆 AOSP 和搜索本地版本并不是对每个人都可行的，因为 AOSP 是巨大的并且不断更新。在线工具也不是完美的解决方案，因为它们通常没有用最新的源代码版本进行更新。然而，谷歌的[新 Android 代码搜索工具](https://cs.android.com/)在被合并到[公共 AOSP Git 库](https://android-review.googlesource.com/)之后，就可以使用代码了。这使得它不仅有助于了解 Android 中的某些功能是如何工作的，而且还有助于在错误报告中提供链接，并在非开发设备上进行快速搜索。该工具还集成了交叉引用支持，允许开发人员搜索 AOSP 其他地方何时使用了某个东西。Android 代码搜索工具也支持更高级的搜索工具，你可以在这里找到所有的[文档](https://cs.android.com/static/oss_searching)。

截至目前，Android 代码搜索工具只能搜索 AOSP 的主分支，即 AOSP 的最新版本，这确实存在限制，因为你无法看到 AOSP 在某些其他版本中的表现。然而，谷歌指出，随着时间的推移，该工具将变得更加复杂，因此我们预计它将在未来获得更多的效用。

* * *

**来源:[安卓开发者博客](https://android-developers.googleblog.com/2019/12/code-search-with-cross-references-for-aosp.html)**