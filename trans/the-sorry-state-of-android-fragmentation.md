# Android 碎片化的可悲状态:理解开发者困境的一个例子

> 原文：<https://www.xda-developers.com/the-sorry-state-of-android-fragmentation/>

自从移动操作系统 Android 发布以来，碎片化就一直是一个有争议的问题。

除了成为网络火拼中的一根大棒，碎片化带来的多样性现在在很大程度上被视为安卓设备消费者的一个积极因素。毕竟，我们被给予了如此多的自由来选择我们想要的那种设备和那种软件，以至于普通消费者很难关心碎片化。可视化令人难以置信的各种 Android 设备产生了一个美丽的 Android 多样化表现的马赛克。

 <picture>![An Example of Android Device Fragmentation based on App Installations of OpenSignal's app. Source: OpenSignal](img/d55772590c83a2e9b8bd5bce12d7b7d0.png)</picture> 

An Example of Android Device Fragmentation based on App Installations of OpenSignal's app. Source: [OpenSignal](https://opensignal.com/reports/2015/08/android-fragmentation/)

但是硬件和软件的分裂并不会让软件开发者快乐。事实上，恰恰相反。在这么多不同的硬件和软件配置上开发一个应用程序在调试时可能会被证明是一件非常麻烦的事情。在开发应用程序时，原始设备制造商可以做出需要考虑的重大或细微的改变，但对于单个开发人员来说，确实没有简单的方法来确保他们的应用程序能够通用。虽然普通消费者早就忘记了碎片化的争论，但这个问题仍然困扰着 Android 应用程序开发人员，除了接受它并在出现错误时处理它们之外，似乎没有什么可以做的。

* * *

**令人遗憾的分裂状态**

有一家 OEM 厂商尤其因为在开发应用程序时引起的麻烦而受到了很多人的憎恨——三星。开发人员多年来一直在咆哮三星，有些人甚至写了一些严厉的文章，如“[Android Hell](http://verybadalloc.com/android/2015/12/19/special-place-for-samsung-in-android-hell/)中有一个三星的特殊位置”，描述了一个源于[三星设备和支持 appcompat 库](https://code.google.com/p/android/issues/detail?id=78377)的特别令人沮丧的错误。我想特别提请注意 Ambri 先生咆哮中的一段话，这段话很好地概括了为什么开发人员仍然关心碎片化:

> 如果你是安卓开发者，你对三星设备的仇恨大概是无边无际的。对于一个普通用户来说，三星是愚蠢的触摸工具和过度膨胀的 T2 的代名词，你鄙视三星是因为你别无选择。因为三星[巨大的市场份额](http://www.cnet.com/news/samsung-continues-to-rule-over-apple-in-smartphone-market/)，你根本无法选择不支持三星设备。而这才是最伤人的；事实是这个选择被剥夺了！

这也不是对 Android 存在的旧时代的咆哮——这篇文章发表于去年 12 月中旬。我将坦率地说，我不确定这个问题是否已经正式修复，但是，Ambri 先生已经在他的帖子中为任何通过谷歌搜索这个漏洞偶然发现他的咆哮的人提供了修复。你所要做的就是用下面的单行代码使用 [ProGuard](http://proguard.sourceforge.net/) :

 `还不算太糟，是吗？然而，问题是这个修复是从堆栈溢出中取出的。别误会，Stack Overflow 是个很棒的网站。但它并不是发现应用程序补丁的理想来源。在 Stack Overflow 上找到一些东西通常需要在多次试错的谷歌搜索后深入链接。有时你甚至会发现另一个用户提到了你遇到的同一个 bug，但是看不到修复的迹象。或者更令人沮丧的是，当你发现一个帖子时，发帖者声称已经找到了一个修复方法，但他们很久以前就放弃了他们的帖子，没有告诉其他人如何修复这个问题。

 <picture>![](img/433168b44aa018cdb7132efee083f82b.png)</picture> 

Source: XKCD

* * *

**一个微妙碎片问题的例子**

我自己并不是一名开发人员，但是经过多年在 Tasker 中的修补，我对 Android 的功能已经足够熟悉，我已经开始对我所面临的问题编写自己的解决方案。当我想不出什么的时候，我会像其他人一样去谷歌一下。当我在写我的上一篇关于[挖掘你的手机设置应用程序的隐藏活动](http://www.xda-developers.com/heres-how-to-access-hidden-settings-on-your-phone/)的文章时，我遇到了一个我无法解释的相当奇怪的错误。华为设备特有的一个 bug。

每当我试图在设置应用程序中启动某些活动(如包含应用程序使用统计数据的“测试”菜单)，我总是会遇到权限错误。特别是，我用来启动活动的应用程序缺少权限**Huawei . Android . permission . HW _ SIGNATURE _ OR _ SYSTEM。**我测试的其他设备都不需要任何独特的权限来启动这些设置活动，只有运行华为版本 Android (EMUI)的手机才需要。对 *com.android.settings* 的分析显示，设置应用中的某些活动确实处于需要[签名或系统许可](https://developer.android.com/guide/topics/manifest/permission-element.html)的保护级别之下。

对我来说不幸的是，这意味着只有安装在/system 下的应用程序或使用与 Settings 应用程序相同的签名签名的应用程序才能使用我尝试的方法打开这些活动。当我谷歌搜索这个错误的答案时，我(你猜对了)遇到了一个[堆栈溢出线程](https://stackoverflow.com/questions/28321686/permission-denial-with-action-pick-activity)。发布他的问题的开发人员遇到了和我一样的问题(尽管他实际上正在开发一个应用程序)。当他试图运行以下代码时，他的问题出现了:

```
 <span >Intent</span><span > mainIntent </span><span >=</span> <span >new</span> <span >Intent</span><span >(</span><span >Intent</span><span >.</span><span >ACTION_MAIN</span><span >,</span> <span >null</span><span >);</span><span >mainIntent</span><span >.</span><span >addCategory</span><span >(</span><span >Intent</span><span >.</span><span >CATEGORY_LAUNCHER</span><span >);</span><span >Intent</span><span > pickIntent </span><span >=</span> <span >new</span> <span >Intent</span><span >(</span><span >Intent</span><span >.</span><span >ACTION_PICK_ACTIVITY</span><span >);</span><span >pickIntent</span><span >.</span><span >putExtra</span><span >(</span><span >Intent</span><span >.</span><span >EXTRA_TITLE</span><span >,</span> <span >"Pick App to Play in"</span><span >);</span><span >pickIntent</span><span >.</span><span >putExtra</span><span >(</span><span >Intent</span><span >.</span><span >EXTRA_INTENT</span><span >,</span><span > mainIntent</span><span >);</span><span >this</span><span >.</span><span >startActivityForResult</span><span >(</span><span >pickIntent</span><span >,</span><span > REQUEST_PICK_APPLICATION</span><span >);</span> 
```

从意图中的字符串和开发者的网页判断，他可能试图允许用户选择第三方应用程序来播放一些媒体。由资深开发者 [CommonsWare](https://stackoverflow.com/users/115145/commonsware) 提供的修复非常简单:使用[意图。CreateChooser](https://developer.android.com/training/sharing/send.html) 而不是 [ACTION_PICK_ACTIVITY](https://developer.android.com/reference/android/content/Intent.html#ACTION_PICK_ACTIVITY) 。然而，*为什么*我们需要实现这个修复？*为什么*华为首先需要这种许可？*为什么*我们需要通过使用非常具体的谷歌搜索在 StackOverflow 上找到答案？

* * *

**选择的悖论**

为了找到答案， [CommonsWare 在 Android bug tracker 上提交了一份 bug 报告](https://code.google.com/p/android/issues/detail?id=133419),要求谷歌调查这个问题。特别是，开发人员要求谷歌禁止未记录的权限要求限制第三方应用程序访问 ACTION_PICK_ACTIVITY。通过在 [CTS](https://source.android.com/compatibility/cts/) 中写入这些要求，华为将被迫遵守这些变化。

不过说实话，这个 bug 本身真的没什么大不了的。尽管我尝试过的其他应用程序(如 Tasker)都无法绕过这个权限要求，在设置应用程序中启动某些活动，但我对结果并不失望。但当我想起安布利先生的咆哮时，我意识到像这样的小变化肯定很难处理，尤其是**因为尽管它们可能很小，但它们无疑会** **累积起来**，有时足以引起头痛。设置应用程序的一个微小变化可能会导致对开发人员的不当负面评价。一个很小的变化没有很好的记录，需要我在互联网上搜索堆栈溢出线程。**其他设备上还有多少其他的小 bug？**

事实证明，移动领域的竞争加剧对消费者来说是好事，但在看到这么多不同产品线之间的这些微妙变化如何影响开发者后，我开始欣赏开发者对碎片化的看法。这不是选择本身的问题，而是社区没有做足够的工作来分类这些问题。正如阿姆布里先生在他的文章中建议的那样，也许 Android 开发者需要他们自己版本的 caniuse.com 或 sdkcritic.com，将所有不为人知的错误收集到一个数据库中。唯一的其他选择是让原始设备制造商适当地记录这些变化，或者从一开始就停止生产，但是*祝你好运。*

*特征图像演职员表:[open signal](https://opensignal.com/reports/2015/08/android-fragmentation/)*`