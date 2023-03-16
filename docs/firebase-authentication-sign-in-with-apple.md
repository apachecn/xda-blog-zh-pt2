# Firebase 认证现在支持 Apple 登录

> 原文：<https://www.xda-developers.com/firebase-authentication-sign-in-with-apple/>

# Firebase 认证现在支持 Apple 登录

Firebase Authentication 是一个 API，它让移动应用程序开发人员可以轻松地在流行的网络服务中添加登录支持，现在它支持苹果的登录。

每当我注册一项新的在线服务或一个应用程序要求我登录以在云中存储一些数据时，我通常会尝试使用“登录方式”选项，通常包括谷歌、脸书、Twitter 或微软，如果他们应该这样做的话。大多数人已经在这些大型提供商那里有了一个或多个帐户，所以以这种方式支持登录对用户和开发人员来说都很方便。对于应用开发者来说，除非你真的想(或者不得不)实现自己的用户认证系统，那么你最好使用现成的认证系统，比如 [Firebase Authentication](https://firebase.google.com/docs/auth/) 。

Firebase Auth SDK 使开发人员可以轻松地为他们的应用程序添加一个完整的登录系统，并附带一个 UI 。它目前支持基本的基于电子邮件/密码和电话号码的身份验证，但它也支持以下联合身份提供者:Google 登录、脸书登录、Twitter 登录、Microsoft Azure Active Directory、Yahoo 和 GitHub。现在，这项服务增加了另一个提供商，谷歌[上周晚些时候宣布【Firebase Authentication 现在支持](https://firebase.googleblog.com/2019/11/sign-in-with-apple-auth.html)[登录苹果](https://developer.apple.com/sign-in-with-apple/)。对苹果登录的支持目前处于测试阶段，但开发人员可以使用最新版本的 Firebase SDKs 将苹果按钮登录添加到他们的 iOS、Android 或 web 应用程序中。开发者不再需要使用[自定义认证系统](https://firebase.google.com/docs/auth/web/custom-auth)和[在他们的网页上手动嵌入“用苹果登录”按钮](https://developer.apple.com/documentation/signinwithapplejs/configuring_your_webpage_for_sign_in_with_apple)。

 <picture>![Sign in with Apple button in a Firebase app](img/e73f4dafed9800daacec4ebd1529110d.png)</picture> 

Sign in with Apple through Firebase Authentication. Source: Google

随着 Firebase Auth 中又增加了一个流行的身份提供者，开发人员可以通过提供一种安全、方便和熟悉的注册方式来鼓励更多的用户注册他们的服务。