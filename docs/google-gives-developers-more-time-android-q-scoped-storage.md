# 谷歌给开发者更多的时间来升级他们的应用程序，以遵守 Android Q 的范围存储要求

> 原文：<https://www.xda-developers.com/google-gives-developers-more-time-android-q-scoped-storage/>

不可避免的是，每一个新的 Android 版本都有一些变化，一些开发者并不太喜欢。Android Q 最大的变化之一是“作用域存储”，，它从根本上改变了应用程序访问手机外部存储的方式。谷歌曾计划限制所有不遵守作用域存储带来的变化的应用程序，但现在他们已经有点退缩了。

在 Android Q 之前，如果他们请求 READ_EXTERNAL_STORAGE 和 WRITE_EXTERNAL_STORAGE 权限，任何应用程序都可以读取或写入任何文件到外部存储(当你将手机插入 PC 时可以看到的文件)。你可能已经注意到应用程序把你的存储塞满了文件，这也是一个隐私/安全问题。作用域存储旨在解决所有这些问题。

谷歌计划让它在 Android Q 中默认情况下只能访问外部存储中自己的数据文件夹(位于/data/media/{user}/Android)。要访问音乐或图像等共享媒体，他们必须请求特定于这些用例的新权限。需要广泛访问外部存储的应用程序，如文件管理器，如果想要继续广泛访问存储，必须从使用 Java APIs 切换到[存储访问框架](https://developer.android.com/guide/topics/providers/document-provider)。

开发人员抱怨这一变化，因为他们觉得谷歌没有给他们足够的时间来做出所有必要的改变，以使用存储访问框架。由于作用域存储会影响 Android Q 上运行的所有应用程序，无论该应用程序是否真的针对 Android Q，开发人员别无选择，只能更新他们的应用程序。否则，当用户试图在下一个 Android 版本上使用他们的应用程序时，他们的应用程序就会被破坏。

好消息是，谷歌已经听取了开发者的反馈，因为 Android Q 将不再对针对 Android Pie 的应用强制实施范围存储。由于[要求以最近的 API 级别](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)为目标，2020 年 8 月 1 日之后发布到谷歌 Play 商店的新应用必须以 Android Q 为目标，而 2020 年 11 月 1 日之后发布的现有应用的更新也必须以 Android Q 为目标。所有这一切意味着开发人员现在必须在 2020 年 8 月或 11 月之前根据 Android Q 的新范围存储修改他们的应用，这应该有足够的时间进行所需的更改。你可以[在这里](https://developer.android.com/preview/privacy/scoped-storage)了解更多关于作用域存储的信息。

* * *

[**来源:安卓开发者**](https://android-developers.googleblog.com/2019/04/android-q-scoped-storage-best-practices.html)

米莎尔·拉赫曼的意见。