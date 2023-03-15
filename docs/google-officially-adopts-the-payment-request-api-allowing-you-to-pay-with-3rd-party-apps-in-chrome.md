# 谷歌正式采用支付请求 API，允许你在 Chrome 中使用第三方应用支付

> 原文：<https://www.xda-developers.com/google-officially-adopts-the-payment-request-api-allowing-you-to-pay-with-3rd-party-apps-in-chrome/>

[将在即将举行的谷歌 I/O 开发者大会上宣布](https://events.google.com/io/schedule/?section=may-17&sid=37a7711e-9e35-43f1-971c-7b8b87e165b2),支付请求 API 将彻底改变我们在移动设备上进行在线支付的方式。Android 上的谷歌 Chrome 用户将不再需要经历漫长的结账过程，包括输入信用卡信息或登录 PayPal。相反，该 API 使网站开发者能够向受支持的第三方支付应用发送意向，以便进行支付。与谷歌为我们准备的许多[其他惊喜](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/)不同，**已经有大量关于这种新支付方式将如何运作的公开信息**。我们已经深入研究了所有这些文件，以便在谷歌本周正式宣布之前给你带来一些信息。

* * *

## 使用付款申请 API 简化付款

让我们首先回顾一下目前网络浏览器是如何处理支付的。当你去任何一个网上商家的结账页面，都会被要求输入你的支付信息。您可以添加商家支持的信用卡，或者使用 PayPal 等集成服务来完成交易。现在，除非你已经在网站上保存了你的信用卡信息(很多人不愿意这样做)或者已经登录了 PayPal，否则起床，去你的钱包，找到你的卡，然后输入卡号，有效期和安全码可能会很麻烦。每次你想在一个新的网站上购物，你都要经历这个过程的一些变化。对于我们这些喜欢寻找交易的人来说，这很快就会变得令人讨厌。

*各种网商结账页面*

许多信用卡和银行机构都可以在谷歌 Play 商店上申请。既然我们已经在使用这些应用程序来监控我们的财务账户，为什么我们不能使用它们来认证支付呢？这正是网络支付工作组背后的思维过程，该工作组由谷歌、Mozilla、三星、阿里巴巴、微软等成员组成。该小组一直在幕后工作，以便**引入一个名为支付请求 API** 的新 API 和一个在支付清单提案中定义的新在线标准，从而促进网络浏览器和在线商家之间的通信，以便在线商家可以使用最终用户设备上的现有应用来处理支付。

### 它是如何工作的

为了完成这项任务，网络浏览器[必须支持支付请求 API](https://w3c.github.io/browser-payment-api/) ，在线商家需要通过实现所谓的[支付方式标识符](https://github.com/zkoch/zkoch.github.io/blob/master/pmi-v2.md)来支持 API，安卓应用[需要实现新的服务](https://docs.google.com/document/d/1izV4uC-tiRJG3JLooqY3YRLU22tYOsLTNq0P_InPJeE/edit)。在不涉及太多细节的情况下，我将简单解释一下在结帐过程中发生了什么。

假设您的网络浏览器支持支付请求 API(稍后将详细介绍)，当您导航到在线商家的支付页面时，您将可以选择使用他们支持的支付处理程序(信用卡/PayPal/等)进行支付。)当你点击按钮进行购买时(例如在下面 Googlers 用来测试支付请求 API 的示例页面上)，支付请求 API 会向支持的支付应用程序发送一个 Android 意向，以便该应用程序验证用户的支付。

假设我们假设的信用卡应用程序安装在一个假设的 Android 设备上，名为 Bob Pay。Bob Pay 会将以下内容添加到他们的 AndroidManifest.xml 文件中:

```
 <span style="font-weight: 400;"><manifest</span> <span style="font-weight: 400;">package=</span><span style="font-weight: 400;">"com.bobpay.app"</span><span style="font-weight: 400;">></span>
<span style="font-weight: 400;">  </span><span style="font-weight: 400;"><service</span> <span style="font-weight: 400;">android:name=</span><span style="font-weight: 400;">".IsReadyToPayService"</span>
<span style="font-weight: 400;">           </span><span style="font-weight: 400;">android:enabled=</span><span style="font-weight: 400;">"true"</span>
<span style="font-weight: 400;">           </span><span style="font-weight: 400;">android:exported=</span><span style="font-weight: 400;">"true"</span><span style="font-weight: 400;">></span>
<span style="font-weight: 400;">    </span><span style="font-weight: 400;"><intent-filter></span>
<span style="font-weight: 400;">      </span><span style="font-weight: 400;"><action</span> <span style="font-weight: 400;">android:name=</span><span style="font-weight: 400;">"org.chromium.intent.action.IS_READY_TO_PAY"</span> <span style="font-weight: 400;">/></span>
<span style="font-weight: 400;">    </span><span style="font-weight: 400;"></intent-filter></span>
<span style="font-weight: 400;">  </span><span style="font-weight: 400;"></service></span>
<span style="font-weight: 400;">  </span><span style="font-weight: 400;"><activity</span> <span style="font-weight: 400;">android:name=</span><span style="font-weight: 400;">".PaymentActivity"</span>
<span style="font-weight: 400;">            </span><span style="font-weight: 400;">android:exported=</span><span style="font-weight: 400;">"true"</span><span style="font-weight: 400;">></span>
<span style="font-weight: 400;">    </span><span style="font-weight: 400;"><intent-filter></span>
<span style="font-weight: 400;">      </span><span style="font-weight: 400;"><action</span> <span style="font-weight: 400;">android:name=</span><span style="font-weight: 400;">"org.chromium.intent.action.PAY"</span> <span style="font-weight: 400;">/></span>
<span style="font-weight: 400;">    </span><span style="font-weight: 400;"></intent-filter></span>
<span style="font-weight: 400;">    </span><span style="font-weight: 400;"><meta-data</span> <span style="font-weight: 400;">android:name=</span><span style="font-weight: 400;">"org.chromium.default_payment_method_name"</span>
<span style="font-weight: 400;">               </span><span style="font-weight: 400;">android:value=</span><span style="font-weight: 400;">"https://bobpay.com/put/optional/path/here"</span> <span style="font-weight: 400;">/></span>
<span style="font-weight: 400;">  </span><span style="font-weight: 400;"></activity></span>
<span style="font-weight: 400;"></manifest></span> 
```

当一个意图被发送到这个假设的信用卡应用程序时，这个应用程序的服务被启动。我们假设的 Bob Pay 应用程序需要所有的信息来了解购买了什么，从哪个供应商那里购买，以及购买了多少钱，这些信息都包含在意向的附加信息中:

```
 Bundle extras = new Bundle();
extras.putString("key", "value");
intent.putExtras(extras); 
```

一旦 Bob Pay 验证了付款，付款请求 API 就会收到 Bob Pay 发送的另一个意向信息:

```
 Intent result = new Intent();
Bundle extras = new Bundle();
extras.putString("key", "value");
result.putExtras(extras);
setResult(RESULT_OK, result); // Change to RESULT_CANCELED on failure.
finish();  
```

但是，支持 Bob Pay 的在线商家如何知道你手机上安装的 Bob Pay 是真正的 Bob Pay，而不是一些旨在实施欺诈的恶意软件？它通过创建浏览器可机读的支付方式清单标识符 JSON 文件来实现这一点。

```
 {
  <span ><span >"</span>name<span >"</span></span><span >:</span> <span ><span >"</span>BobPay - World's Greatest Payment Method<span >"</span></span>,
  <span ><span >"</span>description<span >"</span></span><span >:</span> <span ><span >"</span>This payment method changes lives<span >"</span></span>,
  <span ><span >"</span>short_name<span >"</span></span><span >:</span> <span ><span >"</span>BobPay<span >"</span></span>,
  <span ><span >"</span>icons<span >"</span></span><span >:</span> [{
    <span ><span >"</span>src<span >"</span></span><span >:</span> <span ><span >"</span>icon/lowres.webp<span >"</span></span>,
    <span ><span >"</span>sizes<span >"</span></span><span >:</span> <span ><span >"</span>64x64<span >"</span></span>,
    <span ><span >"</span>type<span >"</span></span><span >:</span> <span ><span >"</span>image/webp<span >"</span></span>
  },{
    <span ><span >"</span>src<span >"</span></span><span >:</span> <span ><span >"</span>icon/lowres.png<span >"</span></span>,
    <span ><span >"</span>sizes<span >"</span></span><span >:</span> <span ><span >"</span>64x64<span >"</span></span>
  }, {
    <span ><span >"</span>src<span >"</span></span><span >:</span> <span ><span >"</span>icon/hd_hi<span >"</span></span>,
    <span ><span >"</span>sizes<span >"</span></span><span >:</span> <span ><span >"</span>128x128<span >"</span></span>
  }],
  <span ><span >"</span>serviceworker<span >"</span></span><span >:</span> {
    <span ><span >"</span>src<span >"</span></span><span >:</span> <span ><span >"</span>payment-sw.js<span >"</span></span>,
    <span ><span >"</span>scope<span >"</span></span><span >:</span> <span ><span >"</span>/pay<span >"</span></span>,
    <span ><span >"</span>use_cache<span >"</span></span><span >:</span> <span >false</span>
  }
  <span ><span >"</span>related_applications<span >"</span></span><span >:</span> [
    {
      <span ><span >"</span>platform<span >"</span></span><span >:</span> <span ><span >"</span>play<span >"</span></span>,
      <span ><span >"</span>url<span >"</span></span><span >:</span> <span ><span >"</span>https://play.google.com/store/apps/details?id=com.bobpay<span >"</span></span>,
      <span ><span >"</span>fingerprints<span >"</span></span><span >:</span> [{
        <span ><span >"</span>type<span >"</span></span><span >:</span> <span ><span >"</span>sha256_cert<span >"</span></span>,
        <span ><span >"</span>value<span >"</span></span><span >:</span> <span ><span >"</span>59:5C:88:65:FF:C4:E8:20:CF:F7:3E:C8...<span >"</span></span>
      }], <span >//new</span>
      <span ><span >"</span>min_version<span >"</span></span><span >:</span> <span ><span >"</span>1<span >"</span></span>, <span >// new</span>
      <span ><span >"</span>id<span >"</span></span><span >:</span> <span ><span >"</span>com.example.app1<span >"</span></span>
    }, {
      <span ><span >"</span>platform<span >"</span></span><span >:</span> <span ><span >"</span>itunes<span >"</span></span>,
      <span ><span >"</span>url<span >"</span></span><span >:</span> <span ><span >"</span>https://itunes.apple.com/app/example-app1/id123456789<span >"</span></span>,
    }
  ]
} 
```

在这个 JSON 文件中有一个签名，用于验证安装在您设备上的应用程序的完整性，该应用程序声称是真正的 Bob Pay。如果签名检查失败，那么 Bob Pay 将不会被接受为付款处理人。

当然，我非常，非常，非常简化了这里涉及的一般过程。支付是一个极其复杂的系统，需要多层安全检查，以确保只进行有效的支付。我之前链接的三个文档概述了浏览器如何完全实现支付请求 API，网站如何实现 JSON 清单文件，以及 Android 应用程序如何处理支付请求 API 发送的意图。下面是一个流程图，概括了我上面总结的一般过程:

*付款流程图。来源:[Rouslan Solomakhin](https://docs.google.com/document/d/1izV4uC-tiRJG3JLooqY3YRLU22tYOsLTNq0P_InPJeE/edit#)*

如您所见，这里涉及到许多步骤。所有这些变化都将由在线商家网站、Android 银行/信用卡应用程序和网络浏览器的开发人员来处理，因此最终用户可能不知道这里到底发生了什么。但要知道，最终结果是，如果所有相关方都实施这些变革，您的在线支付将变得更加简单，这要归功于网络支付工作组的标准化努力，有望成为现实。

* * *

## 付款申请 API 背后的历史记录

万维网联盟(缩写为 W3C)成立于 1994 年，旨在开发平台标准，使所有网站及其用户受益于互兼容性和一致性。为了解决网络支付日益分散的问题，W3C 在 2015 年成立了[网络支付工作组，以标准化在线支付流程的某些方面。此后，网上支付工作组的所有成员开始工作，以便找到加强现有网上支付系统工作方式的方法。](https://www.w3.org/Payments/WG/charter-201510.html)

该小组提出了[支付请求 API](https://w3c.github.io/browser-payment-api/) ，这是一组允许网站使用支付方法而无需将支付方法集成到网站中的方法。[网络浏览器需要更新以支持 API](https://caniuse.com/#feat=payment-request) ，但更困难的部分源于**让网络商家加入**。为此，工作组成员[提出了一个关于网站如何创建标识符来定义他们支持的支付方式的提案](https://github.com/zkoch/zkoch.github.io/blob/master/payment-manifest.md)。这包括创建机器可读的支付清单 JSON 文件(支付方法标识符)，它需要被浏览器读取，以便支付请求 API 可以识别用户是否具有一个或多个与 JSON 文件中识别的支持的支付方法相对应的应用。这一实现受到了谷歌[数字资产链接协议](https://developers.google.com/digital-asset-links/v1/getting-started)的启发，如果你已经安装了该协议，网站会将你从他们的移动网站重定向到他们的应用程序。

在该组织内部反复讨论之后，最终在 2016 年 11 月 25 日，谷歌的扎克·科赫和阿里巴巴的刘大鹏提交了支付方式清单的[初稿，以启动所有成员都同意的支付方式标识符的标准化流程。最终，工作组成员](https://w3c.github.io/webpayments/proposals/Payment-Manifest-Proposal.html)[于 3 月 23 日至 24 日](https://www.w3.org/blog/wpwg/2017/03/31/preparing-to-advance-payment-request-and-payment-handler-apis/)在芝加哥会面，商讨支付请求 API、支付清单提案等事宜。工作组[投票正式采纳了](https://www.w3.org/2017/03/24-wpwg-minutes#item04)支付清单提案的新版本([版本 2](https://github.com/zkoch/zkoch.github.io/blob/master/pmi-v2.md) )，这就是我们今天的立场。

* * *

## 支持付款申请 API

5 月 10 日，由于 web 支付清单先决条件在 blink-dev 分支中获得批准(blink 是 Chrome 使用的渲染引擎的名称)，Chromium 中默认启用了对第三方 Android 支付应用的支持**。请注意，这项功能已经在 Chrome 中测试了几个月，但直到最近，该小组才准备好继续推进这项工作。除了 Android Webview** (它没有 UI，因此无法实现支付请求 API)之外，**所有平台/版本的 Chromium 都将提供这一功能。**

只有经过几个月的幕后工作，我们现在才能看到网络支付工作组所做工作的好处。在谷歌 I/O 大会上，该公司可能会宣布谷歌 Chrome 将启用支付请求 API，前面提到的扎克·科赫将在周四发表演讲，介绍第三方支付提供商如何通过构建支付清单 JSON 文件来支持 API。

其他浏览器也在努力增加对支付请求 API 的支持。Mozilla 和三星已经公开表示支持增加 API，尽管[根据谷歌Rouslan Solomakhin](https://groups.google.com/a/chromium.org/d/msg/blink-dev/gQCGIrnMxFU/Fz0UDLNeBAAJ)还没有消息表明微软的 Edge 浏览器或苹果的 Safari 是否会增加支持。我们应该注意到，微软已经在测试通用 Windows 平台(UWP)应用程序的支付请求 API，至少有一家银行已经在他们的应用程序中实现了对支付请求 API 的支持。

至于将支持这一新支付规范的其他在线商家和 Android 应用程序，据谷歌公司扎克·科赫称:

> #### 需要实现该规范的“支付方式提供商”的数量很少(数百家)，目前我们只直接与其中的一小部分(< 5 家)合作进行测试。如果我们真的遇到了需要更改其中一个字段的情况，我认为我们可以很容易地做到，并且没有太多(如果有的话)互操作风险。我们所有的早期合作伙伴都意识到这个规格可能会改变，并接受这一点。
> 
> #### 推广这一点对于让其他玩家参与公关生态系统至关重要，至少在 Android 上是如此。我真的不想走完全专有的路线来启用 android 原生应用。我们有意将这方面的影响保持在较小的水平，以便为增长和更高级的用例留出空间。

因此，我们可以看到，尽管谷歌是支持支付请求 API 的先锋，但真正看到这种新的支付方式进入所有浏览器、所有在线商家和所有应用程序还需要一段时间。我个人非常高兴看到谷歌支持支付请求 API。多年来，电子商务生态系统一直被支付方式不必要地分割，如果这个新的 API 意味着我再也不用手动将我的信用卡信息输入到网站上，那么我完全支持它。

* * *

你如何看待这个即将到来的标准？请在评论中发表意见，让我们知道你的观点！