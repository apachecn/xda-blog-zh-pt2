# 谷歌 Pixel 2 支持硬件加速共享，以获得更好的电池续航时间

> 原文：<https://www.xda-developers.com/google-pixel-2-hardware-accelerated-tethering/>

关于新的谷歌 Pixel 2/Pixel 2 XL 还有很多尚未被发现。谷歌在科技界耍了一个花招，他们突然宣布新的智能手机嵌入了一个定制的图像处理器，名为 [Pixel Visual Core](https://www.xda-developers.com/pixel-visual-core-google-custom-soc/) ，尽管该处理器尚未启用。我们在 Pixel 2 上还发现了另一件有趣的事情，尽管我们不能 100%确定这项新功能的全部含义。这项名为**硬件加速共享**的功能，通过将所有与数据包转发相关的逻辑和其他共享相关的任务卸载到硬件上，可能会延长移动数据共享期间的电池寿命。

谷歌 Pixel 2 或 Pixel 2 XL 的现有用户可以在网络类别下的开发者选项中找到该功能。默认情况下它是启用的，所以可以推测它已经在这些设备上运行了。在 Android 开源项目(AOSP)中，我们可以在“ [tether-offload](https://android-review.googlesource.com/#/q/tether+offload) ”标签下看到几个与该功能相关的提交。我们可以看到，[将智能手机的数据限制](https://android-review.googlesource.com/#/c/platform/frameworks/base/+/456757/)传递给卸载代码是有逻辑的，这样就不会超过你的数据限制。

最重要的是，我们可以看到“[系绳卸载 HAL](https://android-review.googlesource.com/#/c/platform/hardware/interfaces/+/328689/) ”的实现硬件抽象层(HAL)允许 Android 系统与 SoC 中的 WiFi 芯片接口，该芯片将处理硬件加速共享。Android 使用这个 HAL 来将所有的数据包转发负担从 Android 转移到专用于它的硬件上。

最终结果是，专用于移动数据共享的系统资源将被释放出来用于其他目的。设备的 CPU 负责与网络共享相关的操作越少，节省的电能就越多。当设备进入睡眠状态时，这可能特别有用，因为目前 Android 上基于软件的网络共享需要 CPU 通过唤醒锁保持清醒。通过将捆绑的责任转移到硬件上，CPU 可能会真正进入睡眠状态，从而延长电池寿命。

那么什么设备支持硬件加速共享呢？到目前为止，我们只在谷歌 Pixel 2/Pixel 2 XL 上发现了切换，所以我们假设只有这些设备支持它。根据 HAL 提交的网络共享卸载，谷歌似乎正在测试对谷歌 Nexus 5X (bullhead)的支持。此外，根据谷歌的一些评论，似乎共享卸载 HAL 是相当中立的供应商:

> 虽然这个 HAL 确实有一些高通设置的怪癖，但绝大多数都是厂商中立的。理论上，任何具有适当功能的 SoC 的供应商都可以支持这种共享硬件卸载(他们可能会在设置时跳过额外的 fd 传递，谁知道呢)。

在另一条评论中，一位谷歌员工提到了设备如何混合搭配 WiFi 芯片组并卸载 Hal，但他们构建的 API 仍然旨在在共享时最大限度地延长设备的电池寿命。

> #### 在最顶端，我们定义这个 API 将返回一个静态配置。根据供应商/硬件实施情况，这些功能可能会发生变化。例如，一个设备可以具有来自厂商 A 的 wifi，并卸载来自厂商 B 的 HAL。而另一个设备可以具有来自厂商 B 的 Wifi 芯片组，并卸载来自厂商 B 的 HAL。在这种情况下，卸载能力可能不同。即使能力有限，框架/客户端也可能希望利用有限的硬件卸载。因此，鉴于不同 soc 的实现可能存在差异，API 旨在从硬件中获得最大收益。

如果您拥有一台 Google Pixel 2/Pixel 2 XL，并且想要查看硬件加速共享的状态，您可以输入下面的 [ADB shell 命令](https://android.googlesource.com/platform/frameworks/base.git/+/c2519c5feae397e18561e00acea9d5e456bfaabe)，并查找与“硬件卸载”相关的字符串

```
 adb shell dumpsys connectivity tethering 
```

我们必须进行测试，以实际了解硬件加速共享在提高电池续航时间方面有多有效。网络共享曾经也对性能造成了巨大的影响，但 Android 中 CPU 速度和优化的巨大改进已经在很大程度上解决了这个问题。因此，我们不认为通过卸载 HAL 将网络共享逻辑卸载到 WiFi 芯片组会带来显著的性能提升。