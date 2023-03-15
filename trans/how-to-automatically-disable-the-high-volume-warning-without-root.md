# 如何在没有 Root 的情况下自动禁用高音量警告

> 原文：<https://www.xda-developers.com/how-to-automatically-disable-the-high-volume-warning-without-root/>

那些生活在欧盟成员国之一的人可能在试图提高耳机音量时遇到过警告，如上图所示。

根据欧洲电工标准委员会(CENELEC)制定的规定，2013 年 2 月之后销售的所有能够播放媒体的电子设备必须具有最大 85 dB 的默认输出音量水平。用户可以选择忽略警告，将音量增加到最大 100 dB，但这样做时，警告必须在音乐播放 20 小时后再次出现。

虽然我们不会就这一规定在促进健康方面的功效进行辩论，但经常选择绕过这一警告的用户经常想知道这一过程是否可以自动化。在许多情况下，不得不手动同意覆盖音量限制是相当烦人的，例如当你在蓝牙设备上远程启动音乐播放时，所以我们想找出一种方法来自动绕过这个警告。

如果你搜索我们的论坛，绕过“安全音量限制”的解决方案已经存在，但是到目前为止，所有的解决方案都要求你[安装](https://forum.xda-developers.com/xposed/modules/mod-unsafe-volume-disable-safe-media-t2338474)一个暴露的[模块](https://forum.xda-developers.com/xposed/modules/module-nosafevolumewarning-t2718933/)。这必然会限制谁可以使用它，因为 Xposed 框架要求您拥有 root 访问权限(这意味着大多数手机上都有解锁的引导加载程序)以及 Android 的牛轧糖之前的版本。但是在深入研究了 AOSP 和各种系统设置之后，我发现了一种不需要 root 就可以绕过所有设备上的高音量/安全音频限制**的方法。**

遵循本指南，您将接受以高音量收听媒体所带来的任何风险。

* * *

## 安全音频警告旁路教程

如果你读过我之前的一篇关于[在没有 root 访问权限的情况下启用沉浸式模式](https://www.xda-developers.com/how-to-enable-system-wide-immersive-mode-without-root/)的文章，那么你可能已经开始尝试一些隐藏在手机上的设置了。如果你还没有，我强烈建议你这么做，因为我发现几乎每个设备都有大量的好东西等着你去发现。这个技巧没有什么不同，因为我们将使用一个系统属性来绕过安全音频警告。

具体来说，我们将修改系统。全局属性 *audio_safe_volume_state* 在启动时和定期，因此 Android 将始终认为你已经同意绕过警告。这个属性是在 AOSP 中定义的[，我们在下面复制它。该属性有几种状态，范围从 0 到 3。开机 30 秒后或连续播放音乐每 20 小时后，状态设置为“0”或“未配置”根据您的](https://android.googlesource.com/platform/frameworks/base/+/05274f348e12983eb8613cc6eb9ae561e8197e28/media/java/android/media/AudioService.java)[手机国家代码](https://en.wikipedia.org/wiki/Mobile_country_code)，它将被设置为“1”表示“禁用”或“3”表示“启用”。如果您居住在欧盟，默认情况下该属性设置为“3 ”,但每当用户手动绕过音量警告时，该属性会更改为“2”以表示“不活动”。**我们将把这个属性的值更改为‘不活动’状态**(如果你想知道的话，把它更改为‘禁用’对我来说从来都不起作用)。

```

    // property. Platforms with a different limit must set this property accordingly in their

    // can be set to SAFE_MEDIA_VOLUME_INACTIVE by calling AudioService.disableSafeMediaVolume()

    private final int SAFE_MEDIA_VOLUME_NOT_CONFIGURED = 0;
    private final int SAFE_MEDIA_VOLUME_DISABLED = 1;
    private final int SAFE_MEDIA_VOLUME_INACTIVE = 2;
    private final int SAFE_MEDIA_VOLUME_ACTIVE = 3;
    private Integer mSafeMediaVolumeState;
    private int mMcc = 0;

    private int mSafeMediaVolumeIndex;

    private final int mSafeMediaVolumeDevices = AudioSystem.DEVICE_OUT_WIRED_HEADSET |
                                                AudioSystem.DEVICE_OUT_WIRED_HEADPHONE;

    private int mMusicActiveMs;
    private static final int UNSAFE_VOLUME_MUSIC_ACTIVE_MS_MAX = (20 * 3600 * 1000); 
    private static final int MUSIC_ACTIVE_POLL_PERIOD_MS = 60000; 
    private static final int SAFE_VOLUME_CONFIGURE_TIMEOUT_MS = 30000;  
```

你首先需要安装[任务器](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en)和[自动工具](https://play.google.com/store/apps/details?id=com.joaomgcd.autotools&hl=en)，这样我们就可以自动完成这个把戏。从技术上来说，除了 Tasker 之外的任何其他自动化应用程序都可以使用，但我只熟悉 Tasker，所以如果你喜欢使用不同的应用程序，你必须自己进行调整。不过，AutoTools 对这个技巧至关重要，因为这个插件将允许我们控制设备上的安全设置。

正如我在关于切换沉浸式模式的文章中所解释的，我们需要向自动工具授予 **WRITE_SECURE_SETTINGS** 权限。这是因为控制安全音量状态的命令是在 **[设置下定义的。Global](https://developer.android.com/reference/android/provider/Settings.Global.html)** 类，尽管该命令的确切语法隐藏在 AOSP 中(就像沉浸式模式一样)。如果在阅读了我之前关于沉浸式模式的教程后，您已经授予了 WRITE_SECURE_SETTINGS 权限，那么您可以跳过下一节。如果没有，那么你必须设置它。

* * *

在 Android 的权限管理系统下，应用程序在清单文件中定义它们希望被授予的权限。然后，用户可以授予或拒绝安装权限(前棉花糖)或按需权限(棉花糖+)。但是，有些权限是应用程序即使在清单中请求也不能被授予的，比如 [WRITE_SECURE_SETTINGS](https://developer.android.com/reference/android/Manifest.permission.html#WRITE_SECURE_SETTINGS) 。这是因为授予任何应用程序如此强大的权限都会让该应用程序对您的设备进行大量控制。

但是有一个解决方法，我们可以使用它来授予任何我们想要的应用程序 WRITE_SECURE_SETTINGS 权限。通过使用 ADB 的[包管理器(pm)](https://developer.android.com/studio/command-line/adb.html#pm) 工具，我们可以向任何我们想要的应用程序授予任何权限(假设应用程序在清单文件中请求该权限)。

你需要做的第一件事是[将 ADB 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)安装到你的电脑上，然后为你的设备安装[正确的驱动程序。然后，在开发者选项中启用 USB 调试(进入设置- >关于手机，如果你还没有的话，点击 7 次内部版本号)，将手机连接到电脑上。最后，打开终端后，发送以下命令:](https://developer.android.com/studio/run/oem-usb.html)

`adb shell pm grant com.joaomgcd.autotools android.permission.WRITE_SECURE_SETTINGS`

现在，自动工具将能够更改您设备上的任何全局、安全或系统设置。有各种方法可以使用这些设置，每个类别中的可用设置列表完全取决于您的设备和软件版本，但这一讨论将在其他时间进行。无论如何，我们将继续向您展示如何使用自动工具来控制安全卷状态。

* * *

### 启动时禁用安全音频警告

对于熟悉 Tasker 的人来说，下面是对这个简介的描述。如果您不熟悉 Tasker，请继续阅读逐步说明。

### 启动时禁用安全音频

```
 Profile: Disable Safe Audio On Boot (6)
 Event: Monitor Start
Enter: Anon (7)
 A1: Wait [ MS:0 Seconds:30 Minutes:0 Hours:0 Days:0 ] 
 A2: AutoTools Secure Settings [ Configuration:Setting Type: Global
Name: audio_safe_volume_state
Input Type: Int
Value: 2 Timeout (Seconds):60 ] 
```

打开 Tasker，我们可以创建新的个人资料。点击右下角的 **+** 图标创建新的个人资料。添加一个新的**事件**上下文并转到 **Tasker - > Monitor Start。**我们使用的是 Tasker 启动时触发的事件上下文，而不是手机启动时激活的事件上下文，因为前者远比后者可靠。

无论如何，请按“后退”按钮，因为我们现在将创建一个与此配置文件相关联的任务。给这项任务起任何名字都没关系。进入任务创建屏幕后，按下屏幕底部中间的 **+** 图标，创建一个新动作。对于第一个动作，进入**任务- >等待**，让它等待 **30 秒。**这解释了 Android 中用于设置安全音量状态的“开机后 30 秒”规则。

接下来，创建一个新的操作，并转到**插件- >自动工具- >安全设置。**按铅笔打开自动工具的配置屏幕。转到**自定义设置。**对于设置类型，输入**全局**。输入**音频安全音量状态作为名称。**对于输入类型，使其成为 **int。对于该值，使其为 **2。**检查以确保所有内容都正确，配置应该与下面中间的截图相匹配。命令必须完全按照我写的那样发送，否则不会有任何影响。**

完成后，返回 Tasker 的主菜单，因为我们需要创建另一个配置文件。我们刚刚创建的配置文件考虑了启动 30 秒后设置安全卷状态的情况，但对于那些几乎从不重新启动设备的人，我们将创建另一个配置文件来定期设置该值。

* * *

### 定期禁用安全音频警告

对于熟悉 Tasker 的人来说，下面是对这个简介的描述。如果您不熟悉 Tasker，请继续阅读逐步说明。

### 定期禁用安全音频

```
 Profile: Disable Safe Audio Periodically (21)
 Time: 11:59PM
Enter: Anon (122)
 A1: AutoTools Secure Settings [ Configuration:Setting Type: Global
Name: audio_safe_volume_state
Input Type: Int
Value: 2 Timeout (Seconds):60 ] 
```

创建一个新的概要文件，这次使用一个**时间**上下文。不幸的是，我不知道有什么方法可以在没有 root 用户的情况下获得媒体播放的当前累积时间，所以我们只能每 24 小时将安全音量状态设置为非活动一次(...你们不可能在 24 小时内听 20 小时的音乐，对吧？).不管怎样，Tasker 设置周期性任务的界面有点糟糕，但是它的要点是你想把“从”和“到”的时间设置成相同的时间。这样，Tasker 会像你希望任务在设定的时间只触发一次一样对待它(我把它设定在午夜前 1 分钟)。

至于任务，只需复制您在之前的配置文件中为动作 2 所做的事情。在这种情况下，没有新的或不同的操作，因为我们所做的只是每 24 小时更改一次这个全局系统属性的值。

现在，您已经设置了这两个配置文件，您已经完成了！重启你的手机，现在当你插上耳机时，你应该不会再看到“安全音量”的警告。

* * *

## 下载并导入 Tasker

一如既往，我们提供脚本的 XML 文件，您可以下载和导入。只需从下面的链接下载文件，并将其保存在您的内部存储的任何地方。打开 Tasker，在首选项中禁用初学者模式。然后，回到主屏幕，长按顶部的“个人资料”标签。您应该会看到一个弹出窗口，其中一个选项是“导入”点击它，浏览到保存. prf.xml 文件的位置，并选择要导入的文件。对第二个轮廓重复上述步骤。

[**下载“禁用开机安全音频警告”配置文件**](https://www.androidfilehost.com/?fid=529152257862704598)

[**下载“定期禁用安全音频警告”配置文件**](https://www.androidfilehost.com/?fid=529152257862704597)

我们希望这个提示对你有用。如果这对你有用，请在下面的评论中告诉我们！