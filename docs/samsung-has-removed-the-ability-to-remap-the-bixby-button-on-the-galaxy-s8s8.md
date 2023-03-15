# [更新:三星确认]三星已经删除了 Galaxy S8/S8+上重新映射 Bixby 按钮的功能

> 原文：<https://www.xda-developers.com/samsung-has-removed-the-ability-to-remap-the-bixby-button-on-the-galaxy-s8s8/>

**更新(美国中部时间下午 1:38):我们了解到，三星在 Twitter 上的代表已经确认取消这项重新映射功能。**

**更新 2(美国中部时间下午 2:05):一名在美国拥有 Galaxy S8 审查单元的用户(希望匿名)声称，他们的设备是最新的，仍然能够重新映射 Bixby 按钮。**

虽然三星 Galaxy S8 和 Galaxy S8+尚未到达绝大多数用户的手中，但一些用户已经提前几天拿到了他们的机型。与新发布的智能手机一样，通常会有一些小的 OTA 更新，以修复问答过程中没有发现的一些错误。然而，这一次似乎是通过 OTA 更新来重新设计设备上的某个功能 Bixby 按钮。显然，这次更新是**移除了重新映射 Bixby 按钮**的功能。我们知道这是可能的，但我们没想到三星会真的去做。

简单回顾一下，我们了解到在 4 月 4 日可以重新映射 Bixby 按钮来执行几乎任何你想要的动作。这之所以成为可能，是因为当按下 Bixby 按钮(或任何其他硬件按钮)时，系统会生成一个 key up 和 key down 事件，可访问性服务会截获该事件。因此，在我的教程中，一体式手势应用程序要求您启用其辅助功能服务。

正如你可能猜到的那样，三星要移除重新映射 Bixby 的功能所要做的就是阻止辅助服务拦截这个关键事件。显然，这正是他们现在正在做的，至少根据 XDA 公认的开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) 所说，他是[按钮映射器](https://www.xda-developers.com/xda-spotlight-button-mapper-an-app-to-remap-your-phones-hardware-buttons/)的开发者。

Flar2 在从加拿大 Telus 收到他的三星 Galaxy S8 后不久，正在更新他的[按钮映射器](https://play.google.com/store/apps/details?id=flar2.homebutton&hl=en)应用程序，以支持重新映射 Bixby 按钮。他最初能够让应用程序工作，但在他从三星下载了最新的系统更新(构建版本 NRD90M)之后。G950WVLU1AQD9)，他发现他的应用程序不再工作。原来，三星已经**修改了系统，在它到达可访问性服务之前消耗 Bixby 按钮的关键事件**，有效地使其截至目前无法重新映射 Bixby 按钮(*至少在没有 root 访问权限的情况下*)。

我们对这一发展感到非常失望。我们理解三星希望让用户将 Bixby 按钮用于其预期目的的动机，但许多可用于重新映射 Bixby 按钮的教程只是为那些想要它的用户提供的。如果三星不想让媒体报道用户正在寻找重新映射 Bixby 按钮的事实，也许他们应该首先[努力让该功能完全开箱即用](https://www.xda-developers.com/galaxy-s8s-bixby-voice-assistant-reportedly-wont-be-available-out-of-the-box/)。

* * *

## 更新:三星代表证实

三星美国审查项目负责人菲利普·伯恩(Philip Berne)证实，三星确实停止了重新映射 Bixby 按钮的功能。

虽然 Berne 先生后来说他不能确定为什么行为改变了(我们认为原因是相当明显的)，但我们不同意用于重新映射 Bixby 按钮的方法是“利用系统级行为”的描述启用辅助功能服务来拦截按键事件是一个完全合法的功能，许多应用程序都是围绕这个功能构建的，当用户使用这些应用程序时，不存在任何漏洞。

* * *

## 更新 2:运营商特定？

一位希望匿名的用户在 Twitter 上给我们发来消息，称他的三星 Galaxy S8 review 设备仍然能够重新映射 Bixby 按钮。此外，他声明他的单元是最新的。

我们不排除这是特定于运营商的可能性，但目前我们不认为这是可能的答案，因为它提出的问题对我们来说没有多大意义。首先，为什么加拿大的 Telus 公司(flar2 向其购买 Galaxy S8 的运营商)要求取消这一能力？如果这位用户所说的是真的，我们如何理解三星美国代表的推文？

我们希望能得到三星或 Telus 的官方声明来澄清此事。

* * *

非常感谢 flar2 的独家报道！