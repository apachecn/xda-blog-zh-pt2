# 一个假的 POCO F1 Lite 的真正的 Geekbench 测试愚弄了几十个博客

> 原文：<https://www.xda-developers.com/xiaomi-poco-f1-lite-fake-benchmark/>

新硬件和软件的泄露是在线技术出版物的主要内容，其中包括 XDA 开发者。每个漏洞都应该被怀疑，但是来自基准测试服务的漏洞更是如此。没有办法判断基准测试中列出的设备细节是否真实，因此在没有确凿证据的情况下，最好忽略基准测试泄漏。不幸的是，有几十个流行的在线出版物仍然基于基准测试结果发表文章，无论是为了推动点击量，还是因为他们实际上认为结果确实来自未发布的设备。愚弄数十家在线科技出版物的最新基准泄漏是两个 Geekbench 列表，展示了一个“ [POCO F1 Lite](https://browser.geekbench.com/v4/cpu/12400822) ”据称代号为“[天王星](https://browser.geekbench.com/v4/cpu/12397796)”

我不打算费心去谈论这个“POCO F1 Lite”的规格或者 POCO 推出一款中端产品是否有意义，因为我实际上不知道 POCO 是否准备推出一款中端设备。他们很可能是，我们都知道小米喜欢发布多种价位的新设备。我所知道的是，这些 Geekbench 列表(设备细节，而不是分数)和“天王星”的代号是捏造的。我所在的几个 Telegram 小组都是热爱 meme 的定制 ROM 开发者，3 月 13 日，其中一个人想出了一个好主意，“用小米天王星基准破坏 memebois。”他们想看看他们有多容易欺骗人们相信一款代号为“天王星”的小米设备正在研发中，那将是小米 POCO F1 Lite。他们所要做的就是修改一些系统构建属性并运行 Geekbench。**geek bench 的分数本身是合法的，但运行基准测试的设备肯定不是“POCO F1 Lite”**

基准测试结果中出现的伪造系统属性的问题早已为人所知。这篇来自 2016 年末的 [*AndroidPit*](https://www.androidpit.com/why-has-falsifying-benchmarks-become-so-easy) 文章谈到了这是多么容易，你会经常看到[更多持怀疑态度的用户](https://twitter.com/Sudhanshu1414/status/1107298809661407232)喊出明显伪造的基准。是的，显然那不是一个真实的 POCO F2 结果。那其实是我根源[谷歌 Pixel 2 XL](https://forum.xda-developers.com/pixel-2-xl) 运行[安卓 Q beta](https://www.xda-developers.com/android-q-beta-changes-google-pixel/) 。但是，即使是持怀疑态度的用户仍然会被这些虚假的设备列表所迷惑，事实证明，喊出我的虚假 POCO F2 基准测试的用户与提交虚假 POCO F1 Lite 基准测试的贡献者是同一个人。

我花了几分钟伪造了上面的清单，只是为了展示这是多么容易做到。我甚至懒得去伪造 CPU 信息，因为这样做比仅仅修改一些系统属性需要更多的努力。我伪造的 POCO F2 基准测试已经被两家英文和两家德文出版物采用，可能还有更多我还没有发现的报道。如果我真的在这方面付出努力，有什么能阻止我买一台[小米 9](https://www.xda-developers.com/xiaomi-mi-9-qualcomm-snapdragon-855-gamecube-wii-dolphin-emulator/) 并冒充 LG V45 ThinQ、小米 Mix 3S、谷歌 Pixel 4 XL、一加 7、三星 Galaxy Note X 或任何其他我们希望拥有骁龙 855 的设备呢？**绝对没有。**我们甚至讨论过在[我们的评论单元](https://www.xda-developers.com/xiaomi-mi-9-qualcomm-snapdragon-855-gamecube-wii-dolphin-emulator/)上做这件事，但最终决定不做，因为我们不想助长假新闻的传播。(遗憾的是，我明显伪造的 POCO F2 基准已经被一些地方采用了。)

这是否意味着所有的基准泄漏都不可信？不，如果有人使用实际设备运行基准测试，那么未经宣布的设备的详细信息可能会泄露到基准测试列表中。然而，没有办法验证拥有设备*的人实际上运行了基准*来生成在线列表。**如果基准测试是新设备的唯一证据，那么它应该被忽略。**这就是为什么我们忽略了 1 月下旬出现的谷歌 Pixel 3a XL [Geekbench 列表](https://browser.geekbench.com/v4/cpu/11843461)。我们认为它是假的，直到 Android Q 测试版的谷歌相机库中出现了相同的营销名称。Android Q 中的 Pixel 3a XL 参考不太可能是伪造的(除非谷歌正在以我们为代价玩 4D 象棋)，但正如我在上面展示的那样，伪造 Pixel 3a XL Geekbench 列表真的很容易。

当我们泄露新设备的细节时，我们总是有更可靠的信息来源来支持我们的报告。我们通常通过了解或接触设备或未发布固件版本的人来获取可信信息。没有证据证实 POCO F1 Lite 的存在，所以即使我们没有亲眼看到定制 ROM 开发者阴谋伪造它，也应该忽略这个 Geekbench 列表。如果我们发布新小米设备的信息，你会知道我们的信息来自无法伪造的来源。

## 停止相信基准泄漏

那么是什么促使我写这篇文章呢？正如我所说的，我们通常忽略基准泄漏，因为我们不信任它们。关于 Geekbench 测试是否在该清单声称的硬件上运行，有很多不确定性，但这次我们知道不是这样，所以我们使用假 POCO F1 Lite 基准的广泛报道来提醒你不要相信未经证实的基准泄漏。我希望这个假的 POCO 基准只出现在较小的技术博客上，但遗憾的是事实并非如此。有几十种出版物和拥有数十万或数百万粉丝的 YouTubers 报道了这个由一个无聊的定制 ROM 开发者编造的“漏洞”。

POCOPHONE 全球负责人 Alvin Tse 在 Twitter 上对 POCO F1 Lite 进行了[软否认](https://twitter.com/atytse/status/1106532757885370368)。尽管如此，[的一份出版物](https://www.igyaan.in/178119/xiaomi-poco-f1-lite-spotted-on-geekbench-with-4gb-of-ram/)称“证据表明并非如此”，引用 Geekbench 的列表作为他们的证据。[几本](https://www.hindustantimes.com/tech/xiaomi-poco-f1-lite-key-specifications-revealed-ahead-of-official-launch/story-L47ASENrjxcx5e9lthfj7L.html)[印本](https://gadgets.ndtv.com/mobiles/news/poco-f1-lite-geekbench-listing-4gb-ram-snapdragon-660-soc-specifications-2007986) [龙头](https://www.livemint.com/technology/gadgets/poco-f1-lite-appears-on-benchmark-tests-with-snapdragon-660-4gb-ram-1552627035727.html) [在线](https://www.indiatoday.in/technology/news/story/poco-f1-lite-geekbench-snapdragon-660-specs-price-1478437-2019-03-15) [科技](https://www.ibtimes.co.in/poco-f1-lite-price-key-features-tipped-online-can-it-repeat-poco-f1s-success-793955) [刊物](https://www.bgr.in/news/xiaomi-poco-f1-lite-spotted-online-may-soon-launch-with-snapdragon-660-onboard/) [落本](https://www.91mobiles.com/hub/poco-f1-lite-specifications-geekbench-listing/) [为](https://indianexpress.com/article/technology/mobile-tabs/poco-f1-lite-spotted-on-geekbench-with-snapdragon-660-processor-5628079/)[帖本](https://www.mysmartprice.com/gear/xiaomi-poco-f1-lite/)。为数不多的[出版物](https://www.gsmarena.com/poco_f1_lite_key_specs_revealed_through_geekbench-news-36035.php)[社交媒体网站](https://new.reddit.com/r/Android/comments/b1csl6/poco_f1_lite_spotted_on_geekbench_with_snapdragon/) [欧美流行的](https://pocketnow.com/poco-f1-lite-snapdragon-660)也上当了。这些帖子中有许多措辞谨慎，但有多少人阅读了标题之外的内容？其中一些网站知道这些基准泄漏可能是假的，但仍然选择掩盖它们。这样做只会损害他们的信誉。如果众所周知，一篇声称拥有独家信息的文章会被如此明显的造假所蒙骗，我们怎么能相信它呢？这一最新的惨败无疑让我看到了仍有多少出版物落入这些虚假泄露的陷阱，即使我们多年来一直知道在 Geekbench 的数据库中伪造设备细节是多么容易。

* * *

承认伪造 POCO F1 Lite 列表的定制 ROM 开发者要求我们不要说出他的名字，因为他不想被询问他为什么这么做的消息淹没。