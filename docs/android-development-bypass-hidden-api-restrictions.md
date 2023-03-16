# 开发者:绕过安卓隐藏的 API 限制超级容易

> 原文：<https://www.xda-developers.com/android-development-bypass-hidden-api-restrictions/>

回到一年多前，我们都很期待看到 Android 测试版的新内容。用户期待着新的功能，开发者也期待着一些新的工具来让他们的应用变得更好。不幸的是，对于其中一些开发者来说，第一个 Android P 测试版带来了一点令人讨厌的惊喜:隐藏的 API 限制。在我深入了解它的确切含义之前，让我解释一下它的背景。

## 这是怎么回事？

Android 应用开发者在做一个应用的时候，不必从头开始。谷歌提供工具，使应用程序开发更容易，更少重复。其中一个工具是 Android SDK。SDK 本质上是对开发者可以在他们的应用中安全使用的所有功能的引用。这些功能是谷歌批准的所有 Android 版本的标准配置。不过，SDK 并不详尽。Android 框架中有相当多的“隐藏”部分不是 SDK 的一部分。

这些“隐藏”的部分对于更粗糙或低级的东西来说非常有用。例如，我的 [Widget 抽屉应用](https://www.xda-developers.com/widget-drawer-access-widgets-anywhere/)利用非 SDK 功能来检测用户何时从 Widget 启动应用，这样抽屉就可以自动关闭。你可能会想:“为什么不把这些非 SDK 功能变成 SDK 的一部分呢？”嗯，问题是他们的运作是不完全可预测的。谷歌无法确保该框架的每一个部分都能在它批准的每一台设备上运行，因此选择了更重要的方法进行验证。谷歌不保证框架的其余部分会保持一致。制造商可以更改或完全删除这些隐藏的功能。即使在 AOSP 的不同版本中，你也不知道一个隐藏的功能是否还会存在，或者像以前一样工作。

如果你想知道为什么我一直使用“隐藏”这个词，那是因为这些功能甚至不是 SDK 的一部分。通常，如果你试图在应用程序中使用隐藏的方法或类，它将无法编译。使用它们需要[反射](https://www.geeksforgeeks.org/reflection-in-java/)或修改的 SDK。

对于 Android P，谷歌认为仅仅隐藏它们是不够的。当第一个测试版发布时，[宣布](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/)大多数(不是全部)隐藏功能不再对应用开发者可用。第一个测试版会在你的应用程序使用黑名单功能时警告你。下一个测试版只是让你的应用崩溃了。至少对我来说，这个黑名单很烦人。它不仅破坏了相当多的[导航手势](https://forum.xda-developers.com/android/apps-games/official-xda-navigation-gestures-iphone-t3792361)，而且由于隐藏功能默认被列入黑名单(谷歌不得不手动将一些每次发布的功能列入白名单)，我在让 Widget Drawer 工作时遇到了很多麻烦。

现在，有几种方法可以绕过黑名单。第一个是简单地保持你的应用以 API 27 (Android 8.1)为目标，因为黑名单只适用于以最新 API 为目标的应用。不幸的是，根据谷歌发布到 Play Store 的最低 API 要求(T1 ), API 27 可能只能发布这么久。[截至 2019 年 11 月 1 日](https://www.xda-developers.com/all-apps-require-target-android-pie-play-store/)，Play Store 的所有应用更新必须针对 API 28 或更高版本。

第二个变通办法实际上是谷歌内置在 Android 中的东西。可以运行 ADB 命令来完全禁用黑名单。这对于个人使用和测试来说非常好，但是我可以直接告诉你，试图让最终用户建立和运行 ADB 是一场噩梦。

那我们该怎么办？如果我们想上传到 Play Store，我们不能再以 API 27 为目标，ADB 方法也不可行。但这并不意味着我们别无选择。

## 隐藏的 API“修复”

隐藏的 API 黑名单仅适用于非白名单用户应用程序。系统应用程序、用平台签名签名的应用程序以及在配置文件中指定的应用程序都不在黑名单中。有趣的是，Google Play 服务套件都是在配置文件中指定的。我想谷歌比我们其他人都要好。

不管怎样，还是继续说黑名单吧。我们今天感兴趣的部分是系统应用程序是免税的。这意味着，例如，系统 UI 应用程序可以使用它想要的所有隐藏功能，因为它在系统分区上。显然，我们不能只把一个 app 推送到系统分区。这需要 root，一个好的文件管理器，权限知识....使用亚行会更容易。这不是我们成为系统应用的唯一方式，至少就隐藏的 API 黑名单而言。

回想一下七段前我提到反思的时候。如果你不知道什么是反思，我推荐你阅读[这一页](https://www.geeksforgeeks.org/reflection-in-java/)，但这里有一个快速总结。在 Java 中，反射是一种访问通常不可访问的类、方法和字段的方式。这是一个非常强大的工具。就像我在那段中说的，反射曾经是访问非 SDK 函数的一种方式。API 黑名单阻止了反射的使用，但是并没有阻止*双*-反射的使用。

现在，事情变得有点奇怪了。通常，如果你想调用一个隐藏的方法，你应该这样做(这是在 Kotlin 中，但 Java 是类似的):

```
 val someHiddenClass = Class.forName("android.some.hidden.Class")
val someHiddenMethod = someHiddenClass.getMethod("someHiddenMethod", String::class.java)

someHiddenMethod.invoke(null, "some important string")

```

不过，多亏了 API 黑名单，您只能得到一个 ClassNotFoundException。然而，如果你反思两次，就没问题了:

```
 val forName = Class::class.java.getMethod("forName", String::class.java)
val getMethod = Class::class.java.getMethod("getMethod", String::class.java, arrayOf<Class<*>>()::class.java)
val someHiddenClass = forName.invoke(null, "android.some.hidden.Class") as Class<*>
val someHiddenMethod = getMethod.invoke(someHiddenClass, "someHiddenMethod", String::class.java)

someHiddenMethod.invoke(null, "some important string")

```

很奇怪吧？嗯，是的，但也不是。API 黑名单跟踪谁在调用一个函数。如果源没有被豁免，它就会崩溃。在第一个例子中，来源是应用程序。然而，在第二个例子中，源是系统本身。我们不是用反射直接得到我们想要的东西，而是用它来告诉系统得到我们想要的东西。由于隐藏函数的调用来源是系统，黑名单不再影响我们。

所以我们结束了。我们现在有办法绕过 API 黑名单了。这有点笨拙，但是我们可以写一个包装函数，这样我们就不必每次都进行双重反射。不算很棒，但是聊胜于无。但实际上，我们还没完。有一种更好的方法可以让我们使用普通的反射或者修改过的 SDK，就像以前一样。

由于黑名单的执行是按进程评估的(在大多数情况下，这与按应用相同)，因此系统可能有某种方法来记录有问题的应用是否被豁免。幸运的是，确实有，而且我们也能接触到。使用新发现的双反射技术，我们得到了一个一次性使用的代码块:

```
 val forName = Class::class.java.getDeclaredMethod("forName", String::class.java)
val getDeclaredMethod = Class::class.java.getDeclaredMethod("getDeclaredMethod", String::class.java, arrayOf<Class<*>>()::class.java)

val vmRuntimeClass = forName.invoke(null, "dalvik.system.VMRuntime") as Class<*>
val getRuntime = getDeclaredMethod.invoke(vmRuntimeClass, "getRuntime", null) as Method
val setHiddenApiExemptions = getDeclaredMethod.invoke(vmRuntimeClass, "setHiddenApiExemptions", arrayOf(arrayOf<String>()::class.java)) as Method

val vmRuntime = getRuntime.invoke(null)

setHiddenApiExemptions.invoke(vmRuntime, arrayOf("L"))

```

好吧，所以从技术上来说，这并不是告诉系统我们的应用程序从 API 黑名单中豁免。实际上，您可以运行另一个 ADB 命令来指定不应该列入黑名单的函数。这就是我们在上面所利用的优势。代码基本上覆盖了系统认为对我们的应用程序豁免的任何内容。在末尾传递“L”意味着所有方法都被豁免。如果您想要免除特定的方法，请使用 Smali 语法:`Landroid/some/hidden/Class;Landroid/some/other/hidden/Class;`。

现在我们真的完成了。创建一个定制的应用程序类，将代码放入`onCreate()`方法中，然后就没有任何限制了。

* * *

感谢 XDA 会员舒威，虚拟曝光和太极的开发者，最初发现这个方法。我们还要感谢 XDA 公认的开发者 topjohnwu 为我指出了这个变通办法。这里有更多关于它如何工作的信息，虽然是中文的。我也[写了关于栈溢出的文章](https://stackoverflow.com/questions/55970137/bypass-androids-hidden-api-restrictions/55970138#55970138)，还有一个 JNI 的例子。