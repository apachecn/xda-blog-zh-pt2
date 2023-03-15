# DexPatcher:使用 Java 修补 Android APKs

> 原文：<https://www.xda-developers.com/dexpatcher-patch-android-apks-using-java/>

你可能已经看到或安装了修改过的应用程序，无论是为你的解决方案打了补丁的拨号器，还是添加了功能的自定义 WhatsApp 版本。然而，开发者是如何做到这一点的呢？很多时候，应用程序的源代码甚至都不可用，那么它是如何工作的呢？我们将首先看到这一点，然后看看一个旨在使这个过程变得更容易的新工具，最后将它与流行的 Xposed 框架进行比较，看看它们有什么不同。

# 修改 APKs:它是如何工作的？

你可能听说过 apk 通常是如何被修改的——开发人员将自己插入矩阵，开始在 Smali 中看到一切，并获得使用源代码的力量修改东西的能力。一旦完成，一个电话就足以让他们离开，此时他们准备好分享闪亮的新 apk。

更严重的是……我们从头说起吧。如果你不熟悉修改 Android 应用程序，你可能想知道 smali 是什么。开发者通常使用 Java 编程语言来编写 Android 应用程序。然后，一个程序(编译器)将该代码“翻译”成适合您的设备的另一种格式，结果是。应用程序包(或 APK)中包含的 dex 文件。

此时，您将无法再访问原始源代码(除非您是开发人员或者应用程序是开源的)。然而，你拥有的是 APK，因为它安装在你的设备上。从中，您可以获得 dex 文件(通常是 classes.dex ),然后尝试将其转换回您可以理解的格式。这就是 smali 的用武之地，作为一个可读性更强但忠实的译本。你可以更进一步，把它翻译回 Java，尽管这个过程不够忠实——你会得到一个可以理解的结果，但是你可能不能再反过来翻译它，因为一些细节会在这个过程中丢失。换句话说，你可能做的任何修改都是徒劳的，因为你无法再把它变回 APK 来安装到你的设备上…至少不需要付出很多努力。

smali/baksmali 实际上是 dex 格式的汇编器/反汇编器——这就是它在冰岛语中的字面意思。然而，当我们说“smali”时，我们通常指的是 Smali 理解的格式(把它想象成定义每个小细节的指令，即使它不是我们人类所需要的——因此它比 Java 更冗长)。还要注意，上面的解释有点简化，但应该是一个接近的类比，同时仍然易于理解。

那么，开发者需要做什么来修改一个应用程序(不访问源代码)？这个过程大致如下:

1.  获取 APK(从网络或设备上)。
2.  使用类似`apktool`的东西将 APK 反编译成 Smali。(`apktool`利用了 smali/baksmali，但是使得反编译和重建 apk 变得容易得多，并且还负责像 XML 文件这样的解码资源。)
3.  从 APK 中提取 classes.dex，然后使用`dex2jar`和最后一个 Java 反编译器来获得(不完整，经常出错，但基本上可以理解)Java 代码。(这是可选的，但会有所帮助，因为 Smali 更难理解。)
4.  确定要修改的内容。
5.  实际上通过直接编辑 Smali 代码来修改它。
6.  或者，用 Java 编写修改，编译它，再反编译成 Smali，然后复制生成的 Smali 代码。
7.  一切结束后，再次使用`apktool`来重建 APK。
8.  签署 APK(验证作者的身份；所有包都要签名)最后安装。

编写小代码非常困难，而且容易出错。在 Smali 中可以进行较小的更改，但是用它添加新功能更具挑战性。此外，您不会有任何编译时错误，所以即使是打字错误也可能只在运行时被检测到。扩展和共享 Smali 补丁也可能很麻烦，因为差异往往是特定于特定的 APK 版本的。尽管有一些工具可以使上面解释的部分过程变得更容易(想到了[良性十工作室](http://virtuous-ten-studio.com/))，但它仍然会令人厌倦。

# 介绍 DexPatcher

XDA 资深会员兰雄的 DexPatcher 旨在解决这些问题，方法是简化流程，让开发者完全避免与 Smali 打交道。相反，开发人员可以单独用 Java 编写补丁，让 DexPatcher 处理所有其他事情。

这有一个主要的优点，即补丁文件易于阅读和管理。一般来说，修补 apk 也变得更加方便。我们稍后将看到如何使用 DexPatcher 的完整示例，但这里先快速概述一下它提供的功能:

*   [开源](https://github.com/Lanchon/DexPatcher/)。
*   跨平台:应该可以在 Linux，Mac，Windows 上运行。
*   补丁文件:您所做的修改包含在您可以独立共享的 Java 补丁文件中。
*   Java:不是 Smali。

您还获得了构建时错误检查的优势，因此错误会在开发周期的早期出现。Java compiled 提供了通常的编译时检查(可以访问原始的 APK 符号)，DexPatcher 在打补丁时加强了源代码和补丁的兼容性，提供了有用的信息，并在您似乎在做合法但可疑的事情时发出警告。

除此之外，DexPatcher 还附带了一组[助手脚本](https://github.com/Lanchon/DexPatcher-scripts)(仅在 Linux 上可用，尽管它们也可以移植到其他平台上)。这些负责设置工作区，提取目标 APK 的类和资源，将类反编译成 Java(后者使用了 [CFR Java 反编译器](http://www.benf.org/other/cfr/))，最后在完成后构建并签署修补的 APK。

让我们看一个例子(在 Linux 上):

## 安装 DexPatcher 脚本

```
$ # Make a directory where we can test stuff out and enter it.

$ mkdir xda-test

$CDxda-test

 $ git 克隆 https://github.com/Lanchon/DexPatcher-scripts.git·德克斯帕彻 #克隆德克斯帕彻助手脚本 repo。

CDdex patcher

 $ chmod +x dxp-*  #没有必要，但为了清楚起见:我们需要确保我们稍后调用的文件是可执行的。

## 配置 DexPatcher 脚本

在您最喜欢的文本编辑器中打开`dxp.config`,确保更改必要的变量以适应您的系统。你只需要修改下面一行来指向你的 Android SDK 的安装位置:

```
dxp_android_sdk_dir=(~/android/sdk)

(DexPatcher 将自动选择可用的最高平台版本。此外，您还可以修改其他配置选项，让它使用您自己版本的一些工具，而不是捆绑的缺省值。)

为了便于访问，我们可以将`dexpatcher`目录添加到我们的`PATH`中，或者甚至将不同的`dxp-*`脚本符号链接到已经在您的`PATH`中的位置，例如`~/bin`:

```
export PATH=$PWD:$PATH

修改应用程序
对于这个例子，我们将使用一个简单的开源应用程序。当然，在这种特殊情况下，直接修补源代码是可能的，但这一点也不好玩！

我们将采用 basil2style 的“Get ID”应用程序，该应用程序向您显示有关您设备的一些细节。我们的目标是修改“设备 ID”的“复制”按钮，让它共享这个 ID:

 *   首先，让我们下载我们要修改的 APK:[Get ID](https://f-droid.org/repository/browse/?fdid=makeinfo.com.getid)。 *   反编译应用程序。 *   创建签名密钥，我们稍后将使用该密钥对 APK 进行签名。 

我们也可以通过 shell，使用助手脚本来完成这一切:

```
$ cd dexpatcher # Go to our working directory.

$ curl -O https://f-droid.org/repo/makeinfo.com.getid_1.apk # Download the APK. 

$ dxp-setup-for-apk makeinfo.com.getid_1.apk # Unpack and decompile the APK. 

$ cd makeinfo.com.getid_1 # Go to the newly created directory where everything is unpacked/decompiled to. 

$ dxp-create-keystore # Create the APK signing key. Press 6 times (or fill out the info), then "yes".

您会注意到这里有几个不同的目录:

*   **解码**:你会在这里找到资源和 Smali，由`apktool`解码。

*   **src** :空目录。这是我们放置补丁文件的地方。

*   **src-cfr** :这是`cfr`反编译应用程序(以及错误)的地方。这是一个很好的地方，可以查看以决定要更改什么(您可能还需要上面的 decode 目录中的资源及其 id，但不是针对这个特定的示例)。

*   **src-cfr-nodecode** :同上，但只包含空存根(没有代码，只有骨架)。您可以使用这些文件作为您的补丁的基础，我们稍后会看到。

正如我们之前提到的，我们希望更改设备 ID 的“复制”按钮来共享 ID 文本。如果我们看看源代码，我们会注意到设备 ID 复制按钮(`device_copy` ) `onClick`事件是由`src-cfr/makeinfo/com/getid/MainActivity.java`中的匿名类处理的。虽然我们可以在这里修改它，但通常最好找到一种替代方法，因为匿名类有数字名称(`MainClassName$SomeNumber`，例如`MainActivity$3`)，这可能会在版本之间发生不可预测的变化。

相反，我们将通过修改`MainActivity`类为事件注册我们自己的类。首先，让我们将“骨架”版本从`src-cfr-nocode/makeinfo/com/getid/MainActivity.java`复制到`src/makeinfo/com/getid/MainActivity.java`(记住`src`是我们补丁的所在)。(如果你愿意，也可以复制完整代码的版本，这纯粹是个人喜好问题。)

我们现在可以对其进行如下编辑:

*   为 DexPatcher 注释添加必要的导入:

```
import lanchon.dexpatcher.annotation.*;

 *   添加一个标签来表明我们正在编辑这个类。我们还将 patch 类成员的默认动作设置为`IGNORE`，这意味着这些成员在 Java 编译期间将被我们的代码引用，但将被 DexPatcher 忽略。 

```
@DexEdit(defaultAction = DexAction.IGNORE)

公共 班级 主要活动

 //对 ActionBarActivity 的引用将由符号来满足

//在我们构建补丁时从应用程序中提取。

扩展ActionBarActivity{

 *   此外，向构造函数和`onCreate`方法添加空体，以及我们计划使用的所有其他方法(记住，当我们的补丁实际应用时，它们将被忽略——我们只是添加它们，所以如果需要，我们可以在这里引用它们)。您也可以只添加关键字`native`来代替。 *   如果你好奇的话，我们现在已经可以构建补丁了:

    ```
    $ dxp-make # Output: `patched.apk`.
    ```

    很简单，对吧？不过，让我们继续——我们还没有完成。 *   现在让我们编辑`onCreate`来设置自己的`OnClickListener`，这样我们就可以共享设备 ID，而不是将其复制到剪贴板:

    ```
    // Rename the target method so that we can still call it (the original)// if needed.@DexEdit(target = "onCreate")protected void source_onCreate(Bundle var1) {}// Add our new custom method.@Override@DexAddprotected void onCreate(Bundle var1){ // Call the original method: source_onCreate(var1); // Replace the text and handler: device_copy.setText("Share"); device_copy.setOnClickListener(new DeviceCopyOnClick());}// Note that we don't use an anonymous class to avoid nameclashing with// MainActivity$1, which already exists.// We also could've defined a nested MainActivity.Patch class and used// an anonymous class in MainActivity.Patch.onCreate(), and then called// MainActivity.Patch.onCreate() from MainActivity.onCreate().@DexAddclass DeviceCopyOnClick implements View.OnClickListener { @Override public void onClick(View object) { if (MainActivity.this.val) { Intent intent = new Intent(Intent.ACTION_SEND); intent.setType("text/plain"); intent.putExtra(Intent.EXTRA_SUBJECT, "Device ID"); intent.putExtra(Intent.EXTRA_TEXT, device.getText().toString()); startActivity(Intent.createChooser(intent, "Share Device ID")); } else { Toast.makeText(MainActivity.this.getApplicationContext(), "Nothing to Share", 0).show(); } }}
    ```

     *   看起来我们现在完成了！完整的补丁应该看起来像[这个](https://gist.github.com/GermainZ/5eecb0a32599aae59649)。我们现在可以构建打了补丁的 APK 并安装它:

    ```
    $ dxp-make$ adb install patched.apk
    ```

     *   让我们来看看结果: 

(感谢 Lanchon 帮助编写示例代码！)

DexPatcher 与 Xposed 有何不同
Xposed 非常受欢迎，这是有原因的——它使得开发人员和用户构建、共享和安装 mods 更加简单。DexPatcher 和 Xposed 之间有一些差异，这可能会使一些人更喜欢其中的一个:

 1.  Xposed 通过在运行时挂钩方法，允许开发人员在任何方法之前、之后或替代任何方法做一些事情，来实现它的魔力。另一方面，DexPatcher 在运行时之前修改一切，并生成一个独立的、经过修改的 APK 代码——在方法之前、之后或代替方法运行仍然是可能的，并且您实际上有一些额外的自由。 2.  生产一个独立的 APK 意味着它不依赖于任何外部框架。这也意味着修改用户应用程序不需要 root。 3.  因为你用 DexPatcher 创建了一个新的 APK，它的签名将会不同。这意味着用户无法收到原作者的官方更新，如果签名被检查，可能会导致谷歌应用程序等应用程序出现一些问题。 4.  模块和 DexPatcher 补丁的源代码都可以很容易地分发和修改。如果你对每一个都有点熟悉的话，它们也有许多相似之处。 

现在就去拿
我们已经谈得够多了。现在轮到你试一试了，所以直接去 [DexPatcher 论坛主题](http://forum.xda-developers.com/android/software/tool-dexpatcher-modify-android-dex-apk-t3060854)开始吧！

```

``` 
```

```

``` 
```