# 当任何设备的屏幕关闭时，如何强制“OK Google”热词检测工作[Root]

> 原文：<https://www.xda-developers.com/how-to-force-ok-google-hotword-detection-to-work/>

当 Moto X (2013)首次公布时，最令人兴奋的功能之一(除了环境显示)是它能够通过语音命令唤醒。

后来在谷歌 Nexus 设备中引入，现在在许多旗舰产品中都可以使用，热门词识别功能是一个非常棒的功能，当你需要快速搜索谷歌而不用手里的设备摸索时。当你把手机放在车里，需要开始导航到某个目的地时，这非常有用。用你的声音启动谷歌地图导航比其他任何方式都安全。

不幸的是，要想一直触发“OK Google”命令，你的设备中需要一个特殊的低功耗语音识别芯片。虽然这种硬件存在于许多设备中，但并不是所有设备中都有。甚至像华为 Mate 9 这样强大、昂贵的旗舰也不提供这种优惠。对于像我这样的设备，谷歌提供了在屏幕打开或设备插入充电器时触发“OK Google”语音命令的功能。

几年前，有一个名为 [Open Mic+ for Google Now](https://play.google.com/store/apps/details?id=com.RSen.OpenMic.Pheonix&hl=en) 的应用程序，它可以选择启用后台服务来随时监听语音命令。不幸的是，谷歌要求开发者停止使用该服务，而开发者不再有时间支持该应用程序，所以它半途而废了。唯一现有的选择是使用 [AutoVoice](https://play.google.com/store/apps/details?id=com.joaomgcd.autovoice&hl=en) ，一个流行的 Tasker 插件，但这需要你有足够的 Tasker 知识来设置配置文件以响应特定的命令。

对于那些喜欢依赖谷歌语音识别服务的人来说，我已经找到了一个解决办法，即**在任何根设备上启用“OK Google”热门词汇检测，即使其硬件不支持它。**这个把戏有两个**注意事项**，我们将在下面详细讨论。

* * *

## 任何设备上的“OK Google”热词检测

在考虑这个问题的解决方法时，我问自己的问题是:

> #### 如何让我的设备根据我的命令启用热门词汇识别服务？

由于我目前的手机在屏幕关闭时不支持热门词汇检测，所以只有当我的手机屏幕打开或正在充电时才能实现这一功能。自然地，因为我的目标是在任何时候(甚至在屏幕关闭时)都启用热门词汇检测，所以让屏幕打开会违背这个目的。让我的设备一直插着电源对我来说也是毫无意义的，但是如果我能 ***欺骗*** 我的设备满足这两个条件中的任何一个呢？

幸运的是，通过一点根魔术和调试命令的巧妙使用，这是非常可能的！使用一个用于测试目的的调试外壳命令，我能够**欺骗我的设备认为它正在给**充电，即使它没有连接任何电源。我们将利用的命令是`dumpsys battery`，你可以在罗曼·马祖尔的博客文章[中读到它的参数。](https://stanfy.com/blog/android-shell-part-1-mocking-battery-status/)

注意:这个戏法**完全可以安全**完成。如上所述，这个命令只是欺骗你的设备以为它正在充电。这实际上并不是在充电，即使电池监控应用程序说不是这样(这是因为这些应用程序将被馈送不正确的信息。)

特别值得注意的是`dumpsys battery set`命令，它接受参数来设置设备当前是通过 AC、USB 还是无线充电进行充电。例如，如果我们在 Android 中打开一个 root shell 并输入以下命令，**设备将认为它正在通过交流电源充电。**

```
 su
dumpsys battery set ac 1

```

通过设置该命令(或 USB/无线充电命令)，您现在可以在屏幕关闭时**触发 OK Google 命令。**这是因为无论从哪方面来看，你的设备都在“充电”——满足了激活谷歌热门词汇识别服务的要求。

由于这是一个用于调试的命令(主要是让开发人员在不同的电池条件下测试功能)，以这种方式使用它有一些缺点。特别是两个缺点，我们接下来将讨论这两个缺点。第一个缺点很容易解决，但是第二个缺点就不一样了。

### 缺点#1 -冻结电池指示器

在输入任何“dumpsys battery set”命令后，Android 的 BatteryManager 服务将**立即停止收集**任何关于你的电池状态的数据。这意味着你的电池电量、温度、电流、电压、健康状况将不再被 Android 系统报告。相反，在您输入命令的那一刻，它们将被及时“冻结”。

然而，即使任何应用程序都可以访问这些数据，系统仍在收集这些数据**。如果你想更新你当前的电池电量，你需要耍点小花招。幸运的是，数据很容易获取。如果您有 Tasker 或另一个自动化应用程序，您需要做的就是创建一个通知，用/sys/class/power _ supply/battery/capacity 中存储的当前文本在 tap 上更新。**

在上面的截图中，我的电池指示器(当我下拉状态栏时可以看到)卡在 70%，但正如你在终端中看到的，我的实际电池水平是 69%。定期轮询这个文件以在我的通知栏中发布准确的电池电量很容易，但有一种更简单的方法来解决这个问题。

处理这个特别的缺点是**实际上是极其琐碎的**。仔细想想，这个问题只有在命令启用且屏幕打开时才会出现。但问题是，当屏幕打开时，你不需要启用这个命令，因为默认功能允许你在屏幕打开时访问“OK Google”命令。因此，你所需要做的只是当屏幕在时**禁用这个命令。使用 Tasker 或其他自动化应用程序可能是最简单的方法。只需运行以下命令来禁用该技巧:**

`dumpsys battery reset`

下面您将找到两个 Tasker 配置文件的描述，您需要设置这两个配置文件，以便在屏幕关闭时运行此命令，而在屏幕打开时禁用它。实质上，您将创建两个“事件”上下文，其中一个是“显示关闭”事件，而另一个是“显示解锁”事件。“Display Off”事件的任务将有一个单独的动作，代码->用命令`dumpsys battery set ac 1`运行 Shell。“Display Unlocked”事件的任务也有一个单独的动作，代码- >用命令`dumpsys battery reset`运行 Shell。因此，Tasker 将运行命令来欺骗您的设备，使其认为在屏幕关闭时正在充电(配置文件:启用热门词汇检测)，并在手机解锁时运行命令来禁用此功能(配置文件:禁用热门词汇检测)。

[标签][标签标题= "启用热门词汇检测"]

```
 Profile: Enable Hotword Detection (180)
 Event: Display Off
Enter: Anon (182)
 A1: Run Shell [ Command:dumpsys battery set ac 1 Timeout (Seconds):0 Use Root:On Store Output In: Store Errors In: Store Result In: ] 
```

[/tab][tab title = "禁用热门词汇检测"]

```
 Profile: Disable Hotword Detection (191)
 Event: Display Unlocked
Enter: Anon (192)
 A1: Run Shell [ Command:dumpsys battery reset Timeout (Seconds):0 Use Root:On Store Output In: Store Errors In: Store Result In: ] 
```

[/tab]

[/tabs]

### 缺点 2——电池消耗增加

有一个很好的理由为什么热词检测总是需要一个定制的协处理器，因为否则它会导致 CPU 必须保持清醒的额外电池消耗。当你欺骗你的设备认为它正在充电时，这意味着设备保持处理器运行并运行更多的后台服务，因为它是在假设增加的功率消耗不会有影响，因为设备可以访问电源。

但是这里的情况不是这样，所以启用这个命令会导致电池消耗增加。在我让我的设备整夜处于这种状态的经历中，我的 Mate 9 在 8 小时的过程中耗尽了 **12%的电池。**

在我看来，这算不上是一个交易破坏者，但这可能会让你们当中的一些人望而却步。不幸的是，没有简单的方法来处理这第二个缺点。按照上一节中提到的最后一段，在屏幕打开时禁用该命令将有助于缓解问题，但这是您所能做的。

* * *

## 结论

希望你觉得这一招有用。当然，这并不适合所有人，但是如果你想强制使用 OK Google hotword 检测功能，而你的设备没有必备的硬件，这种变通方法是适合你的。

我概述了这种技巧的两个潜在缺点，第一个可以通过使用自动化应用程序在有意义的时候启用/禁用该命令来解决。不幸的是，后一个缺点是由于您的硬件不是为始终在线的热门词汇检测而构建的，但是如果您只在真正需要时才使用它，那么它应该不是太大的问题。

试试这个技巧，如果它对你有用，请在下面的评论中告诉我们！