# Android 设备安全数据库对比 Android 智能手机安全性

> 原文：<https://www.xda-developers.com/android-device-security-database-compare-smartphone/>

谈到设备，Android 用户有许多选择，有各种规格、功能和不同设备预算的组合。我们被选择宠坏了，但当涉及到不容易衡量和比较的功能时，这让用户感到困惑。以安卓的安全状况为例。Android 安全的现状远非完美，不同 OEM 厂商和不同地区的情况变得更加复杂。因此，如果您必须比较两家不同的 OEM 厂商在其产品组合中提供安全更新的情况，答案可能并不容易找到。一组研究人员通过建立一个关注 Android 设备整体安全水平的数据库来弥补这种情况。

在[虚拟 Android 安全研讨会 2020 活动](https://android.ins.jku.at/symposium/)上，包括 Daniel R. Thomas 先生、Alastair R. Beresfor 先生和 René Mayrhofer 先生在内的一组研究人员发表了一篇名为“Android 设备安全数据库”的演讲。

我们建议观看讲座，以更好地了解数据库的意图和目的，但我们也将尽最大努力封装下面的信息。

[Android 设备安全数据库](https://www.android-device-security.org/)的目的是*收集和发布有关 Android 设备安全态势*的相关数据。这包括关于属性的[信息，如平均补丁频率、保证的最大补丁延迟、最新的安全补丁级别以及其他属性。](https://www.android-device-security.org/attributes/)[数据库目前包括](https://www.android-device-security.org/client/datatable?sort=patchlevel&order=-1)智能手机，如三星 Galaxy S20 (Exynos)、诺基亚 5.3、谷歌 Pixel 4、小米红米 Note 7、华为 P40、索尼 Xperia 10 等。

该演讲提出了一个问题，即智能手机原始设备制造商目前几乎没有动力和可量化的激励来为其智能手机产品组合提供快速和相关的安全更新。智能手机售后支持仍然以 Android 版本更新和设备维修的限制为中心，而整体设备安全并不太重要。对于未来的智能手机，安全更新不是一个营销部门可以轻松地向大多数最终消费者销售的指标，因此这一领域的表现仍然缺乏。由于这些年来发布的智能手机种类繁多，更新不计其数，收集和量化这些数据也是一项艰巨的任务。例如，三星在为其现有设备组合提供安全更新方面做得非常好，如 [Galaxy S10、Galaxy Z Flip、Galaxy A50](https://www.xda-developers.com/samsung-rolls-out-july-2020-security-patch-update-galaxy-s10-z-flip-a50/) 、 [Galaxy Note 10 系列、Galaxy A70](https://www.xda-developers.com/samsung-galaxy-note-10-plus-a70-july-2020-android-security-update-rolling-out/) 和[Galaxy S20 系列](https://www.xda-developers.com/july-2020-android-security-update-google-pixel-samsung-galaxy-s20/)——但仍有太多设备需要评估，而且也没有更大的安全更新进度表来提供历史背景。

Android 设备安全数据库试图以某种方式解决这个问题。早在 2015 年，当一项类似的倡议被采纳时，该团队曾测量过 Android 设备的安全性，并给它们打了满分。旧方法有一些局限性，因为它主要侧重于评估设备是否易受已知漏洞的影响。旧的方法没有考虑设备安全性的其他方面，因此当前的方法试图对整体设备安全性进行更全面的审视。

该团队希望进一步探索的一个领域是预装应用程序在安全性和用户隐私方面的表现。预装的应用程序通常具有提升的权限，这些权限是在平台级别预先授予的。最近一段时间，我们看到对预装应用的关注越来越多——有时表现为对预装三星应用中广告的投诉，有时表现为 T2 在全国范围内禁止几个预装小米应用。如何监管原始设备制造商预装的应用程序？

研究团队正在解决这个问题，他们建议在设备上预装什么应用程序以及他们有权做什么方面增加透明度和问责制。为此，该团队还希望将应用程序风险评级添加到他们的数据库中，并最终创建一个评级系统，以在这方面对设备进行评级。该研究团队还希望其方法得到同行的评审，并寻求其他安全研究人员的反馈，以了解他们应该调查预装应用程序的哪些安全方面。

该数据库旨在成为评估设备整体安全性和 OEM 整体安全体验的基准。在这个阶段，该计划无疑是一项正在进行中的工作，未来的计划包括开发一个以匿名方式收集安全属性的应用程序，并以可比较的方式将其呈现给最终用户，就像当前一代性能基准测试的工作方式一样。随着足够多的用户自愿将这些数据提供给项目，人们可以希望该项目成为一个可行的安全基准，可以用来评估 OEM 的整体安全实践。虽然过去的表现肯定不能保证未来的行动，但这个数据库/基准仍然可以简化目前作为操作系统的 Android 安全性的不透明和复杂的混乱状态。