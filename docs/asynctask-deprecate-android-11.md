# 谷歌在 Android 11 中贬低 Android 的 AsyncTask API

> 原文：<https://www.xda-developers.com/asynctask-deprecate-android-11/>

多年来，Android 的 AsyncTask 一直是初学者和专家开发者的主要工具。如果你曾经在谷歌上搜索过 Android 中任何一种异步逻辑的教程，很可能前几个结果会建议使用 AsyncTask。这也不是一个随机的选择。AsyncTask 最初是为了简化后台操作和应用程序 UI 之间的交互而创建的。有一段时间，它做得很好。AsyncTask 确实有助于简化异步任务。但这并不意味着它是完美的。

许多应用程序需要做的一件事是从远程服务器获取信息。由于网络请求可能需要一段时间，所以异步处理它们通常很重要，这样它们就不会导致应用程序冻结。操作完成后，可以更新 UI。然而，有可能在网络请求完成时，UI 的相关部分已经不存在了，这会导致崩溃或其他错误。虽然 AsyncTask 确实使整个过程更加简单，但它并不尊重 Android 的应用程序生命周期。这意味着没有内置的保护来防止在 UI 更改后 AsyncTask 结束。当然，手动添加检查和其他保护是可能的，但是这增加了许多重复代码(又名样板)。因为这样的问题，AsyncTask 已经被搁置了。谷歌也没有对其工作方式做出太多改变。

好吧，看起来谷歌的观点是 AsyncTask 是不可救药的。在最近的一次 AOSP 提交中，AsyncTask 被弃用了，理由与我刚才谈到的类似。虽然这对最终用户来说并不是一个巨大的变化，但对开发者来说却意义重大。如果你正在维护一个旧的代码库，或者你刚刚开始使用 Android 中的异步任务，你很可能不得不修改一些代码。不过，幸运的是，谷歌并没有将开发者抛在身后。

由于 AsyncTask 的局限性，替代方案随着时间的推移不断涌现，比如 RxJava 和 Kotlin 的新(ish)协程库。这些替代方法往往比 AsyncTask 更灵活，功能更丰富，所以它们很受欢迎。在反对 AsyncTask 的通知中，Google 推荐使用 Java 的并发框架或 Kotlin 协同程序。

就我个人而言，我已经开始使用 Kotlin 的协同程序，并且没有回头。当然，我知道许多人已经围绕 AsyncTask 紧密地集成了他们的代码，所以这对他们来说可能至少是一个小小的不便。好在有很多选择余地。修改代码可能很烦人，但至少这次是可能的。

如果你想要更多的细节，你可以在这里查看提交[。](https://android-review.googlesource.com/c/platform/frameworks/base/+/1156409)提交在今天早些时候被合并，除非有一个 Android 维护版本在管道中，否则我们将在明年的 Android 11 中看到这一变化。