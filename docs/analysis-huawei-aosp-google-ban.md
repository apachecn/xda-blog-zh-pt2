# 由于美中贸易战，华为对 AOSP 的使用可能处于危险之中

> 原文：<https://www.xda-developers.com/analysis-huawei-aosp-google-ban/>

随着最近对华为的贸易限制，其合作伙伴如谷歌、高通、英特尔和其他公司被迫终止与华为的所有未来协议，包括 T2 撤销华为的安卓许可。普遍的理解是，由于 AOSP 是开源的，华为不能被阻止使用它，这只会导致欧洲和亚洲两个不同版本的 Android 的碎片化。一个是谷歌的 Android 授权和播放商店，另一个是替代品牌和独立的应用商店，就像 Bada/Tizen 和三星 Wave 和 Z 设备一样。我在这里告诉你，不幸的是，这不是真的。华为可能会被禁止使用 AOSP、Tizen、KaiOS、PureOS 和 Sailfish 操作系统。

重要的是要记住开放源码许可在我们当前的版权框架内工作。他们利用我们版权框架的设计，给予几乎每个人复制源代码的权利，只要你遵守许可协议的条款。由于它们在我们的版权框架内运作，当版权框架崩溃时，它们也就崩溃了。一个国家禁止其常驻公司与特定公司签订合同，这破坏了我们的版权系统的工作方式，并因此破坏了开源许可证的工作方式。

如果华为不能与谷歌签订合同，那么他们就不能与谷歌签订 Apache 2.0 许可协议，这意味着他们没有分发 AOSP 代码库的许可证。如果他们没有分发该代码的许可，那么华为任何试图分发该代码的行为都是对谷歌版权的侵犯。

路透社 [在其文章](https://www.reuters.com/article/us-huawei-tech-alphabet-exclusive/exclusive-google-suspends-some-business-with-huawei-after-trump-blacklist-source-idUSKCN1SP0NB)中强调，谷歌不打算终止与华为的开源许可协议，然而，只要美国政府允许，他们只能保持这一立场。华为在[实体名单](https://www.bis.doc.gov/index.php/policy-guidance/lists-of-parties-of-concern/entity-list)上，禁止在美国运营的公司向华为出口零部件，包括软件组件。虽然谷歌已经采取行动，遵守谷歌提供主动访问软件的任何软件(例如，早期访问 Android 安全更新，在整个 [Android Q beta 计划](https://www.xda-developers.com/everything-new-android-q-beta-3/)中获得谷歌的支持，能够在新设备上安装 Google Play 服务等)。)，这些限制同样适用于华为可以在谷歌不采取任何针对华为的行动的情况下使用的软件(如 AOSP 知识库)。虽然美国政府不会强迫谷歌关闭 AOSP 知识库，但如果谷歌不采取适当措施防止实体名单上的公司未经授权使用谷歌的知识产权(包括适当追究大规模侵犯版权行为)，他们可以因谷歌未遵守出口管理法规而对谷歌进行罚款。

谢天谢地，事情可能不会发展到那一步。试图因谷歌没有足够积极地追究开源软件的版权侵权行为而对其进行罚款，可能会导致美国政府和 Alphabet 之间的长期法律斗争，双方都不想参与，但有其他选择。具体来说，美国法律对大规模侵犯版权的行为有刑事处罚，未经许可发行 AOSP 可能属于这种行为。这不同于你通常听说的普通民事版权诉讼，因为这是由美国政府自己提起的，而不是由谷歌提起的。

华为表示，自 2012 年以来，他们一直在建立一个备份操作系统，以防他们不再使用谷歌的安卓系统，然而，他们也可能会感到惊讶。虽然这可能是一个完全干净的操作系统，没有与 AOSP 或任何其他在美国有业务的公司拥有版权的操作系统共享代码，但在这种情况下开发的任何东西都不太可能与安卓 15 年的开发和 Linux 内核 28 年的开发，或 iOS(及其 Unix 根源)几十年的工作相抗衡。即使是 Tizen，凭借其 Linux 内核基础和许多大公司超过 14 年(诚然是分散的)的开发(可以追溯到 Maemo 时代)，也难以在手机上竞争。这让华为进退两难，因为这个备份操作系统很可能要么 1)没有竞争力，要么 2)基于他们可能被禁止使用的东西。

如果他们选择继续使用没有谷歌安卓系统的 AOSP，那就给他们留下了两种可能的情况。

### 仅在中国使用

如果华为决定退出在中国的独家运营，他们将创造一种局面，使他们能够继续在本地应用商店的 EMUI 中使用 AOSP(假设他们可以获得制造手机所需的所有零件)，就像他们目前一样(尽管安全补丁和新 Android 版本的更新速度较慢)。中国因选择性地执行外国实体的版权而臭名昭著。这就是法律上和事实上发挥作用的地方。

虽然华为可能被禁止与谷歌达成许可协议，如果他们在这些情况下使用 AOSP 或 Tizen，将违反美国法律，但如果华为没有在中国境外开展任何活动，美国直接执行上述刑事处罚的能力有限。美国政府可以通过民事诉讼向谷歌施压，要求其在中国获得版权，然而，尽管版权归属明确，但打赢这场特定诉讼的能力值得怀疑，Alphabet 也不愿意在法律战上花费时间和金钱。

因此，尽管华为可能违反了法律条文，但实际上他们或许能够在这件事上生存下来。

### 在西方市场的使用

然而，尽管中国很大，但对华为来说可能还不够。他们可能希望扩展到更大的市场。如果华为瞄准了印度和欧洲，事情会变得更复杂。

马上，民事案件变得更有可能成功，因为它们将能够在更有利于外国公司版权诉讼的司法管辖区提起诉讼。这并没有减轻让谷歌追查此案的难度，但这也不是唯一的变化。同时，这些国家中的许多国家都有这种规模的侵犯版权的刑事犯罪(包括[加拿大](https://laws-lois.justice.gc.ca/eng/acts/C-42/page-22.html#h-104349)、[英国](https://www.gov.uk/government/publications/intellectual-property-offences/intellectual-property-offences)、[印度](http://www.copyright.gov.in/Documents/CopyrightRules1957.pdf)等)。这意味着，华为在这些国家投入的任何资产或人员都有卷入上述案件的风险。

不能保证它会达到那种水平，而且要达到那种水平需要出相当多的差错，但是如果美国政府愿意，他们可以在那种程度上遵循法律条文。如果美国政府全力以赴，他们可能会阻止华为在中国以外的任何地区销售 AOSP 手机。

### 这能持续多久？

虽然这听起来很悲观，但事情可能会好得多。这一贸易禁令将对华为和许多依赖它们的公司造成绝对的损害，因此将有巨大的压力来找到解决方案并解除这一禁令。更重要的是，美国商务部了解这些影响，不愿意长期对个别公司实施贸易禁令，而是与这些公司合作，试图找到解决方案。

这种不情愿在仅仅三年前[即 2016 年初](https://www.nytimes.com/2016/03/08/technology/us-restricts-sales-to-zte-saying-it-breached-sanctions.html?module=inline)首次出现，当时由于中兴违反了美国对伊朗和朝鲜的贸易制裁，美国公司被禁止向中兴出售产品。美国商务部立即表示，他们将给予中兴[为期三个月的临时出口许可证](https://www.ft.com/content/9d8d611e-efdd-11e5-9f20-c3a047354386)，以换取配合正在进行的调查，如果中兴[继续配合](https://www.reuters.com/article/us-zte-managementchanges-sanctions-idUSKCN0X20VO)，他们将继续放宽限制。一年后(临时出口许可证多次延期后)，中兴通讯同意与美国商务部达成一项认罪协议，将完全取消对中兴通讯的贸易限制，换取 8.92 亿美元的罚款，解除和/或惩戒策划违反制裁的人员，一个独立的合规监督机构，七年内任何违反协议的行为都将立即恢复禁令，以及 3 亿美元的保证金，如果中兴通讯违反协议条款，保证金将被没收。

不幸的是，中兴[继续违反](https://www.reuters.com/article/us-china-zte/us-bans-american-companies-from-selling-to-chinese-phone-maker-zte-idUSKBN1HN1P1)这些条款，只解雇了 4 名相关人员，反而给另外 35 名参与的员工发奖金，从而恢复了禁令。然而，事情还没有结束，几个月后，美国商务部与中兴通讯达成了[另一项认罪协议](https://www.cnbc.com/2018/06/07/commerce-secretary-wilbur-ross-the-us-strikes-a-deal-with-zte.html)，中兴通讯将在[解除限制，条件是支付另外 10 亿美元的罚款](https://www.xda-developers.com/zte-1-billion-us-government-trade-ban/)，接受进一步的合规监督，更换董事会，并追加 4 亿美元的保证金(因为最初的认罪协议被违反时，之前的 3 亿美元已被没收)。[美国参议院试图阻止](https://www.xda-developers.com/zte-return-to-business-company-signs-agreement-us-government/)2019 财年国防授权法案的认罪协议，然而，最终通过美国众议院[的 NDAA 2019 版本不包括该条款](https://www.reuters.com/article/us-usa-defense-spending/massive-us-defense-policy-bill-passes-without-strict-china-measures-idUSKBN1KM5WT)。截至发稿时，中兴通讯仍能运营，不再有有效的出口限制(尽管他们仍受协议合规要求的约束。)

虽然现在还为时过早，但这一过程已经可以与华为的情况相提并论。在因向伊朗提供被禁止的金融服务(导致谷歌、英特尔、高通和其他公司[暂停未来与华为的合作](https://www.xda-developers.com/google-revoke-huawei-android-ban-blacklist/)而产生的[初步贸易黑名单](https://www.reuters.com/article/us-usa-china-huaweitech-idUSKCN1SL2W4)之后，美国商务部几乎立即给了华为[为期三个月的出口许可](https://www.reuters.com/article/us-huawei-tech-usa-license-idUSKCN1SQ27T)，以便他们能够履行现有订单。在那份声明中，美国商务部强调，他们将继续评估在最初 90 天之后延长许可的可能性。虽然这是我们目前所能做到的，但我不会对进一步延长该许可以换取合作感到震惊，这种合作在大约一两年后(甚至更短时间内)以认罪协议告终，就像中兴通讯发生的情况一样。

如果是这样，就可以避免对 AOSP 的潜在负面影响。如果美国商务部没有就延长出口许可证的工作与华为的法律团队联系，我会感到惊讶，华为意识到，他们距离能够再次与谷歌和高通在未来的项目上合作只有一个认罪协议(或赢得一场法律战)。我们以前见过这种情况，上次结果很好，中兴[重返市场](https://www.xda-developers.com/zte-axon-10-pro-arrives-in-germany/)并在 Google Play 上使用 Android。当美国政府[从冷战一直到 2000 年限制出口密码术](https://en.wikipedia.org/wiki/Export_of_cryptography_from_the_United_States)(包括开源密码术)时，它(最终)也变得很好，当时引人注目的讨论围绕着 Phil Zimmermann 的 PGP、Peter Junger 的诉讼(Junger 诉 Daley)和 Daniel J. Bernstein 的诉讼(Bernstein 诉美国)。

最后，你会看到很多非律师人士发表的关于这个案件的观点。包括我。我不是律师，我也不是你的律师，你不应该使用这里陈述的任何东西作为法律建议。如果不知何故，你最终陷入了这里的讨论直接影响到你的境地，你真的应该去和你的版权律师谈谈。我的背景是解释税法(特别关注新产品类别的消费税),并且我已经为开发者做了关于软件许可基础的[演讲](https://www.youtube.com/watch?v=_umPfRHFWzM)。虽然这还不足以让你盲目地跟随我的分析，但这足以让我把这些点联系起来，把相关的资料放在一起，并描绘出一幅画面。所以，请深入已经链接的资源，通读这篇分析。如果读完之后你得出了同样的结论，那么就把这篇文章分享给大家吧。如果你不同意，请在下面的评论中告诉我原因。