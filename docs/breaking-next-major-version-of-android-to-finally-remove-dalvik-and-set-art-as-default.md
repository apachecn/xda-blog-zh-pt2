# 下一个版本的 Android 将删除 Dalvik，并使艺术默认

> 原文：<https://www.xda-developers.com/breaking-next-major-version-of-android-to-finally-remove-dalvik-and-set-art-as-default/>

# 突破:Android 的下一个主要版本将最终删除 Dalvik 并将 ART 设置为默认！

Android 的下一个主要版本将最终移除 Dalvik 并将 ART 运行时编译器设为默认！

达尔维克走了，艺术运行时编译器默认

自从我们[第一次看到 ART](http://www.xda-developers.com/android/new-runtime-compiler-in-android-4-4/ "BREAKING: New Runtime Compiler in Android 4.4 to Possibly Bring Better Performance in Future Releases") 伴随着 Android 4.4 KitKat 的发布出现，我们都知道它最终会取代老化且相对低效的 Dalvik 运行时编译器。好吧，伙计们，现在是时候了，因为昨晚晚些时候提交给 AOSP 主分支显示达尔维克得到斧头和艺术被设置为默认。

正在讨论的变更是以合并提交的形式出现的 [98553](https://android-review.googlesource.com/98553) 和 [98618](https://android-review.googlesource.com/98618) 。前者负责将 Dalvik 从 AOSP 主分支中移除，后者将默认运行时编译器切换到 ART

下面可以看到他们辉煌的变化:

> | 
> 
> 达尔维克已死，达尔维克万岁！不合并
> 
> croot
> 
> CD libcore
> 
> 回购启动 dal vik-is-dead-long-live-dal vik。
> 
> repo sync-c .
> 
> git RM-r libdvm
> 
> git add Java library . MK(删除 libdvm 引用后，添加 explict core-libart 引用)
> 
> git add Docs.mk(用 libart 替换对 lib dvm 的引用后)
> 
> git add benchmarks/Android . MK(添加 explict core-libart 引用后)
> 
> git add Android.mk(删除后
> 
> 不合并 |
> 
> | 
> 
> 从内核切换到内核-libart
> 
>  |

伙计们，合并是不言自明的。达尔维克死了，达尔维克万岁！从艺术在过去几个月里变得如此可行来判断，Dalvik 可能不会被错过——至少在 XDA 资深公认开发者 rovo89 发布了一个与艺术兼容的 build Xposed 框架后不会。:)

*【来源:AOSP 代码审查(变更 [98553](https://android-review.googlesource.com/98553) 和[98618](https://android-review.googlesource.com/98618))】*