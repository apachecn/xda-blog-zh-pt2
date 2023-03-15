# Firebase 添加了新的本地仿真器 UI、支付处理扩展和 ML 模型管理 API

> 原文：<https://www.xda-developers.com/google-firebase-adds-new-local-emulator-ui-payment-processing-extensions-ml-model-management-api/>

Firebase 是 Google 提供的一个工具集，为移动开发者提供了一个统一的后端即服务(BaaS)平台。简而言之，Firebase 提供了相当多的代码内实用工具，如分析、认证、数据库、配置、推送消息、文件存储等等。整个平台可以帮助开发人员在其应用程序中完成许多常见任务，而无需为这些任务单独构建自己的解决方案。例如， [Firebase Auth SDK 让开发人员可以轻松地为他们的应用程序添加一个完整的登录系统](https://www.xda-developers.com/firebase-authentication-sign-in-with-apple/)和一个附带 UI 的[。最近，F](https://opensource.google/projects/firebaseui) [irebase 增加了新的工具和特性](https://firebase.googleblog.com/2020/07/product-news-and-other-highlights-from.html)，比如新的模拟器 UI、Stripe 支付处理扩展、增强的 TensorFlow lite 部署等等。

## 用于本地开发的新仿真器 UI

Firebase 模拟器套件于去年推出，现在，Firebase 团队在测试版发布渠道推出了新的本地模拟器 UI。该模拟器 UI 将帮助开发人员轻松安全地测试新代码，而无需等待部署或支付费用。您还可以让新开发人员使用几个 CLI 命令来快速创建 Firebase 服务的本地实例。

仿真器套件现在还支持[安全规则](https://firebase.google.com/docs/rules)的即时代码重新加载。

## 条纹付款处理扩展

Firebase 还提供扩展，这些扩展是预打包的代码包，开发人员可以使用它们来自动化常见的开发任务。现在，Firebase 与 Stripe 合作建立了两个新的扩展，允许开发人员快速添加和管理他们应用程序的支付处理功能。 [Send Invoices with Stripe](https://firebase.google.com/products/extensions/firestore-invoice-stripe) 扩展允许开发人员使用 Stripe 支付平台以编程方式创建和发送品牌客户发票。[使用 Stripe](https://firebase.google.com/products/extensions/firestore-stripe-subscriptions) 运行订阅支付扩展可用于为使用 Stripe 的 web 用户创建和同步订阅，以及通过 Firebase 身份验证控制对订阅内容的访问。有了这些扩展，作为开发人员，您不需要学习 Stripe 的 API 或弄清楚如何将 Stripe 与 Firebase 集成——只需安装这些扩展，您就可以开始工作了。

## 增强型 TensorFlow Lite 部署

Firebase 还引入了 ML 模型管理 API，允许开发人员以编程方式将 ML 模型更新和部署到 TensorFlow Lite，而无需使用控制台。当有一个机器学习管道自动用新数据重新训练模型时，这尤其有用，因为您现在可以通过编程将更新的模型上传到 Firebase。这声称可以减少初始应用程序安装大小，允许 A/B 测试多个模型，评估性能，并更新模型，而无需重新发布整个应用程序。

* * *

由于过去几个月没有实体活动，谷歌一直在主持 Firebase Live 视频，就各种相关主题通知和教育开发人员。谷歌在过去一年中也宣布了许多 Firebase 的新功能和改进，包括[早期访问程序 API](https://www.xda-developers.com/google-decouples-ml-kits-on-device-apis-from-firebase-and-introduces-early-access-apis/) 、[c++和 Unity 云 Firestore】，以及](https://www.xda-developers.com/google-for-games-new-developer-tools-play-firebase-android-studio/)[通过 Firebase 认证登录苹果](https://www.xda-developers.com/firebase-authentication-sign-in-with-apple/)。