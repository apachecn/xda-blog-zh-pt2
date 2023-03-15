# 一加不小心预装了一个应用程序，作为 Root 访问的后门

> 原文：<https://www.xda-developers.com/oneplus-root-access-backdoor/>

更新:一加对此事发布了官方回应。在即将到来的更新中，他们将从 EngineerMode 中删除 ADB root 功能。

距离一加被发现收集用于分析的个人身份信息已经一个多月了。该公司很快改变了方针，在一次更新中，该公司承诺将更加透明，明确给予用户选择退出 OxygenOS analytics 的[选项](https://www.xda-developers.com/oneplus-talks-oxygenos-analytics-stops/)。尽管那场灾难已经过去，但另一场灾难今晚又出现了。推特上一个名为“[埃利奥特·奥尔德逊](https://twitter.com/fs0c131y)”(以热门电视连续剧《机器人先生》的主角命名)的用户发现，一加[不小心把高通制作的一个诊断测试应用程序](https://twitter.com/fs0c131y/status/930185109726203906)留在了原处。反编译这个应用程序后，他发现它可以被利用来授予根用户访问权限——有效地充当后门。

该应用程序名为“EngineerMode ”,本质上是一个由高通制造的系统应用程序，提供给一加等原始设备制造商，以便原始设备制造商轻松测试设备的所有硬件组件。该应用程序预安装在所有 OnePlus 3、OnePlus 3T 和 OnePlus 5 设备上，并且可以通过任何活动启动器轻松访问，因为该应用程序的所有活动都已导出。

我们实际上[在几个月前](https://www.xda-developers.com/oneplus-hardware-diagnostic-tests/)报道了这个应用程序的存在，但当时我们不知道它能用来做什么。这位 Twitter 用户反编译了这个应用程序(其源代码已经发布在网上[这里)](https://github.com/fs0c131y/EngineerMode)并且发现了一个叫做 DiagEnabled 的有趣活动。特别是，有一个方法在活动中非常突出:escalatedUp。该方法接受布尔值(真/假)和字符串。该字符串是一个密码，该方法在将系统属性`persist.sys.adbroot`和`oem.selinux.reload_policy`设置为 1 之前会检查该密码。

第一个系统属性特别有趣，因为它允许用户以 root 身份运行 ADB。这立即开启了在手机上获得完全 root 访问权限的可能性——所有这些都不需要解锁引导加载程序。那么，如何让 EngineerMode 应用程序将这些系统属性设置为“1”呢？

@fs0c131y 需要找到正确的密码来发送 intent，以便传递上面发布的方法中的逻辑。然而，找到这个密码并不是一项简单的任务。他反编译了负责生成密码的库(名为 libdoor.so)，找到了密码 hash 所在的位置:`/data/backup/fpwd`。密码是从各种构建属性中生成的，比如`ro.product.model`和`ro.product.brand`，并且不容易进行逆向工程。

幸运的是，在大卫·温斯坦和 T2 的帮助下，他发现了 EngineerMode 需要的密码，以便将 ADB 升级为 root 权限。

我们所要做的就是以这种格式发送一个意图:

```
 adb shell am start -n com.android.engineeringmode/.qualcomm.DiagEnabled --es "code" "angela" 
```

其中，com.android.engineeringmode/.qualcomm.DiagEnabled 是我们正在利用的 DiagEnabled 活动的组件名，“code”是字符串名，“angela”是相关的密码值。

@fs0c131y 声明他将很快[发布一个应用程序](https://twitter.com/fs0c131y/status/930193031394979840)，它将发送这个意图来提升 ADB 的 root 权限，修补启动映像以禁用 dm-verity，并安装 su 二进制文件。请留意 XDA 论坛，看看这个根应用程序何时发布。

这对最终用户来说意味着，您可以**轻松启动您的 OnePlus 3、OnePlus 3T 和 OnePlus 5，而无需解锁您的引导程序**。不过，这种利用不允许恶意应用程序授予自己 root 访问权限，所以除非有人可以物理访问您的设备来设置 ADB，否则您不会被利用。

如果你想保护自己免受这种攻击，你可以[从当前用户](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)卸载应用程序，这将防止意图被发送到 EngineerMode 应用程序。只需在 ADB 中使用以下命令:

```
 adb shell pm uninstall -k --user 0 com.android.engineermode 
```

当然，这仍然被认为是一个漏洞，我们希望一加尽快修补。他们真正需要做的就是从未来的构建中移除这个应用程序。

* * *

## 更新 1:密码是“安吉拉”

用户@fs0c131y 在他的 Twitter 页面上发布了一个更新，提供了进入一个根 ADB shell 所需的密码。那个密码是...安吉拉。对于不看《机器人先生》的人来说，安吉拉是其中一个主角的名字。我猜高通一定有很多机器人先生的粉丝。

如果你在 ADB 中输入我上面发布的命令，你会注意到 ADB 立即断开连接，服务器重启。再输入亚行，你会发现它现在是一个有根的壳。

* * *

## 更新 2:密码是如何导出的

安全公司 Now Secure 发布了一篇博客文章，详细介绍了他们是如何获得发生这种根漏洞攻击所需的密码的。你可以在这里阅读他们的完整帖子。

* * *

## 更新 3:更多设备受到影响

这一最新消息不应该令人惊讶，但更多的设备似乎受到了这种利用的影响。这是因为 EngineerMode 应用程序是一款高通应用程序，所以其他原始设备制造商可能会将其预装在他们的设备上。到目前为止，用户已经在 Twitter 上联系到@fs0c131y，以确认该应用程序安装在[一些华硕 Zenfone 和小米设备](https://twitter.com/fs0c131y/status/930446058081185793)上。进入“设置”并查看安装了哪些应用程序，您可以轻松查看您的设备是否安装了此应用程序。

* * *

## 更新 4:为你的设备找根

通过根 ADB shell 使用几个命令，现在可以[将 su 二进制文件推送到您的设备上](https://twitter.com/fs0c131y/status/930505992084901888)。使用它，你可以安装一个超级用户之类的 root 管理应用，然后自由地授予其他应用的 root 访问权限。无需解锁您的引导程序！

* * *

## 更新 5:一加回应

一加已经正式对局势做出回应。在一篇[博客文章](https://forums.oneplus.net/threads/what-is-engineermode.680377/)中，该公司重申，只有当攻击者能够物理访问设备并启用 USB 调试时，才能利用这一漏洞。为了启用 USB 调试，攻击者还需要您设备的 pin/密码。因此，根后门不容易被任何应用程序或个人利用，但尽管如此，一加将通过从 EngineerMode 应用程序中移除这一功能来解决用户的担忧。