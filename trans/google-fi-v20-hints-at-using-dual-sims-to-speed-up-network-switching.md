# Google Fi v20 暗示使用双 sim 卡加速网络切换

> 原文：<https://www.xda-developers.com/google-fi-v20-hints-at-using-dual-sims-to-speed-up-network-switching/>

如果你不熟悉 Google Fi，那是 Google 自己的 MVNO 运营商。虽然大多数 MVNOs 依赖于一家大型运营商的网络，但 Google Fi 不同，它使用三家运营商:Sprint、T-Mobile 和 U.S. Cellular。兼容手机能够根据覆盖范围在这些网络之间智能切换。Google Fi v20 APK 为 Google Fi 提供了一种新的网络切换方式。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

“专为 Fi 设计”的手机可以通过 eSIM 或传统的 SIM 卡进行网络切换。Fi 有时切换网络很慢，用户经常抱怨这一点。事实上，有[第三方应用](https://play.google.com/store/apps/details?id=com.cheekydevs.fiswitch&hl=en)允许你强制网络切换。Google Fi v20 暗示使用双 sim 卡来加快切换过程，它有可能被用来为更多设备带来网络切换。

```
 <string name="card_configure_starburst_activate">Maximize networks</string>
<string name="card_configure_starburst_init_description">"Unlock faster network switching and more reliable connections by having Fi use both of your phone's SIMs."</string>
<string name="card_configure_starburst_init_title">Maximize your networks</string>
<string name="disable_starburst_auto_switching">Disabling multisim auto switching</string>
<string name="enable_starburst_auto_switching">Enabling multisim auto switching</string>
<string name="enable_starburst_device_failed">Unable to maximize your coverage</string>
<string name="enable_starburst_device_fragment_text">"Unlock faster network switching and a more reliable signal by having Fi use both of your phone's SIMs. Your phone will restart."</string>
<string name="enable_starburst_device_fragment_title">Maximize your coverage</string>
<string name="starburst_failed_body">"We'll try again in a few minutes."</string>
<string name="starburst_failed_title">Unable to activate second SIM</string>
<string name="starburst_feature_not_enabled">Multisim feature not enabled, cannot toggle auto switching.</string>
<string name="starburst_in_progress_title">Maximizing your network connections…</string>
<string name="starburst_success_body">"You now have even faster network switching. Both of your phone's SIMs are now using Google Fi."</string> <string name="starburst_success_title">Your 2 SIMs are active</string> 
```

上面的字符串来自谷歌 Fi v20 APK。我们可以在一些地方看到谷歌提到使用 sim 卡来“解锁更快的网络切换和更可靠的信号。”本质上，一个 SIM 将连接到一个运营商，而另一个 SIM 将连接到不同的运营商。这将允许手机更容易地在它们之间切换。

看起来这款应用将会有一个“最大化网络”的选项。然后它会引导用户激活两个 sim 卡。这可能是一个 eSIM 和一个物理 SIM 或两个物理 SIM。一旦设置完成，你的两个模拟市民将在 Fi 上激活。

像 Pixel 3 和 Pixel 4 这样的手机有 eSIM 和 Fi，传统上这些设备不需要物理 SIM。但是现在你可以使用 eSIM 并充分利用 SIM 卡插槽来改善你的连接。一些手机有双 SIM 卡插槽，它们可能会使用两张 Google Fi SIM 卡来进行网络切换。我们将拭目以待谷歌如何使用这一功能。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*