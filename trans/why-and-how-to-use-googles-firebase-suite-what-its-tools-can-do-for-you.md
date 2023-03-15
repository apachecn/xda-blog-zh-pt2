# 为什么以及如何使用谷歌的 Firebase 套件:它的工具能为你做什么

> 原文：<https://www.xda-developers.com/why-and-how-to-use-googles-firebase-suite-what-its-tools-can-do-for-you/>

Android 应用程序开发的基本构建块可以缩减为一个集成开发环境(IDE)和一个运行它的设备或仿真器，虽然这些足以构建一个应用程序，但许多其他工具可以增强开发人员的体验，帮助产品背后的团队扩展产品，改善用户体验，增加参与度和保留率，并获得更多收入。

Twitter 是这些工具中最强大、最可靠的套件之一 [Fabric](https://fabric.io) 的幕后推手，谷歌通过将其实时数据库收购 Firebase 转变为成熟的移动开发套件，掀起了*的热潮*。Firebase 包括各种各样的工具，实现简单明了，是 Mountain View 的一个令人印象深刻的产品，所以看看它能做什么，并开始在您的产品中实现它。

### 分析学

尽管谷歌分析为应用使用和用户参与的洞察提供了一个强大的解决方案，但出于各种原因，大量专业开发人员选择走第三方路线，选择 Flurry 和 Fabric 等工具。Firebase Analytics 旨在满足这一需求

Firebase Analytics 最简单的用法是记录安装、用户属性和一组预定义的[事件](https://firebase.google.com/docs/reference/android/com/google/firebase/analytics/FirebaseAnalytics.Event)，而[文档](https://firebase.google.com/docs/analytics/android/start/)提供了更高级用法的说明。实施分析套件是开发人员可以采取的最有益的步骤之一，因为它提供了有关用户行为、目标人口统计、潜在陷阱、体验异常和使用热图的数据，有助于决策和营销。

##### 简单用法

```
compile 'com.google.firebase:firebase-core:9.2.0'
```

```
private FirebaseAnalytics mFirebaseAnalytics;

mfirebase analytics = firebase analytics . getinstance(this)；

作家（author 的简写）

如今，大多数应用程序需要知道用户的身份，这使得它们能够存储每个用户的独特数据。这反过来允许产品识别用户，并提供跨平台的个性化无缝体验。鉴于用户群在身份验证提供者方面的偏好各不相同，身份验证通常是一个繁琐的过程。

 [Firebase 认证](https://firebase.google.com/docs/auth/)封装了这个过程，通过供应商谷歌、脸书和推特，通过 OAuth 2.0 和 OpenID 等行业标准进行认证，不需要任何服务器端代码。

使用谷歌认证的简单用法

```
compile 'com.google.firebase:firebase-auth:9.2.0'

编译“com . Google . Android . GMS:play-services-auth:9 . 2 . 0”

```
GoogleSignInOptions gso = new GoogleSignInOptions.Builder(GoogleSignInOptions.DEFAULT_SIGN_IN)  .requestIdToken(getString(R.string.default_web_client_id))  .requestEmail()  .build();
```

数据库

Firebase 最初是一个实时数据库产品，后来被谷歌收购，并在很长一段时间内保持这种状态，后来经历了一次课程调整。仍然是该套件的基石， [Firebase 实时数据库](https://firebase.google.com/docs/database/)允许开发人员将数据以 JSON 格式存储在 NoSQL 数据库中，为所有连接的设备提供实时同步选项和离线可用性。

免费的 Firebase 计划对并发数据库连接和每秒写入次数有限制，而付费层提供了更大的灵活性。该模型实现起来非常简单，提供了一个功能强大的工具，只需几行代码，控制台提供了高级选项，如可选的身份验证。

简单用法

```
compile 'com.google.firebase:firebase-database:9.2.0'

```
FirebaseDatabase database = FirebaseDatabase.getInstance();

数据库参考 迈雷夫  =  数据库 。get reference(【消息】)； 

myRef 。setValue(“你好，世界！”)；
```

### 储存；储备

大多数应用程序需要在云上存储一定量的数据，无论是图像、音频还是视频。这些应用程序中的大多数依赖于私有服务器来交付这些数据，而 [Firebase Storage](https://firebase.google.com/docs/storage/) 旨在为此提供一个更简单的解决方案。在谷歌云存储的支持下，无论网络质量如何，该工具都可以提供安全的文件上传和下载，甚至为免费计划提供了大量的空间。

##### 简单用法

```
compile 'com.google.firebase:firebase-storage:9.2.0' 编制 'com.google.firebase:firebase-auth:9.2.0'

```
FirebaseStorage storage = FirebaseStorage.getInstance();
```

主办；主持

虚拟主机是整个互联网的基石，好的免费主机很难找到。 [Firebase Hosting](https://firebase.google.com/docs/hosting/) 旨在成为构建和部署 web 应用程序的完美解决方案，以及轻松将静态内容部署到全球 CDN(内容交付网络)中。它还提供了一个在托管内容上放置自定义域的选项，使开发者能够为他们的 web 应用程序提供友好的 URL。

Firebase Hosting 提供 SSL 配置的存储和 SSD 缓存，确保快速安全地加载内容。部署是通过简单的命令行执行完成的，控制台中有一个选项可以回滚到旧版本。

简单用法

```
npm install -g firebase-tools

火灾基地初始化

消防基地部署
```

远程配置

在衡量应用的成功和增长时，用户体验可能是最关键的指标，提供完美的用户体验通常需要进行一定数量的实验，探索多种选择以找到正确的选择。此前，这是通过连续更新和后续分析收集来实现的，但 [Firebase Remote Config](https://firebase.google.com/docs/remote-config/) 通过允许行为和外观变化而无需任何更新，消除了所有复杂性。

远程配置由应用程序向服务器请求某组参数来执行，如果用户属于所需的部分，则从控制台检索开发人员定义的值，在任何负面结果的情况下，返回到默认的应用程序内值

简单用法

```
compile 'com.google.firebase:firebase-config:9.2.0'

```
mFirebaseRemoteConfig = FirebaseRemoteConfig.getInstance();
```

### 测试实验室(仅 Blaze 计划)

作为测试实验室的设备农场最近获得了巨大的牵引力，尽管 Google Play 开发者控制台提供了一个测试实验室的基本版本，但 [Firebase 测试实验室](https://firebase.google.com/docs/test-lab/)将其提升了一个档次，自动提供一键部署到各种设备和设备配置。结果包括日志、屏幕截图以及执行和崩溃的屏幕记录，允许开发人员在设备上进行强大的测试后，在发布之前识别并修复潜在的错误。

该测试实验室仅适用于现收现付的 Blaze 计划，测试价格为 5 美元/设备小时。该过程可以从 Android Studio 本身启动，并与 CI(持续集成)设置很好地集成。

### 碰撞

Android 上的崩溃报告经历了与分析类似的命运，Crashlytics 是大多数开发人员选择的广受欢迎的解决方案。然而， [Firebase 崩溃报告](https://firebase.google.com/docs/crash/)是谷歌在该领域的玩法，因为这是扩展应用程序的一个关键领域，通常是成败的因素。

Firebase 崩溃报告通过简单地将该库添加到 Gradle 构建脚本，根据严重性、堆栈跟踪、受影响的用户等对错误进行分类和分组，来自动报告崩溃。该库还支持更高级的实现，允许开发人员记录导致崩溃的事件。

##### 简单用法

```
compile 'com.google.firebase:firebase-crash:9.2.0'
```

### 通知

以前被称为 C2DM(云到设备消息传递)，谷歌的云消息服务经历了又一次命名转变，摆脱了谷歌云消息传递的绰号，成为 Firebase 云消息传递。该服务允许开发者免费向设备发送少量数据，无论是通知、即时消息还是同步信息。

一个基本的实现只需要将这个库添加到 Gradle build 脚本中，允许开发人员向设备发送基本的推送通知。更高级的实现包括消息接收处理、设备到云回复等。

##### 简单用法

```
compile 'com.google.firebase:firebase-messaging:9.2.0'
```

### 动态链接

动态链接是智能 URL，可以根据激活它们的平台打开不同的内容。虽然这不是一个新概念，但 Firebase 动态链接允许目标细分市场增加获取、保留和生命周期价值，还可以跨应用程序安装工作，如果相关应用程序不在设备上，则挂钩到 Google Play 以提示安装。

Firebase 动态链接还包括以前称为 Google AppInvites 的东西，允许用户与他们的圈子共享应用程序，如果应用程序已安装，则提示打开，如果应用程序不存在，则提示安装。

##### 在控制台中创建动态链接后的简单用法

```
compile 'com.google.firebase:firebase-invites:9.2.0'
```

```
<intent-filter>  <action android:name="android.intent.action.VIEW"/>  <category android:name="android.intent.category.DEFAULT"/>  <category android:name="android.intent.category.BROWSABLE"/>  <data android:host="example.com" android:scheme="http"/>  <data android:host="example.com" android:scheme="https"/>

</意图过滤> 
```

### AdMob

谷歌历史悠久的移动广告平台已经纳入 Firebase 的保护伞下，与 Firebase Analytics 相连，以提供更多的使用细节。现有的 AdMob 配置可以保持不变，无缝集成，唯一的要求是一个小的[链接过程](https://support.google.com/admob/answer/6383165)。

##### 简单用法

```
Getting Started with AdMob
``` 
```

``` 
```

```

```