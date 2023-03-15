# 对赛百味安卓应用进行逆向工程

> 原文：<https://www.xda-developers.com/reverse-engineering-the-subway-android-app/>

很高兴看到 Android 应用程序越来越多地采用证书锁定。当我在尝试代理请求时遇到一个抛出连接错误的应用程序时，我倾向于更深入地研究。我最近用地铁 app 的时候就是这样。逆转 APK 揭示了其他一些有趣的发现中的 cert pinning。

代理请求时启动应用程序导致了此错误:

钉住很简单，可以绕过。我从反编译应用程序和分析固定关键词的源代码开始。实际上，我发现在实现了 X509TrustManager 的两个单独的类中固定实现。以下是强制固定的方法之一:

```
 // Code removed at request of Subway leadership
```

绕过这一点很简单，只需在 smali 代码中添加一个 return 语句，跳过上面方法中的锁定代码。注意下面增加的返回-作废语句:

```
 // Code removed at request of Subway leadership
```

在重新编译和安装应用程序后，我惊讶地看到了这个新错误:

赛百味使用定制的应用程序签名验证过程，以防止他们的 APK 被逆转。寻找这个过程的来源，我追溯到下面的方法:

```
 // Code removed at request of Subway leadership
```

这是防止逆向工程的一个有趣的尝试，尽管它实际上只造成了一点延迟。为了绕过这个过程，我简单地添加了一行，通过添加另一个 return-void 行来跳过方法的执行，类似于上面的 pinning bypass 过程。

```
 // Code removed at request of Subway leadership
```

在重新编译和安装应用程序后，我能够成功地代理请求:

在我的研究中，我偶然发现了 Reddit 上的这篇文章。显然，赛百味也在确定用户的设备是否被植入了根。我在源代码中搜索了一下，确认了提到的根检测方法。

```
 // Code removed at request of Subway leadership
```

这是一个应用程序非常重视安全性的很好的例子，但我不太清楚根检查过程背后的推理。尽管证书锁定和签名验证技术通常是一个好主意，但它们只会略微妨碍逆向工程过程。