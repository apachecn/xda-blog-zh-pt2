# 如何让你的 OnePlus 3/3T 的 WiFi 速度翻倍(在特定条件下)

> 原文：<https://www.xda-developers.com/how-to-double-the-wifi-speed-on-your-oneplus-3-3t/>

当调整新智能手机的软件时，有时公司必须做出他们认为最符合大多数客户利益的决定。

有时这些决定是不明智的，在被指出后会在 OTA 更新中被修复。其他时候，默认设置保持原样是有正当理由的，但是修改的好处是我们可以*选择*来定制设置以满足我们的需求。我们在这里讨论后一种情况。

在我们的论坛上，流传着一个窍门，即**在 [OnePlus 3](https://forum.xda-developers.com/oneplus-3) 和 [OnePlus 3T](https://forum.xda-developers.com/oneplus-3t) 上几乎将你的 WiFi 速度**提高一倍——这当然有效，但只是在特定条件下**。**请注意，我们将在下面讨论的技巧**需要 root 访问权限**才能实现。

* * *

## 将 OnePlus 3/3T WiFi 速度提高一倍

据 XDA 资深会员 [dreinulldrei](https://forum.xda-developers.com/member.php?u=7053867) 透露，OnePlus 3 和 3T 使用的 WiFi 配置文件是高通提供的默认文件。这本身并不是一个问题，但用户发现默认配置**在 2.4GHz 频率下禁用** **信道绑定。** 5GHz 频率网络启用了信道绑定(如果您可以访问该频率，那么建议您连接到它)，但是如果您的路由器只支持 2.4GHz 频率，那么这个技巧可能对您有用。

随着信道宽度从 **20MHz** 增加到 **40MHz** ，启用信道绑定理论上应该会使您的无线吞吐量翻倍(只要您的路由器支持信道绑定)。这个技巧很容易实现，因为你只需要**修改 WCNSS_qcom_cfg.ini** (位于 **/system/etc/wifi)** 中的一行。

只是改变

`gChannelBondingMode24GHz=0`

到

`gChannelBondingMode24GHz=1`

或者，您可以简单地使用 Magisk 模块来实现这个补丁，该模块可以在官方存储库中找到。这个补丁适用于所有版本的 Oxygen 操作系统，前提是你拥有之前提到的 T2 根权限。

我们论坛上的用户发现，修改这条线路确实会使他们的无线速度翻倍。下面的截图是从详细描述这个修复的 [XDA 线程中截取的，所以测试这个的功劳属于那些用户。](https://forum.xda-developers.com/apps/magisk/magisk-oneplus-3t-wifi-channel-bonding-t3520885)

正如你所看到的，很明显这个修复*可以让你的 WiFi 速度翻倍。然而，如果你对无线网络有所了解，那么你可能知道为什么一加没有默认启用这个功能。这是因为**无线干扰**的可能性。引用一个 [Linksys 支持页面](http://www.linksys.com/in/support-article?articleNum=139627)关于此功能的内容:*

> #### Linksys 双频带路由器的无线网络模式将因您选择启用的频带而异。在 2.4 GHz 频率下，Wi-Fi 信号范围被划分为每个间隔为 5 MHz 的信道。相邻频道重叠，在 20 MHz 频段会相互干扰。将频道宽度设置为 40 MHz 网络将允许您使用整个 Wi-Fi 频段的 2/3。因此更有可能与其他无线网络重叠和干扰。同时，如果将信道宽度设置为 20 MHz，网络将只与该频率前后的两个信道重叠。

本质上，如果启用 40MHz 的信道宽度，无线干扰的可能性更大。它增加干扰的确切原因是[比本文需要涵盖的更复杂](http://www.networkcomputing.com/wireless/channel-bonding-wifi-rules-and-regulations/199326059)，但一般来说，引用 XDA 知名开发商 [SultanXDA](https://forum.xda-developers.com/member.php?u=4800121) 的话说，“2.4GHz 以上的 40MHz 宽信道**在 WiFi 接入点密度高的城市地区**不是一个好主意”。

然而，如果你是在一个更农村或郊区的地区，那里很少有无线网络干扰你自己的，这个修复提供了一个免费的方法来加倍你的手机的网络速度。试试看，让我们知道它是否适合你！