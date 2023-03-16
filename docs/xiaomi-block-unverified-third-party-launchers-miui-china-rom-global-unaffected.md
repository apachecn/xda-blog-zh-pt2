# 小米在 MIUI 中国 rom 上屏蔽“未经验证”的第三方启动器；MIUI 全球版不受影响

> 原文：<https://www.xda-developers.com/xiaomi-block-unverified-third-party-launchers-miui-china-rom-global-unaffected/>

谈到安卓和安卓体验，中国消费者经常吃亏。对于该地区的许多消费者来说，只有通过经销商购买手机才是可行的，经销商最终会利用这种情况，在他们销售的设备上安装带有广告软件的外观相似的发射器。然后，消费者会对广告软件的来源感到疑惑，并继续用对这些广告软件的投诉来堵塞客户服务机器。鉴于这种情况，[华为决定在中国 EMUI 9 版本](https://www.xda-developers.com/huawei-confirms-blocking-third-party-launchers-chinese-emui-9/)上屏蔽第三方启动器，现在小米正在中国 rom 上做同样的事情。

这一变化最初是在 Mi 9 的 MIUI 10 中国 9.3.18 版本的固件转储中发现的。“安全中心”APK 内部的字符串表明，小米将阻止“未经验证的”第三方启动器被设置为设备上的默认启动器:

```
 <string name="third_desktop_dialog_<wbr />title">Error</string>
<string name="third_desktop_dialog_<wbr />content">As launcher apps from third parties may result in problems like data leak, abnormal battery drain and lagging, etc., only those verified by MIUI can be set as your default launcher.</string>
<string name="third_desktop_dialog_ok"<wbr />>Got it</string> 
```

这些字符串随后继续在 2019 年 3 月 18 日之后发布的固件中出现。最后，MIUI 10 中国 9.4.1，即 2019 年 4 月 1 日发布的小米 9 版本，禁止用户将其他启动器设置为默认的主屏幕启动器。

我们联系了小米，以了解情况并获得一份声明:

经过验证程序后，中国基于 ROM 的小米智能手机允许使用第三方启动器。任何获准在 Mi 应用商店(我们在中国大陆的应用市场)上市的启动器都将被自动验证，并可以在运行中国 ROM 的 MIUI 智能手机上使用。没有计划在全球(包括印度)固件上实施启动器验证流程。

根据小米发言人的声明，小米采取了比华为相对更软的立场。中国和中国 rom 上的 MIUI 用户没有被完全禁止将其他启动器设置为默认启动器。他们可以将第三方启动器设置为他们的设备默认，只要启动器经过小米的“验证”。我们根据上下文推测，这种验证是为了检查启动器是否会导致异常的设备行为。通过验证过程的启动器可以被设置为设备上的默认启动器。被批准在 Mi 应用程序商店上列出的启动器也将被自动验证，因此应该有一个健康的备选启动器选项可供选择。

我们还向发言人澄清了 launcher-block 是否会进入 MIUI 的全球固件，答案是否定的。MIUI 10 全球固件不受这一变化的影响，用户可以继续将第三方启动器设置为设备上的默认启动器，没有任何障碍。这种封锁不会影响到中国以外的固件，因此也不需要“验证”程序。

即使采取了更温和的立场，这一变化也确实影响了中国消费者，他们希望尝试尚未在小米应用商店上市的新发射器。但这种附带损害似乎符合中国消费者的更大利益。中国设备上的 flash 全球 rom 也因相关原因被小米屏蔽，所以这也是不可能的。我们还没有经过验证的方法绕过这个启动程序块，但是移除安全应用程序应该足够了。

* * *

**对于小米决定在 MIUI 中国 rom 上屏蔽未经验证的第三方启动器，你有什么想法？小米和华为等公司有没有其他选择来对抗经销商的相似广告软件？请在下面的评论中告诉我们你的想法！**