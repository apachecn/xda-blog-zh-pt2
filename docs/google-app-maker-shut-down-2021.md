# 谷歌应用制造商将于 2021 年关闭

> 原文：<https://www.xda-developers.com/google-app-maker-shut-down-2021/>

到目前为止，得知谷歌正在关闭自己的一项服务应该不会让人感到意外。谷歌墓地的名单很长:谷歌阅读器、收件箱、[谷歌+](https://www.xda-developers.com/google-plus-shutdown-data-breach/) 、Talk、Hangouts、 [Allo](https://www.xda-developers.com/google-allo-shutting-down/) 、Picasa...这种情况一直持续下去。该公司尤其迂腐的是，如果它发现服务的使用率没有达到应有的水平，就会关闭服务。现在，它宣布面向企业用户的 GSuite 服务 Google App Maker 将于 2021 年 1 月 19 日关闭。

谷歌应用制造商[于 2016 年 12 月宣布面向 GSuite 用户](https://www.xda-developers.com/google-announces-app-maker-for-g-suite-customers/)。GSuite 用户为生产力和存储解决方案付费，谷歌提供了几项 GSuite 专有服务，比如面向企业的 [Hangouts Chat 和 Hangouts Meet](https://www.xda-developers.com/hangouts-chat-slack-alternative-g-suite/) 。由于模板和 UI 元素的拖放功能，App Maker 是一个让企业无需编写太多代码就能构建应用程序的工具。它可以用来构建内部工具。在 2016 年发布预览版后，它在 2018 年作为稳定版本推出。谷歌的论点是，企业不应该担心代码来构建供内部使用的应用程序。然而，GSuite 用户似乎并不接受这项服务，这导致了它被关闭的预期结果。

谷歌表示，“由于使用率低，谷歌应用制造商将在 2020 年期间逐渐关闭，并于 2021 年 1 月 19 日正式关闭”。管理员需要审查其所在领域的 App Maker 使用情况。管理员、最终用户和开发人员都会受到此次发布的影响。

即使 App Maker 不再处于积极开发中，现有的应用程序今天仍将继续工作。然而，从 2020 年 4 月 15 日开始，用户将不再能够创建新的 App Maker 应用，但仍然可以编辑和部署现有的应用。从 2021 年 1 月 19 日开始，现有的 App Maker 应用程序将停止工作，用户将不再能够访问它们。存储在云 SQL 中的 App Maker 数据将保持不变，并将遵循用户 GCP 帐户建立的策略。

谷歌还表示，由于 App Maker 使用的特定源代码，用户不能直接将他们的应用程序迁移到另一个平台，这可能不会让 App Maker 的低量用户高兴。Google 推荐 AppSheet 作为自动化复杂业务流程的替代品。AppSheet 两周前被谷歌收购，由于它支持云 SQL 数据库(App Maker 数据也存储在云 SQL 中)，它允许用户在现有数据库上构建一个与他们的 App Maker 应用程序绑定的应用程序。

另一方面，App Engine 被 Google 推荐作为 App Maker 的替代品，作为一个 App 构建工具。这是一个完全托管的平台，可以构建和部署谷歌云平台(GCP)应用。App Engine 应用程序可以构建在与用户的 App Maker 应用程序相关的现有云 SQL 数据库之上。最后，在数据收集方面，该公司推荐谷歌表单作为替代品，指出它有许多在 App Maker 推出时不可用的新功能。

谷歌建议企业删除不再使用的 App Maker 应用，同时指出 App Maker 数据属于用户的组织。构成 App Maker 应用程序本身的数据从 App Maker 编辑器中导出，此导出功能将一直工作到 2021 年 1 月 19 日。该公司表示，最近它向用户域的主要管理员发送了电子邮件，并提供了一个 CSV 文件，其中包含用户组织中正在使用的 App Maker 应用程序的列表，该列表包括应用程序名称、创建者名称、每个应用程序的上次修改数据，以及一个指向用户管理控制台的链接，其中包含特定应用程序的使用统计数据和项目信息。

App Maker 在理论上是一个好主意，但正如许多谷歌服务一样，它并没有获得很大的人气。谷歌收购 App Sheet——被宣传为无代码移动应用构建平台——是否会是一场同样注定失败的冒险，还有待观察。

* * *

**来源:[谷歌](https://gsuiteupdates.googleblog.com/2020/01/app-maker-update.html)**